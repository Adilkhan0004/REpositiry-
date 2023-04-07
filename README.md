### 1.Write a function that takes a string and returns a new string with all the words reversed using the spread operator.
```
function newString(str) {
  return [...str].reverse().join("");
}
console.log(newString("My name is adil khan"));
```

### 2.Create a function that takes in an array and uses the rest operator to remove the ?first element from the array and finally return the array without first element.
```
let arr = [3, 4, 2, 3, 2, 4, 3, 42, 4, 14];
function combine() {
  return ([, ...a] = arr);
}
console.log(combine());
```

### 3.Create a function that takes in an unknown number of arrays and uses the rest operator to flatten them into a single array
```
function single(arr, arr2, arr3) {
  return [...arr, ...arr2, ...arr3];
}
console.log(single([3, 5, 6], [3, 3, 4], [7, 8, 9, 6]));
```

### 4.Write a function that takes an object as a parameter and returns the value of its "x" property if it exists, otherwise it returns null. Hint : (Use optional chaining)
```
let obj = {
  name: "Adil khan",
  age: 21,
  address: {
    city: "Jaipur",
    pincode: 302012,
  },
};
function test(obj) {
  if (obj?.address?.pincodes) {
    console.log("Yes");
  } else {
    console.log(null);
  }
}
test(obj);
```

### 5.Write a function which takes in an array and create two separate arrays for odd numbers and even numbers and finally merge them in the order that all odd numbers will move to the left of the array and all even numbers to right of the array.

let arr = [2, 5, 6, 7, 7, 5, 4, 4, 6];
let oddNumber = arr.filter((a) => a % 2 === 1);
let evenNumber = arr.filter((a) => a % 2 === 0);
let ans = [...oddNumber, ...evenNumber];
console.log(ans);

### 6.Create an array of numbers. Now change the position of each element with their next element.

For example : [1,2,3,4,5,6,7]
Output : [2,1,4,3,6,5,7]

### 7.Ask user below questions
#### What is your age  : 12
#### What is your mobile : 9581894461
#### What is your address : Jaipur
#### Now create an object and use enhanced object literal property computation to create below object
```
let age = 21;
let mobileNum = 8384789432;
let address = "Naguar";
let obj = {
  ["age " + 12 + true]: age,
  ["Mobile " + false]: mobileNum,
  ["address+12" + address]: address,
};
console.log(obj);

let details = {
  ["myAge" + age]: age,
  [mobile]: "mobile",
  [address + age + "address"]: address,
};
console.log(details);
```

### 8.Using enhanced object literal function, create a function sum which takes an array as parameter and return sum of all the numbers in the array.
```
let obj = {
  sum: function (arr) {
    return arr.reduce((a, c) => a + c, 0);
  },
};
let arr = [4, 3, 3, 4, 5];
console.log(obj.sum(arr));
```

### 9.Take a number and check if number is greater than 80 or not. If yes then assign 100 to number else assign 200. Use short circuiting whereever possible.
```
let num = 9;
result = (num > 80 && 100) || 200;
console.log(result);
```

### 10.Create an array of 10 numbers. Now create a new array of 0 and 1 using Array destructring based on if number is odd then 1 else 0
```
let arr = [3, 2, 2, 3, 4, 4];

let binary = arr.map((num) => {
  let ans = num % 2 === 0 ? 0 : 1;
  return ans;
});
console.log(binary);
```

### 11.Given an array of price, use map function to return a new array where each price is converted to new price including tax, which is the price with a 10% tax added.
```
let price = [5, 3, 6, 7, 3, 5];
let priceTax = price.map((price) => {
  const result = price * 1.1;
  return result;
});
console.log(priceTax);
```

### 12.Given an array of strings, use reduce to return the total number of characters in all the strings.
```
let str = "My name is adil khan";
let ans = str.split("").reduce((a, b) => {
  return a + b.length;
}, 0);
console.log(ans);
```

### 13.Given an array of strings, use map and reduce to return the total number of characters in all the strings with a length less than 5.
let strArr = [
  "adil",
  "ravindra",
  "manish",
  "sajid",
  "harshit",
  "wecode",
  "ravi",
  "adil",
];
let allCharcter = strArr
  .filter((strArr) => strArr.length < 5)
  .map((strArr) => strArr.length)
  .reduce((a, b) => {
    return a + b;
  }, 0);
console.log(allCharcter);

### 14.Given an array of numbers, use map, filter, and reduce to return the sum of all the odd numbers multiplied by 3
```
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let ans = arr
  .filter((arrMap) => arrMap % 2 === 1)
  .map((arrFilter) => arrFilter * 3)
  .reduce((array, val) => {
    return array + val;
  }, 0);
console.log(ans);

### 15.Given a string, reverse the order of the words in the string. For example, "the quick brown fox" becomes "fox brown quick the".
```
let str1 = "the quick brown fox";
let ans = str1.split(" ").reverse().join(" ");
console.log(ans);
```
