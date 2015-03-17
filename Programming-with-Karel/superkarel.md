# SuperKarel

## A Smarter Karel the Dog
Introducing... SuperKarel! 

SuperKarel already knows ```turnRight()``` and ```turnAround()```, so you don't need to create your own functions for those two commands anymore!

Here is an example of Karel jumping a hurdle:
```
function jumpHurdle() {
    turnLeft();
    move();
    turnRight();
    move();
    turnRight();
    move();
    turnLeft();
}

function turnRight() { 
    turnLeft();
    turnLeft();
    turnLeft();
}
```
And here is SuperKarel jumping a hurdle:
```
function jumpHurdle() {
    turnLeft();
    move();
    turnRight(); 
    move();
    turnRight();
    move();
    turnLeft();
}
```
SuperKarel will automatically turn right when ```turnRight()``` is called, and will turn around when ```turnAround()``` is called.

