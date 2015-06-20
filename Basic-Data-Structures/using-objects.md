## Using Objects

We want to use objects in situations where we want to associate one thing with another. For example, in the previous section, we associated words with definitions using an object. Now let's explore other situations where objects would be useful.

Let's say that we want to create a menu for a restaurant. Thus, we want to associate items on the menu with their respective prices. We can use the code snippet below to create a menu object and add soda, hot dogs, hamburgers, and french fries.

```
var menu = {};
menu["Soda"] = 1;
menu["Hot dog"] = 2;
menu["Hamburger"] = 3;
menu["French fries"] = 2;
```

Now, our menu looks something like this:

|ITEM | PRICE|
|---|---|
|Soda | 1 |
|Hot dog | 2 |
|Hamburger | 3 |
|French fries | 2 |

#### Printing out the menu

We want to print out our menu to the console.  Of course, we can print out our menu one by one. For example, we could do this:
```
println("Soda costs $" + menu["Soda"]);
println("Hot dog costs $" + menu["Hot dog"]);
println("Hamburger costs $" + menu["Hamburger"]);
println("French fries costs $" + menu["French fries"]);
```
Printing out our menu one item at a time takes a lot of effort, and the code would have to change whenever we want to make a change to our menu. A better way of printing out our menu would be to loop through our menu. 

How would we accomplish this? For loops would not work, since we cannot use an integer to access values in our menu. A while loop would not work either, since there is no condition that we could work with. Thus, to loop over an object, we have no choice but to use a new type of loop, a for-each loop. 

A for-each loop allows us to run a segment of code for each key in an object. A for each loop is structured like so:
```
for(var ___ in ___){
    //do something
}
```
The first blank will contain a name for the keys in the object and the second blank will contain the object that you want to loop over. For example, if we wanted to print out the items in our menu, we would do so like this:
```
for(var item in menu){
    println(item);
}
```
We would read this loop as "for each item in the menu, print out the item". Thus, this loop would print out:
```
Soda
Hot dog
Hamburger
French fries
```
We are almost done printing out our menu! All we need to do is add the prices to the items. Since we are looping through the keys of an object, we can use the keys to look up their respective values. Using what we learned from the last section, we know that we can look up the prices of our items using:
```
var price = menu[item];
```
Now, all we have to do is change our print statement so that it contains the price.
```
println(item + ": $" + price);
```
Once we put everything together, this is the resulting code.
```
function start(){
	var menu = {};

    menu["Soda"] = 1;
    menu["Hot dog"] = 2;
    menu["Hamburger"] = 3;
    menu["French fries"] = 2;
	
	for(var item in menu){
		var price = menu[item];
		println(item + ": $" + price);
	}
}
```
This code prints out the following menu to the console.
```
Soda: $1
Hot dog: $2
Hamburger: $3
French fries: $2
```


