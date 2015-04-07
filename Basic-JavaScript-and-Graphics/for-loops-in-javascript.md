#For Loops in JavaScript

For loops allow us to repeat code a fixed number of times. A for loop is structured like this:

```
for (var i = 0; i < COUNT; i++) {
    //Code segment that is executed COUNT times.
}
```

## Breaking Down the For Loop

A for loop can be divided into three major parts. The first part **initializes** the loop variable, the second part tests some **condition**, and the third part **increments** or **decrements** the loop variable. Each part of the for loop is separated by a semicolon (`;`). 

Let's break down the following example into its three major parts:

```
for (var i = 0; i < 3; i++) {
    println(i);
}
```

#### Initialize

The first part of a for loop initializes some variable. In the example above, `var i = 0` initially sets the variable `i` equal to `0`. 

#### Condition

The second part of a for loop tests a condition. If the condition is true, the code within the for loop executes. If the condition is false, the code within the for loop is skipped. In the example above, `i < 3` compares the current value of our variable `i` to determine if it is less than `3`. Each time `i` is less than `3`, the value of `i` will be printed to the screen. This happens three times.

#### Increment/Decrement

The third part of a for loop changes the variable after each time the loop runs.


