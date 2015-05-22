# Key Events

We now know how to handle different types of input from the mouse, but let's not forget about the keyboard. We can handle input from the keyboard similiarly to how we handled input from the mouse. We use special event methods that take a callback function!

## Key Event Methods

There are three useful methods for detecting key events. They are given in the table below:

| Keyboard Method | Responds To |
| -- | -- |
| keyDownMethod(callbackFunction); | Key pressed down |
| keyUpMethod(callbackFunction); | Key released |
| isKeyPressed(keyCode); | Is a key with a given `keyCode` pressed down? Returns **true** or **false**. |

### Using Key Events

We handle key events much in the same way we handle mouse events. We use one of the special keyboard methods to detect a key event and pass it a callback function. Each time a key is pressed, this callback function gets called automatically.

```
function start(){
    // This tells the program that when a key
    // is pressed down, the function named
    // 'callbackFunction' should be called
    keyDownMethod(callbackFunction);
}

// This is the callback function
function callbackFunction(e){
    //Code here to do something when a key is pressed.
}
```

It is important to notice that the callback function will be called when **any** key gets pressed. It does not rely on **one** specific key being pressed down. Thus, we still need some way of determing which specific key is being pushed. How can we do this?

## Detecting a Specific Key

We make use of our callback function's parameter `e` to detect a specific key. Each key on the keyboard is assigned a unique number or id. We use `e.keyCode` to return the unique numerical id of the key being pressed.

```
function start(){
    // This tells the program that when a key
    // is pressed down, the function named
    // 'keyDown' should be called
    keyDownMethod(keyDown);
}

// This is the callback function named keyDown
function keyDown(e) {
	println(e.keyCode);
}
```

This program will print out the unique id of a key. The id will vary depending on which key is pressed.

### Using Keyboard Constants and Methods

You don't have to memorize the numerical id of each key on the keyboard. That would be a nightmare! Instead, you can make use of the convenient constants and methods given below:

| Constant or Method | Represents which key?|
| -- | -- |
| Keyboard.LEFT | Left arrow key |
| Keyboard.RIGHT | Right arrow key |
| Keyboard.UP | Up arrow key  |
| Keyboard.DOWN | Down arrow key  |
| Keyboard.ENTER | Enter key |
| Keyboard.SPACE | Spacebar |
| Keyboard.letter('L')| The L key |
| Keyboard.digit('2') | The number 2 |

The constants are written in all capital letters and represent only **one** specific key. The two methods, `keyboard.letter()` and `keyboard.digit()`, will represent the key for any letter or number within the parenthesis `()`.

### Detecting an Arrow Key

Let's get some practice using constants and methods to detect specific keys. On a key press, this program will check to see if it was one of the four arrow keys. If the user presses an arrow key, it will print out which arrow key was pressed. Otherwise, it will inform the user that they did not press an arrow key at all.

```
function start(){
    println("Press an arrow key!");
    // This tells the program that when a key
    // is pressed down, the function named
    // 'keyDown' should be called
    keyDownMethod(keyDown);
}

// This is the callback function named keyDown
function keyDown(e) {
    if (e.keyCode == Keyboard.LEFT) {
        println("You pressed the left arrow key.");
    } else if(e.keyCode == Keyboard.RIGHT){
        println("You pressed the right arrow key.");
    } else if(e.keyCode == Keyboard.DOWN){
        println("You pressed the down arrow key.");
    } else if(e.keyCode == Keyboard.UP){
        println("You pressed the up arrow key.");
    } else {
        println("You did not press an arrow key.");
    }
}
```

By comparing `e.keyCode` with each of the directional key constants, we can tell which arrow key is pressed.

### Detecting a Number

This program asks the user to enter a digit between 0 and 9. It then uses a for loop to detect which number key was pressed.

```
function start(){
    println("Enter a digit (0-9).");
    // This tells the program that when a key
    // is pressed down, the function named
    // 'keyDown' should be called
    keyDownMethod(keyDown);
}

// This is the callback function named keyDown
function keyDown(e) {
    for(var i = 0; i <= 9; i++){
        if (e.keyCode == Keyboard.digit(i)) {
            println("You pressed the " + i + " key.")
        }
    }
}
```


## Keyboard Square Program

In this program, the user controls a square using the directional keys. The square will move in the direction of the key that is pushed.

```
var square;

function start(){
	square = new Rectangle(40, 40);
	square.setPosition(100, 100);
	add(square);
	
	keyDownMethod(keyDown);
}

function keyDown(e){
	if(e.keyCode == Keyboard.LEFT || e.keyCode == Keyboard.letter('a')){
		square.move(-5, 0);
	}
	
	if(e.keyCode == Keyboard.RIGHT || e.keyCode == Keyboard.letter('d')){
		square.move(5, 0);
	}
	
	if(e.keyCode == Keyboard.UP || e.keyCode == Keyboard.letter('w')){
		square.move(0, -5);
	}
	
	if(e.keyCode == Keyboard.DOWN || e.keyCode == Keyboard.letter('s')){
		square.move(0, 5);
	}
}
```

Alternatively, the user can choose to use the `w`, `a`, `s`, and `d` keys instead of the arrow keys. `w` moves the square up, `a` moves it left, `s` moves it down, and `d` moves it right. 

