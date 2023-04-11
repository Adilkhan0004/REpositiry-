### 1.How can you convert a string to a number in JavaScript? write all the ways.
```
let str = "22.6";
console.log(typeof +str, str);
console.log(typeof Number(str), str);
console.log(typeof parseInt(str), str);
console.log(typeof parseFloat(str), str);
console.log(typeof (str * 1), str);
console.log(typeof (str / 1), str);
console.log(typeof (str - 0), str);
console.log(typeof Math.floor(str), str);
console.log(typeof Math.ceil(str), str);
console.log(typeof Math.round(str), str);
```

### 2.How do you round a number to a certain number of decimal places in JavaScript?
```
let num = 323.4233425;
console.log(Math.round(num));
```

### 3.How can you generate a random number between two values in JavaScript?
```
function randomNum(min, max) {
  return Math.floor(Math.random() * (max - min + 1) + min);
}
let ans = randomNum(1000, 9999);
console.log(ans);

const num = Math.floor(Math.random() * 10000 + 1 * 999);
console.log(num);
```

### 4.How do you convert a number to a binary, octal, or hexadecimal format in JavaScript?
```
let num = 123;
let binary = num.toString(2);
let octal = num.toString(8);
let hexadecimal = num.toString(16);

console.log(binary);
console.log(octal);
console.log(hexadecimal);
```

### 5.How do you add or subtract a certain number of days from a date in JavaScript?
```
let date = new Date();
date.setDate(date.getDate() - 10);
console.log(date.toLocaleString());

let date = new Date();
date.setDate(date.getDate() + 10);
console.log(date.toLocaleString());
```

### 6.How do you compare two dates in JavaScript? Check if a date is small or large or equal to other date?
```
let date = new Date();
let year23 = new Date("01/01/2001");

if (date > year23) {
  console.log(`${date} is greater than to ${year23}`);
} else if (date < year23) {
  console.log(`${date} is less than to ${year23}`);
} else {
  console.log(`${date} is equal to ${year23}`);
}
```

### 7.How can you format a date in JavaScript according to the user's locale?
```
console.log(
  new Intl.DateTimeFormat("hi", {
    dateStyle: "full",
    timeStyle: "short",
    timeZone: "Australia/Sydney",
    // timeZoneName: "long",
  }).format(new Date())
);
```

### 8.How do you calculate the difference between two dates in JavaScript?
```
let date = new Date();
let date2 = new Date("12/12/2010");
let days = date2.getDate() - date.getDate();
let month = date2.getMonth() - date.getMonth();
let year = date2.getFullYear() - date.getFullYear();
console.log(`DDMMYY : ${days}-${month}${year}`);
```

### 9.How do you check if a year is a leap year in JavaScript?
```
function leapYear(year) {
  return year % 4 === 0;
}
console.log(leapYear(2016));
```

### 10.How do you convert a string to a date in JavaScript? Write all ways.
```
let str = "12/3/1221";
let date = new Date(str);
console.log(date);

var d = new Date("May 1,2019 11:20:00");
console.log(d);

var d = new Date("May 1, 2019 ");
function formatDate(date) {
  return String(date);
}
console.log(formatDate(d));
```
### 11.How can you parse a date from a string in a specific format in JavaScript?
```
let date = Date.parse("March 21, 2034");
console.log(date);
```

### 12.How can you get the time in a specific timezone in JavaScript?
```
let indiaTimeZone = new Date().toLocaleString("hi", {
  timeZone: "Asia/Kolkata",
});
console.log(indiaTimeZone + " - Indian Time Zone");
```

### 13.Print date and time after every 1 second in the format 'MM/DD/YYYY HH:MM:SS'
```
let date;
setInterval(function () {
  date = new Date();
  console.log(
    `Date - ${date.getDate()}/${date.getMonth()}/${date.getFullYear()} Time - ${date.getHours()}:${date.getMinutes()}:${date.getSeconds()}`
  );
}, 1000);
setInterval(date);
```

### 14.Write a JavaScript Function to get the number of days in a month. Pass month and year as an arugment to the function. for example : getDays(2, 2023). Answer will be 28

```
function days(month, year, day = 0) {
  return new Date(year, month, day).getDate();
}

console.log(days(1, 2023));
console.log(days(2, 2022));
console.log(days(9, 2056));
console.log(days(2, 2013));
```

### 15.Write a JavaScript Function to get the week day name for the given date.

```
let weekDay = new Date("march,24,2023 8:15:30");
let ans = weekDay.getDay();
let day;
if (ans === 0) {
  console.log("Sunday");
} else if (ans === 1) {
  console.log("monday");
} else if (ans === 2) {
  console.log("tuesday");
} else if (ans === 3) {
  console.log("wednesday");
} else if (ans === 4) {
  console.log("thursday");
} else if (ans === 5) {
  console.log("friday");
} else if (ans === 6) {
  console.log("saturday");
}
```

### 16.Write a JavaScript Function to get the month name from the given date
```
let monthName = new Date("August,24,2023 8:15:30");
let ans = monthName.getMonth();
console.log(ans);
if (ans === 0) {
  console.log("January");
} else if (ans === 1) {
  console.log("Fabuary");
} else if (ans === 2) {
  console.log("March");
} else if (ans === 3) {
  console.log("April");
} else if (ans === 4) {
  console.log("May");
} else if (ans === 5) {
  console.log("June");
} else if (ans === 6) {
  console.log("July");
} else if (ans === 7) {
  console.log("August");
} else if (ans === 8) {
  console.log("September");
} else if (ans === 9) {
  console.log("October");
} else if (ans === 10) {
  console.log("November");
} else if (ans === 11) {
  console.log("December");
}
```
### 17.Write a JavaScript Function to check if given date is on weekend or not (Saturday/Sunday).
```
let weekend = new Date("march,26,2023 8:15:30");
let ans = weekend.getDay();
console.log(ans);
if (ans === 4 || ans === 0) {
  console.log("Weekend");
} else {
  console.log("weekDay");
}
```

### 18.Ask your about his date of birth. Now write a JavaScript Function to calculate age based on the given date of birth.
```
let curr = new Date();
let dob = new Date("01/01/2002");
let age = new Date(curr - dob);
console.log(age.getFullYear() - 1970);
```

### 19.Write a Javascript Function to using setInterval to show alert box when date is your birth date.

### 20.Show your birth date in Arabic
```
console.log(
  new Intl.DateTimeFormat("ar-sa", { timeZone: "EST" }).format(
    new Date("09/02/2002")
  )
);
```

### 20.Show your birth date in chinese
```
console.log(
  new Intl.DateTimeFormat("zn-tw", {
    timeZone: "asia/kolkata",
    timeStyle: "full",
  }).format(new Date("2/3/2002"))
);
```

### 21.Write a JavaScript Function to convert a binary number to a decimal number.
```
let  binary = "1101000"; // code for 104
let  digit = parseInt(binary, 2);
console.log(digit);

let binary = " 011101000011";
let numDecimal = parseInt(binary, 2);
console.log(numDecimal);
```
### 22.Write a JavaScript function to convert a decimal number to binary, hexadecimal or octal number.
