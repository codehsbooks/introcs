# Random Numbers

Random numbers bring flavor and variety to our programs. Creating random elements in our programs is easy with the use of randomly generated numbers. 

## Randomizer

CodeHS makes it easy to generate random numbers with its built-in Randomizer method. For example, we can generate a random number between 1 and 4 by doing the following:

```
var randomNumber = Randomizer.nextInt(1, 4);
```
The variable, `randomNumber`, now holds some random value between 1 and 4. This is *inclusive*. There are four possible random numbers - 1, 2, 3, or 4.

## Rolling Dice

We can use random numbers to simulate the act of rolling a die.

```
var roll = Randomizer.nextInt(1,6);
println("You rolled a " + roll);
```

Each time we run the above code, the number printed to the screen changes.

## More Things to do with the Randomizer

In addition to creating random numbers, the Randomizer can be used to generate a few other random things.

| Type | Usage |
| -- | -- |
| Randomizer.nextInt(*low*, *high*); | Creates a random number between *low* and *high*. |
| Randomizer.nextBoolean(); | Creates a random boolean value - either *true* or *false*. |
| Randomizer.nextFloat(*low*, *high*); | Creates a random decimal value float between *low* and *high*. |
| Randomizer.nextColor(); | Creates a random color.  |

## Flipping a Coin

Now that we can create random boolean values, let's create a simple program to simulate flipping a coin.

```
var isHeads = Randomizer.nextBoolean();
if (isHeads) {
    println("You flipped heads!");
} else {
    println("You flipped tails!");
}
```
Each time we run this code, the variable `isHeads` is assigned either a *true* or *false* boolean value. The program will print either `You flipped heads!` or `You flipped tails!` depending on this randomly generated boolean value.

