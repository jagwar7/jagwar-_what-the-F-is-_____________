
==============================================================================================================================================
What is Babel, in Simple Terms?  
--------------------------------

Babel is a JavaScript compiler. Its main job is to transform code.

In this time (2025) we developers write modern Javascript code (ES6+) , bable translate our modern codes into  old  Javascript,  so  that  old 
version browser which doesnt support latest Javascript, can run latest website.

Example => There is a browser internet explorer running on windows xp or windows 7, which support old version of Javascript. The new   website
           which is built on ES6+, can be ran in that old internet explorer. So, Bable translates new version code into  old  version  of code
==============================================================================================================================================





==============================================================================================================================================
How Babel Actually Works ?
--------------------------
Babel's process is typically a three-step process: Parse, Transform, Generate.

Parse:=> Babel reads your modern JavaScript code and turns it into a data structure called an Abstract Syntax Tree (AST). This is a fancy  way
         of saying it understands the structure and meaning of your code (e.g., this is a variable declaration, that is a function call).

Transform:=> This is the most important step. Babel traverses the AST and applies a series of plugins. Each plugin is   a  small    JavaScript
         program that knows how to transform one specific piece of modern syntax into its older equivalent.

Generate:=> Babel takes the transformed AST and converts it back into regular JavaScript code, now written in the older, target syntax.
==============================================================================================================================================




==============================================================================================================================================
Example:=> 
        Modern Code(ES6+):
            const myFunction = () => {
                console.log("Hello from an arrow function!");
            };


        Bable transformed  old code:
            var myFunction = function myFunction() {
                console.log("Hello from an arrow function!");
            };
==============================================================================================================================================





==============================================================================================================================================
Bable in React JS:
------------------

In React Projects (and Web Projects in general)
JSX: React uses JSX (the HTML-like syntax inside JavaScript: <MyComponent prop="value"/>). Browsers do not understand JSX. It's not a standard
JavaScript feature. The number one job of Babel in  a React  project (via the @babel/preset-react preset)  is  to  compile  JSX  into  regular
JavaScript function calls (React.createElement(MyComponent, { prop: "value" })).

Modern JavaScript: As explained above, it also compiles modern ES6+ JavaScript down to ES5 for broader browser compatibility.



Bable in Android:
-----------------

In Android (React Native) Projects, When you see Babel in an Android project, Its mean you are working with React Native App development   for
Android. React Native lets you write mobile apps using JavaScript and React. The JavaScript code you write for React Native also uses JSX  and 
modern JavaScript (ES6+).
However, this code doesn't run in a browser it runs on a JavaScript engine inside the mobile app (e.g Hermes on Android/iOS or JavaScriptCore)

These mobile JavaScript engines may not support all the latest JS features. So Babel is used during the build process of your React Native app 
to transform your source code into a version of JavaScript that the mobile engine can execute reliably.
==============================================================================================================================================
