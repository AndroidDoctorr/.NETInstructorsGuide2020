03_Conditionals Assembly  
ConditionalExamples.cs

```C#
using System;
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace _03_Conditionals
{
	[TestClass]
	public class ConditionalExamples
	{
		[TestMethod]
		public void IfStatements()
		{
			bool userIsHungry = true;
			if (userIsHungry)
			{
				// Put code that should fire off if the userIsHungry condition is true inside these braces
				Console.WriteLine("Eat something!")
			}

			string hoursSpentStudying = 1;
			if (hoursSpentStudying < 16)
			{
				Console.WriteLine("Are you even trying?");
			}
		}

		[TestMethod]
		public void IfElseStatements()
		{	
			bool choresAreDone = false;

			if (choresAreDone)
			{
				Console.WriteLine("Have fun at the movies!");
			}
			else 
			{
				Console.WriteLine("You must stay home and finish your chores!");
			}


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
			
			
			int age = 7;

			// Here we have chained if else statements.
			if (age > 17)
			{
				Console.WriteLine("You're an adult.");
			}
			else if (age > 6)
			{
				Console.WriteLine("You're a kid.");
			}
			else if (age > 0)
			{
				Console.WriteLine("You're far too young to be on a computer");
			}
			else
			{
				Console.WriteLine("You're not born yet.");
			}

			// We also have more comparators to show off here
			if (age < 65 && age > 18)
			{
				// And comparison
			}

			if (age > 65 || age < 18)
			{
				// Or comparison
			}

			if (age == 21)
			{
				// Is equal to
			}

			if (age != 19)
			{
				// Not equals to
				// Bang operator
			}
		}

		[TestMethod]
		public void SwitchCases()
		{
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
		}

		[TestMethod]
		public void Ternaries()
		{
			int age = 31;

			// (Condition/Boolean) ? trueResult : falseResult;
			bool isAdult = (age > 17) ? true : false;

			int numOne = 10;

			int numTwo = (numOne == 10) ? 30 : 20;
			Console.WriteLine(numTwo);

			Console.WriteLine((numOne == 10) ? "True" : "False");
		}
	}
}
```