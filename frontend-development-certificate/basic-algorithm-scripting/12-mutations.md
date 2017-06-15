# Mutations

### Problem Description

Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.

### Problem Script

```javascript
function mutation(arr) {
  return arr;
}

mutation(["hello", "hey"]);
```

### Expected Outcome

* `mutation(["hello", "hey"])` should return `false`.
* `mutation(["hello", "Hello"])` should return `true`.
* `mutation(["zyxwvutsrqponmlkjihgfedcba", "qrstu"])` should return `true`.
* `mutation(["Mary", "Army"])` should return `true`.
* `mutation(["Mary", "Aarmy"])` should return `true`.
* `mutation(["Alien", "line"])` should return `true`.
* `mutation(["floor", "for"])` should return `true`.
* `mutation(["hello", "neo"])` should return `false`.
* `mutation(["voodoo", "no"])` should return `false`.

### Solution Script

```javascript
function mutation(arr) {
  var firstArr = arr[0].toLowerCase();
  var secondArr = arr[1].toLowerCase();

  for (i = 0; i < secondArr.length; i++) {
    if (firstArr.indexOf(secondArr[i]) < 0) {
      return false;
    }
  }
  return true;
 }

mutation(["hello", "hey"]);
```

### Solution Explanation

1. As `indexOf()` method is case-sensitive, we need to transform both arguments to lower case
2. Now, we step through each character in the `secondArr`
3. While stepping through characters `secondArr`, we check if `firstArr` has the same character using `indexOf()` method
4. If `firstArr` has characters of `secondArr`, it would return 1, thus breaking from the if loop.
5. If `firstArr` doesn't have the character, it return -1, thus returning false.

### Useful Links

* `String.prototype.indexOf()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf)
