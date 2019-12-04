In this section you'll be introducing loops in C#.

You'll want to start by covering these loops:

* while loops
* for loops
* foreach loops
* [do while loops](https://i.redd.it/6wksqjmmyw321.jpg)
	* For do while loops, you're welcome to mention them to students, but we won't spend too much time on this now.

### While Loops

```C#
int total = 1;

while (total != 10)
{
	Console.WriteLine(total);
	total++;
}

while (true)
{
	break;
}

int total = 1;

while (total != 10)
{
	Console.WriteLine(total);
	total++;
}

total = 0;

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

<br>

### For Loops

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

int studentCount = 11;
for (int i = 0; i < studentCount; i++)
{
	Console.WriteLine(i);
}

for (int i = 0; i > -100; i--)
{
	Console.WriteLine(i);
}
```

<br>

### Foreach Loops

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

string[] students = { "Joshua", "Lawrence", "Luke", "Ransford" };

foreach (string student in students)
{
	Console.WriteLine($"{student} is a .NET student.");
}
```