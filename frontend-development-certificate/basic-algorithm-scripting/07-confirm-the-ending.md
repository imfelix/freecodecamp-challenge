# Problem Script

```javascript
function confirmEnding(str, target) {
  // "Never give up and good luck will find you."
  // -- Falcor
  return str;
}

confirmEnding("Bastian", "n");
```

# Solution Script

```javascript
function confirmEnding(str, target) {
  // Since substr() was given a negative number
  // It will only take the last number of charaters
  // Then check if it equals target
  return (str.substr(-target.length) === target);
}

confirmEnding("Bastian", "n");
```

# Useful Links

* `str.substr()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substr)
