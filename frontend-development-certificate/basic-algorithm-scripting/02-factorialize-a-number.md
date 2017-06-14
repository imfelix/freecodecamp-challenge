# Problem Script

```javascript
function factorialize(num) {
  return num;
}

factorialize(5);
```

# Solution Script

```javascript
function factorialize(num) {
  if (num === 0) {
    return 1;
  }

  return num * factorialize(num - 1);
}

factorialize(5);
```
