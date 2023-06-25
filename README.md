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
