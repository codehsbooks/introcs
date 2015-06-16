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

We want to find the sum of all these numbers. Now how do we accomplish this? We would have to loop over the array, but what type of loop would we use? To access a number in the grid, we would need two variables that point to the row and the column. Thus, the best way to accomplish this task is to use two nested for-loops, one for the row and one for the column.

The loop structure we would want to use is as follows:

```
for(var row = 0; row < grid.numRows(); row++){ //this loops over the rows
    for(var column = 0; column < grid.numCols(); column++){ //this loops over the columns
        //do something
    }
}
```

Thus, if we wanted to find the sum of the numbers in the grid, we would use 
