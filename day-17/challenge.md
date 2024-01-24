/**
 * Removes falsy values from the array and returns a new array with only truthy values
 * @param {Array} arr - The input array
 * @returns {Array} - The new array with only truthy values
 */
export const removeFalsy = (arr) => {
    return arr.filter(value => !!value);
}

// Sample Test Case
const arr = [0, 1, false, 2, '', 3];
const result = removeFalsy(arr);
console.log(result); // should log [1, 2, 3]
