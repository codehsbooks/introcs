# Commenting Your Code
Now that we know how to structure our program, let's discuss how to style our program.  Your code is useless if nobody else can tell what it does.  You'd be surprised how fast it even becomes useless to you yourself because you've forgotten what the goal of the program is. To avoid this unfortunate problem, each program you write must first be structured in a logical way.  Each small step gets tucked away inside of a function.  Then, all of your code must contain comments to more completely describe in English what happens in your program.  Naming your functions sensibly goes a long way, but English is often more quickly decipherable.  


## Commenting Code
Comments are special lines of your program that are not written in code, but in plain English.  Comment lines begin with special characters, as shown below

```
/*  This is a multiline comment.  That
* means that every line that starts with
* a star (astrisk) is a comment. It must
* be ended correctly or it will extend
* forever
*/

// This is a single line comment. It ends here.

```
Comments are absolutely essential in allowing other people to read and understand your code.  At the very least, every single one of your functions should have a comment.  If you have a complicated chunk of code, or need to explain the process, then you can (and are encouraged!) to put single line comments inside of your functions.  However, you do **not** need to comment *every* line of your program.  


### Preconditions and Postconditions
We said that all of your functions should have comments.  What should those comments look like?  

Every function comment should contain a few words describing the goal of the function.  This can be captured in the  precondition and postcondition of your function.  The precondition describes what assumptions about the world the function makes and what must be true in the world **before** the function is done.  Postconditions describe the state of the world **after** the function is called. 

Remember, 
1. Precondition - what is true about the world before the function is called
2. Postcondition - what is true about the world after the function is called.


##  Test Your Understanding
See how well you understand comments:

---
<p>
For each question, is each code snippet commented correctly?  Some of the functions aren't all the way implemented.  That's ok.  Focus on the quality of the comments.
</p>
<p>
// Moves Karel to the end of the street </br>
move(); </br>
move(); </br>
move(); </br>
</p>
- [x] Yes
- [ ] No

> Right!
> This is not correct.  This code is not commented usefully because we know that 3 moves will move Karel 3 spaces forward, the comment describes the purpose of the commands. 

<p>
/*
This function moves Karel </br>
</br>
function turnRight(){ </br>
} </br>
</p>
- [ ] Yes
- [x] No

> This is not correct.  First, the comment isn't formatted correctly.  There should be a "*/" at the end of the comment, or it should be a single line comment and use "//".  Second, the comment doesn't help us understand what the function's purpose is.
> Right! 

<p>
// moves forward one space </br>
move(); </br>
// moves forward another space </br>
move(); </br>
</p>
- [ ] Yes
- [x] No

> This is not correct.  This piece of code has too many comments!  We know what the move function does.
> Right! 

<p>
/*
* This function makes Karel jump over a hurdle </br>
* Precondition: Karel is standing directly in front of a hurdle, and is facing East </br>
* Postcondition: Karel is standing directly behind a hurdle, and is facing East </br>
*/ </br>
</br>
function jumpHurdle(){ </br>
    // code would go here. </br>
} </br>
</p>
- [x] Yes
- [ ] No

> Right!
> This is not correct.  The comment above is exactly what a function comment should look like.  It describes the purpose of the function, the preconditions (what we assume is true about the world before the function is called), and the postconditions (what the world will be like after the function is called) 

---
