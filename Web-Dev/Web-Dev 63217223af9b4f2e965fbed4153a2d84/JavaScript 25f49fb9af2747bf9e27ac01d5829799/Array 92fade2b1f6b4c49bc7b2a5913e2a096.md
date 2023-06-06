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

# **Exersices**

LEVEL ONE

```jsx
const countries = [
  'Albania',
  'Bolivia',
  'Canada',
  'Denmark',
  'Ethiopia',
  'Finland',
  'Germany',
  'Hungary',
  'Ireland',
  'Japan',
  'Kenya'
]

const webTechs = [
  'HTML',
  'CSS',
  'JavaScript',
  'React',
  'Redux',
  'Node',
  'MongoDB'
]
```

1. Declare an *empty* array;

```jsx
let emptyArray = [];
```

1. Declare an array with more than 5 number of elements

```jsx
emptyArray=[1,2,3,4,5];
```

1. Find the length of your array 

```jsx
console.log(emptyArray.length);
```

1. Get the first item, the middle item and the last item of the array 

```jsx
console.log(emptyArray[0]);
console.log(emptyArray[Math.floor(emptyArray.length/2)]);
console.log(emptyArray[emptyArray.length-1]);
```

1. Declare an array called *mixedDataTypes*, put different data types in the array and find the length of the array. The array size should be greater than 5 

```jsx
let mixedDataTypes = [1, 'a', 'sami', true,{ country: 'Finland', city: 'Helsinki' }];
console.log(mixedDataTypes.length)
```

1. Declare an array variable name itCompanies and assign initial values Facebook, Google, Microsoft, Apple, IBM, Oracle and Amazon 

```jsx
let itCompanies = ["Facebook", "Google", "Microsoft", "Apple", "IBM", "Oracle", "Amazon"];
```

1. Print the array using *console.log()* 

```jsx
console.log(itCompanies);
```

1. Print the number of companies in the array 

```jsx
console.log(itCompanies.length);
```

1. Print the first company, middle and last company 

```jsx
console.log(itCompanies[0]);
console.log(itCompanies[Math.floor(itCompanies.length/2)]);
console.log(itCompanies[itCompanies.length-1]);
```

1. Print out each company

```jsx
for(i of itCompanies){
  console.log(i);
}
```

1. Change each company name to uppercase one by one and print them out 

```jsx
for(i of itCompanies){
  console.log(i.toUpperCase());
}
```

1. Print the array like as a sentence: Facebook, Google, Microsoft, Apple, IBM,Oracle and Amazon are big IT companies. 

```jsx
console.log(itCompanies.join(' '));
```

1. Check if a certain company exists in the itCompanies array. If it exist return the company else return a company is *not found* 

```jsx
if (itCompanies.includes(searchCompany)) {
  console.log('Company Exists');
} else {
  console.log("Company not found");
}
```

1. Filter out companies which have more than one 'o' without the filter method 

```jsx
let itCompanies = ["Facebook", "Google", "Microsoft", "Apple", "IBM", "Oracle", "Amazon"];

let copyItCompanies = itCompanies.concat();
let fillCompany = [];

for(var i = 0; i<copyItCompanies.length ; i++){
  let count = 0;
  for(var j = 0; j < copyItCompanies[i].length ; j++){
    if(copyItCompanies[i][j] === 'o'){
      count++;
      if(count>1){
        break;
      }
    }
  }
  if(count<1){
    fillCompany.push(copyItCompanies[i]);
  }
}

console.log(fillCompany);
```

1. Sort the array using *sort()* method 

```jsx
console.log(itCompanies.sort());
```

1. Reverse the array using *reverse()* method 

```jsx
console.log(itCompanies.reverse());
```

1. Slice out the first 3 companies from the array 

```jsx
console.log(itCompanies.slice(0,4));
```

1. Slice out the last 3 companies from the array 

```jsx
console.log(itCompanies.slice(3,7));
```

1. Slice out the middle IT company or companies from the array 

```jsx
console.log(itCompanies.slice(2,4));
```

1. Remove the first IT company from the array 

```jsx
let spliceCompany = ["Facebook", "Google", "Microsoft", "Apple", "IBM", "Oracle", "Amazon"];
spliceCompany.splice(0,1)//first item
console.log(spliceCompany);
```

1. Remove the middle IT company or companies from the array 

```jsx
let middleIndex = Math.floor(itCompanies.length / 2);//middle index
let middleCompanies = itCompanies.splice(middleIndex, middleIndex + 1);
console.log(middleCompanies);
console.log(spliceCompany);
```

1. Remove the last IT company from the array 

```jsx
let lastCompany = itCompanies.splice(itCompanies.length - 1, 1);
console.log(lastCompany);
console.log(itCompanies);
```

1. Remove all IT companies

```jsx
console.log(spliceCompany.splice());
```

# Exersice 2

1. Create a separate countries.js file and store the countries array in to this file, create a separate file web_techs.js and store the webTechs array in to this file. Access both file in main.js file

