### Strings
Earlier we discussed the `char` type and how they only hold one character at a time. To spell "Eleven Fifty Academy" you need a total of 20 characters. Sure you could slim that down by reusing the space, the lowercase e, etc. Obviously this doesn't seem like a nice way to do it. Imagine having ~20 different variables every time you wanted to display a few words.

To work around this, we have something called a **string**. Strings are a collection of `char` objects. This means we can make a single string hold a bunch of characters.

Let's show some examples.

```C#
// Like other types we can simply declare a variable of the string type
string thisIsDeclaration;

// We can also declare and then later initialize a value
string declared;
declared = "This is initialized.";

// Declaration and Initialization
string declarationAndInitialization = "This is both declaring and initializing.";
```

Strings are our way to show a collection of characters (char) in C#. Strings can contain a collection of any letter, number, symbol, etc. Instead of having to declare each character at a time we just declare a string and give it its entire value.

If a string is declared but not given an initial value, it will be **null**. What are the differences between zero and null?

0 is a value.  
If you have a string with a value of "", it still has a value.  
Null is absolutely nothing. It's the lack of value.

[Here's a visual aid!](https://i.redd.it/3370lkxk56ny.jpg)

This stands true for all reference types.

#### Manipulating Strings

We have a few different methods of manipulating strings. Start by declaring a few new strings.

```C#
string firstName = "Joshua";
string lastName = "Tucker";

// Here we see concatenation. This is where we take different values and smash them together, more or less
// Why are we adding the " " part between the first and last names?
string concatenatedFullName = firstName + " " + lastName;

// We also have what's called composite formatting, where you declare a space for a variable and then later give the variables
// While this part will probably make more sense later once we start talking about methods, you can see here we're using curly braces and indexes (starting at 0) to place variables into the given string.
string compositeFullName = string.Format("{0} {1}", firstName, lastName);

// Here we're using string interpolation
// It's similar to composite formatting, but instead of indexes we plug the variables in directly to the string
// Notice the $ in front of the string. This is very important!
string interpolatedFullName = $"{firstName} {lastName}";

```

We can see there are a few different ways to manipulate and build strings. Students should not worry too much about knowing them all, as long as they're familiar with the concepts and have their notes. Whatever they like best is fine to work with for now.

<br>

### Collections
So we used the word Collection earlier when talking about strings. They're collections of characters, right? Well we can have collections that hold other types as well.

#### Arrays

In C# there are a decent amount of collection types. One of the simpler collections is what is known as an array. An array is a type, so just like all other types when you create an instance of an array you need to declare it as an array. How do we do that?

```C#
// Here we've declared another example string so that we can use it in our array
string stringExample = "Hello World!";

// Here we're declaring our array, using the square brackets []
// Notice the type that the array holds is given before the brackets, in this case it's string[]. This means this array only holds strings
string[] stringArray = { "Hello", "World!", "Why", "is it", "always", stringExample, "?" };
```

This allows us to refer to a collection of strings by one name, `stringArray`, the same way that we refer to a collection of characters, e.g. `stringExample`.

So this is a pretty important concept we're starting to discuss. In C#, a language that falls under the OOP (Object Oriented Programming) category, we're always working with objects. It's very important that students start to think about everything as an object and the items it contains.  
This will really start to get nailed down with classes later on.

Now that we have a collection, we can show how to grab items from the collection. Reminder that C# using zero-based indexing, which means that you start counting at zero.

With arrays, and most collections in C# for that matter, you can use square brackets (`[]`) to reach into a collection a specified location. For example, here we can grab the third item (located at index of 2) in our `stringArray` array.

```C#
string thirdItem = stringArray[2];
```

We can also use the indexing to assign/update a value.

```C#
stringArray[0] = "Hey there";
```

We'll see this technique used later with our other collections as well. Speaking of, let's cover more collection types.

#### Lists

We'll be seeing a few different collection types, and while we'll need to dive deeper into them later, right now we just want to introduce them.

Lists are the first type we want to show. Often you'll find yourself using Lists instead of arrays, because a List can grow dynamically where an array has its size defined at initialization.

Like we did with the DateTimes earlier, we're going to use the `new` keyword here. Remember this is how we new up a brand new instance of the type (in this case an instance of the List class) we're declaring.

```C#
List<string> listOfStrings = new List<string>();
List<int> listOfIntegers = new List<int>();
```

Similar to the way our `string[]` has the type declared, we declare the type that the collection holds inside the angle brackets (`<>`);

Because Lists can grow dynamically, we don't use indexing for assignments, at least not at first. We can call a method called `Add()` and give it a new item to add to our list. Don't worry about methods too much quite yet, we'll get there soon.

```C#
listOfStrings.Add("First string for our list");
listOfIntegers.Add(461012);
```

Most of our collections will have a similar way of adding items to the collection. In this case Lists just hold items in no particular order, so we can just add it without worrying about the order.

#### Queues

We also have a collection type called Queues, which are structured as FIFO, or First In, First Out. This means when you get added, the only things that are going to come out of the queue are things that were added before you.

Example:
```C#
// Here we new up a new Queue that holds strings
Queue<string> firstInFirstOut = new Queue<string>();

// Unlike Lists, we have the Enqueue method instead of an Add method to add items to the Queue
firstInFirstOut.Enqueue("I'm first!");
firstInFirstOut.Enqueue("I'm next!");
```


#### Dictionaries

Another collection type in C# that you'll need to know about is the Dictionary type.

Dictionaries are Key Value pairs, and we'll definitely see more on these later. For now we can just show an example or two.

```C#
// Here we're declarying a new Dictionary that has int as its key type and string as its value type
Dictionary<int, string> keyAndValue = new Dictionary<int, string>();

// With our dictionary now declared, we can add something to it with the Add method
// Notice we need to give it both the Key's value and the Value's value
keyAndValue.Add(7, "Agent");
```

With dictionaries we don't use indexing by number, we do it by key. So instead of getting our `Agent` value from the dictionary here by saying something like `keyAndValue[0]`, we would do `keyAndValue[7]` and this would return the string `"Agent"`.

We will see all of these collections, and more, later on. Don't spend too much time on this.

#### Other Collection types

The above three collections are types you will definitely see and need to understand in C#. Some other types you may show at some point but don't need to really hit on, maybe just include that they exist, are listed below. Just make it clear there are more types of collections in C#. The ones listed above are just the most common.

```C#
SortedList<int, string> sortedKeyAndValue = new SortedList<int, string>(); 
HashSet<int> uniqueList = new HashSet<int>();
Stack<string> lastInFirstOut = new Stack<string>();
```

Later on we'll see how we can really start to utilize collections.

<br>

### Classes

For now just briefly mention classes. If you just include that instances of classes are reference types that's probably good enough. They've seen all sorts of classes with the collections above, but if you want to show them more now is the time to just mention it. You'll discuss classes in the next couple days a lot more.

A quick example of a class would be the Random class. Again, don't spend too much time on this for now.

```C#
Random rng = new Random();
```

<br>

### What now?

Now that we have discussed a decent amount of value and reference types, let's move on to briefly discuss how they interact and work with your computer's memory.
