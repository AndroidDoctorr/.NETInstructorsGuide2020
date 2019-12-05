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

<br>

### Comparators

Aside from general arithmetic operators, we also have operators used to compare values.

```C#
int age = 24;

// Equal
bool equals = age == 41;
```

Can also use equal to comparison on more than just numbers.

```C#
string username = "Joshua";

bool userIsAdam = username == "Adam";
```

One thing to understand is how comparing items works. With value types it's pretty straight forward: Is this value equal to the other value?

With reference types it's a little different. It's not comparing the object's value, it's comparing the stored address that's being used as the reference. If we think back to the Memory section, remember references have memory addresses that *reference* a value elsewhere.

If we want to check the opposite, and check if something is NOT equal to some value, then we use the bang (`!`) operator.

```C#
// Not Equal
bool notEqual = age != 112; //-- Bang operator

bool userIsNotJustin = username != "Justin";
```

We also can check values by greater than, greater than or equal, less than, and less than or equal.

```C#
// Greater than
bool greaterThan = age > 12;

// Greater than or Equal to
bool greaterThanOrEqual = age >= 24;

// Less than
bool lessThan = age < 66;

// Less than or Equal to
bool lessThanOrEqual = age <= 24;
```