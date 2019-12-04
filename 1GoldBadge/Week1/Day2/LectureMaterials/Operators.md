In this section we'll be covering different operator types available in C#.

Introduce different operators.

```C#
int sum = a + b;
int difference = a - b;
int product = a * b;
int quotient = a / b; //-- With whole numbers it drops any remainder/decimal
int remainder = a % b; //-- Returns only the remainder of the operation
```

Certain other types can be set up to use operators as well. The built in DateTime type is built to allow this.

```C#
DateTime today = DateTimeUtc.Now;
DateTime someDay = new DateTime(1978, 1, 1);
TimeSpan timeSpan = today - someDay; //-- Again we see the subtraction operator being used
```

<br>

### Operator Challenge

Have the students spend 5-10 minutes creating new variables and using the operators. Have them write the operation results to the Console as well practice using breakpoints.

If you're using test methods, have them check the output in the Test Explorer. Otherwise, have them display their output to the Console.