# Problem Script

```javascript
function truncateString(str, num) {
  // Clear out that junk in your trunk
  return str;
}

truncateString("A-tisket a-tasket A green and yellow basket", 11);
```

# Solution Script

```javascript
function truncateString(str, num) {
  if (str.length <= num) {
    return str;
  } else {
    return str.slice(0, num > 3 ? num - 3 : num) + '...';
  }
}

truncateString("A-tisket a-tasket A green and yellow basket", 11);
```

# Explanation

1. Check if the length of `str` is greater than or equal to `num`. If it's less than, return `str`
2. If `str.length` is greater, we truncate the text to length of `num` given
3. After truncating the text, you add `...` at the end 
4. **But** the tricky part here is that `...` will add to the length of the string.
5. Here, we used a ternary operator to decide if `num` is greater than 3 (because of `...`):

    5.1 If true, we take out 3 more charaters from `str` to add `...`
    5.2 If false, we return the `num` of `str`
