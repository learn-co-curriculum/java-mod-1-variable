# Variable

## Learning Goals

- Explain what a variable is in Java
- Discuss the different data types a variable can have
- Primitives vs. References

## Introduction

Let's look at our `Bicycle` class example from earlier and look closer at the properties.

```java
public class Bicycle {
    String color; 
    int height;
} 
```

When I tell you that my bicycle is 36 inches high, and you tell me that your bicycle is 42 inches high,
we have both stored this information somewhere in our heads. Something like this:  

- John's bike is 36 inches high  
- Claire's bike is 42 inches high

If we had other bikes, we could imagine there would be a lot of different heights. In other words, the "height" property
of the bike can "vary" from bike to bike. So we call it a **variable** and we give it a name, so we can refer to it
later. In Java, we do that as follows:

```java
int height; 
```

The first part of that statement is the type of variable, which indicates to Java the kind of value we are expecting to
store in this variable. The second part is the name we want to be able to refer to the variable as.
Once we define a variable, we can give it a value, and we can refer to it at a later stage.

## Why does a variable have a type?

A variable has a type so that we can control what values can be assigned to it. In our example, we expect the height of
the bike to be expressed in inches, so a word would not be a good value to assign to the `height` variable.
This is important because we expect to be able to do specific things with specific variables based on their type.

For example, if we know the height of both our bikes, we would expect to be able to calculate whether our bikes are the
same height. If they are, we could use each other's bikes. This is easy to do if we know the height of the bike is a
number:

- Take the number from the height of your bike: `42`
- Subtract the height of my bike: `36`
- The result is `12`

Now imagine that instead of `42`, the height of your bike is stored as `tall`. What is `"tall" minus 36` supposed to
be? Type mismatches can cause a lot of issues in programming, so Java guards against that by forcing us to specify a
type with each variable we define. This is why Java is considered a strongly typed programming language.

Note that not all languages are "typed", meaning that not all languages force variables to have types.
Discussing the pros and cons of typed vs non-typed languages is outside the scope of this course.
Just know that Java is typed and will therefore warn you when you try to perform operations on variables of different
types that are not compatible.

## Different Data Types

There are quite a few data types that a variable could be and for some of them, we will consider the size of the
average value we would be working with to determine what data type to use.

Before we get into that, let us talk about how we measure these data types. Data types are measured based off of how
much memory they can hold. We measure this in **bytes**. A **byte** is equivalent to 8 **bits**. A bit is the smallest
unit of storage and can store one binary digit (0 or 1).

| Data Type | Size    | Description                                                                   |
|-----------|---------|-------------------------------------------------------------------------------|
| `boolean` | 1 bit   | Stores true or false values                                                   |
| `byte`    | 1 byte  | Stores whole numbers from -128 to 127                                         |
 | `char`    | 2 bytes | Stores a single character or ASCII value                                      |
 | `int`     | 4 bytes | Stores whole numbers from -2.147 x 10<sup>9</sup> to 2.147 x 10<sup>9</sup>   |
| `long`    | 8 bytes | Stores whole numbers from -9.223 x 10<sup>18</sup> to 9.223 x 10<sup>18</sup> |
| `float`   | 4 bytes | Stores fractional numbers up to a precision of 6 to 7 decimal digits          |
| `double`  | 8 bytes | Stores fractional numbers up to a precision of 15 decimal digits              |

When it comes to true/false values, we tend to use **boolean** as the data type. When we want to store a letter or a
single character, we use the data type **char**. For whole numbers, we usually use **int** as the data type and
**double** for decimal values.

If we want to store a word or a sentence of words, we would use the data type **String**.

A String is a little different from the above data types. All the above data types in the table are **primitive types**.
**Primitive data types** are pre-defined in Java and stored within the memory stack. Non-primitive data types or
**reference data types** are stored slightly differently in memory in that they point to objects in the heap space.
We will talk more about memory in a minute, but for now know that the two types are stored differently within memory.
An example of a reference data type is a `String` or an Object like our `Bicycle`.

Now let us dive into what memory is and how it is used in Java!

## Resources

[Primitive Data Type table](https://www.w3schools.com/java/java_data_types.asp)
