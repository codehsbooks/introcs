## Introduction to Objects

Imagine that you are going to be tested on the meaning of a word that you didn't know. How would you find out the meaning of this word?
You could ask a friend or make up a meaning, but the best approach would be to look up the word in a dictionary.
Dictionaries are useful because they pair up a word with a definition. To find the definition of a particular word, you open
the dictionary, turn to the page that has that word, and read the definition for the keyword.


|WORD | DEFINITION|
|---|---|
|apple | a type of fruit|
|ball |a round object that Karel likes|
|code | instructions you write to a computer in a program|


In computer programming, this type of data structure is very useful. Not surprisingly, programmers call this 
data structure a dicinoatry as well, though you will often heard them referred to as objects or maps.

### Keys and Values
Like a dictionary of words in a book, a dictionary data structure contains pairs of "keywords" and "definitions." However,
in programming these are called "keys" and "values." 

#### Keys are Unique
In a book dictionary, each keyword usually only appears once -- though there may be multiple definitions
for one word, there are not two separate entries for the word. You would not normally see this in a dictionary:

|WORD | DEFINITION|
|---|---|
|apple | a type of fruit|
|ball |a round object that Karel likes|
|ball |a type of formal dance gathering|
|code | instructions you write to a computer in a program|

Each word, or key is unique. Rather than have the keyword listed multiple times, you would simply have more
than one definition:

|WORD | DEFINITION|
|---|---|
|apple | a type of fruit|
|ball |1. a round object that Karel likes; 2. a type of formal dance gathering|
|code | instructions you write to a computer in a program|

This same structure holds for computer dictionaries. Each key can only appear once.

### Creating an Object, Map, or Dictionary
To create a programming dictionary, you first declare a dictionary variable:

```
var myDictionary = {};
```

Once you have an empty dictionary, you can add items to it as pairs of keys and values. There is a specifc way
of doing this: `nameOfDictionary['nameOfKey'] = 'value';`

We can create a dictionary of Karel's favorite things like so:

```
var karelsFavoriteThings = {};

karelsFavoriteThings['food'] = 'doggie treats';
karelsFavoriteThings['toy'] = 'tennis ball';
karelsFavoriteThings['sound'] = 'dogs barking';
karelsFavoriteThings['hobby'] = 'coding';
karelsFavoriteThings['number'] = 42;
```

This gives us a map of Karel's favorite things that would look like:

|KEY | VALUE|
|---|---|
|food | doggie treats|
|toy | tennis ball|
|sound | dogs barking|
|hobby | coding |
|number | 42 |

### Getting Items out of a Dictionary

Now that we have an object containing Karel's favorite things, we may want to look up some information about
Karel. This is how to look something up in a programming dictionary: `nameOfDictionary['nameOfKey'];`. This will return the value associated with that key, which you can store this into a variable, print, and so on.

Let's get some of Karel's favorite things out of the dictionary:

```
println("Some of Karel's favorite things: ");

var favToy = karelsFavoriteThings['toy'];
println("Karel's favorite toy is: ");
println(favToy);

println("Karel's favorite food is: " + karelsFavoriteThings['food']);

println(karelsFavoriteThings['number']);
println("That is Karel's favorite number.");
```

This program would print the following to the console:

```
Some of Karel's favorite things:
Karel's favorite toy is:
tennis ball
Karel's favorite food is: doggie treats
42
That is Karel's favorite number.
```
