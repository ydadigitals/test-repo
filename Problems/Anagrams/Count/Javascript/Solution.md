function countAnagrams(dictionary) {
  const map = {};

  // Step 1: Fill map with sorted word counts
  for (const word of dictionary) {
    const sorted = word.split('').sort().join('');
    map[sorted] = (map[sorted] || 0) + 1;
  }

  // Step 2: Build output with original words
  const result = dictionary.map(word => {
    const sorted = word.split('').sort().join('');
    return `${word},${map[sorted] - 1}`; // subtract 1 to exclude self
  });

  return result;
}

// Example usage
const dictionary = ["rat", "cat", "bus", "art", "tar", "usb"];
const output = countAnagrams(dictionary);
console.log(output.join('\n'));
