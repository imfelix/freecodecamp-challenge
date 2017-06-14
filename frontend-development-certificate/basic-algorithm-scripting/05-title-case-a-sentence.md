# Problem Script

```javascript
function titleCase(str) {
  return str;
}

titleCase("I'm a little tea pot");
```

# Solution Script

```javascript
function titleCase(str) {
  var words = str.split(' ');
  words = words.map(function(word) {
    // Take the first character of the word
    // Convert the character to upper case
    // Concatenate it with the rest of the word
    // Also, convert the rest of the words to lower case.
    return word.charAt(0).toUpperCase().concat(word.slice(1).toLowerCase());
  });
  return words.join(' ');
}

titleCase("I'm a little tea pot");
```
