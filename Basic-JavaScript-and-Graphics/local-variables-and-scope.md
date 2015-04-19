#Local Variables and Scope



###What are Local Variables?
 You have already been using local variables! Local variables are variables that are declared using the keyword ```var```. Since we always declare variables with the keyword ```var```, why aren't all variables local variables? The thing that makes local variables *local* is that they are declared *inside* of a function or loop.  Since they are declared inside of the function, they belong only to that one function and no other functions.  It's like calling someone who was born in  particular town a local (or native) to the town.  You can think of a function as a town whose people are all of the variables that are declared inside of it.  Unlike real people, however, our variable people don't ever move from their town. The code snippet below illustrates local variables.
 
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
 // Local variables are total and result
 // total and result are out of scope
 function averageNumbers(x,y,z){
 // total and result are in scope
    var total = x + y + z;
    var result = total/3.0;
    return result;
 }
 // total and result are out of scope
 function computeTax(total, taxRate){
    var taxCharged = total * taxRate;
    var result = total + taxCharged;
    return result;
 }
 
 ```
###Why do I need to worry about Scope?

### Test Your Understanding