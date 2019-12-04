```C#
using System;
using System.Collections.Generic;
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace _01_VariablesAndTypes
{
	[TestClass]
	public class ReferenceTypeExamples
	{
		[TestMethod]
		public void Strings()
		{
			string firstName = "Joshua";
			string lastName = "Tucker";

			// Concatenation
			string concatenatedFullName = firstName + " " + lastName;

			// Composite Formatting
			string compositeFullName =
					string.Format("Hi my name is {0} {1}", firstName, lastName);

			// String Interpolation
			string interpolatedFullName = $"{firstName} {lastName}";

			Console.WriteLine(firstName);
			Console.WriteLine(lastName);
			Console.WriteLine(concatenatedFullName);
			Console.WriteLine(compositeFullName);
			Console.WriteLine(interpolatedFullName);
		}

		[TestMethod]
		public void Collections()
		{
			//-- Arrays
			// Here we've declared another example string so that we can use it in our array
			string stringExample = "Hello World!";

			// Here we're declaring our array, using the square brackets []
			string[] stringArray = { "Hello", "World!", "Why", "is it", "always", stringExample, "?" };

			string thirdItem = stringArray[2];
			Console.WriteLine(thirdItem);

			stringArray[0] = "Hey there";
			Console.WriteLine(stringArray[0]);

			//-- Lists
			List<string> listOfStrings = new List<string>();
			List<int> listOfIntegers = new List<int>();

			listOfStrings.Add("First string for our list");
			listOfIntegers.Add(461012);

			//-- Queues
			// Here we new up a new Queue that holds strings
			Queue<string> firstInFirstOut = new Queue<string>();

			// Unlike Lists, we have the Enqueue method instead of an Add method to add items to the Queue
			firstInFirstOut.Enqueue("I'm first!");
			firstInFirstOut.Enqueue("I'm next!");

			//-- Dictionaries
			// Here we're declarying a new Dictionary that has int as its key type and string as its value type
			Dictionary<int, string> keyAndValue = new Dictionary<int, string>();

			// With our dictionary now declared, we can add something to it with the Add method
			// Notice we need to give it both the Key's value and the Value's value
			keyAndValue.Add(7, "Agent");

			string valueSeven = keyAndValue[7];

			//-- Other Collection Examples
			SortedList<int, string> sortedKeyAndValue = new SortedList<int, string>(); 
			HashSet<int> uniqueList = new HashSet<int>();
			Stack<string> lastInFirstOut = new Stack<string>();
		}

		[TestMethod]
		public void Classes()
		{
			// Using the new keyword to new up an instance of a class
			Random rng = new Random();

			// Calling a member of the class by using the . (dot) operator
			// We also saw this with the collections above
			int randomNumber = rng.Next();
		}
	}
}
```