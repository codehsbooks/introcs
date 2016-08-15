# Loop-and-a-half

Loops are powerful and efficient. At this point you are familiar with the for loop and the while loop.
Now we'll combine a few concepts together to introduce a new style of loop: the loop-and-a-half.

## The Infinite Loop

Up until now, you've likely been avoiding writing infinite loops in your code. Infinite loops are loops that have no exit condition.
Once a program starts running such a loop, there is no escape. The loop will continue to execute forever, causing the program to freeze and crash.

An example of an infinite loop is:

```
while(true) {
    // code to execute
}
```

This loop executes as long as the condition it checks is true. But the condition it checks is just `true`!

## The Break Statement

Break statements allow us to exit a loop. If a program is executing a loop and it runs across the `break` keyword,
it will "break out" of the loop and move on to the next commands after the loop.

This can be combined with the while loop given above to provide a way to exit the loop:

```
while(true) {
    // code to execute
    
    if(condition) {
        break;
    }
}
```

Once the condition becomes true, the if statement is run, `break` is called, and the loop is finished.

## The Sentinel

It is often useful to check values against a "sentinel" value. A sentinel value can be any predetermined value.
For example, if you were writing a program to respond to a user if the user types "hello world,"
you could set up a global sentinel value containing the string "hello world."

```
var SENTINEL = "hello world";

function start() {
    var input = readLine("Type in some text: ");
    if(input == SENTINEL) {
        println("Hello to you as well!");
    }
}
```

Sentinels can be used with loops and breaks to create a "loop-and-a-half." A while loop can be set to execute with a
`true` condition. Then, if the condition checked equals the `SENTINEL` variable, break will be called, thereby 
ending the loop.

```
var SENTINEL = -1;

function start(){
    while(true){
        var num = readInt("Enter a number: ");
        if(num == SENTINEL){
            break;
        }
        println(num);
    }
}
```

The program above loops until the user enters the sentinel value of `-1`.

It is often easier to reason through the logic behind a loop-and-a-half. 
Additionally, loop-and-a-half structure is preferred because it avoids repeating code outside and inside the loop. 
