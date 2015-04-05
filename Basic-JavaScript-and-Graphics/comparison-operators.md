# Comparison Operators

Comparison operators allow us to compare two values against one another. The table below lists each of the comparison operators:

|  Operator      |  Usage           |  
| -------------- | ---------------- |
| >              | Greater Than     |  
| <              | Less Than        |  
| >=             | Greater Than Or Equal To|  
| <=             | Less Than Or Equal To|   
| ==             | Equal To   |          
| !=             | Not Equal To |   

## Example Comparisons

In the following example, we compare two variables `x` and `y`. We store the result in variable `z`.

```
var x = 10;
var y = 8;

var z = x > y;
println(z);
```
What will get printed to the screen? The above comparison, `x > y`, is evaluating if 10 is greater than 8. Because 10 is indeed greater than 8, `z` is assigned a value of true. Thus, `true` will get printed to the screen.

Take a look at the following code segment:

```
var a = 3;
var b = 5;
var c = 2;
var d = 3;

var t = a > 0;
var u = d <= a
var v = a != d;
var w = a == d;
var x = d >= b;
var y = b > c;
var z = 4 <= c;

println(t);
println(u);
println(v);
println(w);
println(x);
println(y);
println(z);

```

When we run this code, what boolean values (**true** or **false**) will get printed to the screen for variables t - z?

## Using Comparison Operators

Suppose we want to write a program which restricts people under a certain height from riding on a roller coaster. For this particular roller coaster, people who are under 4 feet (48 inches) are not allowed on the ride. How would we do this?

```
var height = readInt("How tall are you (in inches)? ");
var isTallEnough = height >= 48;
println("Can ride on the roller coaster: " + isTallEnough);
```

## Pitfalls

A common mistake is using `=` when you actually want to use `==`. `=` is used for assignment of variables whereas `==` is used for comparing the equality of two values.

For example, `x = 5` stores the value `5` into the variable `x`. However, `x == 5` tests to see if the value `5` is equal to the variable `x` and then returns either true or false. **They are not the same thing!**