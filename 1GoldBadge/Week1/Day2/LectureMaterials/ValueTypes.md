

### Booleans (bool)

Booleans are types that represent true/false values. We'll see where these come in when we start discussing conditionals. Right now, just know they're a pretty simple type that holds only a **true** or **false** value.

```C#
bool isExcited = true;
bool canFly = false;
```

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

An example of a struct that can be shown would be a `DateTime`.