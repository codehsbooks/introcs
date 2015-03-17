# Introduction to Programming with Karel the Dog

In this chapter we are going to introduce you to programming with Karel the Dog. Programming is the process of
giving instructions to a computer. Giving a list of instructions to the computer is similar to the way you can give commands to a dog.

### What is Karel?

Karel is a dog that lives in a grid world. Karel can move around the grid world and put down and take tennis balls,
and we can use Karel to solve different problems and explore the basics of programming. Karel understands a few basic commands that you can use when writing your programs.

## Karel's World

Karel lives in a grid world. Each point on the grid is marked by a dot, and is a location that Karel can be in.

The world has streets and avenues. The streets run horizontally and the avenues run vertically. The first street is the first row at the bottom of the grid, and the first avenue is the leftmost column of the grid.

Karel can face four different directions - north, south, east, or west.

## Commands in Karel

Karel can move around the grid world and put down and take tennis balls. In order to get Karel to do something,
you need to give Karel a command. A command is an instruction for an action that Karel can do.

Karel only knows four commands:

    move();
    putBall();
    takeBall();
    turnLeft();

These are the only four words that Karel understands.

## What does each command do?

The `move()` command moves Karel one spot in the direction that Karel is facing.

The `putBall()` command puts down one tennis ball in the spot that Karel is currently in.

The `takeBall()` command removes one tennis ball from the spot that Karel is currently in.

The `turnLeft()` command turns Karel 90 degrees to the left.

## The parts of a command

There are a few important things to note when you write a command.

* You need to write the command exactly as it appears

* You need to match the exact capitalization

`move();` is different from `Move();`

* Make sure to end every command with a `();`

This is how Karel can understand the command. These rules are called the syntax.

* Each command goes on its own line.

## Our First Karel Program

![Start and Ending World](https://www.evernote.com/shard/s4/sh/ecab1bdc-c74d-4394-b92c-11790f95a86f/c3b1398ee6eb5154c4a9601e3c03ec50/deep/0/Introduction-to-Programming-With-Karel---CodeHS.png)

Imagine you have Karel starting in the world on the left: in the bottom left corner, facing east. You want to get Karel to the world on the right. What would be the code that you write?

Remember, Karel has four commands, and we can use those commands to write this program. Below you can find the program.

```
move();
move();
putBall();
move();
move();
```

Great job, you did it!









