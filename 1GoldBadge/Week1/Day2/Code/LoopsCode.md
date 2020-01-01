04_Loops Assembly  
LoopExamples.cs

```C#
using System;
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace _04_Loops
{
	[TestClass]
	public class LoopExamples
	{
		[TestMethod]
		public void WhileLoops()
		{
			int total = 1;

			while (total != 10)
			{
				Console.WriteLine(total);
				total++;
			}

			total = 0;

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
		}
		
		[TestMethod]
		public void ForLoops()
		{
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

			for (int i = 0; i > -100; i--)
			{
				Console.WriteLine(i);
			}
		}

		[TestMethod]
		public void ForeachLoops()
		{
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

			List<string> ourClass = new List<string>();
			ourClass.Add("Josh");
			ourClass.Add("Will");
			ourClass.Add("Ben");
			ourClass.Add("Banana");

			foreach (string person in ourClass)
			{
				// Continue iterating if the instructor's name comes up
				if (person == "Joshua") 
				{
					continue;
				}

				Console.WriteLine($"{person} is a student!");
			}
		}

	}
}
```