# JavaScript

## **Comments**

```jsx
// single line comment

/* Also this is a mulit-line comment
	as you see */
```

## Variables & Data-types

```jsx
/* Data types in js */
// number string null boolean undefined symbol object

// declare a variable named myname
// that can be used in the entire program
var myname = "Ahmed";
console.log(myname); // print myname
myname = 8; // change the variable data-type is possible
console.log(myname);
// declare a variable named age
// that can be used in the block of initialization 
let age = 20;
console.log(age);
// declare a constant variable pi
const pi = 3.14;
```

## null vs undefined

```jsx
// null vs undefined
var name; // undefined (No assignment)
var size = null; // A variable is assigned to null (nothing or void)
console.log(name, size);
```

## Declaration vs Initialization

```jsx
var a = 5; // declare and initialize a var "a"
var b; // declare variable "b"
console.log(b) // "undefined" due to no Initialization
b = a
console.log(b) // 5
```

### **NOTE: Naming in js is case-sensitive**

### **NOTE: You can end lines with ";" or not but the convention says to put ";"**

## Mathematical operators

```jsx
var a = 10;
// increment
a++ // or a = a + 1 or ++a
// decrement
a--; // or a = a + 1 or --a
console.log(a)
a += 9
a -= 9
a *= 9
a /= 9
console.log(a)
```

## Escape sequences

```jsx
/* use '\' to escape lateral quotes */
var s = "s is a \"double qouted\" string"
// or you can use single quote (but this is still a problem when using ' inside str)
var str1 = 's is a "double qouted" string"'
/* the ultimate solution is to use '`' instead of ' or " */
var str = `'HI' "iam ahmed" `
console.log(s,"\n",str)
/*** other escape sequences
\n -> new line \t -> tab \f -> form feed \r -> carriage return \b -> backspace \\ \" \'
***/
```

## String concatenation & Manipulation

```jsx
var a = "i am a ";
var b = a + "string";
/* also you can use this
b += "string"
*/
console.log(b);
/*************************************************************************/
/*   Manipulation    *****************************************************/
var greeting = "gi, my name is ahmed";
var str_length = greeting.length;
var firstElement = greeting[0]; 
var lastElement = greeting[greeting.length - 1]
console.log(greeting.length,"\n",firstElement, lastElement);
/******************************************************/
// string is immutable
/******************************************************/
greeting[0] = "s"; // error
greeting = "hi, my name is ahmed"; // changing the whole value is possible
```

## Lists

```jsx
var mylist = [1,2,3,54];
/* Remove item from list */
var popedValue = mylist.pop(); // remove from the back
console.log(popedValue);

var shiftedValue = mylist.shift(); // remove from the beginning
console.log(shiftedValue);
/* Add new item to the list */
var numOfElements = mylist.push(500); // push from the back (returns num of elements)
console.log(numOfElements);

numOfElements = mylist.unshift(100); // push to the beginning (returns num of elements)
console.log(numOfElements);
console.log(mylist); // print the list
```

## Functions

```jsx
// defination of function
function greeting(name) {
  console.log("Hallo, MR." + name);
}
// call the function
greeting("Ahmed");
```

## Global Scope vs Local Scope

```jsx
// global scope
var num1 = 10;
var num2 = 5;

function localScope() {
  var var1 = 10; // local variable
  let var2 = 10; // local variable
  var3 = 10;     // global variable
}
// function contain 1 positional argument & 1 keyword argument
function add(num1, num2=1) {
  if(typeof num1 != "undefined" || typeof num2 != "undefined") {
    console.log(num1 + num2);
  }
}
add(num1);
add(num1, num2);
```

```jsx
/********** Local variable precedence against 
						global one at the same name     
 ************/
var language = "Arabic";
function sayYourLanguage() {
	var language = "English";
	return language;
}
console.log(sayYourLanguage()); // English
console.log(language); // Arabic
```

## Boolean

```jsx
// Boolean variables takes values (true or false)
function checkState(state) {
  if (state) {
    console.log("yes, that was true");
  } 
  else {
    console.log("no, that was not true");
  }
}
checkState(true);
checkState(false);
```

## Comparison Operators

```jsx
/***** Operators in js
== , === (strict equality operator), != , !== 
< , <= , > , >= 
&& , || 
 *****/
