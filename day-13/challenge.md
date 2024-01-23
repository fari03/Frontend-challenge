// Function to sum even numbers in the array
export const sumOfEvens = (arr) => {
	// Use the reduce method to sum even numbers
	return arr.reduce((sum, num) => {
	  // Check if the number is even
	  if (num % 2 === 0) {
		// Add the even number to the sum
		return sum + num;
	  } else {
		// Otherwise, return the current sum unchanged
		return sum;
	  }
	}, 0); // Start with an initial sum of 0
  };
  
