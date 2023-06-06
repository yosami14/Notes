# Accessing JS Files in JS

Here's how you can achieve that.

1. Create a `countries.js` file:

```jsx
// countries.js
const countries = ["Afghanistan", "Albania", "Algeria", "Andorra", "Angola", "Antigua and Barbuda", ...]; // Add the list of countries here

module.exports = countries;

```

1. Create a `web_techs.js` file:

```jsx
// web_techs.js
const webTechs = ["HTML", "CSS", "JavaScript", "React", "Angular", "Vue.js", ...]; // Add the list of web technologies here

module.exports = webTechs;

```

1. Create a `main.js` file:

```jsx
// main.js
const countries = require('./countries');
const webTechs = require('./web_techs');

console.log("Countries:", countries);
console.log("Web Technologies:", webTechs);

```

1. Now, if you run the `main.js` file, you should see the lists of countries and web technologies printed in the console.

Make sure that all three files (`countries.js`, `web_techs.js`, and `main.js`) are in the same directory for this to work properly.

1. **ES6 Modules**: If you are working in an environment that supports ES6 modules (such as recent versions of Node.js or modern browsers), you can use the `export` and `import` statements to export and import the arrays directly. Here's an example:
    
    ```jsx
    // countries.js
    export const countries = ["Afghanistan", "Albania", "Algeria", "Andorra", "Angola", "Antigua and Barbuda", ...]; // Add the list of countries here
    
    // web_techs.js
    export const webTechs = ["HTML", "CSS", "JavaScript", "React", "Angular", "Vue.js", ...]; // Add the list of web technologies here
    
    // main.js
    import { countries } from './countries';
    import { webTechs } from './web_techs';
    
    console.log("Countries:", countries);
    console.log("Web Technologies:", webTechs);
    
    ```
    
    Note that to use ES6 modules in Node.js, you'll need to specify `"type": "module"` in your `package.json` file or use the `.mjs` file extension.
    
2. **Browser Environment**: If you're working in a browser environment, you can include the `countries.js` and `web_techs.js` scripts using `<script>` tags in your HTML file. Then, you can access the exported arrays from the global scope in your `main.js` file. Here's an example:
    
    ```jsx
    <!-- index.html -->
    <html>
      <body>
        <script src="countries.js"></script>
        <script src="web_techs.js"></script>
        <script src="main.js"></script>
      </body>
    </html>
    
    <!-- countries.js -->
    const countries = ["Afghanistan", "Albania", "Algeria", "Andorra", "Angola", "Antigua and Barbuda", ...]; // Add the list of countries here
    window.countries = countries;
    
    <!-- web_techs.js -->
    const webTechs = ["HTML", "CSS", "JavaScript", "React", "Angular", "Vue.js", ...]; // Add the list of web technologies here
    window.webTechs = webTechs;
    
    <!-- main.js -->
    console.log("Countries:", countries);
    console.log("Web Technologies:", webTechs);
    
    ```
    
    In this case, the arrays are attached to the `window` object and can be accessed from any script in your HTML file.
    

These are just a couple of examples. The specific method you choose will depend on the environment you're working in and the module system you prefer to use.

## Export the entire file

 To export the entire file, you can assign the `module.exports` to an object that contains all the exports. Here's an example:

In the `countries.js` file:

```jsx
// countries.js
const countries = ["Afghanistan", "Albania", "Algeria", "Andorra", "Angola", "Antigua and Barbuda", ...]; // Add the list of countries here
const countryCount = countries.length;

module.exports = {
  countries,
  countryCount
};

```

In the `web_techs.js` file:

```jsx
// web_techs.js
const webTechs = ["HTML", "CSS", "JavaScript", "React", "Angular", "Vue.js", ...]; // Add the list of web technologies here
const webTechCount = webTechs.length;

module.exports = {
  webTechs,
  webTechCount
};

```

In the `main.js` file:

```jsx
// main.js
const countriesFile = require('./countries');
const webTechsFile = require('./web_techs');

console.log("Countries:", countriesFile.countries);
console.log("Country Count:", countriesFile.countryCount);
console.log("Web Technologies:", webTechsFile.webTechs);
console.log("Web Tech Count:", webTechsFile.webTechCount);

```

Now, when you run the `main.js` file, it will access the exported objects from the `countries.js` and `web_techs.js` files, and you can access the arrays and other variables defined in those files using dot notation (`countriesFile.countries`, `countriesFile.countryCount`, `webTechsFile.webTechs`, `webTechsFile.webTechCount`).

This approach allows you to export multiple variables, functions, or objects from a file and access them individually in other files.