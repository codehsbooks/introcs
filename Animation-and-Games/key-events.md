# Key Events

We now know how to handle different types of input from the mouse, but let's not neglect the keyboard. We can handle input from the keyboard similiarly to how we handled input from the mouse. We use key events!

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

It is important to notice that the callback function will be called when **any** key gets pressed. It does not rely on **one** specific key being pressed down. Thus, we still need some way of determing which specific key is being pushed 

### Detecting a Specific Key

We make use of our callback function's parameter `e` to detect a specific key. Each key on the keyboard is assigned a unique numer or id. We use `e.keyCode` to return the unique numerical id of the key being pressed.

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

## Using Keyboard Constants and Methods

You don't have to memorize the numerical id of each key on the keyboard. That would be a nightmare! Instead, you can make use of the convenient constants and methods given below:

| Constant or Method | Description |
| -- | -- |
| Keyboard.LEFT | 1:2 |
| Keyboard.RIGHT | 1:3 |
| Keyboard.UP | 1:4 |
| Keyboard.DOWN | 1:5 |
| Keyboard.ENTER | 1:6 |
| Keyboard.SPACE | 1:7 |
| Keyboard.letter('c')| 1:8 |
| Keyboard.digit('#') | 1:9 |

The program below uses the `Keyboard.LEFT` and `Keyboard.SPACE` constants to determine if those keys are pressed. It also makes use of the `Keyboard.letter()` method to check if the letter `K` is pressed. 

```
function start(){
    // This tells the program that when a key
    // is pressed down, the function named
    // 'keyDown' should be called
    keyDownMethod(keyDown);
}

// This is the callback function named keyDown
function keyDown(e) {
	if (e.keyCode == Keyboard.LEFT) {
		println("You pressed the left arrow key.");
	}
	if(e.keyCode == Keyboard.SPACE){
		println("You pressed the space bar.");
	}
	if(e.keyCode == Keyboard.letter('K')){
		println("You pressed K.");
	}
}
```

By comparing the pressed key, `e.keyCode`, with one of the constants or methods, we can tell which key is pressed.

## Keyboard Square Program

//Todo

