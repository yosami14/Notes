# Array

In contrast to variables, an array can store *multiple values*. Each value in an array has an *index*, and each index has *a reference in a memory address*. Each value can be accessed by using their *indexes*. The index of an array starts from *zero*, and the index of the last element is less by one from the length of the array.

An array is a collection of different data types which are ordered and changeable(modifiable). An array allows storing duplicate elements and different data types. An array can be empty, or it may have different data type values.

### How to create an empty array

In JavaScript, we can create an array in different ways. Let us see different ways to create an array. It is very common to use *const* instead of *let* to declare an array variable. If you ar using const it means you do not use that variable name again.

Using Array constructor

```jsx
// syntax
const arr = Array()
// or
// let arr = new Array()
console.log(arr) // []
```

Using square brackets([])

```jsx
// syntax
// This the most recommended way to create an empty list
const arr = []
console.log(arr)
```

### How to create an array with values

Array with initial values. We use *length* property to find the length of an array.

```jsx
const numbers = [0, 3.14, 9.81, 37, 98.6, 100] // array of numbers
const fruits = ['banana', 'orange', 'mango', 'lemon'] // array of strings, fruits

// Print the array and its length

console.log('Numbers:', numbers)
console.log('Number of numbers:', numbers.length)

console.log('Fruits:', fruits)
console.log('Number of fruits:', fruits.length)
```

Array can have items of different data types

```jsx
const arr = [
    'Asabeneh',
    250,
    true,
    { country: 'Finland', city: 'Helsinki' },
    { skills: ['HTML', 'CSS', 'JS', 'React', 'Python'] }
] // arr containing different data types
console.log(arr)
```

### Creating an array using split

As we have seen in the earlier section, we can split a string at different positions, and we can change to an array. Let us see the examples below.

```jsx
let js = 'JavaScript'
const charsInJavaScript = js.split('')

console.log(charsInJavaScript) // ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"]

let companiesString = 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon'
const companies = companiesString.split(',')

console.log(companies) // ["Facebook", " Google", " Microsoft", " Apple", " IBM", " Oracle", " Amazon"]
let txt =
  'I love teaching and empowering people. I teach HTML, CSS, JS, React, Python.'
const words = txt.split(' ')

console.log(words)
// the text has special characters think how you can just get only the words
// ["I", "love", "teaching", "and", "empowering", "people.", "I", "teach", "HTML,", "CSS,", "JS,", "React,", "Python"]
```

## **Arrays are objects**

In JavaScript, arrays are objects. That means that arrays also have some built-in properties and methods.

One of the most commonly used built-in methods on arrays are the **push()** and the **pop()** methods.

To add new items to an array, I can use the **push()** method:

```jsx
var fruits = [];

fruits.push("apple"); // ['apple']

fruits.push('pear'); // ['apple', 'pear']
```

To remove the last item from an array, I can use the **pop()** method:

```jsx
fruits.pop();

console.log(fruits); // ['apple']
```

Tying into some earlier lessons in this course, I can now build a function that takes all its arguments and pushes them into an array, like this:

```jsx
function arrayBuilder(one, two, three) {
    var arr = [];
    arr.push(one);
    arr.push(two);
    arr.push(three);
    console.log(arr);
}
```

I can now call the **arrayBuilder()** function, for example, like this:

```jsx
arrayBuilder('apple', 'pear', 'plum'); // ['apple', 'pear', 'plum']
```

Even better, I don't have to console log the newly built array.

Instead, I can return it:

```jsx
function arrayBuilder(one, two, three) {
    var arr = [];
    arr.push(one);
    arr.push(two);
    arr.push(three);
    return arr;
}
```

Additionally, I can save this function call to a variable.

I can name it anything, but this time I'll use the name: **simpleArr**.

```jsx
var simpleArr = arrayBuilder('apple', 'pear', 'plum');
```

And now I can console log the values stored in **simpleArr**:

```jsx
console.log(simpleArr); // ['apple','pear','plum']
```

### .Include

The **`.includes()`** method is a built-in JavaScript method that is used to check whether a string contains a specified substring or an array contains a specified element. Here's how you can use it:

```jsx
const fruits = ["apple", "banana", "orange"];

function checkFruit(fruit) {
  if (fruits.includes(fruit)) {
    console.log(`Yes, we have ${fruit}!`);
  } else {
    console.log(`Sorry, we don't have ${fruit}.`);
  }
}

checkFruit("apple");   // Output: Yes, we have apple!
checkFruit("pear");    // Output: Sorry, we don't have pear.
checkFruit("banana");  // Output: Yes, we have banana!
```