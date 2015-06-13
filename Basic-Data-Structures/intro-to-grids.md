## Intro to Grids

#### Creating a new grid

Let's say that we want to make a new grid named "dogs" that has 2 rows and 3 columns. We can do this like so:

```
var dogs = new Grid(2, 3); //(rows, columns)
```

#### Structure of a grid

Before we can start using our grid, we need to understand the structure of the grid. Using our above example of a grid with 2 rows and 3 columns, the indexes of each element are laid out like below.

**Note: Remember that indexes start from 0, not 1.**
<table>
  <tr>
    <td> (0, 0) </td>
    <td> (0, 1) </td>
    <td> (0, 2) </td>
  </tr>
  <tr>
    <td> (1, 0) </td>
    <td> (1, 1) </td> 
    <td> (1, 2) </td>
  </tr>
  
</table>

#### Using Grids

##### Setting elements in a grid

Since we haven't set any elements in our grid, all of the elements in our grid are set to "undefined".

There are three ways that we can set elements in our grid:

###### Setting them all to be the same

Say we wanted to set all of the elements of our "dogs" grid to be equal to "Golden Retriever". We can do this by using the init() function.

```
dogs.init("Golden Retriever");
```
After we run the above code snippet, every cell of our grid will contain "Golden Retriever".

<table>
  <tr>
    <td> Golden Retriever </td>
    <td> Golden Retriever </td>
    <td> Golden Retriever </td>
  </tr>
  <tr>
    <td> Golden Retriever </td>
    <td> Golden Retriever </td> 
    <td> Golden Retriever </td>
  </tr>
</table>

###### Setting elements one at a time
Now what if we want to set elements one at a time? In order to set an element in a grid, we want to use the set() function. The set() function uses three arguments, row, column, and the value that you want to set the element to. For instance, if you want to set the element at row 1, column 1 of our dogs array to "Labrador":

```
dogs.set(1, 1, "Labrador");
```
After running the above line of code, our grid of dogs will now look like:

<table>
  <tr>
    <td> Golden Retriever </td>
    <td> Golden Retriever </td>
    <td> Golden Retriever </td>
  </tr>
  <tr>
    <td> Golden Retriever </td>
    <td>Labrador</td> 
    <td> Golden Retriever </td>
  </tr>
</table>

###### Setting elements using arrays



##### Accessing elements in a grid







