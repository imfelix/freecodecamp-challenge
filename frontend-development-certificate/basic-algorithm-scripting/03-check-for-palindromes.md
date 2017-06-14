# Problem Script

```javascript

function palindrome(str) {
  // Good luck!
  return true;
}

palindrome("eye");
```

# Solution Script

```javascript
function palindrome(str) {
  // Remove punctuation and make the string lowercase
  str = str.replace(/[\W_]+/g, "").toLowerCase();
  // Reverse the string and check for palindrome
  return str === str.split("").reverse().join("");
}

palindrome("eye");
```

# Regex Explanation

* `/ ... /g` - It's a global regex and will operate on multiple matches in a string.
* `[ ... ]` - This creates a character set matching any single character within the listed set of characters.
* `\W_` - This matches special characters and underscores. 
* `+` - Matches the preceding expression 1 or more times