```

```jsx
function equalOrIdentical(val1, val2) {
  if (val1 === val2) {
    console.log("Identical");
  } else if (val1 == val2) {
    console.log("Equal");
  }
}
equalOrIdentical("15",'15');  // Identical
equalOrIdentical("15",15);    // Equal
```

## Switch statement

```jsx
/* The same as in C */
function useSwitch(index) {
  switch(index) {
    case 0:
      console.log("football");
      break;
    case 1:
    case 2:
    case 3:
    case 4:
      console.log("Swimming");
      break;
    default:
      console.log("Handball");
      break;  
  }
}
useSwitch(0); // football
useSwitch(1);useSwitch(2);useSwitch(3);useSwitch(4); // Swimming
useSwitch(6); // Handball
```

## Objects

```jsx
// Create an object
var identity = {
 // property     value
  "first name": "Ahmed",
  "last name": "farouk",
  "age": 20,
  2: 'cairo',
  "gender": "male" 
};
// accessing properties 
identity.age = 10;
var myFisrtName = identity["first name"];

// accessing property '2' by "country"  
var country = 2;

// add property
identity.id = 123154654;
identity["status"] = "single";

// delete property
delete identity.age
// print
console.log(identity[country]);
console.log(myFisrtName, identity.age);
```


```jsx
// check for existance of a property
var a = identity.hasOwnProperty("age")
// print
console.log(a); // true
```

## Accessing complex data e.g. array of objects

```jsx
// Create an object
var identities = [
  {
   // property     value
    "first name": "Ahmed",
    "last name": "farouk",
    "age": 20,
    2: 'cairo',
    "gender": "male" 
  },
  {
    // property     value
    "first name": "Ishak",
    "last name": "yacob",
    age: 50,
    2: 'cairo',
    gender: "male" 
  }
];
// print
console.log(identities[1].gender);
```


## While and For Loops: the same as in C

## Do While loop

```jsx
var i = 10;
do {
  console.log(i);
  i++;
}while (i < 0)
```

## Useful functions (random, floor, parseInt)

```jsx
// create randon float 0 -> 1
console.log(Math.random())
// get the whole number (without fraction)
console.log(Math.floor(Math.random()*20))
// convert str to int (str, base) 
console.log(parseInt("11111111",2));
```

## Ternary Operator

```jsx
// ternary operator
// condition ? true statement: false statement;
var a = 0;
a == 0? a++: a--;
console.log(a);
// nested ternary operator
// condition ? true statement: (false statement)condition ? true statement: false statement;
```

## let vs var keywords

```jsx
/******* 
declaration
********/
// error "duple declaration"
let name = "ahmed";
let name = "hany";
// no error
var name = "ahmed";
var name = "hany";
```

```jsx
/****  scopes  ******/
var i = 0;  // global & local 
if (true) {
  var i = 10;
  console.log(i);
}
console.log(i);
/***********************************************/
let k = 0; // global = 0
if (true) {
  let k = 10; // local = 10
  console.log(k); // = 10
}
console.log(k); // 0
```
## Strict Mode
### "use strict" to get into strict mode
### Useful link: https://www.w3schools.com/js/js_strict.asp


## Anonomous Function

```jsx
/* anonomous function without parameters */
var date = () => Date();
console.log(date())
/* anonomous function with parameters */
var square = (num) => num*num;
console.log(square(5));
```

## Rest Operator

```jsx
/* rest operator */
// collect all arguments into array
// So, allow variable number of arguments
function printArgs(...args) {
  return args;
}

console.log(printArgs(54,54,564));
```

## Spread Operator

```jsx
// spread operator
var arr = [1,2,3];
var arr2 = [...arr]; // independent
arr2[0] = 4564;
console.log(arr, arr2); // arr2 changed but arr not
/********************************* */
var arr2 = arr; // dependent
arr2[0] = 4564;
console.log(arr, arr2); // arr2 and arr changed
```