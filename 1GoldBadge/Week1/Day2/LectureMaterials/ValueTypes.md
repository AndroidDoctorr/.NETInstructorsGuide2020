### Booleans (bool)

Booleans are types that represent true/false values. We'll see where these come in when we start discussing conditionals. Right now, just know they're a pretty simple type that holds only a **true** or **false** value.

When creating a new variable you have two steps to complete. Variables require both **Declaration** and **Initialization**/**Assignment**.

When you declare something, you give it both the **type** and its **name**.  
When you initialize something, you're **assigning** it a **value**.  
You can do these at the same time or in separate statements.

```C#
//Here we've declared a variable called declared
bool declared;

// Now we've called our variable and assigned a value to it
declared = true;

// In this example, we're declaring AND initializing it all at once
bool declarationAndInitalized = false;

// You can call a variable by its name and assign it a new value even if it has a value already.
declarationAndInitialized = true;
```

Notice that all of the statements end with a semicolon (`;`). This indicates it is the end of a statement. Statements can sometimes take up multiple lines, so keep an eye out for the hard stop that is the semicolon. It's just like the period (.) in an English sentence or "stop" in a telegram.

Now that we have a couple examples, we can discuss the naming convention in C#. For variables we use camelCase where each word except the first in a name is capitalized.  
**Ex:** thisIsACamelCaseVariableName

<br>

### Characters (char)

In C# we have a type called **char** that allows us to represent any character. This can be a letter, number, symbol, etc. They can also be [special characters/escape sequences](https://devblogs.microsoft.com/csharpfaq/what-character-escape-sequences-are-available/).

```C#
char character = 'a';
char symbol = '?';
char number = '7';
char space = ' ';
char specialCharacter = '\n';
```

Note that a char holds a SINGLE character. This means that you **cannot** have `char number = '100';` because that has three different characters in it. Soon we'll discuss strings, which are collections of characters.

<br>

### Numeric Types

In C# we have a bunch of different number types. It isn't necessary for students to know every single one. Like most topics, just knowing that there are options or that something does exist is a good enough place to start.

#### Whole Numbers

```C#
byte byteMin = 0; 
byte byteMax = 255;
short shortMin = -32768;
short shortMax = 32768;
int intMin = -2147483648;
int intMax = 2147483648;
long longMin = -9223372036854775808;
long longMax = 9223372036854775808;
int a = 15;
int b = -10;
```

*For these examples you don't need to show the min/max values, they're just examples. That said they are a good way to display how large some of the values are.*

#### Decimals

```C#
float floatExample = 1.045231f;
double doubleExample = 1.789053278907036d;
decimal decimalExample = 1.2578907289045789789789789787897m;
```

_*Note that floats, doubles, and decimals all have a suffix (Fun fact: suffixes in C# are not case sensitive)._

Make sure you explain that each of these have different uses. Also, double is the *default* or implicit decimal type for C#.

<br>

### Enums

As we proceed through C# we'll find outself making new types. Exciting, right‽ One of the easiest ways to do this is with an **enum**.

An enum has two main parts:
* A name (the name of the type)
* Collection of possible values

``` C#
enum PastryType { Cake, Cupcake, Eclaire, PetitFour, Croissant };
```

Here we've created a new type called PastryType. This means we can now make a new variable with that type!

The same way we've declared variables of other types, we can declare one of the type PastryType.

``` C#
PastryType myPastry = PastryType.Crossaint;
```

Notice that when we assign the variable a value we're calling the value directly from our defined values. You can discuss the dot (.) access operator now or later, that's up to you.

<br>

### Structs

While understanding what a struct is may be difficult for the students to start off, it may be good to introduce them to the concept to start off.

An example of a struct that can be shown would be a `DateTime` or `TimeSpan`.

```C#
DateTime today = DateTime.Today;
DateTime birthday = new DateTime(1972, 6, 20);
```

We'll see this `new` keyword more as we start working with more complex objects. This keyword literally creates a NEW instance of whatever type you're using, meaning it must allocate memory for the new object.  
This should start to make more sense once you get into reference types.

You can show off a TimeSpan object later in the Operators section.
