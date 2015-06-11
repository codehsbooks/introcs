## Intro to Sets

Sets are useful when you want to create a collection of elements, *but the order does not matter*. 

#### Properties of sets

As stated above, the elements in a set do not follow a certain order. Additionally, sets do not contain duplicates, which means that an element can only show up once in a set. All that matters is whether the element is in the set or not. Using the above example, 


#### Creating a new set
Let's say we wanted to create a new set that will contain all different types of dogs, which we will call **dogs**. To create a this new set, we can initialize it like so:

```
var dogs = new Set();
```

#### Using Sets

##### Adding to a set

Adding to a set is very simple. If we wanted to add "Corgi" and "German Shepard" to the set of dogs that we created above, we can do so like so:

```
dogs.add("Corgi");
dogs.add("German Shepard");
```

Now, "Corgi" and "German Shepard" are contained in the set.

##### Removing from a set

We can also remove from a set. It is very similar to adding from a set. Now, if we wanted to remove "German Shepard" from our list of dogs, we can do so by using: 

```
dogs.remove("German Shepard");
```

Now that we have removed "German Shepard" from  the set, all that remains in the set is "Corgi".

##### Finding the size of a set

In order to find out how many elements are in the set, we can use the .size() function. We can find the size of our dogs set like so:






