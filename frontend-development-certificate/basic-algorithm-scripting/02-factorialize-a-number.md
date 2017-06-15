# Factorialize a Number 

### Problem Description

Return the factorial of the provided integer.

### Problem Script

```javascript
function factorialize(num) {
  return num;
}

factorialize(5);
```

### Expected Outcome

* `factorialize(5)` should return a number.
* `factorialize(5)` should return 120.
* `factorialize(10)` should return 3628800.
* `factorialize(20)` should return 2432902008176640000.
* `factorialize(0)` should return 1.

### Solution Script

```javascript
function factorialize(num) {
  if (num === 0) {
    return 1;
  }

  return num * factorialize(num - 1);
}

factorialize(5);
```

### Solution Explanation

1. Check if the number given is 0, if true return 1. 
2. Else, return the product of all positive integers less than or equal to number given.
