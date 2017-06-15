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
  return (str.substr(-target.length) === target);
}

confirmEnding("Bastian", "n");
```

# Explanation

1. Since substr() was given a negative number
2. It will only take the last number of charaters
3. Then check if it equals target

# Useful Links

* `String.prototype.substr()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substr)
