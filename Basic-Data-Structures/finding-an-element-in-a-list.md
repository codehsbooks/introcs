# Finding an Element in a List

You will often need to search through the contents of arrays to find where specific elements occur. Take this grocery list as an example:

```
var list = ["bread", "eggs", "milk", "cookies", "bananas", 
	"tuna", "lettuce", "yogurt", "cheese", "chicken", "cucumbers", 
	"orange juice", "salt", "doritos", "lemonade", "apples", 
	"paper towels", "red onion", "minced garlic", "tumeric", 
	"donuts", "bagels", "crackers", "red pepper", "green pepper",
	"spinach", "canola oil", "vanilla", "flour", "brown sugar", 
	"powdered sugar", "lime"];
```

Suppose you want to find the location of where "bread" occurs in this array. Or suppose you want to find the position of where "paper towels" occurs in the array. How can you do this without having to manually count through each position of the array yourself?

You will recall that each individual location or position in an array is called an index. The starting index in an array is always 0. Thus, "bread" occurs in this array at index 0. The remaining indices are numbered consecutively up until the last element in the array. For example, "lettuce" occurs at index 6.

You can find the index of any element in an array by writing your own `indexOf()` function.

## Writing an Array indexOf Function

Let's say we are given this as a `start()` function to work with:

```
function start(){
	var list = ["bread", "eggs", "milk", "cookies", "bananas", 
	"tuna", "lettuce", "yogurt", "cheese", "chicken", "cucumbers", 
	"orange juice", "salt", "doritos", "lemonade", "apples", 
	"paper towels", "red onion", "minced garlic", "tumeric", 
	"donuts", "bagels", "crackers", "red pepper", "green pepper",
	"spinach", "canola oil", "vanilla", "flour", "brown sugar", 
	"powdered sugar", "lime"];
	
	var idx = indexOf(list, "bread");
	println("The index of bread is: " + idx);
}
```

This code will not run because we first need to define our own  `indexOf()` function:

```
function indexOf(arr, str){
	for(var i = 0; i < arr.length; i++){
		var cur = arr[i];
		if(cur == str){
			return i;
		}
	}
	return -1;
}
```

The `indexOf()` function takes in an array, `arr`, and a string to search for within the array, `str`. We begin by looping through the contents of the array using for loop iteration. On each iteration, we get the current element using `arr[i]` and store it into a variable called `cur`. We then check to see if the current element, `cur`, is equal to the string we are searching for, `str`. If it is, we return the index as kept track by our for loop variable, `i`. 

However, if the element is not found after searching through the entire array, we return -1. Why -1? Because a array's index can't be negative! This tells us that the element is not in the array at all.

## Putting It All Together

```
function start(){
	var list = ["bread", "eggs", "milk", "cookies", "bananas", 
	"tuna", "lettuce", "yogurt", "cheese", "chicken", "cucumbers", 
	"orange juice", "salt", "doritos", "lemonade", "apples", 
	"paper towels", "red onion", "minced garlic", "tumeric", 
	"donuts", "bagels", "crackers", "red pepper", "green pepper",
	"spinach", "canola oil", "vanilla", "flour", "brown sugar", 
	"powdered sugar", "lime"];
	
	var idx = indexOf(list, "bread");
	println("The index of bread is: " + idx);
}

function indexOf(arr, str){
	for(var i = 0; i < arr.length; i++){
		var cur = arr[i];
		if(cur == str){
			return i;
		}
	}
	return -1;
}
```

Now that we have our `start()` and `indexOf()` functions combined and thoroughly explained, let's verify that it works. What will get printed to the screen after running this program?

The program prints:

`The index of bread is: 0`

### More Practice with Searches

Using the same grocery list and `indexOf()` function, let's get a little more practice searching through arrays.

```
function start(){
	var list = ["bread", "eggs", "milk", "cookies", "bananas", 
	"tuna", "lettuce", "yogurt", "cheese", "chicken", "cucumbers", 
	"orange juice", "salt", "doritos", "lemonade", "apples", 
	"paper towels", "red onion", "minced garlic", "tumeric", 
	"donuts", "bagels", "crackers", "red pepper", "green pepper",
	"spinach", "canola oil", "vanilla", "flour", "brown sugar", 
	"powdered sugar", "lime"];
	
	var idx = indexOf(list, "bread");
	println("The index of bread is: " + idx);
	
	println("The index of lettuce is: " + indexOf(list, "lettuce"));
	println("The index of paper towels is: " + indexOf(list, "paper towels"));
	println("The index of apple juice is: " + indexOf(list, "apple juice"));
}

function indexOf(arr, str){
	for(var i = 0; i < arr.length; i++){
		var cur = arr[i];
		if(cur == str){
			return i;
		}
	}
	return -1;
}
```

We already know that "bread" occurs at index 0. Here we are also finding the indices for "lettuce", "paper towels", and "apple juice". What will get printed to the screen? What index values will be returned for each of these things?

Answer:

```
The index of bread is: 0
The index of lettuce is: 6
The index of paper towels is: 16
The index of apple juice is: -1
```

Since apple juice is not in the list at all, it returns -1.

## JavaScript has its Own Built-in indexOf Method!

Javascript has an indexOf method of its own:

`arrayName.indexOf(str);`

We can use this to ensure the results match with the `indexOf()` function that we built ourselves.

```
function start(){
	var list = ["bread", "eggs", "milk", "cookies", "bananas", 
	"tuna", "lettuce", "yogurt", "cheese", "chicken", "cucumbers", 
	"orange juice", "salt", "doritos", "lemonade", "apples", 
	"paper towels", "red onion", "minced garlic", "tumeric", 
	"donuts", "bagels", "crackers", "red pepper", "green pepper",
	"spinach", "canola oil", "vanilla", "flour", "brown sugar", 
	"powdered sugar", "lime"];
	
	// Using our own indexOf function
	println("Using our own indexOf function:");
	
	var idx = indexOf(list, "bread");
	println("The index of bread is: " + idx);
	
	println("The index of lettuce is: " + indexOf(list, "lettuce"));
	println("The index of paper towels is: " + indexOf(list, "paper towels"));
	println("The index of apple juice is: " + indexOf(list, "apple juice"));
	
	// Using JavaScript's built-in indexOf method
	println("\nUsing Javascript's built-in indexOf method gives the same results:");
	
	var idx2 = list.indexOf("bread");
	println("The index of bread is: " + idx2);
	
	println("The index of lettuce is: " + list.indexOf("lettuce"));
	println("The index of paper towels is: " + list.indexOf("paper towels"));
	println("The index of apple juice is: " + list.indexOf("apple juice"));
}

function indexOf(arr, str){
	for(var i = 0; i < arr.length; i++){
		var cur = arr[i];
		if(cur == str){
			return i;
		}
	}
	return -1;
}
```

Resulting output:
```
Using our own indexOf function:
The index of bread is: 0
The index of lettuce is: 6
The index of paper towels is: 16
The index of apple juice is: -1

Using Javascript's built-in indexOf method gives the same results:
The index of bread is: 0
The index of lettuce is: 6
The index of paper towels is: 16
The index of apple juice is: -1
```

We have thus verified that the two methods are indeed identical.




