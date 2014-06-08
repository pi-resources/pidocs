## Syntax
Python is an interpreted language. Each command goes on a new line. Lines are
terminated with a semicolon

## Code blocks
Some parts of the syntax require code blocks. These sections are identified
using indentation. Indentation should be a single tab. The section will be
assumed to have ended when the indentation goes back to the previous state.

## Variables
Variables are how you store a value for use later. Each variable has a name,
which you use to refer to it. Variable names are case sensitive.

The generally accepted standard for variable names is that they start with a
lower case letter, but use camelCase. In camel case, the first letter of each
contained word is captialised.

Variables are set using a single equals sign. The variable name is on the left,
and the value on the right.

There are a number of variable types:

| Type    | Used to store           |
| ------- | ----------------------- |
| integer | Whole numbers           |
| float   | Decimals                |
| string  | Alphanumeric characters |


### Tuples
A tuple is a collection of other types of variables that are related. They are
enclosed in parenthesis.

### Lists
A list stores an array of values that are referenced by a numeric key. Lists are
enclosed in square brackets.

### Dictionary
A dictionary is an array of values that are rerefenced by an alphanumeric key. A
dictionary is enclosed in curly braces.

```python
exampleInteger = 1;
exampleFloat = 1.2;
exampleString = "This is some text";
exampleTuple = (10, 20);
exampleList = ["red", "green", "blue"];
exampleDictionary = {"house": "brick", "shed": "wood", "greenhouse": "glass" };
```

## Comments
Comments allow you to put notes in your program. This helps when someone else
is reading it, as it assists them in understanding what the program is doing.
It is also useful when looking back at a program that you wrote a long time ago,
as you may not remember the exact flow of the program.

Comments are denoted by a hash symbol. Once the interpreter hits a hash symbol,
it will ignore the rest of that line.

```python
# This is a comment
# Just setting two to equal 2
two = 2; # This is a comment on the same line as some code
```

## Functions
Functions are a way of reusing common bits of code.

For example, if oyu need to read in the contents of a file a number of times,
you might put the code that opens the file and reads the contents into a
function. This saves space in your program, and also makes it easier to read.

Functions can take a number of parameters. There are two types of parameter:
required and optional. Required parameters must be specified or an error will
be raised. Optional parameters usually have a default value, so do not need
to be specified unless you want to change that value.

Functions can also return a value.

```python
# Defining a function for use later
# This function takes two required parameters
def add(x, y):
	return x + y;

# Calling functions:
z = add(2, 3);

# z will now be 5
```

## Modules
Modules in python allow you to group together related code. They are used
primarily to import functionality into your program.

Importing a module is done using the `import` keyword.

```python
import os;
```

You can also import only specific bits of modules:

```python
# Only get the version variable from sys
from sys import version;

print(version); # This will output the version of python that is running
```

## Flow control
Flow control is used to control how the interpreter flows through your program.

### Logical expressions
Before uing flow control, you must have an understanding of logical expressions.
Logical expressions allow you to make decisions when running your program.
For example, if you wanted a function to tell you if an integer was greater or
less than zero, you would use logical expressions.

The following logical operators are available:

| Symbol | Meaning                     | Can be used on         |
| ------ | --------------------------- | ---------------------- |
| ==     | is equal to                 | float, integer, string |
| !=     | is not equal to             | float, integer, string |
| <      | is less than                | float, integer         |
| >      | is greater than             | float, integer         |
| <=     | is less than or equal to    | float, integer         |
| >=     | is greater than or equal to | float, integer         |

### Boolean operators
If you want to evaluate multiple logical expressions, you can use a Boolean
operator.

#### And
The And keyword means both conditions must be met.

#### Or
The Or keyword means either condition must be met. Or will also evaluate to true
in the event that both conditions are met.

### If statements
If statements are used to execute a block of code only if one or more conditions
are met.

The block of code immediately after the if statement will be executed if the
statement evaluates to true. Optionally, you can include an else block, which
will be executed if the statement is false.

```python
# Personalise greeting if we have a name in variable name
if name != "":
	print("Your name is:");
	print(name);
else:
	print("Hello, whoever you are!");
```

### Looping
Sometimes you will need to repeat the same section of code either a fixed number
of times, or until a condition is met.

#### For loops
For loops iterate a set number of times. As an example, you can use a for loop
to count to 10:

```python
# The range command generates a list of integers starting with the first number,
# and finishing below the second. The following code will output 1 to 10
for a in range(1, 11):
	print(a);
```

#### While loops
While loops evaluate for as long as a condition is true. The following snippet
will do the same as the above for loop:

```python
a = 1;
while a <= 10:
	print(a);
	a = a + 1;
```
