# Problem Script

```javascript
function findLongestWord(str) {
  return str.length;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```

# Solution Script

```javascript
function findLongestWord(str) {
  var words = str.split(' ');
  var longestWordLengthCount = 0;
  
  words.forEach(function(word) {
    if (longestWordLengthCount < word.length) {
      longestWordLengthCount = word.length;
    }
  });
  
  return longestWordLengthCount;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```
