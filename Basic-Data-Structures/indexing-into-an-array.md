<h1>Indexing Into an Array</h1>

<h3>The Array Index</h3>
Arrays are ordered lists. Each element can be accessed by its index (its position in the list).

<u>The first element in an array corresponds to index 0.</u> Each subsequent element's index corresponds to the element's distance from the first element.

Consider the following scenario. I have an array consisting of the following elements, in order: "California", "Wyoming", "Vermont", "Wisconsin". 

The elements are indexed as such:
<nl>0 -- "California"
<nl>1 -- "Wyoming"
<nl>2 -- "Vermont"
<nl>3 -- "Wisconsin"

<h3>Indexing Syntax</h3>
Here we see the use of square brackets again. An element can be retrieved by the name of the array, followed by the index surrounded by square brackets. See the code snippet below for an example.

```
var myStates = ["California", "Wyoming", "Vermont", "Wisconsin"];
print(myStates[0] + " is 3 thousand miles from " + myStates[2] + ".");
```

This code produces the following output:
```
California is 3 thousand miles from Vermont.
```

<h3>Out of Bounds Warning</h3>
Only indices 0 through 1 less than the length of the array are valid for any given array. If you attempt to retrieve the element corresponding to an index that is "out of bounds," meaning it is negative, or greater than or equal to the length of the array, you will not get useful results. On the CodeHS platform, the following code:

```
var arr = ["cat"];
print(arr[1]);
```
produces the following output:
```
undefined
```

On most other programming platforms, you will encounter a compiler error that notifies you that you are attempting to retrieve an element for an invalid index.




