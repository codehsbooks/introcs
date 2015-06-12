# Iterating Over an Array

Suppose you are given an array representing a student's test grades for the year:

```
var examGrades = [98, 82, 88, 91, 77, 84, 92, 88, 100, 67, 79];
```

To print out the grades, you will recall that we write a for loop which iterates through each of the array's indices:

```
for (var i = 0; i < examGrades.length; i++) {
    println("Exam " + i + ": " + examGrades[i]);
} 
```

The resulting output looks like:

```
Exam0: 98
Exam1: 82
Exam2: 88
Exam3: 91
Exam4: 77
Exam5: 84
Exam6: 92
Exam7: 88
Exam8: 100
Exam9: 67
Exam10: 79
```

You can accomplish a lot by iterating over arrays. You are not limited to simply printing out the contents!

## More Things to do Using Iteration!

What else can you do with a list of grades? To start, you might be interested to know what the student's **average** exam grade is. With iteration, calculating the average is easy!

```
function start(){
	var examGrades = [98, 82, 88, 91, 77, 84, 92, 88, 100, 67, 79];
    var examAverage = calculateAverage(examGrades);
    println("Overall average exam grade: " + examAverage);
}

function calculateAverage(arr) {
    // Declare and initialize variables
    var total = 0;
    var average = 0;
    var arrayLength = arr.length;
    // Sum all the grades
    for (var i = 0; i < arrayLength; i++) {
        total += arr[i];
    }
    // Calculate the average
    average = total / arrayLength;
    return average;
}
```

In our `calculateAverage` function, we start by declaring our variables. We set the initial values of `total` and `average` to 0. The `arrayLength` variable represents the total number of grades in the array. In this particular example, the `examGrades` array has 11 total grades, so `arrayLength` is equal to 11.

After setting up our variables, we loop through the array and add all of the grades together. The resulting sum is stored into `total`. To compute the `average`, we just divide the `total` by the number of grades in the array, `arrayLength`. The program will print:

```
Overall average exam grade: 86
```








## Flipping Coins

In this example, 

```
var NUM_FLIPS = 100;

/* Write a program to flip a coin NUM_FLIPS
 * times an put the results into an array.
 * We also want to print that array.
 */
function start(){
	var flips = flipCoins();
	printArray(flips);
}

// This function should flip a coin NUM_FLIPS
// times, and add the result to an array. We
// return the result to the caller.
function flipCoins(){
	var flips = [];
	for(var i = 0; i < NUM_FLIPS; i++){
		if(Randomizer.nextBoolean()){
			flips.push("Heads");
		}else{
			flips.push("Tails");
		}
	}
	return flips;
}

function printArray(arr){
	for(var i = 0; i < arr.length; i++){
		println(i + ": " + arr[i]);
	}
}
```

