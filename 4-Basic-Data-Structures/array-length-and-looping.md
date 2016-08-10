<h1>Array Length and Looping</h1>
Knowing the length of an array is very useful, especially in the context of looping, or iterating. 

<h3>Length</h3>
You can find the length of an array using the ```length
``` attribute. An attribute is different than a function. Whereas a function requires parameters and returns a value, an attribute is simply a variable that has been made public to you. 

```
var animals = ["cat", "dog", "bird"];
print(animals.length);
```

Output:
```
3
```

Note that we used ```animals.length```, NOT ```animals.length()```.

<h3>Looping</h3>
When you know the length of an array, you can use a for loop to access each element. The following code prints each element of the ```animals``` array in order.


```
for (var i = 0; i < animals.length; i += 1) {
    println(animals[i]);
}
```

Output:
```
cat
dog
bird
```



