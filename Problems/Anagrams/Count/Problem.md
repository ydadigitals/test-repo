### Count Anagrams in Dictionary 
* Give a dictionary of words, we need to count anagrams except present word. Dictionary can have meaningful or unmeaningful words.
```
Input Dictionary: {"rat", "cat", "bus", "art", "tar", "usb"}
Output:
  rat,2     //rat,art,tar are anagrams but we output 2 since present word is not counted
  cat,0     //cat does not have anagram in dictionary
  bus,1     //bus,usb are anagrams
```
