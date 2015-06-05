<h1>Adding and Removing from an Array</h1>
Arrays on the CodeHS platform are mutable, meaning we can add and remove elements with ease. The key functions you will need to know are ```push()
```, ```pop()```, and ```remove()```. 

<h3>Adding Elements</h3>
The```push()``` function adds an element to the end of an array. Suppose we have an array ```fruit```.
```
var fruit = ["apples", "bananas"];
fruit.push("mangos");
print(fruit[2]);
```

Output:
```
mangos
```

Inserting an element at any position other than the last will require looping through the array, which you will learn in the coming sections.

<h3>Removing Elements</h3>
The function ```remove(int i)``` removes the element at index i. Additionally, this function updates the positions of all elements with indices greater than i.

```
var colors = ["red", "white", "blue", "magenta"];
println("Before:");
println(colors[1]);
println(colors[2]);

colors.remove(1);

println();
println("After:");
println(colors[1]);
println(colors[2]);
```

Output:
```
Before:
white
blue

After:
blue
magenta
```

Another function you can use to remove elements is ```pop()```. This removes the last element in the array.

```
var subjects = ["chemistry", "comp sci", "art", "math"];
println(subjects.pop());
println(subjects[2]);
println(subjects[3]);
```

Output:
```
math
art
undefined
```









