## Approch, Sort, map

### Logic
* 1. Sort each word and store count in map
```
input:      {"rat", "cat", "bus", "art", "tar"}
sorted:     {"art", "act", "bsu", "art", "art"}
map:
  art,3 | act,1 | bsu,1
```
* 2. Iterate thru original Dictionary, sort each word and search in map
```
input:      {"rat", "cat", "bus", "art", "tar"}
word: rat => art, search art in map, if found push count on vector
  <(rat,2)
  
word: cat => act, search act in map, if found push count on vector
  <(rat,2), (cat,0)..
```

## Complexity
### Time:
n*mlogm
m: length of longest word in dictionary. mlogm
n: length of dictionary.

### Space: 
2m*n
n: number of words in dictionary
m: max length of word in dictionary
m*n: storing map
m*n: storing output.
