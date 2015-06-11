## Intro to Sets

Sets are useful when you want to create a collection of elements, *but the order does not matter*. 

#### Properties of sets

As stated above, the elements in a set do not follow a certain order. Instead, all that matters is whether the element is in the set or not. Using the above example, 


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

We can also remove from a set. 

##### Finding the size of a set
