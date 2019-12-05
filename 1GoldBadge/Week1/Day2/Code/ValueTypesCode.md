01_Types Assembly  
ValueTypeExamples.cs

```C#
using System;
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace _01_Types
{
	[TestClass]
	public class ValueTypeExamples
	{
		[TestMethod]
		public void Booleans()
		{
			bool declared;  // This is declaration
			declared = true;  // Here we're assigning/initializing our value

			// In this example, we're declaring AND initializing it all at once
			bool declarationAndInitalized = false;

			// You can call a variable by its name and assign it a new value even if it has a value already.
			declarationAndInitialized = true;
		}

		[TestMethod]
		public void Characters()
		{
			char character = 'a';
			char symbol = '?';
			char number = '7';
			char space = ' ';
			char specialCharacter = '\n';
		}

		[TestMethod]
		public void WholeNumbers()
		{
			byte byteExample = 255;
			sbyte sByteMax = -128;
			short shortExample = 32767;
			Int16 anotherShortExample = 32000;
			int intMin = -2147483648;
			Int32 intMax = 2147483647;
			long longExample = 9223372036854775807;
			Int64 longMin = -9223372036854775808;

			int a = 15;
			int b = -10;
		}

		[TestMethod]
		public void Decimals()
		{
			float floatExample = 1.045231f;
			double doubleExample = 1.789053278907036d;
			decimal decimalExample = 1.2578907289045789789789789787897m;
		}

		// Here we've declared our enum, our custom type and its 5 possible values
		enum PastryType { Cake, Cupcake, Eclaire, PetitFour, Croissant };

		[TestMethod]
		public void Enums()
		{
			PastryType myPastry = PastryType.Crossaint;
			PastryType anotherOne = PastryType.Cake;
		}

		// Number types in C# are structs as well, but we use the keywords so we don't notice it as much. That's why numbers have a default value of 0 when they are declared.
		[TestMethod]
		public void Structs()
		{
			// If we hover over the int keyword intellisense will show us that it is a struct
			int age = 42;

			DateTime today = DateTime.Today;
			DateTime birthday = new DateTime(1972, 6, 20);
		}
	}
}
```