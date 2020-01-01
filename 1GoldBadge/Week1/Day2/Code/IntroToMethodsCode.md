05_Methods Assembly  
MethodExamples.cs

```C#
using System;
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace _05_Methods
{
	[TestClass]
	public class MethodExamples
	{
		[TestMethod]
		public void MethodTests()
		{
			int sumOne = AddTwoNumbers(4, 17);
			AddTwoNumbers(6, 25);

			int numberOne = int.Parse("17");

			string response = "5";
			int numberTwo = int.Parse(response);
			
			int sumTwo = AddTwoNumbers(numberOne, numberTwo);
			
			int x = 4, y = 4;
			int sumThree = AddTwoNumbers(x, y);

			float dividend = DivideTwoNumbers(8, 3);
			Console.WriteLine(dividend);

			int difference = SubTwoNumbers(4, 2);

			int product = MultiplyTwoNumbers(4, 4);
		}

		//Access modifier (public, private, internal)
		//Return type (The type that the method returns or spits out)
		//Method signature (Method name, and the parameters)

		//Access modifier   return type   Name(Parameters)
		private int AddTwoNumbers(int x, int y)
		{
			int sum = y + x;
			return sum;
		}

		private int SubTwoNumbers(int x, int y)
		{
			return x - y;
		}

		private int MultiplyTwoNumbers(int x, int y)
		{
			// f(x, y) = x * y
			return x * y;
		}

		private float DivideTwoNumbers(float x, float y)
		{
			return x / y;
		}
	}
}

```