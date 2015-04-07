# Logical Operators

## What Are Logical Operators?

Boolean variables can only take on one of two possible values, true or false. Logical operators allow you to combine and connect booleans in useful ways.

There are three fundamental boolean operators:

- NOT
- OR
- AND

These should look quite familiar; in fact, we use them in speech every day! The NOT operator is used on a single boolean, wheres AND and OR are used across multiple boolean values.

## The NOT Operator

NOT is represented in JavaScript as `!`. When placed in front of a boolean value, NOT causes the boolean to take on its opposite value. For example "NOT true" gives the answer "false." This is fairly intuitive -- if something is not true, then it must be false. Similarly, if something is not false, then it must be true.

The example below sets up a variable `hungry` as being true. Then it prints out NOT `hungry`.

```
var hungry = true;
println(!hungry);   // prints "false"
```

For a variable `p` that can be `true` or `false`:

| p     | !p    |
|-------|-------|
| true  | false |
| false | true  |


## The AND Operator

AND is represent in JavaScript as `&&`. An expression using AND is true only when all its component parts are true. If any of the boolean values are false, the whole expression evaluates to false.

For example, if it is 6:30am AND it is a school day, you should wake up. You can test the expression of "6:30am AND a school day." If both are true, then the whole expression evaluates to true. If either or both are false, then the whole expression is false, and you should stay in bed.

```
var sixThirty = true;
var schoolDay = false;
println(sixThirty && schoolDay);  // both values are not true, so it prints "false"
```
