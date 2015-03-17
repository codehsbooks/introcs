# How To Indent Your Code

Indentation is a fundamental aspect of code styling, and plays a large role in influencing readability. That being said, indentation errors can be hugely misleading. Consider the following code:

```
while(notFacingLeft())
    turnLeft();
    move();
```

Because the code on line 3 is indented, it may seem to be part of the body of the while loop. But, remember that without brackets, the while loop body can only consist of one line of code. So, this code is really equivalent to:

```
while(notFacingLeft()) {
    turnLeft();
}
move();
```




