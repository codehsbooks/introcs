## Intro to Sets

Sets are useful when you want to create a collection of elements, *but the order does not matter*. Additionally, sets do not contain duplicates, which means that an element can only show up once in a set. In short, all that matters is whether the element is contained within the set.


#### Creating a new set
Let's say we wanted to create a new set that will contain all different types of dogs, which we will call **dogs**. To create a this new set, we can initialize it like so :

```
var dogs = new Set();
```

We have now successfully created our set of dogs. However, it is currently empty, since we have not yet added anything to the set.

#### Using Sets

##### Adding to a set

Adding to a set is simple. For example, if we wanted to add "Corgi" and "German Shepard" to the set of dogs that we created above, we can do so like so :

```
dogs.add("Corgi");
dogs.add("German Shepard");
```

Now, "Corgi" and "German Shepard" are contained in the set. We can check this by printing out the set using the code snippet below :

```
println(dogs);
```

This would output the following to the console.
```
Set: {Corgi, German Shepard}
```



##### Removing from a set

We can also remove from a set. It is very similar to adding from a set. Now, if we wanted to remove "German Shepard" from our list of dogs, we can do so by using the following: 

```
dogs.remove("German Shepard");
```

Now that we have removed "German Shepard" from the set, all that remains in the set is "Corgi".

##### Finding the size of a set

In order to find out how many elements are in the set, we can use the .size() function. The following code would allow us to figure out the size of our dogs set and stores it in the variable numberOfDogs.

```
var numberOfDogs = dogs.size();
```

Since we know that our set only contains "Corgi", we know that numberOfDogs will be equal to 1.

##### Searching the set

Now sets are great and all, however they wouldn't be very useful if there was no way to check if an element is contained in a set. Luckily, we can use the contains() function to check to see if a set contains an element. For example, if we wanted to search through dogs to see if "Poodle" was contained in the set, we can use the code below :
```
dogs.contains("Poodle");
```
(Note: This code will return "false", since we know that "Poodle" is *not* in our set of dogs. If we search for "Corgi" instead, this will return "true", since we know that "Corgi" is in our set of dogs.)







