# Falsy Bouncer

### Problem Description

Remove all falsy values from an array.

Falsy values in JavaScript are `false`, `null`, 0, "", `undefined`, and `NaN`.

### Problem Script

```javascript
function bouncer(arr) {
  // Don't show a false ID to this bouncer.
  return arr;
}

bouncer([7, "ate", "", false, 9]);
```

### Expected Outcome

* `bouncer([7, "ate", "", false, 9])` should return `[7, "ate", 9]`.
* `bouncer(["a", "b", "c"])` should return `["a", "b", "c"]`.
* `bouncer([false, null, 0, NaN, undefined, ""])` should return `[]`.
* `bouncer([1, null, NaN, 2, undefined])` should return `[1, 2]`.

### Solution Script

```javascript
function bouncer(arr) {
  return arr.filter(Boolean);
}

bouncer([7, "ate", "", false, 9]);
```

### Solution Explanation

1. `filter()` returns a new array with all elements that pass the condition.
2. `Boolean` being the condition, any falsy values won't be included in the new array.

### Useful Links

* `Boolean Object` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)
* `Array.prototype.filter()` - [MDN link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter?v=example)
