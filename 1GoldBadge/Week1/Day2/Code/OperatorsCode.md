02_Operators Assembly  
OperatorExamples.cs

```C#
using System;
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace _01_VariablesAndTypes
{
	[TestClass]
	public class OperatorExamples
	{
		[TestMethod]
		public void SimpleOperators()
		{
			// Addition
			int sum = a + b;
			Console.WriteLine(sum);

			// Subtraction
			int difference = a - b;
			Console.WriteLine(difference);

			// Multiplication
			int product = a * b;
			Console.WriteLine(product);

			// Division
			int quotient = a / b; //-- With whole numbers it drops any remainder/decimal
			Console.WriteLine(quotient);

			// Remainder
			int remainder = a % b; //-- Returns only the remainder of the operation
			Console.WriteLine(remainder);
		}

		[TestMethod]
		public void OtherUseExamples()
		{
			DateTime today = DateTimeUtc.Now;
			DateTime someDay = new DateTime(1978, 1, 1);
			TimeSpan timeSpan = today - someDay; //-- Again we see the subtraction operator being used
		}

		[TestMethod]
		public void Comparisons()
		{
			int age = 24;
			string username = "Joshua";

			// Equal
			bool equals = age == 41;
			bool userIsAdam = username == "Adam";

			// Not Equal
			bool notEqual = age != 112; //-- Bang operator
			bool userIsNotJustin = username != "Justin";
			
			// Greater than
			bool greaterThan = age > 12;

			// Greater than or Equal to
			bool greaterThanOrEqual = age >= 24;

			// Less than
			bool lessThan = age < 66;

			// Less than or Equal to
			bool lessThanOrEqual = age <= 24;

			// OR comparison
			bool orValue = equals || lessThan;

			bool trueValue = true;
			bool falseValue = false;

			bool tOrT = trueValue || trueValue;
			bool tOrF = trueValue || falseValue;
			bool fOrT = falseValue || trueValue;
			bool fOrF = falseValue || falseValue;

			// AND comparison
			bool andValue = greaterThan && orValue;

			bool tAndT = trueValue && trueValue;
			bool tAndF = trueValue && falseValue;
			bool fAndT = falseValue && trueValue;
			bool fAndF = falseValue && falseValue;
		}
	}
}
```