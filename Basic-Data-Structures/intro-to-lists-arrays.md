<h1>Intro to Lists and Arrays</h1>

Storing, accessing, and manipulating lists of data is an essential and fundamental facet of programming. The most basic storage type is called an <b>array</b>. 

Arrays are ordered lists. Each item in the array is called a <b>member</b>, and each member's position is called its <b>index</b>.

<h3>Array Syntax</h3>
Arrays are denoted by square brackets []. When creating an array, write each element inside the square brackets, separated by a comma. 

See the code snippet below for an example.
```
var myArray = [1, 10, 100, 1000];
```

Arrays with no elements an be created using the following syntax:
```
var myEmptyArray = [];
```

<h3>Special Note on Mutability</h3>
Arrays on most programming platforms have finite length. That means that the number of elements in the array cannot differ from the number of elements at the time that the array was created. <u>This rule does not apply on the CodeHS platform.</u> Our arrays have mutable length, meaning you can add and remove elements as you wish. 
