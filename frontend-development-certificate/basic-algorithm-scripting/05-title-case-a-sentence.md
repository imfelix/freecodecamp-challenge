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
    return word.charAt(0).toUpperCase().concat(word.slice(1).toLowerCase());
  });
  return words.join(' ');
}

titleCase("I'm a little tea pot");
```

# Explanation

1. Take the first character of the word
2. Convert the character to uppercase
3. Concatenate it with the rest of the word
4. Also, convert the rest of the words to lowercase.
