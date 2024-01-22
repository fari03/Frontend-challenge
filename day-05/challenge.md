/**
 * @param {number[]} nums
 * @return {void} Do not return anything, modify nums in-place instead.
 */
export function moveZeroes(nums) {
    let nonZeroIndex = 0;

    // Iterate through the array
    for (let i = 0; i < nums.length; i++) {
        // If the current element is non-zero
        if (nums[i] !== 0) {
            // Swap the non-zero element with the element at nonZeroIndex
            [nums[i], nums[nonZeroIndex]] = [nums[nonZeroIndex], nums[i]];
            nonZeroIndex++;
        }
    }
}

// Example usage:
// const nums = [0, 1, 0, 3, 12];
// moveZeroes(nums);
// console.log(nums); // Output: [1, 3, 12, 0, 0]
