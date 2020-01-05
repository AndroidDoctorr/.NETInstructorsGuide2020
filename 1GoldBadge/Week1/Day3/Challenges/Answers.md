## Morning Whiteboard Challenge Answers

1. Declare and initialize three variables. One of type `int`, one of type `string`, and one of type `DateTime`.
```C#
int age = 29;
string name = "Alexander";
DateTime birthday = new DateTime(1990, 3, 14);
```

2. Create a method that subtracts to numbers and returns the value.
```C#
public int SimpleSubtraction(int numOne, int numTwo)
{
    int result = numOne - numTwo;
    return result;
}
```

3. Create a method that takes two strings from the user and outputs a string.
```C#
public void TwoStrings(string one, string two)
{
    Console.WriteLine($"Here is the first string passed in {one} and here is the second string passed in {two}");
}
```

4. Write a switch case that asks the user if they are wearing clothes.
```C#
switch(input)
{
case "y":
    Console.WriteLine("Thank you");
    break;
case "n":
    Console.WriteLine("Put something on");
    break;
default:
    Console.WriteLine("What are you wearing");
    break;
}
```
5. Write a if else statement that uses a boolean to check if the user is happy.
```C#
if (isHappy)
{
    Console.WriteLine("I'm glad to hear it! :)");
}
else
{
    Console.WriteLine("Don't worry, being happy is overrated.");
}
```

6. Write a if else if else that asks the user how much money they make a year. Check ranges between 1,000-10,000, 11,000-50,000, and 51,000-100,000. Output to the test runner based on each salary range. Have an else statement to prepare for the user not giving their salary range or out of the ranges we are checking.
```C#
int input = int.Parse(Console.ReadLine());
if (input <= 10000 || input > 15000)
{
    Console.WriteLine("Cool");
}
else if (input <= 50000)
{
    Console.WriteLine("Okay");
}
else if (input <= 100000)
{
    Console.WriteLine("That is a little bit");
}
else
{
    Console.WriteLine("What do you do?");
}
```