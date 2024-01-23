/**
 * The functions returns a sorted array after adding the new element
 * @param {number[]} array
 * @param {number} element
 * @returns {number[]}
 */
export function addAndSort(array, element) {
    array.push(element); // Add the new element to the array
    return array.sort((a, b) => a - b); // Sort the array in ascending order
}

// Sample Test Cases
console.log(addAndSort([5, 7, 1, 6], 3)); // Expected Output: [1, 3, 5, 6, 7]
console.log(addAndSort([15, 7, 2, 26], 10)); // Expected Output: [2, 7, 10, 15, 26]
console.log(addAndSort([25, 27, 21, 16], 19)); // Expected Output: [16, 19, 21, 25, 27]
