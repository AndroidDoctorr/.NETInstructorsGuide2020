In this section you'll be introducing loops in C#.

You'll want to start by covering these loops:

* while loops
* for loops
* foreach loops
* [do while loops](https://i.redd.it/6wksqjmmyw321.jpg)
	* For do while loops, you're welcome to mention them to students, but we won't spend too much time on this now.

So what are loops? At their core, loops are a tool that allows us to write repeatable code. In this section we'll be covering three main types of loops.

While there are different types of loops, they all have some things in common. Each loop starts with a keyword (**while** for **while loops**, **for** for **for loops**, and **foreach** for **foreach loops**) followed by some condition that must be met. If the condition evaluates to true, then the loop runs another iteration. If it is not true then the code will continue on past the loop.

This also means that if the condtion is not met before the loop begins, it's possible for the loop's body to never fire off.

### While Loops

We'll start off by discussing **While Loops**. While loops are pretty simple in concept. While a given condition/boolean is true, continue looping.

```C#
int total = 1;

while (total != 10)
{
	Console.WriteLine(total);
	total++;
}
```
Here we see we have a conditon that our **total** is **not** 10. If our variable **total** ever contains the value of 10 our loop will end the next time it checks the conditon.

Make sure with all of these loop examples you use breakpoints to step through the process. I encourage you to change the code up to introduce different examples and scenarios.

<br>

#### Introducing the break keyword

Because we're only checking a boolean value we can actually plug in the default boolean values of true and false. Next we have an example where we have a while loop with the conditon of true.

This means the loop reads as: while true is true, keep looping. This would keep us in an infinite loop. Obviously this is not ideal. It does allow us to introduce a new concept, the **break** keyword.

Anytime during a loop we can use the keyword **break** to break out of the loop. This means we could exit before our evaluated condition is false. In the case of the value true, it will never be false so we'll need to utilize the break keyword.

*_In the case of a method, as we'll see later on, the return keyword can accomplish a similar outcome. This may not be helpful to students but it's good for you to keep in mind._

```C#
total = 0; // We're resetting our starting variable total that we declared above

// while true is true, keep looping
while (true)
{
	if (total == 10)
	{
		break;
	}
	Console.WriteLine("Always printing");
	total++;
}
```

We can also change it so that our true condition is a custom boolean that we can manipulate. Let's add another method that takes in a boolean and modifies it after some time.

```C#
bool continueLooping = true;
int loopCount = 0;

while (continueLooping)
{
	loopCount += 2;

	if (loopCount > 13)
	{
		continueLooping = false;
	}
}
```

<br>

### For Loops

Notice that so far we've been building out our while loops are iterating for a certain amount of iterations. In C# if we know how many iterations we want we can use another type of loop, the **for** loop.

Here we know we have a certain amount of students in the class. We can take that number and use it as our target number of iterations. It doesn't have to be 1 to 1, but it's a good place to start.

Build out the first for loop with the labels provided below.

```C#
int studentCount = 21;

//1 Starting Point
//2 While this condition is true, keep looping
//3 What we do after each loop
//4 Code we execute each loop
//for   //1         //2           //3
for (int i = 0; i < studentCount; i++) // i = i + 1
{
	//4
	Console.WriteLine(i);
}
```

We can see that the structure takes us through all 21 iterations in this case. This is because we start at 0 and count up by 1 until our number is no longer less than our target condition.

We can also go the other way, and subtract until we're no longer greater than a value as well.

```C#
for (int i = 0; i > -100; i--)
{
	Console.WriteLine(i);
}
```

For loops are not just for counting up or down. Their structure definitely allows for it, but they really are just good at letting you know exactly how many iterations there will be.

<br>

### Foreach Loops

Now we can discuss the foreach loop. Remember to check in with the students and see what they remember/know about it. 

Foreach loops are good for doing something **for each** object in a collection. If I wanted to grade each project, I could take the collection of objects and assess **EACH** one.

What this means that in a foreach loop, we write a single chunk of code that happens for each item in the given collection.

Remember how we discussed that strings are collections of characters? We can run strings through a foreach loop.

```C#
string name = "Joshua Tucker";

//1 Collection being worked on
//2 Name of the current iteration
//3 Type in the collection
//4 in keyword used to seperate the individual and the collection
//foreach //3  //2  //4  //1
foreach (char letter in name)
{
	Console.WriteLine(letter);
}
```
Have the students create a new collection of objects, in this case strings, and add to it at least a few items. In this case we're using students and adding it to a list.

This can also be an array, but just have them mess around with adding a few things and seeing the different output results.

After they have their collection built out, have them run it through a foreach loop.

```C#
List<string> ourClass = new List<string>();
ourClass.Add("Joshua");
ourClass.Add("Will");
ourClass.Add("Ben");
ourClass.Add("Banana");

foreach (string person in ourClass)
{
	Console.WriteLine($"{person} is a student!");
}
```

<br>

#### Using the continue keyword

Another thing before moving on is to introduce the **continue** keyword. The continue keyword acts similarly to the break keyword, but instead of breaking us out of the loop it **continues on to the next iteration**. This means we can skip certain iterations if a certain case is met.

In our student example, let's modify our foreach loop to include continuing if the name presented is the instructor's name.

```C#
foreach (string person in ourClass)
{
	if (person == "Joshua") 
	{
		continue;
	}

	Console.WriteLine($"{person} is a student!");
}
```

Loops are very helpful tool in programming. You definitely will find yourself needing to utilize them in the future.