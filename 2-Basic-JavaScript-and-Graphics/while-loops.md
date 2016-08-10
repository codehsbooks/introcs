# While Loops
While loops should sound familiar.  Remember doing while loops with Karel?  While loops in JavaScript work exactly the same way!


### What are While Loops?
While loops are a way to repeat a block of code.  The basic syntax of a while loop is shown below.

``` 
while(condition){
    // code block to be done if condition is true
}

// code executed if condition is false
```

The code that goes inside of the curly braces will be executed repeatedly until the condition in parenthesis becomes false. Once the condition becomes false, the program continues to the code following the while loop body.  For example, suppose you are eating a bowl of cereal for breakfast.  If you were a program, the while loop controlling your actions could look like 

```
while(cerealLeftInBowl == true){
    eatCereal();
}
```
In English, this means that while there is cereal left in your bowl, you will eat the cereal.  Once the cereal is gone, you will stop eating cereal and continue on to the next part of your day.  In the same way, once the while condition ```cerealLeftInBowl == true``` evaluates to false, the program will continue to the next statement.

Notice that while loops are similar to for loops.  The main difference is while loops allow code to be repeated even if you don't know how many times the code needs to be repeated.  While loops are also convenient when you want to repeat code based on user input.

### While Loop Syntax
As you have seen above, to use a while loop, use the **while** keyword followed by a condition to evaluate in parenthesis. This condition can be any valid Boolean expression or combination of Boolean expressions.  It can even be a single Boolean variable.  If the Boolean variable's value is true, this has the same effect as an expression evaluating to true.  Then, any code that should be executed if the condition is true goes inside the curly braces following the condition.

There are a few things to be careful about.  Do not put a semicolon after the parenthesis.  To the computer, this means that the while loop has no block of code to execute that belongs to it.

```
// THIS IS WRONG!!!!
while(condition); {
    // The semicolon often creates an infinite loop -- your program will simply stall 
    
    // this part is not attached to the while loop
    // if the condition is false, this code will be executed anyway
    // because of the semicolon after the parenthesis
}

```
In addition, do not put a semicolon after the closing curly brace.
```
// THIS IS WRONG!!!!
while (condition) {
    // code to execute if condition is true
    
};  // this semicolon should NOT be here

```

The code in the curly braces after the while loop should be indented to indicate to other people reading the code that the code is part of the while loop.

Let's look at a correctly formatted while loop:
```
// This while loop is formatted correctly.
// There are no extra semicolons and the block is indented

while(condition){
    // code block to execute if condition is true
}

// This while loop is also formatted correctly.
// The curly braces can be placed like this, too.
// Just be consistent with your curly brace styling!

while(condition)
{
    // code block to execute if condition is true
    
}

// code that is executed if condition is false


```
### While Loop Examples
Let's look at a few examples of how to use while loops.
##### Counting Down
This while loop counts down from 10 to 1, printing out the numbers as it goes.

```
var i = 10;
while (i > 0){
    println(i);
    i--;
}
println("Done Counting!");

```

The output of this loop would be 
```
10
9
8
7
6
5
4
3
2
1

```


This while loops depends on user input to decide when to quit looping

```
var code = 3;
var userGuess = 0;

while(userGuess != code){
    userGuess = readInt("Guess my number! ");
}

println("Yup! 3 is my number!");

```
While the user guesses an incorrect number, he'll be asked to input another number.  As soon as he gets it right, the program will end.

### Beware of Infinite Loops
One last warning before we end.  Beware of infinite loops!  Infinite loops occur when there is no way that the condition can become true.  For example, if we had forgotten to put ```i--;``` in the first example while loop, the value of ```i``` would never change.  Every time the condition was checked, ```i``` would be 10.  The loop would run forever!

```
// This is an infinite loop!!

var i = 10;
while (i > 0){
    println(i);
}

// the value of i never changes!!
```


To avoid infinite loops, double check that the condition you are using can become false INSIDE of the while loop body.  Some variable that is used inside of the condition must be modified inside of the loop.

```
// Not an infinite loop

var i = 10;
while (i > 0){
    println(i);
    i --; // this line changes the value of i
            // now the condition will eventually evaluate to false.
}

```