```jsx
// countries.js
export const countries = ["Afghanistan", "Albania", "Algeria", "Andorra", 
"Angola"]; // Add the list of countries here

// web_techs.js
export const webTechs = ["HTML", "CSS", "JavaScript", "React", "Angular",
 "Vue.js"]; // Add the list of web technologies here

//or
// countries.js
const countries = ["Afghanistan", "Albania", "Algeria", "Andorra", "Angola", 
"Antigua and Barbuda", ...]; // Add the list of countries here

module.exports = countries;

// web_techs.js
const webTechs = ["HTML", "CSS", "JavaScript", "React", "Angular", 
"Vue.js", ...]; // Add the list of web technologies here

module.exports = webTechs;

// main.js
const c = require('./countries');
const w =  require ('./web_techs');

console.log("Countries:", c);
console.log("Web Technologies:", w);

/*
=============
//for many exports
=============
*/

//for many exports
// countries.js
const countries = ["Afghanistan", "Albania", "Algeria", "Andorra", "Angola", "Antigua and Barbuda", ...]; // Add the list of countries here
const countryCount = countries.length;

module.exports = {
  countries,
  countryCount
};

// web_techs.js
const webTechs = ["HTML", "CSS", "JavaScript", "React", "Angular", "Vue.js", ...]; // Add the list of web technologies here
const webTechCount = webTechs.length;

module.exports = {
  webTechs,
  webTechCount
};

// main.js
const countriesFile = require('./countries');
const webTechsFile = require('./web_techs');

console.log("Countries:", countriesFile.countries);
console.log("Country Count:", countriesFile.countryCount);
console.log("Web Technologies:", webTechsFile.webTechs);
console.log("Web Tech Count:", webTechsFile.webTechCount);

```

1. First remove all the punctuations and change the string to array and count the number of words in the array

```jsx
let text =
'I love teaching and empowering people. I teach HTML, CSS, JS, React, Python.'
// Remove punctuations from the text using regular expressions
let cleanedText = text.replace(/[^\w\s]/gi, '');

// Convert the cleaned text to an array of words
let words = cleanedText.split(' ');

console.log(words);
console.log(words.length);
```

Explaination

NOTE
Certainly! Let's break down the parameters used in the `replace` method:

1. `/[^\\w\\s]/gi` - This is a regular expression pattern used to match the characters that we want to remove from the `text` string.
    - `/` - The forward slashes indicate the start and end of the regular expression pattern.
    - `[^\\w\\s]` - The square brackets define a character set that matches any character not included in the set.
        - `\\w` - Matches any word character, which includes letters, digits, and underscores.
        - `\\s` - Matches any whitespace character, such as spaces, tabs, or line breaks.
        - `^` - The caret symbol inside the character set negates the set, matching any character not included in the set.
    - `/gi` - These are flags that modify how the regular expression is matched.
        - `g` - Global flag. Matches all occurrences of the pattern, rather than stopping after the first match.
        - `i` - Case-insensitive flag. Makes the pattern match regardless of case.
2. `''` - This is the replacement string that is used to replace the matched characters with an empty string. In this case, we want to remove the matched characters, so we replace them with nothing.

So, in summary, the `replace` method with the regular expression `/[^\\w\\s]/gi` and the replacement string `''` is used to remove all characters from the `text` string that are not word characters (`\\w`) or whitespace characters (`\\s`).

```jsx
//or
const texts = 'I love teaching and empowering people. I teach HTML, CSS, JS, React, Python.';

const words = text.split(/\W+/).filter(word => word.length > 0);

console.log(words);
console.log(words.length);
```

NOTE
Certainly! Let's break down the parameters used in the simplified version of the code:

1. `/\\W+/` - This is a regular expression pattern used as the separator for the `split` method.
    - `\\W` - The capital `\\W` is a shorthand character class that matches any non-word character. It is the inverse of `\\w`, which matches word characters.
    - `+` - The `+` quantifier ensures that consecutive non-word characters are treated as a single separator. It allows multiple non-word characters to be considered as a single delimiter.
2. `text.split(/\\W+/)` - This is the `split` method called on the `text` string with the regular expression `/\\W+/` as the separator.
    - `split()` - The `split` method is used to split the `text` string into an array of substrings based on the specified separator.
    - `/\\W+/` - This regular expression is used as the separator for the `split` method. It matches one or more consecutive non-word characters, effectively splitting the `text` into an array of words.
3. `words` - This is the resulting array after splitting the `text` string into words using the specified separator.
4. `console.log(words)` - This statement logs the `words` array to the console, displaying all the words from the `text` string.
5. `console.log(words.length)` - This statement logs the `length` property of the `words` array to the console, displaying the number of words in the array.

In summary, the `split` method with the regular expression `/\\W+/` is used to split the `text` string into an array of words based on consecutive non-word characters.

```jsx
//output
["I", "love", "teaching", "and", "empowering", "people", "I", "teach"
, "HTML", "CSS", "JS", "React", "Python"]

13
```

1.In the following shopping cart add, remove, edit items

- add 'Meat' in the beginning of your shopping cart if it has not been already added
- add Sugar at the end of you shopping cart if it has not been already added
- remove 'Honey' if you are allergic to honey
- modify Tea to 'Green Tea'

```jsx
const shoppingCart = ['Milk', 'Coffee', 'Tea', 'Honey']
```

1. In countries array check if 'Ethiopia' exists in the array if it exists print 'ETHIOPIA'. If it does not exist add to the countries list.

```jsx
const countries = [
  'Albania',
  'Bolivia',
  'Canada',
  'Denmark',
  'Ethiopia',
  'Finland',
  'Germany',
  'Hungary',
  'Ireland',
  'Japan',
  'Kenya'
]

if (countries.includes('Ethiopia')) {
  let indexOfEthio = countries.indexOf('Ethiopia');
   countries[indexOfEthio] = countries[indexOfEthio].toUpperCase();
  console.log(countries);
}
```

1. Concatenate the following two variables and store it in a fullStack variable.

```jsx
const frontEnd = ['HTML', 'CSS', 'JS', 'React', 'Redux']
const backEnd = ['Node','Express', 'MongoDB']

 let fullStack = frontEnd.concat(backEnd);
 console.log('FullStack: ',fullStack);
```