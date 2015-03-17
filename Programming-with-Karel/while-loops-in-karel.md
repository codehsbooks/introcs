# While Loops in Karel
 
## Repeating Karel Actions
We've already learned that we can repeat Karel actions with a for loop. What if we want to move all the way to a wall? In this case, since we don't know how long the world is, we can't put a fixed number in the loop. Is there another type of loop that can handle repeating code when we don't know how many times to repeat? Yes!

## Introducing While Loops
Let's say that we're baking a cake: The recipe says that we need to mix the ingredients together until the batter isn't clumpy. That may take five minutes or it may take ten, but we need to keep stirring until the batter is smooth.  

While loops will allow us to repeat code as long as a condition is true. This is different from for loops, which repeat a fixed number of times. 

A while loop looks like: 
```
while(condition) {
   // code to execute while
   // condition is true
}
```
The code above is saying, "While some condition is true, execute the code in the curly brackets until the condition is false." 

### While Loop Example
Let's look at the question above. What if we want to move all the way to a wall?
```
while(frontIsClear()) {
    move();
}
```
If the front is clear when Karel starts out, she will move forward once. Then, we'll go back to the start of the loop and ask, "Is the front still clear?" If yes, then Karel will move again.

We'll keep repeating until we ask "Is the front still clear?" and the answer is no, at which point Karel will stop moving. This same logic will work on worlds of different sizes, too! 

So, while the condition "you enjoy coding" is true, read on!
