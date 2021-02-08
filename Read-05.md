## Comparison and Logical Operators

 * **Comparison operators** — operators that compare values and return true or false. The operators include:( >, <, >=, <=, ===, and !==).

* **Logical operators** — operators that combine multiple boolean expressions or values and provide a single boolean output. The operators include: (&&, ||, and !).

## Comparison Operators

You may be familiar with comparison operators from math class. Let’s make sure there aren’t any gaps in your knowledge.

* Less than (<) — returns true if the value on the left is less than the value on the right, otherwise it returns false.

* Greater than (>) — returns true if the value on the left is greater than the value on the right, otherwise it returns false.

* Less than or equal to (<=) — returns true if the value on the left is less than or equal to the value on the right, otherwise it returns false.

* Greater than or equal to (>=) — returns true if the value on the left is greater than or equal to the value on the right, otherwise it returns false.

* Equal to (===) — returns true if the value on the left is equal to the value on the right, otherwise it returns false.

* Not equal to (!==) — returns true if the value on the left is not equal to the value on the right, otherwise it returns false.

## Logical Operators
Comparison operators allow us to assert the equality of a statement with JavaScript.

There are scenarios, however, in which we must assert whether multiple values or expressions are true. In JavaScript, we can use logical operators to make these assertions.
* && (and) — This operator will be truthy (act like true) if and only if the expressions on both sides of it are true.

* || (or) — This operator will be truthy if the expression on either side of it is true. Otherwise, it will be falsy (act like false).
```<script>```

```var color ="red";```

```if(5>=5 && color==='red' )```

```</script>```

The && operator requires that both expressions be true in order for the expression to be truthy. Because one expression is false and the other is true, the expression is falsy and evaluates to false.


# Loops

## While Loop

The **while** loop creates a loop that is executed as long as a specified condition evaluates to **true**. The loop will continue to run until the condition evaluates to **false**. The condition is specified before the loop, and usually, some variable is incremented or altered in the **while** loop body to determine when the loop should stop.

```<script>```

```var sum=0;```

```var i=0;```

```while(i>20){```

```sum+=i;```

```}```

```</script>```

## For Loop
A **for** loop declares looping instructions, with three important pieces of information separated by semicolons ```;```:

* The initialization defines where to begin the loop by declaring (or referencing) the iterator variable.

* The stopping condition determines when to stop looping (when the expression evaluates to false).

* The iteration statement updates the iterator each time the loop is completed.

```<script>```

```for(var i=0;i< 20 ;i++){```

 ```consol.log(i);```

```}```