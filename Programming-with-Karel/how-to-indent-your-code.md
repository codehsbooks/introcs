# How To Indent Your Code

## The Reason You Want to Indent

Before we talk about how to indent code, let's briefly discuss *why* you want to indent your code.

Indentation is a fundamental aspect of code styling, and plays a large role in influencing readability.  First of all, indented code is easier to read through than unindented code.  Compare the following:

```javascript
//Oh no! Ugly unindented code!
function start(){
turnLeft();
move();
putBall();
if (frontIsClear()){
move();
}
}
```

```javascript
//This indented code looks nicer!
function start(){
    turnLeft();
    move();
    putBall();
    if (frontIsClear()){
        move();
    }
}
```

With unindented code, the overall **structure** of the code might be somewhat difficult to see.  However, with indented code, the overall structure of the code jumps out at you.  Tabs tell you that a line of code is inside a function, loop, if statement, or else statement.  Knowing which parts of the code is inside what will become especially important in the non-Karel Javascript sections.

In addition, indentation errors can be hugely misleading. Consider the following code:

```javascript
while(notFacingLeft())
    turnLeft();
    move();
```

Because the code on line 3 is indented, it may seem to be part of the body of the while loop. But, remember that without brackets, the while loop body can only consist of one line of code. So, this code is really equivalent to:

```javascript
while(notFacingLeft()) {
    turnLeft();
}
move();
```

This is why we like to **always put brackets** for our loops and if/else statements, because without them, it is easy for beginner programmers to make mistakes!

And lastly, if you plan on pursuing a career in computer science or any similar career in which you write code, many companies will want you to properly indent your code as you write your programs.

## How You Should Indent Your Code

Basically, the general rule for indenting is that **code between curly brackets should be indented**.  Curly brackets are `{` and `}`.

So let's take a look at this unindented code:

```javascript
function example(){
move();
move();
turnLeft();
turnRight();
turnAround();
turnAround();
putBall();
takeBall();
}
```

How should this be indented? Well, let's remember our general rule... **code between curly brackets should be indented**.  See the curly brackets in the `example()` function? Now we look at everything in between those curly brackets, and we indent all the code there one time by pressing the tab key.  So the correctly indented version would be this:

```javascript
function example(){
    move();
    move();
    turnLeft();
    turnRight();
    turnAround();
    turnAround();
    putBall();
    takeBall();
}
```

So how about if inside of a set of brackets is another set of brackets? Well, if there is a set of brackets inside another set of brackets, you will indent one time for each set of brackets your code is in between.

So for example, let's say that we have this unindented code:

```javascript
function karelImpressesVegeta(){
for(var i = 0; i < 9001; i++){
putBall();
}
}
```

Notice how there is a set of curly brackets for the `karelImpressesVegeta()` function and a set of curly brackets for the for loop that is inside.  To indent this code properly, we can think of this in two steps:

**Step 1:** Indent everything between the function's brackets
```javascript
function karelImpressesVegeta(){
    for(var i = 0; i < 9001; i++){
    putBall();
    }
}
```

**Step 2:** Indent everything between the for loop's brackets:
```javascript
function karelImpressesVegeta(){
    for(var i = 0; i < 9001; i++){
        putBall();
    }
}
```

And there you go! Another successfully indented piece of code!

What if we had more brackets? What if we had many brackets?

```javascript
function karelIsBored(){
if(frontIsClear()){
while(ballsPresent()){
takeBall();
}
move();
}
else{
while(ballsPresent()){
takeBall();
if(facingNorth()){
turnLeft();
}
else if(facingSouth()){
turnRight();
}
}
turnLeft();
if(frontIsClear()){
move();
}
turnRight();
}
}
```

Try to see if you can indent all that code correctly...

The correctly indented version for the above example is this:

```javascript
function karelIsBored(){
    if(frontIsClear()){
        while(ballsPresent()){
            takeBall();
        }
        move();
    }
    else{
        while(ballsPresent()){
            takeBall();
            if(facingNorth()){
                turnLeft();
            }
            else if(facingSouth()){
                turnRight();
            }
        }
        turnLeft();
        if(frontIsClear()){
            move();
        }
        turnRight();
    }
}
```

## Should You Use Tab or Space to Indent?

Technically, it is fine to either indent using the tab key or with the space bar.  Indenting once with the tab key means just pressing the tab key once.  Indenting once with the space bar means pressing the space bar 4 times.

Even though you can indent using tab or space, ***indenting using the tab key is recommended***, because there are higher chances of making mistakes in indenting if you use the space bar (like if you press the space bar 3 times instead of 4).
