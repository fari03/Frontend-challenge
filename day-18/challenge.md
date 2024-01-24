/**
 * Removes all whitespaces from the input string
 * @param {string} string - The input string
 * @returns {string} - The string with all whitespaces removed
 */
export const removeWhitespaces = (string) => {
    // Use a regular expression to match and remove all whitespace characters
    return string.replace(/\s/g, '');
}

// Sample Test Cases
console.log(removeWhitespaces('Hello,   World!')); // Output: 'Hello,World!'
console.log(removeWhitespaces('  This is a sentence.\nIt contains some whitespace.  ')); // Output: 'Thisisasentence.Itcontainssomewhitespace.'
console.log(removeWhitespaces('\t  \n\n')); // Output: ''
