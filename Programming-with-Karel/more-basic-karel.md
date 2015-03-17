# More Basic Karel

## Karel's World
You can think of Karel's world as a grid. At any time, Karel occupies the space at a specific row and column. We call rows **streets** and columns **avenues**. 

## Karel's Directions
The world is organized along the basic cardinal directions (clockwise, from the top: North, East, South, West). Karel is aware of the direction he's facing. You can use functions like ``facingEast()`` and ``notFacingEast()`` to control Karel's direction, but we'll get more into that later.

## Using Karel's Commands 
We can use Karel's commands to create new **programs**. A program is like a list of actions that we want Karel to perform.

Let's have Karel put down a ball in the middle of the world, as shown below.

![Move, turn, and put a ball](../static/karel-more-basic-karel.gif)

The first command we'll need is `move();` to have Karel move forward. Then Karel will `turnLeft();` and `move();` again to get to the center of the world. Once there, Karel can use `putBall();` to set down a ball, then `turnLeft();` three times to face the starting direction.

We can write out the program like a list:

    move();
    turnLeft();
    move();
    putBall();
    turnLeft();
    turnLeft();
    turnLeft();








