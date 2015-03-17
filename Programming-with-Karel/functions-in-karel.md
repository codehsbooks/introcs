# Functions in Karel
## What Is a Function?

 In the last section, we introduced functions.  But what exactly are functions?  One way of thinking about functions is to think of them being little blocks of commands that Karel knows by a single name.   For example, if we wanted Karel to get the newspaper, we could say "Karel, get the newspaper."  Karel knows that `getNewspaper()` means to go outside, go to the end of the driveway, pick up the newspaper, and bring it back.  Similarly, in our code, we can combine or abstract away many instructions into a single function call.  
   
    
## Why Use Functions?

Why do programmers really really like to use functions?  Simply because they are an easy way  to make code clean, easily understandable, and reusable.  By grouping many instructions together and giving them a single name, we can make the code read like a story. Remember teaching Karel how to turn right?  It's much easier to understand `turnRight()` than to mentally compute what calling `turnLeft()` 3 times does every time we see it.

Furthermore, creating functions lets us break down the problem we are trying to solve.  If we have a very complicated problem, such as getting the newspaper, we want to break it down into steps.  This has two big advantages over trying to cram all of the code into a single space.  First, we can focus on one step at a time.  Sometimes we don't know how to solve all of the pieces of the problem, but we can get started by solving the pieces we do know. For example, we might know how to get Karel to pick up the newspaper, but we're unsure about how to get Karel to the newspaper.  We can define 2 functions, `pickUpNewspaper()` and `goToNewspaper()`.  Then we can focus on making `pickUpNewspaper()` first.  Second, it saves us time.  Once we break down the problem, it's possible that we notice that some of the parts are really just repeats of the same problem.  For example, in getting the newspaper, going to the newspaper and coming back will both require pointing Karel in the right direction and moving.  We can group these instructions into the same command, or function, and reuse the function in both places!

## Creating Functions

Now we've seen why functions are great.  How do we go about creating them?  There are a few specific rules that MUST be followed to create a function that Karel will understand.

### Naming is Crucial

The very first thing we have to decide when creating a function is what to name it.  The name of the function is an extremely important aspect of how useful the function will be. The name of a function should always be an action describing the function, just like `move()` or `putBall()` are actions.  The name of the function should specifically describe what the function does.  Naming a function `functionOne()` or `doStuff()` is not useful at all.  What do these functions do?  You can't tell from the names!

Function names must also follow a particular format. Functions whose names are are made up of more than one word are always written in a style called Camel Case.  The first word of a function is lowercase, but all of the other words begin with upper case letters.  For example, `goToEnd()` is in Camel Case, but `StopAtWall()` and `buildtower()` are not.  Functions should always start with a letter and not contain any other characters besides letters and numbers.  This means that a function name MUST NOT contain spaces.  For example, `34BallPickUp()` is not a valid function name, nor is `pickUpBalls!()`, and neither is `pick up all the balls()`.  These are bad function names.  However, `pickUp34Balls()` is good because it starts with a letter and only contains letters and numbers.  Note, however, that usually functions can be named successfully only using letters.

### Rules for Defining a Function

After the function has a legal, descriptive name, the next step in creating a function is to declare and define the function.  A function is made up of 3 parts: the keyword *function*, the name of the function followed by parenthesis, and the body of the function.  The body of the function must be between two curly braces {}.  An example of a function is below.

```
function pickUpThreeBalls() {
  // code to pick up three balls goes here
}
```

Note the keyword *function* appears before the name of the function.  The name of the function is legal.  It has no spaces, is in Camel Case, and only has letters. After the name is a set of parenthesis.  Then come the curly braces with the commands we want Karel to do when we call `getNewspaper()` inside of them.  

### Defining a Function vs. Calling a Function

At this point, we have defined a function called `pickUpThreeBalls()`.  The above example is the definition of the function.  In order to use the function, we have to call the function.  This means we simply write `pickUpThreeBalls();` in our code.  We don't have to have *function* or the function body; those parts belong to the definition. For example, calling our function would look like the following.

```
move();
pickUpThreeBalls();
move();
```

The surrounding `move()` commands, or function calls, aren't required to use our function. They are merely there for illustration.  The only required part of calling the function is using the function's name followed by a set of parenthesis and ended with a semicolon.

## Function Definition Practice

Use this quiz to test your understanding of functions!

---

Which of the following are good function names?
- [x]  goToEnd()
- [ ] function one()
- [ ] superimportantfunction()
- [ ] otherSuperImportantFunction()
- [x] climbUpTower()
- [ ] 123EasyAsPie()

> Yes! It describes what it does, is in Camel Case, and doesn't have any illegal characters.
>
> No! Function names cannot have spaces, and this name does not describe what the function does.
>
> No! It is not in Camel Case or very descriptive.
>
> No! It is not a very descriptive name.
>
> Yes! It describes what it does, is in Camel Case, and doesn't have any illegal characters.
>
> No! Functions cannot start with a number.

---

## The `turnAround()` Function

Let's make a new function to teach Karel how to turn around.  After we call this function, we want Karel to be facing the opposite direction than the direction Karel was facing before.

### Defining `turnAround()`

##### Step One: Naming the Function 
The action we want Karel to take is to turn around, so we will name our function `turnAround()`.  Note the name is Camel Case, has no spaces, and has only letters.  The name is an action, and it exactly describes what the function accomplishes.

##### Step Two: Declaring the Function 
We need to tell Karel we're going to define a new command, or function. The function declaration looks like

```
function turnAround(){

}
 ``` 
##### Step Three: Defining the Function 
The function needs commands in the function body.  One implementation, or group of commands to solve the problem, is the following.

```
function turnAround(){
    turnLeft();
    turnLeft();
}
```

Note that the commands that define the function go inside of the curly braces.

That's it! We now have a definition for the function `turnAround()`.

### Calling `turnAround()`
Defining a new function is pretty pointless unless we actually use it.  

Let's create a program to make Karel walk forward, turn around, and come back.
It would look like

```
move();
move();
move();
turnAround();
move(); 
move();
move();
```

That's all it takes to use our function.  Can you spot another place in this program where using a function would be useful?  Try it out!







 