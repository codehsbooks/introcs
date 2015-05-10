# Mouse Click Events

Sometimes we want the user to be able to interact with our programs.  We've seen how to do this by asking questions, but suppose we want the user to pick  location on the screen.  It'd be annoying for the user to have to figure out the X and Y coordinates of the spot.  This is one instance where using Mouse Click Events comes in handy.  All the user has to do is click on the chosen spot, and the program gets all of the information it needs.


## What are Events?
In spoken English, events usually refer to special gatherings, like sporting events or parties.  In computer science, events are actions that occur that the program needs or wants to respond to.  Here, we are specifically talking about mouse events.  Mouse events are "triggered" or "fired" whenever the user does something with the mouse, such as moving the mouse or clicking the mouse.

## Responding to Events
To respond to an event, we have to set up special method called a Callback Method.  This method gets called when the program detects an event.  We also have to tell the program that we want to associate a particular method with an event. This is referred to as "registering a callback".  For mouse click events, this looks like

```
// This tells the program that when a mouse
// click happens, the function named
// 'callbackFunction' should be called
mouseClickMethod(callbackFunction);

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
4.  The callback method is **always** called when the event it's registered to occurs

## Getting Event Information


## Putting It All Together