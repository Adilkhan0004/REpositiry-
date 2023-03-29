### 1.Write a function that uses the call method to print the name of an object.
```
obj = {
  name: "adil khan",
  class: 12 + "th",
};
function printD(a) {
  console.log(obj);
}
printD.call(obj);
```

### 2.Write a function that uses the apply method to find the minimum value in an array of numbers.
```
let arr = [2, 3, 5, 6, 7, 43, -4, 1, 2];
let min = arr[0];
function min1(arr1) {
  for (let value of arr) {
    if (value < min) {
      min = value;
    }
  }
  console.log(min);
}
min1.apply();
```

### 3.Write a function that uses the bind method to create a new function that always has a specific "this" value.

### 4.Write a function that uses the call method to add two numbers together.
```
let a;
function sum(a, b) {
  console.log(a + b);
}
sum.call(a, 10, 22);
```



### 5.Write a function that uses the apply method to concatenate two arrays.
```
let arr = [2, 4, 6, 7];
let arr1 = [1, 5, 6, 7];
function concat() {
  console.log(arr.concat(arr1));
}
concat.apply();
```

### 6.Write a function that uses the bind method to create a new function that multiplies a number by a specified value.
```
let obj;
function multi(a, b) {
  console.log(a * 2);
}
let ans = multi.bind(obj, 45);
ans();
```

### 7.Write a function that uses the call method to find the length of a string.
```
let str = " My name is JavaScript and I'm most popular language of 2023";
function len() {
  console.log(str.length);
}
len.call();
```

### 8.Write a function that uses the apply method to find the sum of all numbers in an array.
```
let arr = [2, 4, 3, 5, 7, 8, 9, 0, 5, 4, 3, 2];
let ans = 0;
function sum() {
  for (let value of arr) {
    ans = ans + value;
  }
  console.log(ans);
}
sum();
```

### 09.Write a function that uses the bind method to create a new function that logs a message with a specific prefix.

### 10.Write a function that uses the call method to convert a string to uppercase.
```
let str = " My name is JavaScript and I'm most popular language of 2023";
function uppercase() {
  console.log(str.toUpperCase());
}
uppercase.call();
```

