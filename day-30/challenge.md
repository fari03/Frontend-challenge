/**
 * @param {Function[]} functions
 * @param {number} n
 * @return {Function}
 */
export async function promisePool(functions, n) {
	const results = [];
	const promises = [];
  
	for (let i = 0; i < functions.length; i++) {
	  const currentFunction = functions[i];
	  const currentPromise = currentFunction();
	  promises.push(currentPromise);
  
	  if (promises.length === n || i === functions.length - 1) {
		await Promise.all(promises).then((values) => {
		  results.push(values);
		  promises.length = 0; // Reset promises array
		});
	  }
	}
  
	return [results.flat(), results.reduce((acc, cur) => Math.max(acc, ...cur), 0)];
  }
  
  /**
   * Example usage:
   * const sleep = (t) => new Promise(res => setTimeout(res, t));
   * promisePool([() => sleep(500), () => sleep(400)], 1)
   *   .then(console.log) // After 900ms
   */
  
