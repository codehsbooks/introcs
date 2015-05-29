## Using Timers

Timers are a key part of creating animations. As such, they are often used to create fun and interesting graphical programs. Let's take a look at one such program:

```
var MAX_RADIUS = 100;
var MAX_CIRCLES = 1000;
var counter = 0;

function start(){
	setTimer(draw, 50);
}

function draw(){
	drawCircle(Randomizer.nextInt(0, MAX_RADIUS),
			   Randomizer.nextColor(),
			   Randomizer.nextInt(0, getWidth()),
			   Randomizer.nextInt(0, getHeight()));
	
	counter++;
	
	if(counter == MAX_CIRCLES){
		stopTimer(draw);
	}
}

function drawCircle(radius, color, x, y){
	var circle = new Circle(radius);
	circle.setColor(color);
	circle.setPosition(x, y);
	add(circle);
}
```

Let's start by examining the timer. The timer is created at the very beginning of the program in the `start` function.

---

What function is the timer calling?

- ( ) `makeBall`
- (x) `draw`
- ( ) `drawCircle`
- ( ) `start`
- ( ) `timer`

> There is no `makeBall` function in the code.
> Correct!
> The `drawCircle` function is called by the `draw` function, not the timer.
> The `start` function is not called by the timer.
> The timer cannot call itself.

How often does the timer call this function?

- ( ) Every minute
- ( ) Every 50 seconds
- ( ) Every 5 milliseconds
- ( ) Every 5 seconds
- (X) Every 50 milliseconds 

> Incorrect.
> The delay is given in milliseconds, not seconds.
> Note that it is 50 and not 5.
> 
> Correct!

---
