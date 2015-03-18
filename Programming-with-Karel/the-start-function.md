# The Start Function
So far, we've been talking about functions as a way to communicate with Karel.  There might be one question you have now - How does Karel know which commands to do and in what order? 

## Where Does Our Program Start?
 You might think that Karel will start at the top of the file and simply read down through it.  This is almost correct.  Remember that we can define different functions in the same file and in any order we please.  You may be tempted to organize your file with commands inserted among your functions. **This is never the way to write code.**
 You can see how this can get terribly confusing very quickly.  Where should Karel start? From the bottom? From the top?  We now introduce a special function called `start()`.

## The `start()` Function
The `start()` function is a very special function.  All of the commands you wish to execute must go inside of the start function, between the curly braces.  The commands will be executed in the order that they appear.  The start function looks like this

```
function start(){
    // all of your program commands go here
}

// none of your program commands should go here
```

Remember: 
* There can only be one start function
* You have to have a start function
* All of your code must be inside the start function or another function body 
* All function definitions must be outside of the start function


## Program Readability
The `start()` function is the first step in making our program easy to understand by humans and by Karel.  We know that all of the commands that we make will be contained inside of the start function.  The next part in making our code easy to understand is how we organize the commands inside of the start function.

### The Story of Our Program
We want our code to read like a story.  For example, suppose we have code like the following.
```
function start(){
    goToStore();
    buyChocolate();
    comeHomeAndCelebrate();
}

function goToStore(){
    // commands go here
}
```

We've only declared one of the needed functions in this example, but the point should be clear.  All of the commands we want to execute are inside of the start function.  We can read the script and tell exactly what will happen.  It's like a short story of how we went to the store, bought chocolate, and came home and ate it! Notice that the function declaration is OUTSIDE of the start function.

### Test Your Understanding
Consider each code snippet.  Decide if the start function is formatted correctly and answer the question below the piece of code.

---

<p></p>

<p>
function Start() {</br>                        
    // program commands go here </br>
    }                          </br>       
</p>
Is this start function declared correctly?
- (x) Yes
- ( ) No

> Yes.  All commands go inside of the start function
> Not quite.  This is declared correctly since all of the commands are inside of the start function.


<p>
       function start() {           </br>
                                       </br>
        }                              </br>
          // program commands go here   </br>
</p>
Is this start function declared correctly?
- ( ) Yes
- (x) No

> No!  Program commands must go INSIDE the start function

> Correct!


<p>
function start() { </br>
        start();        </br>           
        // program commands go here </br>
    }                         </br>
</p>
Is this start function declared correctly?
- ( ) Yes
- (x) No

> No!  Do not call the start function!  It gets called automatically.

> Correct!


<p>
    function start() { </br>
        function putThreeBalls(){  </br>
            // function definition goes here </br> 
        }     </br>
        // program commands go here  </br>
    }  </br>
</p>
Is this start function declared correctly?
- ( ) Yes
- (x) No

> No! Do not define functions inside of the start function.

> Correct!


<p>
    function start() { </br>
        // program commands go here </br>
     </br>
    function putThreeBalls(){  </br>
        // function definition goes here </br>
    } </br>
</p>
Is this start function declared correctly?
- (x) Yes
- ( ) No

> Yes! Functions can be declared outside of the start function.

> Not quite! Functions can be declared outside of the start function.

---

















