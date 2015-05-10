# Mouse Click Events

Sometimes we want the user to be able to interact with our programs.  We've seen how to do this by asking questions, but suppose we want the user to pick  location on the screen.  It'd be annoying for the user to have to figure out the X and Y coordinates of the spot.  This is one instance where using Mouse Click Events comes in handy.  All the user has to do is click on the chosen spot, and the program gets all of the information it needs.


## What are Events?
In spoken English, events usually refer to special gatherings, like sporting events or parties.  In computer science, events are actions that happen that the program needs or wants to respond to.  Here, we are specifically talking about mouse events.  Mouse events are "triggered" or "fired" whenever the user does something with the mouse, such as moving the mouse or clicking the mouse.  In this section, we'll focus on mouse click events.

## Responding to Events
To respond to an event, we have to set up special method called a Callback Method.  This method gets called when the program detects an event.  We also have to tell the program that we want to associate a particular method with an event. This is referred to as "registering a callback".  For mouse click events, this looks like

```
function someFunction(){
    // This tells the program that when a mouse
    // click happens, the function named
    // 'callbackFunction' should be called
    mouseClickMethod(callbackFunction);
}
// This is the callback function
// Notice it has a single parameter, e
function callbackFunction(e){
}
```


Let's look at an example.  Suppose I want to print out a star every time the user clicks anywhere on the screen.  The code would look like the following

```
function start(){
    // register the callback function
    mouseClickMethod(printStar);
}

// Callback method
// Prints out a single * 
function printStar(e){
    print("*");
}
```

There are a few things to note about this code.
1.  The callback method can be named any legal function name
2.  The callback method for mouse clicks must be registered by using ```mouseClickMethod```
2.  Do not put () after the function name when registering the callback
3.  The callback method always takes  single parameter, typically named ```e```
4.  The callback method is **always** called when the event it is registered to occurs

## Getting Event Information
Now that we've seen a basic callback function, let's discuss the parameter ```e```.  This parameter is an Event object.  It holds information about the event that called the callback function.  Remember using Circles and Rectangles?  You could call methods like ```circle.getX()``` to get the circle's x position.  You can do the same thing with the event object!

The event object has 2 functions we're interested in right now.  It has ```getX()``` and ```getY()```.  These methods return the X and Y position of the mouse click.  For example, the following code snippet will print out the X and Y locations of where the user clicked.

```
function start(){
    // register the callback function
    mouseClickMethod(printCoordinates);
}

// Callback method
// Prints out the (x,y) coordinates of the 
// mouse click
function printCoordinates(e){
    println("You clicked on spot (" + e.getX() + ", " + e.getY() + ")");
}
```

One output looks like this
```
You clicked on spot (42.90625, 77.5555419921875)
You clicked on spot (242.90625, 255.5555419921875)
You clicked on spot (78.90625, 372.5555419921875)
You clicked on spot (245.90625, 386.5555419921875)
```
## Putting It All Together
One final point to consider is the fact that the callback method only takes a single parameter.  What if the function you really want to call needs more parameters?  Then you use the callback method to call the actual function you want and pass it all the parameters you'd like.

Let's look at a bigger example to wrap up.  Suppose you are writing a program to emulate an alarm system on your house.  You need to know when your Mom comes home because she won't let you eat cookies before dinner.  You've worked out a deal with your little sister.  When she sees your Mom coming, she'll let you know.  In return, you'll give her some cookies.  The number of cookies she gets depends on how close she let your mom get before warning you.  The closer she lets your mom get, the less cookies she gets.

Let's represent your little sister seeing your Mom coming home as a mouse click event.  Every time the mouse is clicked, it means that your little sister saw your Mom.  When she warns you, you have to give some cookies to your sister.  The number of cookies she gets depends on how close she lets your mom get before warning you.

In this program, the mouse click event is your little sister warning you about your mom coming.  The position of the mouse click represents where your mom is in relation to the house.  The callback function is giving your sister cookies.  However, since we can't pass parameters to the callback function, we need another function to use as the callback function and call ```giveCookies()``` from that function.  Notice this also lets us decide after the event what the parameters should be based on the details of the event.

Our program could look like

```
function start(){
    drawHouse();
    mouseClickMethod(warning);
}

// Callback function
// called when your sister warns you
// Notice that you can call the function you actually want, giveCookies,
// with a parameter
function warning(e){
    // figure out how far away your mom is
    var dist = computeDistance(e.getX(), e.getY());
    var height = getHeight()/2;
    // Give your sister cookies based on the distance
    if (dist > height/3){
        // mom is more than 1/3 of the screen away
        giveCookies(3);
    } else if(dist > height/4){
        // mom is more than 1/3 of the screen, but less than 1/4 of the screen
        giveCookies(2);
    } else{
        // mom is less than 1/4 of the screen away
        giveCookies(1);
    }
}

// gives cookies to your sister
function giveCookies(numCookies){
    println("Your sister earned " + numCookies + " cookies.");
}

////////////////// other functions /////////////////////////
// draws your house
function drawHouse(){
    var house = new Rectangle(100,50);
    house.setColor(Color.red);
    house.setPosition(getWidth()/2, getHeight()/2);
    add(house);
}
// computes the  distance from position (x,y) to your house
// Don't worry if you don't understand this calculation
function computeDistance(x,y){
    var houseX = getWidth()/2;
    var houseY = getHeight()/2;
    return Math.sqrt((houseX- x)*(houseX-x) + (houseY-y)*(houseY-y));
}

```

Try it out in your editor!