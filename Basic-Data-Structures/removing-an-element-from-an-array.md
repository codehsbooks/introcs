
# Removing an Element from an Array

You have already learned how to remove the last element from an array. You just use the array `pop()` method!

```
var arr = [2, 6, 12, 4, 13, 7, 11, 9];
println("Before using arr.pop(): " + arr);
var elem = arr.pop();
println(elem + " has been removed from the array!");
println("After using arr.pop(): " + arr);
```

Calling `pop()` on an array returns the value of the element removed. This value can be stored into a variable for future use. Here we store this value into a variable called `elem` and then print it out.

When the above code is run, the result is:

```
Before using arr.pop(): 2,6,12,4,13,7,11,9
9 has been removed from the array!
After using arr.pop(): 2,6,12,4,13,7,11
```

Being able to remove the last elements from an array is useful, but what if you wanted to remove elements from within the array? What if you wanted to remove multiple elements from within an array? 

## Array Remove Method

To remove an element from within an array, you use the `remove(index#)` method.

```
var arr = [2, 6, 12, 4, 13, 7, 11, 9];
println("Before using arr.remove(2): " + arr);
arr.remove(2);
println("After using arr.remove(2): " + arr);
```

The code above prints:

```
Before using arr.remove(2): 2,6,12,4,13,7,11,9
After using arr.remove(2): 2,6,4,13,7,11,9
```

Since arrays are numbered starting at index 0, index 2 in the array above is the value `12`. Thus, the value `12` gets removed from inside the array.

Just like with `pop()`, `remove(#)` returns the value of the element removed. You can store this value and do things with it.

```
var arr = [2, 6, 12, 4, 13, 7, 11, 9];
println("Before using arr.remove(2): " + arr);
var elem = arr.remove(2);
println(elem + " was removed from inside of the array!");
println("After using arr.remove(2): " + arr);
```

The code above prints:

```
Before using arr.remove(2): 2,6,12,4,13,7,11,9
12 was removed from inside of the array!
After using arr.remove(2): 2,6,4,13,7,11,9
```

## Array Splice Method

You can also use the `splice(index#, amountToRemove)` method to remove elements from within an array. It requires two arguments, `index#` and `amountToRemove`. The first argument is the starting index to remove. The second argument is the amount of elements to remove from the given starting index. For example:

```
var arr = [2, 6, 12, 4, 13, 7, 11, 9];
println("Before using arr.splice(2, 1): " + arr);
var elem = arr.splice(2, 1);
println(elem + " was removed from inside of the array!");
println("After using arr.splice(2, 1): " + arr);
```

The code above prints:

```
Before using arr.splice(2, 1): 2,6,12,4,13,7,11,9
12 was removed from inside of the array!
After using arr.splice(2, 1): 2,6,4,13,7,11,9
```

Notice that `arr.splice(2, 1)` does the exact same thing as `arr.remove(2)` because we are only splicing out one element!

However, you are not limited to removing just one element! You can remove multiple elements with splicing. The second argument determines the amount of elements to remove. Below, we are removing 4 elements rather than just 1.

```
var arr = [2, 6, 12, 4, 13, 7, 11, 9];
println("Before using arr.splice(2, 4): " + arr);
var multipleElements = arr.splice(2, 4);
println(multipleElements + " were removed from inside of the array!");
println("After using arr.splice(2, 4): " + arr);

```

After running the code, the program prints:

```
Before using arr.splice(2, 4): 2,6,12,4,13,7,11,9
12,4,13,7 were removed from inside of the array!
After using arr.splice(2, 4): 2,6,11,9
```