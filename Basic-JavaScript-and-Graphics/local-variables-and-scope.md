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
Now that we know what local variable
```
 // Local variables are total and result
 function averageNumbers(x,y,z){
    var total = x + y + z;
    var result = total/3.0;
    return result;
 }
 
 function computeTax(total, taxRate){
    var taxCharged = total * taxRate;
    var result = total + taxCharged;
    return result;
 }
 
 ```
###Why do I need to worry about Scope?

### Test Your Understanding