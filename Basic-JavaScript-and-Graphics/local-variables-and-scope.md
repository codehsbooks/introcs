#Local Variables and Scope



###What are Local Variables?
 You have already been using local variables! Local variables are variables that are declared using the keyword ```var```. Since we always declare variables with the keyword ```var```, why aren't all variables local variables? The thing that makes local variables *local* is that they are declared *inside* of a function or loop.  Since they are declared inside of the function, they belong only to that one function and no other functions.  It's like calling someone who was born in  particular town a local (or native) to the town.  You can think of a function as a town whose people are all of the variables that are declared inside of it or passed into it.  Unlike real people, however, our variable people don't ever move from their town. The code snippet below illustrates local variables.
 
 ```
 // The variables x, y and townName are local variables
 function makeATown(){
    var x = 4;
    var y = 10;
    var townName = "Madison";
    println("This function is town " + townName);
    println("It has 3 local variables, or townspeople");
    println("The local variables are x,y, and townName.");
    println("x: " + x + ", y: " + y);
 }
 
 // This variable is not a local variable.  
 // You (usually) don't declare variables outside of functions.
 var notALocal;
 ```
 
 For the more curious reader, the variable ```notALocal``` is a global variable.   That means it lives in all of the functions.  However, you only use global variables for special purposes, such as constant values that never change, as we'll see in later sections.   For now, unless told otherwise, your variables should be local variables.
 

###What is Scope?
Now that we know what local variables are, we can define "scope".  A variable's scope is the function or loop where a variable exists.  The scope is defined by the block of code where a variable has been defined and has a valid value.  

Let's look at a bit of code to clear things up.  In the function ```averageNumbers()``` below,  there are 2 local variables and 3 function argument variables.  The local variables are ```total``` and ```result```.  The function arguments are ```x```, ```y```, and ```z```.  The scope of the local variables is the function ```averageNumbers```.  The scope of the function arguments is also the function ```averageNumbers```.  This means that ```total```, ```average```, ```x```, ```y```, and ```z``` can be used in the function ```averageNumbers``` because they are considered defined and have a value.  These variables cannot be used outside of ```averageNumbers``` because their value is undefined outside of their scope. 


```
 // variables are out of scope here
 function averageNumbers(x,y,z){
 // variables are in scope
    var total = x + y + z;
    var result = total/3.0;
    return result;
 }
 // variables  are out of scope
 
 ```
Here is an example of scoping rules with loops.

```
function start(){
    // variable i is out of scope
    for(var i  = 0; i < 10; i++){
        // variable i is in scope
        println(i);
    }
    
    // variable i is out of scope
}
```

To summarize, scope tells us where we can use a particular variable.  Scopes are usually functions or loop bodies.  A variable's scope is determined by where it is declared.  Function arguments' scope is the function they're passed in to.

###Why do I need to worry about Scope?
Why do we even care where  a variable's scope is?  We use scope to help keep variables with the same name straight.  You cannot have two variables with the same name in the same scope.  This will either cause an error or one of the variables will be hidden by another.  

For example, suppose you have an Uncle Tom and a best friend named Tom. Let's say one day you start telling a story about Tom to your other best friend Susie.  Since Susie doesn't know about your Uncle Tom, Susie immediately assumes you're telling her a story about your best friend Tom.  You could say that your best friend Tom is "in scope" when you are talking to Susie because the only Tom that is "defined" is your best friend Tom.  

Likewise, when you're using variables in your code, you can only use variables that are "in scope" because the function doesn't know about the other variables in the program.

Let's look at another code example.
```
// computeTax scope begins
function computeTax(total, taxRate){
    var taxCharged = total * taxRate;
    var result = total + taxCharged; 
    return result;
}
// computeTax scope ends

// computeTip scope begins
function computeTip(total, tipRate){
    var tip = total*tipRate;
    var result = total + tip; 
    return result;
}
// computeTip scope ends
```
Notice that both of these functions have a local variable named ```result```.  However, ```computeTax``` doesn't know about  the variable named ```result``` in ```computeTip```.  Each function uses the value of it's local variable ```result```.  

Here's another example.

```
function start(){
    var x = 3;
    var y = 2;
    var changedX = addFour(x);
    println(x);
    println(changedX);
    println(y);
}

function addFour(x){
    var y = 4;
    var result = x + y;
    return result;
}
```

Here we've used ```x``` and ```y``` in both functions!  How does the computer know which ```x``` we're talking about?  The computer will use the ```x``` that is in scope.  This means that in ```main```, the value of ```x``` is 3 and the value of ```y``` is 2.  Even after we call ```addFour```, these variables are not changed.  In ```addFour```, the value of ```x``` is whatever gets passed in, and the value of ```y``` is 4.  Try it out and see for yourself!

There is one last mistake that you can easily make.  Take a look at the code below.

```
function computeSquareArea(side){
    var side = 3;
    return side * side;
}
```

In this function, there is a function parameter and a local variable named ```side```.  When this happens, the function parameter gets hidden by the local variable.  That means that the value of the function parameter is never used.  Whenever ```side``` is used in the function, the value of the local variable is used.  Thus, this function will always return 9 no matter what is passed in.
