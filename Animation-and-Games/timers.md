# Timers
Animation is a key aspect of many types of computer programs. This is especially true of games. For example, you'll to create a game like Breakout, you'll need to make use of animations to bounce a ball around the screen and move the player's paddle. A good understanding how animation works will be beneficial as you design and build more complex programs. 

## The Idea of Animation
Animation can be broken down into three basic steps:
- Draw
- Wait and Move
- Repeat

You may recall creating flipbook animations in the corner of a notebook -- this is essentially the same process. Each page of a flipbook draws a similar image that is moved slightly. Flipping rapidly through the pages of the flip book causes the image to appear to move. This is one of the earliest forms of animation, known originally as the kineograph.

![Basics of Animation](../static/javaScript/animation_timers_flipbook.png "Linnet kineograph 1886 by Original author is de:John Barnes Linnet. Original uploader was Lothar Laaf at de.wikipedia - Zeitgenössische Illustration (1886), via de.wikipedia. Licensed under Public Domain via Wikimedia Commons - http://commons.wikimedia.org/wiki/File:Linnet_kineograph_1886.jpg#/media/File:Linnet_kineograph_1886.jpg")

We can explore the basics of animation by having a circle move across the canvas from top to bottom.

#### Draw
Drawing is how elements are displayed on the canvas. As you learned in the previous chapter, an element is first created and given a position, then it is added to the canvas.

In this case, we will draw a black circle at position `(50, 50)`.

var ball;

```
function start(){
	ball = new Circle(20);
	ball.setPosition(50, 50);
	add(ball);
}
```

![Basics of Animation](../static/javaScript/animation_timers_ball1.png "Basics of Animation")

#### Wait and Move
Now that the ball is on the screen, we want to wait a moment, then move the ball toward the bottom of the canvas. If we moved the ball right away without waiting, then the user would only see the ball after it has been moved. This delay is essential to creating the animation effect.

We can move the ball with the `move(x, y)` method. This method will move the object `x` pixels in the x direction, and `y` pixels in the y direction. In our case, we want the ball to fall straight down, so we will have `x` change by 0 and `y` change by 5.

```
ball.move(0, 5);
```

But how do we have the program wait before moving the ball? And what about repeating the process? A loop won't quite work, as there's no way to have a loop pause between iterations. We'll need to use a new tool, the **timer**, to create our animation.



## Introducting Timers

## Using a Timer

