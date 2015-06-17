## Looping over a Grid

Let's say we are given a grid of numbers like below.

<table>
  <tr>
    <td> 3 </td>
    <td> 8 </td>
    <td> 9 </td>
  </tr>
  <tr>
    <td> 4 </td>
    <td> 3 </td> 
    <td> 6 </td>
  </tr>
  <tr>
    <td> 1 </td>
    <td> 7 </td> 
    <td> 5 </td>
  </tr>
</table>

### Finding the sum

We want to create a function that will print the sum of all these numbers. Now how do we accomplish this? We would have to loop over the array, but what type of loop would we use? To access a number in the grid, we would need two variables that point to the row and the column. Thus, the best way to accomplish this task is to use two nested for-loops, one for the row and one for the column.

The loop structure we would want to use is as follows:

```
function printSum(grid){
    for(var row = 0; row < grid.numRows(); row++){ //this loops over the rows
        for(var column = 0; column < grid.numCols(); column++){ //this loops over the columns
            //do something
        }
    }
}
```

Thus, all we would have to do is create a variable to hold our sum and fill out the body of the for-loop. First, let's create a variable to hold our sum.
```
var sum = 0;
```

Next, we need to add a line that will access the elements in the grid. As shown in the previous section, we can use the row and the column to pinpoint an element in the grid using get(). We can then add the element to our sum. Thus, the body of the for loop will contain:
```
sum += grid.get(row, column);
```
Of course we still need to print out our sum to the console. We can just use a simple print statement:
```
println(sum);
```
When put together, our finished function should look something like this:
```
function printSum(grid){
    var sum = 0;
    for(var row = 0; row < grid.numRows(); row++){ 
        for(var column = 0; column < grid.numCols(); column++){
            sum += grid.get(row, column);
        }
    }
    println(sum);
}
```

This will print out the sum, 46, to the console.

Now let's try another example.

### Finding Waldo!

Let's say that we are given a grid of random objects, and we have to figure out which row and which column waldo is in.
For example,

<table>
  <tr>
    <td> Table </td>
    <td> Bob </td>
    <td> Door </td>
  </tr>
  <tr>
    <td> John </td>
    <td> Apple </td> 
    <td> Waldo </td>
  </tr>
  <tr>
    <td> Karel </td>
    <td> Pencil </td> 
    <td> Book </td>
  </tr>
</table>

Like above, we will be using the nested for-loop structure.

```
function findWaldo(grid){
    for(var row = 0; row < grid.numRows(); row++){ 
        for(var column = 0; column < grid.numCols(); column++){
            //do something
        }
    }
}
```
When approaching this problem, there are two questions that we need to ask. First, "How will we find Waldo?" and secondly, "What should it do once we find Waldo?".

We already know that we can access elements in the grid using get(), so we can compare the elements to "Waldo" using "==". 

After we find Waldo, we can print out the row and column that we found Waldo in using `println()`. Just remember that since rows and columns start from 0, we have to add 1 to both the column and the row before printing out the values.
```
if(grid.get(row, column) == "Waldo"){
    var waldoRow = row + 1;
    var waldoCol = column + 1;
    println("Waldo is in row " + waldoRow + ", column " + waldoCol + ".");
}
```

Once we put everything together, our function should end up as:
```
function findWaldo(grid){
    for(var row = 0; row < grid.numRows(); row++){ 
        for(var column = 0; column < grid.numCols(); column++){
            if(grid.get(row, column) == "Waldo"){
                var waldoRow = row + 1;
                var waldoCol = column + 1;
                println("Waldo is in row " + waldoRow + ", column " + waldoCol + ".");
            }
        }
    }
}
```
Using our example grid, our function prints out 
```
Waldo is in row 2, column 3.
```




