- map[sorted] gives count of all words with that sorted form.
- map[sorted] - 1 excludes the word itself (because its own sorted form will match).

* Time & Space Complexity

- Time: O(n * m log m)
where n = # of words, m = max length of word (for sorting)

- Space: O(n * m) for map + output