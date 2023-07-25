# Enabling-ES-Module-Export-Syntax

For ES6 module export/import syntax (e.g: export default todoList; or import  todoList from './daily_todo.js';) set "type": "module" in the package.json or use the .mjs extension.
hence created package.json using npm init
added "type": "module" in package.json and now export working fine

1. linkedinCover.js  --->

<code>

// Today's mood: skip everything, only code
import  todoList from './daily_todo.js';
console.log(todoList);
const mood = (tasks) => tasks.map(task => task = "coding");   
console.log(mood(todoList));

</code>

2. daily_todo.js  ---->

<code>

const todoList = ['a', 'b', 'c'];
export default todoList;

</code>

3. package.json -->

<code>
  
{
  "name": "linkedin_cover",
  "version": "1.0.0",
  "description": "",
  "main": "daily_todo.js",
  "type": "module",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}

</code>


# Suggestions from chatGPT:

Starting from Node.js version 13.2.0, you can use the ES module syntax by either setting "type": "module" in your package.json file or by using the .mjs file extension for your JavaScript files.

To resolve this issue, you have a couple of options:

Option 1: Set "type": "module" in package.json:

Open your package.json file.
Add the following line: "type": "module".
Save the file.
Now you can use the ES module syntax in your code.

Option 2: Rename the file to use the .mjs extension:

Rename your file from daily_todo.js to daily_todo.mjs.
Update the import statement in your code accordingly to use the new file extension.
For example, if you were previously using import { todoList } from './daily_todo.js';, you would now use import { todoList } from './daily_todo.mjs';.
Choose one of these options based on your preference. After making the necessary changes, you should be able to use ES module syntax in your Node.js code without encountering the SyntaxError related to the export statement.
