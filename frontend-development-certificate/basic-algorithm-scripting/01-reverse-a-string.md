# Reverse a String

### Problem

Reverse the provided string.

```javascript
function reverseString(str) {
  return str;
}

reverseString('hello');
```

### Expected Outcome

* `reverseString("hello")` should return a `string`.
* `reverseString("hello")` should become `"olleh"`.
* `reverseString("Howdy")` should become `"ydwoH"`.
* `reverseString("Greetings from Earth")` should return `"htraE morf sgniteerG"`.

### Solution Script

```javascript
function reverseString(str) {
  return str.split('').reverse().join('');
}

reverseString('hello');
```

### Solution Explanation

1. Split the string argument given in the function with `split()` method
2. `split('')` will split each element within the string and return an array of strings
3. Then, reverse the split array of strings with `reverse()` method
4. Finally, join the array of strings with the method `join()`

### Useful Links

* `String.prototype.split()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
* `Array.prototype.reverse()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse?v=example)
* `Array.prototype.join()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join?v=example)
