# For Loops

## Repeating Karel Actions
We've learned that functions are a great way to reuse code. But what if we want Karel to put down 100 tennis balls? Let's take a look at the **for loop**!

## Introducing the For Loop
When we want to repeat any of Karel's actions for a fixed number of times, then we can use a for loop. This will allow us to have a bit of code run any number of times that we need. 

The structure of a for loop looks like this: 
```
for(var i = 0; i < count; i++) {
  /* code to execute count times */
}
```
For now, all you need is to set the value of the variable, ```count```. What this code says is, "Repeat the code between the curly braces, count number of times."

Calling the move(); command is the same, but using a For loop is *much* easier:
```
move();
move();
move();
move();
move();
```
is equal to:
```
for(var i = 0; i < 5; i++) {
    move();
}
```
So if you want to repeat commands for a fixed number of times, a for loop will be your new best friend. 

### For Loop Example
So now that we've learned the basics of a for loop, how do we put down five tennis balls?
```
for(var i = 0; i < 5; i++){
    putBall();
}
```
