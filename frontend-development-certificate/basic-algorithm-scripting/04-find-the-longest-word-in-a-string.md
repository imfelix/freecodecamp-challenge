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
  // Split all words in str into an array
  var words = str.split(' ');
  var longest = 0;
  
  words.forEach(function(word) {
    if (longest < word.length) {
      longest = word.length;
    }
  });
  
  return longest;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```
