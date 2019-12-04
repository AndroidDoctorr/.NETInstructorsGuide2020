In this section you'll be covering Conditionals. You'll need to introduce and explain:

* `if statements`
	* You'll also want to include `if, else if, else` examples
* `Switch Cases`
* `Ternaries`

<br>

### If Statements

Humans use conditionals every day of their life, even if they don't realize it. A few classic examples of conditional logic humans use are:

* If I am hungry, I should eat.
* If I am tired, I should sleep.
* If I am bad, I should get good.

The concept of a conditional is exactly that. You declare a condition and write out should happen if the condition is true.

For example, if you're not hungry you don't need to eat. If you ARE hungry, then you should eat. That can be written as a simple if statement.

```C#
if (userIsHungry)
{
	// Put code that should fire off if the userIsHungry condition is true inside these braces
}
```

So now we know how to set up a block of code to fire off only if a condition is true. What happens if we want to a block of code to fire off only when the if statement doesn't fire off?

Let's image a situation where a kid wants to go to the movies with his friends. In this case he needs to get permission from his parents. His parents will want to evaluate whether he has finished his chores or not. **If** he is done with his chores he can go to the movies or **else** he must stay home and finish them.  
How would we write that in code?

We've shown how if statements work, so let's write one out for this. For this example let's imagine we have a boolean called `choresAreDone`.

```C#
if (choresAreDone)
{
	Console.WriteLine("Have fun at the movies!");
}
```

Great, that looks good to me. **If** the chores are done, the parents will tell him to have fun. Remember we said **if** they are done he can go, **else** he must stay home.

Let's add an else block of code to our if.

```C#
else
{
	Console.WriteLine("You must stay home and finish your chores!");
}
```

The **else** must always come right after the **if** statement is completed.

We can also nest an **if** inside an already existing **else** block. This will allow situations where we can say if else if. We can also simply do if with an if inside of it.

Have the students build out something that evaluates a given number of hours of sleep.

```C#
// This is just an example of how you can set up getting the totalHours value
// If you're using a Console application, you can replace the initial value with a Console.ReadLine();
string input = "7";
int totalHours = int.Parse(input);

if (totalHourse >= 8) //-- first if
{
	Console.WriteLine("You should be well rested.");
}
else //-- first else
{
	Console.WriteLine("You might be tired today.");

	// Here you can see another if statement embedded inside our first if's else
	if (totalHours < 4) //-- second if
	{
		Console.WriteLine("You should get more sleep!");
	}
}
```

Before moving on have the students mess around with this. Change up the input value and step through different scenarios with breakpoints.

If you only want to stack if statements you can ignore the first part in the else and just do an `if, else if`:

```C#
if (conditionOne)
{
	// Code if conditionOne is true
}
else if (conditionTwo)
{
	// Code if conditionOne is false and conditonTwo is true
}
```

<br>

### Switch Cases

Switch Cases have a similar structure to if statements, except they have different use cases.

If statements are good for boolean statments. My age is greater than 18. I am of the type Human. These are both booleans. My age is either greater than 18 or it is not. I am either an instance of the Human type or I am not.

Switch cases are different. With a Switch statement, we write the code to do in each specific case. 

Our structure is as follows:
	
	The switch keyword.
	The value being evaluated (Located in the parentheses)
	The cases {Located in the curly braces}
		Each case has the keyword "case" followed by the value expected.
		If we're evaluating (age), I might have a "case 18:"
			After the case comes the code that will execute if this case is met.
			Each case also has to have some sort of escape.
			Often this will be done with a "break;" at the end.

Here we can see an example of this:

```C#
int input = 1;

switch (input)
{
	case 1:
		Console.WriteLine("Hello");
		break;
	case 2:
		Console.WriteLine("What you doing?");
		break;
	default:
		Console.WriteLine("This is default. It will execute if no other case is evaluates as true. Defaults are not required.");
		break;
}
```

Now we can look at another example that deals with ages. Notice, if we want to cover a range we have to start defining A LOT of cases. With C# switches are not good for ranges like this.

```C#
int age = 37;

switch (age)
{
	case 18:
		// Code for 18 year olds
		break;
	case 19:
		// Code for 19 year olds
		break;
	case 20:
		// Code for 20 year olds
		break;
	case 21: //-- Here we see we can stack cases together over one chunk of code
	case 22:
	case 23:
		// Code for ages from 21-23
		break;
	default:
		// If no specific case is met then you can use a default set of code
		break;
}
```

Ask the students how they would build out an if statement that fulfills a similar goal. Let them experiment and build one out.

<br>

### Ternaries

The ternary operator in C# is a conditional operator that evaluates a boolean and then returns/outputs the predefined true or false value.

It's basically a one line if else statement. The biggest difference is that, in C#, ternaries are only good for value assignment. This means we can't just have a ternary that executes code.

Its structure is as follows:

	variable = (boolean) ? trueValue : falseValue;

Here are a couple examples of ternaries in C#.

```C#
int age = 31;

// variable = (Condition/Boolean) ? trueResult : falseResult;
bool isAdult = (age > 17) ? true : false;

int numOne = 10;

int numTwo = (numOne == 10) ? 30 : 20;
Console.WriteLine(numTwo);

Console.WriteLine((numOne == 10) ? "True" : "False");
```

Again, encourage your students to take time to breakpoint through the code. Make sure you're demonstrating this as you go.