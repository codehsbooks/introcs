# Mouse Move Events

In the previous chapter, you learned how to respond to a mouse click by using events. But what if you want to respond to a user moving a mouse? What if the user holds the mouse button down? What if they drag the mouse? Surely, there must be a way to handle these other types of events! Well, good news! There is!

## More Mouse Methods

The `mouseClickMethod` is just one of many different mouse methods available. Several more are given below:

| Mouse Method | Responds To|
| -- | -- |
| mouseClickMethod(callbackFunction); | Mouse click |
| mouseMoveMethod(callbackFunction); | Mouse movement |
| mouseDownMethod(callbackFunction); | Mouse pressed down |
| mouseUpMethod(callbackFunction); | Mouse released|
| mouseDragMethod(callbackFunction);| Mouse dragged |

## Using Mouse Methods

If you recall, we respond to a mouse click by doing the following:


```
function start(){
    // This tells the program that when a mouse
    // click happens, the function named
    // 'callbackFunction' should be called
    mouseClickMethod(callbackFunction);
}

// This is the callback function
function callbackFunction(e){
    //Code here to do something when the mouse is clicked.
}
```

Other mouse methods take on the same basic structure. You can just substitute the appropriate mouse method in the `start()` function. For example, we would respond to a mouse being moved by doing:

```
function start(){
    // This tells the program that when a mouse
    // movement happens, the function named
    // 'callbackFunction' should be called
    mouseMoveMethod(callbackFunction);
}

// This is the callback function
function callbackFunction(e){
    //Code here to do something when the mouse is moved.
}
```

### Painting with the Mouse

Let's create a simple painting program using the mouse move method. This program will paint circles along a path when the mouse is moved:

```
function start(){
	mouseMoveMethod(paint);
}

function paint(e){
	var circle = new Circle(15);
	circle.setPosition(e.getX(), e.getY());
	add(circle);
}
```

The `mouseMoveMethod` in the `start()` function automatically detects when the mouse is moved. Each time it detects mouse movement, the `paint(e)` function gets called. 

Within our `paint(e)` function, we create a circle of radius 15. We then set the circle's position. Recall that `e.getX()` and `e.getY()` return the X and Y positions of the mouse's location. Thus, we are setting the circle's position at the mouse's current location. Finally, we add the circle to the screen.

Remember, the `paint(e)` function is called **every time** the mouse moves to a new location. This results in a snake-like trail of circles along the mouse's path.

### Improving Our Painting Program

```
var CIRCLE_RADIUS = 15;

function start(){
	mouseDragMethod(paint);
}

function paint(e){
	var circle = new Circle(CIRCLE_RADIUS);
	circle.setColor(Randomizer.nextColor());
	circle.setPosition(e.getX(), e.getY());
	add(circle);
}
```

### Counting Circles

```
var CIRCLE_RADIUS = 15;
var txt;
var numCircles = 0;

function start(){
    initializeCirclesCounter();
	mouseDragMethod(paint);
}

function paint(e){
	var circle = new Circle(CIRCLE_RADIUS);
	circle.setColor(Randomizer.nextColor());
	circle.setPosition(e.getX(), e.getY());
	add(circle);
	
	updateCounter();
}

function initializeCirclesCounter(){
    txt = new Text("NUMBER OF CIRCLES: ", "14pt Arial");
    txt.setPosition(getWidth()/2 - txt.getWidth()/2, txt.getHeight());
    txt.setColor(Color.blue);
    add(txt);
}

function updateCounter(){
    txt.setText("NUMBER OF CIRCLES: " + ++numCircles);
}
```








