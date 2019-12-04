Introduce methods structure and implementation

Method structure:

1. Access modifier (public, private, internal)
2. Return type (The type that the method returns or spits out)
3. Method signature (Method name, and the parameters)

```C#
public string SayHello(string surname)
{
	Console.WriteLine($"Hello, Mr. {surname}");
}

string surname = "Wagner";

SayHello(surname);
```

### Method Challenge

In unit test project make a Calculator method that takes in two numbers, adds them together, and returns the sum. Have the students write both the method and a test method.

Complete this for the rest of the operators including the remainder operator.

Try to limit this to about 15 minutes.

Example code:

```C#
public int Add(int kung, int fu)
{
	int kungFu = kung + fu;
	return kungFu;
}

int numberOne = 10;
int numberTwo = 12;
int sum = Add(numberOne, numberTwo);

Console.WriteLine(sum);
```