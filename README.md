# Variable

## Learning Goals

- Explain what a variable is in Java

## Introduction
A variable is a label that points to a value in the memory.

Here's our `Bicycle` class example from earlier. Let's explore what we're
doing here.

```java
public class Bicycle {
    String color; 
    int height; 
    int position; 
} 
```

When I tell you that my bicycle is 36 inches high and you tell me that your bicycle is 42 inches high, 
we have both stored this information somewhere in our heads. Something like this:  
* John's bike is 36 inches high  
* Claire's bike is 42 inches high 

If we had other bikes, we could imagine they could be a lot of different heights. In other words, the "height" property 
of the bike can "vary" from bike to bike. So we call it a "variable" and we give it a name, so we can refer to it later. 
In Java, we do that as follows: 

```java 
int height; 
```

The first part of that statement is the type of the variable, which indicates to Java the kind of value I'm expecting to 
store in this variable. The second part is the name I want to be able to refer to the variable as.
Once we define a variable, we can give it a value and we can refer to it at a later stage. 

## Why does a variable have a type?

A variable has a type so that we can control what values can be assigned to it. In our example, we expect the height of 
the bike to be expressed in inches, so a word would not be a good value to assign to the `height` variable. This is important 
because we expect to be able to do specific things with specific variables based on their type. 

For example, if I know the height of both our bikes, I would expect to be able to calculate whether our bikes are the same 
height, and based on the calculation be able to determine whether we could use each other's bikes. This is easy to do 
if I know the height of the bike is a number: 
* Take the number from the height of your bike: `42` 
* Subtract the height of my bike: `36` 
* The result is `12` 

Now imagine that instead of `42`, the height of your bike is stored as `tall`. What is `"tall" minus 36` supposed to be? Type 
mismatches can cause a lot of issues in programming, so Java guards against that by forcing us to specify a type with each variable
we define. 

Note that not all languages are "typed", meaning that not all languages force variables to have types. Discussing the pros and 
cons of typed vs non-typed languages it outside the scope of this course. Just know that Java is typed and will therefore warn 
you when you try to perform operations on variables of different types that are not compatible. 
