# Comparison Operators

Comparison operators allow us to compare two values against one another.

## An Example Comparison

In the following example, we compare two variables `x` and `y`. We store the result in variable `z`.

```
var x = 10;
var y = 8;

var z = x > y;
println(z);
```
What will get printed to the screen? The above comparison, `x > y`, is evaluating if 10 is greater than 8. Because 10 is indeed greater than 8, `z` is assigned a value of true. Thus, `true` will get printed to the screen.

## Table of Comparison Operators

The table below lists each of the comparison operators:

|  Operator      |  Usage           |  
| -------------- | ---------------- |
| >              | Greater Than     |  
| <              | Less Than        |  
| >=             | Greater Than Or Equal To|  
| <=             | Less Than Or Equal To|   
| ==             | Equal To   |          
| !=             | Not Equal To |   

A common mistake is using `=` when you actually want to use `==`. `=` is used for assignment of variables whereas `==` is used for comparing the equality of the values.

## Using Comparison Operators

Suppose we want to write a program which restricts people under a certain height from riding on a roller coaster. For this particular roller coaster, people who are under 4 feet (48 inches) are not allowed on the ride. How would we do this?

```
var height = readInt("How tall are you (in inches)? ");
var isTallEnough = height >= 48;
println("Can ride on the roller coaster: " + isTallEnough);
```