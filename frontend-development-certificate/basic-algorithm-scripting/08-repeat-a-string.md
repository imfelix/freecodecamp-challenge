# Problem Script

```javascript
function repeatStringNumTimes(str, num) {
  // repeat after me
  return str;
}

repeatStringNumTimes("abc", 3);
```

# Solution Script

```javascript
function repeatStringNumTimes(str, num) {
  // repeat after me
  var result = "";
  if (num < 0) {
    return result;
  } else {
    for (var i = 0; i < num; i++) {
      result = result + str;
    }
    return result;
  }
}

repeatStringNumTimes("abc", 3);
```

# Explanation

1. Check if `num` is negative (meaning greater than 0)
2. If the num is not negative, repeat the `str` `num` times
3. Using a for loop to determine the number of times
