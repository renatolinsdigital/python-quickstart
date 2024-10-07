# Python quickstart - Essential notes by Renato Lins

Python was initially created by Guido van Rossum in 1991 with the intention of creating a language that emphasizes code readability and simplicity. Over the years, Python has grown to become one of the most popular and versatile programming languages, utilized in web development, data analysis, artificial intelligence, scientific computing, and more.

## Table of Contents

- [1. Considerations: Why to learn Python](#1-considerations-why-to-learn-python)
- [2. Variables](#2-variables)
- [3. Data types](#3-data-types)
- [4. Type conversions](#4-type-conversions)
- [5. Operators](#5-operators)
- [6. Control Flow in Python - 'if' Statement](#6-control-flow-in-python---if-statement)
- [7. Control Flow II - Falsy and Truthy Values](#7-control-flow-ii---falsy-and-truthy-values)
- [8. Control flow III - Loops](#8-control-flow-iii---loops)
- [9. Control flow IV - match-case statements](#9-control-flow-iv---match-case-statements)
- [10. Basics of functions](#10-basics-of-functions)

---

### 1. Considerations: Why to learn Python

__Versatility Across Domains:__ Python is indispensable in various domains such as web development, data science, machine learning, automation, and scientific computing, demonstrating its broad applicability.

__Ease of Learning and Readability:__ Python's simple and concise syntax, along with its focus on readability, makes it easy to learn and understand, even for beginners.

__Multi-Paradigm Language:__ Python supports multiple programming paradigms, including object-oriented, imperative, and functional programming, offering developers flexibility in designing solutions.

__Rich Ecosystem of Libraries:__ Python boasts a vast collection of libraries and frameworks like NumPy, Pandas, Django, and TensorFlow, empowering developers with tools for diverse tasks ranging from data manipulation to web development and machine learning.

__Productivity and Rapid Development:__ Python enables rapid prototyping and development with its extensive standard library and third-party packages, facilitating efficient coding practices and quick iteration.

__Active Community and Support:__ Python enjoys a vibrant and supportive community, offering resources, tutorials, and forums for assistance. This active community contributes to Python's evolution and fosters collaboration among developers worldwide.

__Abundance of Job Opportunities:__ Proficiency in Python opens doors to a wide range of career opportunities in industries such as technology, finance, healthcare, and academia, thanks to its widespread adoption and versatility.

Ps. If you're new to Python and looking for a coding environment, consider using __pythononlinecompiler.com__ or __trinket.io__ to write and execute Python code interactively. These platforms offer a convenient way to experiment with Python syntax and observe the output of your code.

---

### 2. Variables

A variable is a named storage location in your computer's memory. Think of it as a labeled box where you can store and retrieve information. You create a variable in Python by simply assigning a value to a name.

```python
# Example of declaring a variable and assigning a text value
message = "Hello, Python!"

# Example of declaring and assigning a variable with numerical value
my_number = 42
```

Python does not have built-in support for constants in the same way that some other programming languages do (such as Java or C++). However, it does have conventions to indicate that a variable should be treated as a constant.

```python
# Example of declaring a constant variable
PI = 3.14
```

NOTE: In Python, when naming variables, it's recommended to adhere to a specific naming convention known as __snake_case__. This convention involves writing variable names with all lowercase letters and separating words using underscores. For example, if you want to represent the maximum temperature, you could name a variable as 'max_temperature'. Similarly, if you need to name a constant temperature value, it can be 'BASE_TEMPERATURE'. This is one of the practices that helps improve code readability and consistency, aligning with the conventions outlined in the Python Enhancement Proposal 8 (PEP 8), which is the official style guide for Python code. If you want to known more about Python style of coding, you can refer to __peps.python.org/pep-0008__.

---

### 3. Data types

Variables in Python are containers that store data values. They allow you to assign names to values, making it easier to reference and manipulate data in your code. Python supports several types of variables, each serving a different purpose. So we have commonly used data types such as:

__String:__ Represents text and is enclosed in single or double quotes.

```python
greeting = "Hello, World!"
```

__Integer and Float:__ Represents numerical values, including integers and floating-point numbers.

```python
age = 25  # An integer representing age
weight = 78.5  # A float representing weight
```

__Boolean:__ Represents either True or False, often used for logical operations.

```python
is_coding_fun = True
```

__List:__ Represents a sequentially ordered collection of values.

```python
colors = ["red", "green", "blue"]
print(colors[0])  # Output: red
```

__Dictionary:__ Represents a collection of key-value pairs.

```python
person = {
    "name": "John",
    "age": 30,
    "is_student": False
}
```

__Tuple:__ A Python tuple is an ordered collection defined with parentheses `()`. Tuples are immutable, meaning their elements cannot be changed, added, or removed after creation.

```python
my_tuple = (1, 2, 3, 'hello', True)
print(my_tuple[0])  # Output: 1
print(my_tuple[3])  # Output: 'hello'
```

__Set:__ A set in Python is an unordered collection of unique elements. It is defined by curly braces `{}` and can contain various data types.

```python
my_set = {1, 2, 3, 4, 5}
my_set.add(6) # Add element 6 to the set (will be added as it is unique)
my_set.add(2)  # Adding a duplicate element (won't be added again)
my_set.remove(3) # Removing elements from the set
```

Python variables are dynamically typed, meaning their type is inferred based on the assigned value. This allows for flexibility and simplicity in variable declaration.

NOTE: In Python, lists are ordered sequences of elements, defined using square brackets `[]`. Elements in a list can be modified, added, or removed after creation. Collections, on the other hand, refer to a broader category of data structures in Python, which includes sets, dictionaries, and tuples. Unlike lists, collections can have different characteristics and properties depending on the specific type. For instance, sets have unique elements, dictionaries have key-value pairs, and tuples are immutable.

---

### 4. Type conversions

In Python, type conversion refers to the process of converting a value from one data type to another. This is a common operation in programming, especially when you need to perform operations or comparisons involving different data types. Python provides several built-in functions to perform type conversions conveniently. Let's discuss some of the most commonly used type conversion functions:

__int(value)__: This function converts `value` to an integer. If `value` is a float, it truncates the decimal part. If `value` is a string, it converts a valid integer string into an integer.

__float(value)__: This function converts `value` to a floating-point number. If `value` is an integer, it appends `.0` to make it a float. If `value` is a string representing a valid float, it converts it to a float.

__str(value)__: This function converts `value` to a string. It can convert integers, floats, booleans, and other data types to their string representations.

__bool(value)__: This function converts `value` to a boolean value. It returns `False` if `value` is `0`, an empty sequence (e.g., empty string, list, tuple), or False itself. Otherwise, it returns `True`.

__list(value)__: This function converts `value` to a list. It can convert tuples, strings, and other iterable objects into a list.

__tuple(value)__: This function converts `value` to a tuple. It can convert lists, strings, and other iterable objects into a tuple.

__set(value)__: This function converts `value` to a set. It can convert lists, tuples, strings, and other iterable objects into a set, removing any duplicate elements.

There are several other built-in functions that perform type conversions or checks. Here are some additional type conversion functions and related built-in functions:

```python
complex_value = complex(10)  # Convert to complex number
char = chr(65)  # Convert Unicode code point to character
unicode_code = ord('A')  # Convert character to Unicode code point
bytes_data = bytes("hello", encoding='utf-8')  # Convert string to bytes
bytearray_data = bytearray("hello", encoding='utf-8')  # Convert string to bytearray
obj_repr = repr([1, 2, 3])  # Get string representation of an object
```

---

### 5. Operators

Operators in Python are symbols that perform operations on variables and values. They enable you to create expressions, combining and manipulating data. Let's explore some fundamental operators with code examples:

__Assignment Operator (=):__ Assigns a value to a variable (as seen previously).

```python
my_value = 10
```

__Arithmetic Operators (+, -, *, /, %):__ Perform basic mathematical operations.

```python
sum = 5 + 3       # Calculate sum: 5 + 3 = 8
difference = 7 - 2  # Calculate difference: 7 - 2 = 5
product = 4 * 6     # Calculate product: 4 * 6 = 24
quotient = 10 / 2   # Calculate quotient: 10 / 2 = 5
remainder = 15 % 4  # Calculate remainder: 15 % 4 = 3
```

__Comparison Operators (==, !=, >, <, >=, <=):__ Compare values and return a Boolean result.

```python
is_equal = (5 == '5')   # True, values are equal
is_not_equal = (10 != '10')   # False, values are not equal
is_greater_than = (15 > 10)   # True, 15 is greater than 10
is_less_than = (5 < 8)        # True, 5 is less than 8
is_greater_or_equal = (20 >= 20)  # True, 20 is equal to 20
is_less_or_equal = (30 <= 25)     # False, 30 is not less than or equal to 25
```

__Logical Operators (and, or, not):__ Combine multiple conditions and perform logical comparisons.

```python
is_true = (True and False)   # False
is_either_true = (True or False)  # True
is_not_true = not True   # False
```

__Unary Operators (++, --):__ Increment or decrement a variable by 1.

```python
counter = 5
counter += 1   # Increment by 1
counter -= 1   # Decrement by 1
```

__String Concatenation Operator (+):__ Concatenates two or more strings.

```python
first_name = 'John'
last_name = 'Doe'
full_name = first_name + ' ' + last_name   # 'John Doe'
```

NOTE: F-strings, or formatted strings, offer a convenient way to include variables and expressions within string literals. They are often used to express the result of operations. Example:

```python
# Define variables
first_name = 'John'
last_name = 'Doe'
age = 30

# Using f-strings for string concatenation
full_name = f"{first_name} {last_name}"  # 'John Doe'
greeting = f"Hello, {first_name}!"       # 'Hello, John!'
profile = f"Name: {full_name}, Age: {age}"  # 'Name: John Doe, Age: 30'
```

---

### 6. Control Flow in Python - 'if' Statement

In Python, the `if` statement is used to conditionally execute a block of code. It allows you to specify a condition, and if that condition evaluates to true, the code inside the `if` block will be executed. If the condition is false, the code inside the if block will be skipped. Let's look at a simple example:

```python
temperature = 25

if temperature > 20:
    print("It's a warm day!")
```

In this example, if the temperature variable is greater than 20, the message "It's a warm day!" will be printed. You can also use an else statement to specify a block of code that will be executed if the condition in the `if` statement is `False`:

```python
temperature = 25

if temperature > 20:
    print("It's a warm day!")
else:
    print("It's a cool day.")
```

In this case, if the temperature is not greater than 20, the message "It's a cool day." will be printed. You can also chain multiple conditions using `elif`:

```python
temperature = 25

if temperature > 30:
    print("It's a hot day!")
elif temperature > 20:
    print("It's a warm day!")
else:
    print("It's a cool day.")
```

Here, if the temperature is greater than 30, the message "It's a hot day!" will be printed. If the temperature is not greater than 30 but is greater than 20, the message "It's a warm day!" will be printed. Otherwise, the message "It's a cool day." will be printed.

These are basic examples, and `if` statements can become more complex with logical operators and other Python features.

Python has a ternary operator, often referred to as a conditional expression. It follows the syntax: `x if condition else y`. Let's see:

```python
temperature = 25
weather_is_nice = True
message_to_display = ""

# Ternary operator
message_to_display = "Go for a walk!" if weather_is_nice else "Stay indoors."


print(message_to_display)  # Output: "Go for a walk!"
```

You can also chain multiple operators to create one-liner if-else statements. For example:

```python
score = 78
result = "A" if score >= 90 else "B" if score >= 80 else "C" if score >= 70 else "D" if score >= 60 else "F"
print(result) # Output: C
```

However, it is important to mention that chaining too many operators in one line can reduce readability. In some cases, using regular if statements or refactoring the code might lead to clearer and more maintainable code. Additionally, we can consider using parentheses `()` or backslashes `\` to separate each expression onto its own line, enhancing readability.

We can do this:

```python
score = 78
result = (
    "A" if score >= 90 else
    "B" if score >= 80 else
    "C" if score >= 70 else
    "D" if score >= 60 else
    "F"
)
print(result) # Output: C
```

Or this:

```python
score = 78
result = "A" if score >= 90 else \
         "B" if score >= 80 else \
         "C" if score >= 70 else \
         "D" if score >= 60 else \
         "F"
print(result) # Output: C
```

In terms of functionality and outcome, the difference between the two code snippets above is purely aesthetic. Both snippets achieve the same result and execute the same conditional logic. The choice between them often comes down to personal preference and coding style guidelines in a given project or team.

__IMPORTANT NOTE:__ Python uses indentation to define blocks of code, such as those within conditions or functions. It's a crucial part of Python syntax for structuring code and determining the scope of what will be executed. The standard convention is to use four spaces for each level of indentation. Here's a brief example:

```python
if condition:
    print("This code is inside the if block.")
    print("This code is also inside the if block.")
print("This code is outside the if block.")
```

If you don't follow the indentation rules in Python, you'll encounter indentation errors. These errors indicate that Python was unable to parse your code properly because the indentation does not match the expected structure. For instance, if you mix tabs and spaces for indentation or if you have inconsistent indentation levels within the same block, Python will raise an `IndentationError`:

```python
if condition:
    print("This code is inside the if block.")
  print("This code is incorrectly indented.")  
  # The line above has an extra space at the beginning, it will raise an IndentationError
```

The recommended indentation of 4 spaces applies not only to code blocks like functions and loops but also to objects, including classes and dictionaries. Consistently using 4 spaces for indentation helps maintain uniformity and readability throughout a Python codebase.

---

### 7. Control Flow II - Falsy and Truthy Values

In Python, values can be broadly categorized into two groups: truthy and falsy.

__Truthy Values:__ A value is truthy if, when used in a condition (like in an `if` statement), it's treated as `True`. For example, any non-empty string, any number other than 0, `True` itself, or any non-empty object is truthy.

__Falsy Values:__ A value is falsy if, in a condition, it's treated as `False`. Examples include `False` itself, the number 0, an empty string (`""`), `None`, and `NaN` (which stands for Not a Number). Example:

```python
if "Hello":
    # This code will run because "Hello" is truthy
    print("Truthy!")

if 0:
    # This code won't run because 0 is falsy
    print("Falsy!")
```

__Default value:__ The 'default value' or 'fallback pattern' is a common practice in Python for assigning a value to a variable if the intended value might be falsy. This pattern often involves using the logical OR (`or`) operator. Here's an example to illustrate the concept:

```python
my_var = "Hello, World!"
message = my_var or "Default Value"

print(message)  # Output: "Hello, World!"
```

---

### 8. Control flow III - Loops

Loops provide a convenient means to execute a block of code repeatedly for each item in the sequence. Let's check a couple of common ways of establishing loop iterations in Python.

__'for' loop:__ The `for` loop in Python is a control flow statement used to iterate over a sequence of elements. It's commonly used when you need to perform the same operation on each element of a list, tuple, string, dictionary, set, range, or any other iterable object. Let's see a couple of use cases:

* When we know the range of values in advance

```python
# Print numbers from 1 to 5 using a for loop
for i in range(1, 6):
    print(i)
```

Regarding `range()`: In the example above, the function call creates a sequence of numbers starting from 1 (inclusive) up to 6 (exclusive). So, it generates the sequence [1, 2, 3, 4, 5]. It's important to note that range() generates numbers up to, but not including, the second argument.

If you want to start from 0, you can simply use range(`<number>`) because `range()` starts from 0 by default:

```python
# Using range to iterate from 0 to 9
for i in range(10):
    print(i)
```

* Lists

 ```python
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num) # Prints 1 to 5
```

* Strings

 ```python
message = "Hello"
for char in message:
    print(char) # Prints each letter
```

* Dictionaries

```python
# Define a dictionary representing information about a person
person = {"name": "John", "age": 30, "city": "New York"}

# Iterate over the keys of the dictionary and print each key
for key in person:
    print(key)

# Iterate over the values of the dictionary and print each value
for value in person.values():
    print(value)

# Iterate over the key-value pairs of the dictionary and print each pair
for key, value in person.items():
    print(key, ":", value)
```

__'while' loop:__ The `while` loop is used when the number of iterations is not known in advance, and the loop continues as long as a specified condition is `True`.

```python
# Example: Print numbers from 1 to 5 using a while loop
i = 1
while i <= 5:
    print(i)
    i += 1
```

__Loop control statements:__ Python provides loop control statements like `break` and `continue` to alter the flow of a loop.

```python
# Example 1: Use break to exit a loop early
for i in range(1, 11):
    if i == 5:
        break  # Exit the loop when i is 5
    print(i)  # Shows 1 to 4

# Example 2: Use continue to skip the current iteration
for i in range(1, 6):
    if i == 3:
        continue  # Skip the iteration when i is 3
    print(i)  # Shows 1 to 5 excluding 3
```

__IMPORTANT CONSIDERATION:__ Loops are one of the most frequently used features in any programming language, and Python provides these and other ways to loop through values. Having a good understanding of loops (in any language) is never a 'time wasted,' considering how often they are used.

---

### 9. Control flow IV - match-case statements

The `match-case` statement in Python makes value evaluation straightforward. Unlike some languages, Python avoids the `switch-case` structure in favor of clear and readable `if-elif-else` statements. Yet, managing many conditions with `if-elif-else` can get hard to maintain. That's where Python's answer comes in: the `match-case` statement introduced in __Python 3.10__. Let's see how it workd by the following example:

```python
number = 5

# Using the match-case statement to evaluate 'number'
match number:
    # Check if 'number' is greater than 0
    case n if n > 0:
        print(f"{number} is a positive number.")
    # Check if 'number' is less than 0
    case n if n < 0:
        print(f"{number} is a negative number.")
    # Default case if 'number' is zero or any other value
    case _:
        print(f"{number} is zero.")
```

Each case block specifies a pattern to match against the expression being evaluated. The underscore (`_`) pattern serves as a wildcard, matching any value not covered by preceding case blocks. This makes it a common practice to use `_` as the final case block to provide a default or 'catch-all' response for unmatched values. 

NOTE: In the `match-case` statement, the variable `n` represents the matched value of the expression being evaluated. While it's possible to use `number` instead, shorter variable names are commonly used for brevity and clarity. They make the code more concise and readable, especially within the context of pattern matching, where the focus is on the pattern rather than the variable name. Shorter variable names are preferred to avoid cluttering the code with longer names.

If for some reason you are coding in an older version of Python, the same result can be achieved in two different ways:

1) Using `if-elif-else`:

```python
number = 5

# Check if 'number' is greater than 0
if number > 0:
    print(f"{number} is a positive number.")
# Check if 'number' is less than 0
elif number < 0:
    print(f"{number} is a negative number.")
# Default case if 'number' is zero or any other value
else:
    print(f"{number} is zero.")
```

2) Utilizing dictionaries, lambda functions, and a mapping function for associating conditions with corresponding actions (slightly more verbose, yet effective):

```python
number = 5

# Define a dictionary where keys are lambda functions and values are corresponding messages
number_cases = {
    lambda n: n > 0: lambda number: print(f"{number} is a positive number."),
    lambda n: n < 0: lambda number: print(f"{number} is a negative number."),
    lambda n: True: lambda number: print(f"{number} is zero.")
}

# Function to match the number based on defined cases
def match_number(number):
    for condition, action in number_cases.items():
        if condition(number):
            action(number)
            break

# Test the function with different numbers
match_number(5)  # Output: 5 is a positive number.
match_number(-3) # Output: -3 is a negative number.
match_number(0)  # Output: 0 is zero.
```

Both functions and lambda functions will be covered next.

__Performance considerations:__ In overall performance, the `match-case` statement and `if-elif-else` statements tend to be better optimized and more efficient compared to the approach using dictionaries, lambda functions, and a mapping function. However, the differences in performance between these approaches are generally minimal for most applications, and other factors such as readability, maintainability, and adherence to Python best practices should also be considered when choosing the most suitable approach for a specific scenario.

---

### 10. Basics of functions

In Python, functions are blocks of reusable code that can be defined and called upon to perform specific tasks. They play a crucial role in organizing and structuring code, promoting reusability, and enhancing maintainability. There are two common ways to define functions in Python: function definitions and lambda functions.

__Function Definitions__: A function definition is a way to define a function with the def keyword, followed by the function name, a list of parameters enclosed in parentheses, and a block of code indented below.

```python
# Defining the function
def add(x, y):
    # Calculating the sum of x and y
    sum_value = x + y
    
    # Returning the calculated sum
    return sum_value

# Calling the function and storing the returned value
my_sum = add(3, 7)

# Displaying the result
print(my_sum) # Output: 10
```

In this example:

`add` is the function name.
`(x, y)` are the parameters that represent the data the function receives when called.
`sum_value = x + y` represents the function body, where the actual code is executed.
`return sum_value` is the result returned after the code is executed.

__Lambda Functions__: Lambda functions, also known as anonymous functions, are a way to define small, unnamed functions using the lambda keyword. They are commonly used for short, one-liner functions.

```python
# Defining a lambda function for subtracting two numbers
subtract = lambda x, y: x - y

# Calling the lambda function and storing the returned value
my_subtract = subtract(7, 3)

# Displaying the result
print(my_subtract) # Output: 4
```

In this example:

The `lambda` keyword is used to define the lambda function.
`x` and `y` are the parameters.
`x - y` represents the expression that calculates the result.
`:` separates the parameters from the expression. In lambda functions, the result of evaluating the expression after the colon is automatically returned as the result of the function.

Both function definitions and lambda functions serve similar purposes but are used in different contexts. Function definitions are more suitable for complex or multi-line functions, while lambda functions are preferred for short, one-liner functions.

NOTE: Unlike JavaScript, Python does not hoist variable or function declarations. In Python, variables and functions must be explicitly defined before they are used. This means Python does not automatically move declarations to the top of the scope. If you attempt to access a variable or function before it's defined, Python will raise a `NameError`:

```python
# Attempting to access a variable before it's defined
print(my_variable)  # This will raise a NameError

# Defining the variable after the attempt
my_variable = 42
```

---

### 11. String Manipulation & Formatting

1) String Manipulation: Essential Techniques and Functions

__Concatenation:__ Concatenation involves merging strings together. Example:

```python
first_name = "John"
last_name = "Doe"

full_name = first_name + " " + last_name

print(full_name)  # Output: John Doe
```

__Formatted Strings:__ Formatted strings offer a concise way to embed expressions within strings, reducing reliance on concatenation. Example:

```python
name = "Alice"
age = 30

greeting_message = f"Hello, {name}! You are {age} years old."

print(greeting_message)  # Output: Hello, Alice! You are 30 years old.
```

__.len():__ The `len()` function retrieves the number of characters in a string. Example:

```python
greeting = "Hello, Python!"
length_of_greeting = len(greeting)

print(f"The length of the greeting is {length_of_greeting} characters.")
```

__.strip():__ The `strip()` method eliminates leading and trailing whitespace from a string. Example:

```python
spaced_string = "   Trim me!   "
trimmed_string = spaced_string.strip()

print(f"Original String: \"{spaced_string}\"")
print(f"Trimmed String: \"{trimmed_string}\"")
```

__slicing notation:__ The feature that enables using `[]` to slice a string is known as "slicing notation" or simply "slicing." It allows you to extract a portion of a sequence, like a string, list, or tuple, by specifying a start index, an end index, and an optional step size.

```python
sentence = "This is a sample sentence."

# Extract a substring from index 5 to 10 (excluding 10)
substring = sentence[5:10]

print(f"Substring: {substring}")  # Output: Substring: is a
```

__.upper() and .lower():__ These methods convert strings to uppercase or lowercase, respectively.

```python
# Original mixed-case string
mixed_case = "My teXt MesSage"

# Convert the string to uppercase
upper_case = mixed_case.upper()

# Convert the string to lowercase
lower_case = mixed_case.lower()

# Log the uppercase and lowercase versions to the console
print(f"Uppercase: {upper_case}")
# Output: Uppercase: MY TEXT MESSAGE

print(f"Lowercase: {lower_case}")
# Output: Lowercase: my text message
```

__.replace():__ This method searches for a specified value (searchValue) in a string and replaces it with another value (replaceValue). Example:

```python
string = "Hello, World!"
print(string.replace("World", "Universe"))  # Outputs "Hello, Universe!"
```

In Python, a plethora of string methods, including `.find()`, `.split()`, `.startswith()`, `.endswith()`, and more, are available. Comprehensive references such as the Python documentation or online tutorials offer detailed explanations of each method. 

Ps. For a deeper understanding in string manipulation, consider exploring the Python Language Reference, which provides detailed insights into the language's specifications.

2) Strings Formatting:

Here are four common ways of formatting strings in Python:

__Using the `%` Operator__: 

This is one of the older methods of string formatting in Python. It involves using the % operator followed by a tuple of values to insert into the string.

```python
name = "Alice"
age = 30
formatted_string = "My name is %s and I am %d years old." % (name, age)
print(formatted_string)
```

In this example, `%s` is used for string substitution and `%d` is used for integer substitution. This method is somewhat limited compared to newer methods like f-strings and `.format`.

__Using `.format` Method__: 

Introduced in Python 2.6 and widely used in Python 3.x, the `.format` method provides more flexibility and readability than `%` formatting.

```python
name = "Bob"
age = 25
formatted_string = "My name is {} and I am {} years old.".format(name, age)
print(formatted_string)
```

Here, `{}` acts as a placeholder for the values provided in the `.format` method. You can also specify the order of insertion or use named placeholders for more complex formatting.

__Using f-Strings (Formatted String Literals)__:

Introduced in Python 3.6, f-strings provide a more concise and readable way to format strings by prefixing the string with `f` or `F` and embedding expressions directly within curly braces `{}`.

```python
name = "Charlie"
age = 35
formatted_string = f"My name is {name} and I am {age} years old."
print(formatted_string)
```

The expressions within `{}` are evaluated at runtime, making f-strings very convenient for complex formatting and variable interpolation.

__Using Template Strings__:

The `string.Template` class provides a simple and convenient way to perform string substitution using placeholders.

```python
from string import Template

name = "David"
age = 40
template = Template("My name is $name and I am $age years old.")
formatted_string = template.substitute(name=name, age=age)
print(formatted_string)
```

Here, `$name` and `$age` are placeholders that are replaced by values provided in the substitute method. Template strings are useful when you want to ensure that only specific variables are substituted, avoiding accidental substitutions.

When considering string formatting methods in Python, each has its advantages influenced by factors such as Python version compatibility, readability, and personal preference. However, for modern Python development, F-strings are typically preferred due to their simplicity, readability, and flexibility. They are concise and straightforward, evaluating expressions within `{}` at runtime for clearer code understanding. Additionally, F-strings accommodate any valid Python expression within `{}`, enhancing their versatility for complex formatting needs. Moreover, they offer superior performance compared to `%` formatting and `.format` method, particularly noticeable with large strings or repeated formatting tasks.

---

### 12. Scope I: Types of Scope

In Python, scope refers to the visibility and accessibility of variables, functions, and objects within your code. Understanding scope is crucial because it determines where variables and functions are accessible and where they are not. There are primarily three types of scope in Python: local scope, enclosing (non-local) scope, and global scope.

__Local Scope__: Variables that are defined inside a function have local scope, which means they are accessible only within that function. Once the function execution ends, the variables are no longer accessible. Example:

```python
def my_function():
    local_var = 10  # local variable
    print(local_var)  # 10

my_function()
print(local_var)  # NameError: name 'local_var' is not defined
```

__Enclosing (Non-Local) Scope__: Enclosing scope refers to the scope of variables defined in an enclosing function (if any). If a variable is not found in the local scope, Python looks for it in the enclosing scope. Example:

```python
def outer_function():
    outer_var = 20  # outer variable

    def inner_function():
        print(outer_var)  # accessing outer_var from enclosing scope

    inner_function()

outer_function()
print(outer_var)  # NameError: name 'outer_var' is not defined
```

__Global Scope__: Variables that are defined outside of any function or block have global scope, which means they are accessible throughout your entire code. Example:

```python
global_var = 30  # global variable

def another_function():
    print(global_var)  # 30

another_function()
print(global_var)  # 30
```

__Module Scope__: Module scope in Python refers to the accessibility and reach of elements defined at the top level of a Python module. When you create a Python file and save it with a .py extension, it becomes a module. Elements like variables, functions, or classes that are defined outside of specific structures within this module gain module scope. If you import a module into another Python script or module and there is a variable defined at the module level (module scope variable) in the imported module, you can access and modify it.

Consider a module named my_module.py:

```python
# my_module.py

module_var = 50  # This is a variable with module scope
```

Now, in another Python script or module, say main.py, you import my_module and access its module-level variable module_var:

```python
# main.py
import my_module

print(my_module.module_var)  # Accessing module-level variable from my_module

my_module.module_var = 100  # Modifying module-level variable in my_module
print(my_module.module_var)  # Updated value after modification
```

---

### 13. Scope II: Keywords and best practices

__nonlocal Keyword__: In Python, the `nonlocal` keyword allows you to modify variables in the enclosing (non-local) scope from within a nested function. Example:

```python
def outer_function():
    outer_var = 20  # outer variable

    def inner_function():
        nonlocal outer_var
        outer_var += 5  # modifying outer_var from inner function
        print(outer_var)  # 25

    inner_function()

outer_function()
```

__global Keyword__: The `global` keyword is used to declare that a variable inside a function is referring to a global variable defined outside the function's scope. This keyword allows you to modify global variables from within a function, which would otherwise create a new local variable with the same name if not explicitly declared as global. Here's an example to illustrate the use of the global keyword:

```python
global_var = 30  # global variable

def modify_global():
    global global_var
    global_var += 5  # modifying the global variable
    print(global_var)  # 35

modify_global()
print(global_var)  # 35
```

__Best practices related to scope:__

* Avoid Using Global Variables: Limiting the use of global variables in Python is recommended to avoid namespace pollution and improve code maintainability. Prefer defining variables within functions whenever possible to keep their scope limited and prevent unintended side effects.

* Avoid using both the `nonlocal` and `global` keywords: While these keywords serve specific purposes, relying heavily on them can make your code harder to understand and maintain. Instead, consider alternative approaches such as passing variables as arguments or returning modified values from functions. This practice not only promotes code clarity but also helps in organizing and structuring your code in a more manageable way.

* Avoid Shadowing Variables: Variable shadowing occurs when a variable declared within a local scope has the same name as a variable in an outer scope, effectively hiding the outer variable within that scope. Be mindful of variable names to avoid unintentionally shadowing variables from outer scopes, which can lead to confusion and bugs. 

* Use `if __name__ == "__main__:"` in your main Python file (application entry point): Using `if __name__ == "__main__:"` in your main file (e.g., main.py) is a recommended practice for scoping and organizing code. It ensures that certain parts of your script execute only when run directly, enhancing code clarity and structure. Here's an illustration using a simple Python script named main.py:

```python
# main.py

def greet(name):
    print(f"Hello, {name}!")

# This block will only execute if the script is run directly
if __name__ == "__main__":
    user_name = input("Enter your name: ")
    greet(user_name)
```

In this script: The greet function is defined to print a greeting message with the given name. The if `__name__ == "__main__":` block contains code that asks the user for their name and then calls the greet function with that name, printing a personalized greeting. When you run main.py directly, it prompts you to enter your name and then greets you with the message `"Hello, [your name]!"`. However, if you import main.py into another script or module, the code inside the if `__name__ == "__main__":` block will not run automatically. Instead, you can use the `greet` function as part of the imported module in the other script.

---

### 14. Processing Iterables with .map() and .filter() 

Python provides powerful tools like `map()`, `filter()` (as well as many others) for processing iterables efficiently. These methods align with functional programming principles, promoting clarity, immutability, and composability in code. Benefits are:

* Clarity: Expressive operations like mapping and filtering make code easier to understand.
* Immutability: Working with immutable data structures reduces bugs and simplifies debugging.
* Composability: Functions can be combined into pipelines for complex transformations.
* Testability: Stateless functions facilitate unit testing, ensuring code reliability.
* Parallelism: Functional programming supports parallel and concurrent execution, enhancing performance.

By embracing these methods and principles, developers can craft cleaner, more efficient codebases that are easier to maintain and scale. 

__Iterables vs. Iterators__: Before exploring `.map()` and `.filter()`, it's crucial to understand the concepts of iterators, as well as the distinction between an iterable and an iterator. An iterable, like a list or string, refers to anything you can loop over. Conversely, an iterator is a specific object designed to aid in looping over an iterable. Iterators grant access to individual items in the sequence one by one. The `next()` function plays a key role in advancing the iterator to the next item and retrieving it. For example:

```python
# Iterable: List
my_list = [1, 2, 3, 4, 5]

# You can loop over the list directly
for item in my_list:
    print(item)  # Output: 1, 2, 3, 4, 5
```

Iterator Example:

```python
# Iterable: List
my_list = [1, 2, 3, 4, 5]

# Get an iterator object from the iterable
my_iterator = iter(my_list)

# Use the iterator to get items one at a time
print(next(my_iterator))  # Output: 1
print(next(my_iterator))  # Output: 2
print(next(my_iterator))  # Output: 3
print(next(my_iterator))  # Output: 4
print(next(my_iterator))  # Output: 5

# After all items are exhausted, next() raises StopIteration
# print(next(my_iterator))  # Uncommenting this line would raise StopIteration
```

__map():__ In Python, the `map()` function can transform any iterable, not just lists. It can operate on tuples, sets, dictionaries, strings, and other iterable objects. The function applies a specified function to each item in the iterable and returns an iterator containing the results.

Example: Doubling each element in a list

```python
# Define a function to add 1 to a number
def add_one(x):
    return x + 1

# Example: Using map with a list
numbers = [1, 2, 3, 4, 5]

# Apply add_one function to each item in the list using map
mapped_numbers = map(add_one, numbers)

# Convert the mapped_numbers iterator to a list (iterable)
result = list(mapped_numbers)

# Output the result
print(result)  # Output: [2, 3, 4, 5, 6]
```

__filter():__ The `filter()` function in Python takes two arguments: a function and an iterable. It applies the function to each element in the iterable and returns an iterator containing only the elements for which the function returns `True`. If no function is provided, `filter()` uses the default behavior of considering truthy values for filtering.

Example: Filtering even numbers from a list

```python
# Define a function to check if a number is even
def is_even(x):
    return x % 2 == 0

# Example: Using filter with a list
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Apply is_even function to each item in the list using filter
filtered_numbers = filter(is_even, numbers)

# Convert the filtered_numbers iterator to a list (iterable)
result = list(filtered_numbers)

# Output the result
print(result)  # Output: [2, 4, 6, 8, 10]
```

---

### 15. Built-In Python mathematical features

Python provides built-in mathematical constants and functions through the `math` module, which allows developers to perform a wide range of mathematical operations. This includes functions for trigonometry, logarithms, rounding, and more. Python makes it easy to handle complex mathematical computations efficiently.

__Mathematical constants:__ Python's `math` module includes predefined constants for fundamental mathematical values, which can be accessed as follows:

```python
import math

# Pi (π): Represents the ratio of the circumference of a circle to its diameter
pi = math.pi  # Approximately 3.14159

# Euler's number (e): Represents the base of the natural logarithm
e = math.e  # Approximately 2.71828

# Square root of 2 (√2): Represents the square root of 2
sqrt2 = math.sqrt(2)  # Approximately 1.41421

# Reciprocal of the square root of 2 (1/√2)
sqrt1_2 = 1 / math.sqrt(2)  # Approximately 0.70711

# Natural logarithm of 2 (ln(2))
ln2 = math.log(2)  # Approximately 0.69315

# Natural logarithm of 10 (ln(10))
ln10 = math.log(10)  # Approximately 2.30259
```

__Mathematical functions:__ Python's `math` module offers a variety of functions for common mathematical operations. Here’s how to use them:

```python
import math

# Exponentiation (math.pow)
result = math.pow(2, 3)  # result equals 8 (2 raised to the power of 3)

# Square Root (math.sqrt)
square_root = math.sqrt(25)  # square_root equals 5 (square root of 25)

# Absolute Value (abs)
absolute_value = abs(-10)  # absolute_value equals 10 (absolute value of -10)

# Trigonometric Functions: sine (math.sin), cosine (math.cos), tangent (math.tan)
sine_value = math.sin(math.pi / 2)  # sine_value equals 1 (sin(π/2) is 1)
cosine_value = math.cos(math.pi)  # cosine_value equals -1 (cos(π) is -1)
tangent_value = math.tan(0)  # tangent_value equals 0 (tan(0) is 0)

# Rounding: Round (round), Ceil (math.ceil), Floor (math.floor)
rounded_number = round(4.6)  # rounded_number equals 5 (rounds to the nearest integer)
ceiled_number = math.ceil(4.3)  # ceiled_number equals 5 (rounds up to the nearest integer)
floored_number = math.floor(4.9)  # floored_number equals 4 (rounds down to the nearest integer)

# Logarithmic Functions: Natural Logarithm (math.log), Base 10 Logarithm (math.log10)
natural_log = math.log(math.e)  # natural_log equals 1 (ln(e) is 1)
log_base10 = math.log10(100)  # log_base10 equals 2 (log10(100) is 2)
```

In Python, these constants and functions are part of the `math` module, which provides precise floating-point arithmetic for most practical programming tasks. The values, though approximations due to floating-point precision, are accurate enough for a wide range of applications.

---

### 16. Understanding 'in' Better

In Python, the `in` keyword is used as an operator to test if a value is present in a sequence (such as a list, tuple, string, or set). It is not a reserved word like `if` or `for`, but rather an operator that checks for membership in a collection. The in operator works with a wide range of iterable types, making it a versatile tool for checking if an element exists within a any iterable. To exemplify:

__Strings__:
```python
my_string = "Hello, World!"
if 'o' in my_string:
    print("'o' is in the string")
```

__Lists and Tuples__:
```python
my_list = [1, 2, 3, 4, 5]
if 3 in my_list:
    print("3 is in the list")
```

__Sets__:
```python
my_set = {1, 2, 3}
if 2 in my_set:
    print("2 is in the set")
```

__Dictionaries (Checking for Keys)__:
```python
my_dict = {'a': 1, 'b': 2, 'c': 3}
if 'b' in my_dict:
    print("Key 'b' exists in the dictionary")
```

In each of these cases, the in operator is used to check if a specific element (or key in the case of dictionaries) exists within the iterable. If the element is found, the condition evaluates to True, allowing you to perform actions based on that information.

---

### 17. Understanding Sets

A set in Python is an unordered collection of unique elements. It is defined by curly braces `{}` and can contain various data types such as integers, floats, strings, and even other sets or tuples. The key characteristics of a set are:

* Uniqueness: A set cannot contain duplicate elements. If you try to add an element that is already present in the set, it won't be added again.
* Unordered: The elements in a set are not stored in any particular order. When you iterate over a set or print it, the order of elements may vary each time.
* Mutable: Sets are mutable, which means you can add or remove elements from a set after it has been created.

Sets are useful for various operations such as checking membership (whether an element is in the set), performing set operations like union, intersection, difference, and symmetric difference, and removing duplicates from a collection of elements. Here's an example of creating and working with sets in Python:

```Python
# Creating a set
my_set = {1, 2, 3, 4, 5}

# Adding elements to the set
my_set.add(6)
my_set.add(2)  # Adding a duplicate element (won't be added again)

# Removing elements from the set
my_set.remove(3)

# Checking membership
print(2 in my_set)  # Output: True
print(7 in my_set)  # Output: False
```

Set operations example:

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

union_set = set1.union(set2)  # Union of two sets
intersection_set = set1.intersection(set2)  # Intersection of two sets
difference_set = set1.difference(set2)  # Difference between two sets
symmetric_difference_set = set1.symmetric_difference(set2)  # Symmetric difference 

print(union_set)  # Output: {1, 2, 3, 4, 5}
print(intersection_set)  # Output: {3}
print(difference_set)  # Output: {1, 2}
print(symmetric_difference_set)  # Output: {1, 2, 4, 5}
# Ps. Symmetric difference refers to the elements that are present in either of two sets, but not in both.
```

Sets are versatile data structures that are commonly used in Python for various programming tasks due to their unique properties and efficient set operations.

---

### 18. Exploring Tuples

A tuple in Python is a data structure that allows you to store a collection of elements. It is similar to a list, but unlike lists, tuples are immutable, which means once a tuple is created, its elements cannot be modified, added, or removed. Tuples are defined using parentheses `()` and can contain elements of different data types. Here are some key points about tuples and their common use cases:

* Immutable Sequences: Tuples are used to store an ordered sequence of elements that cannot be changed after creation. This immutability makes tuples suitable for situations where you want to ensure that the data remains constant throughout your program.

* Multiple Values: Tuples can store multiple values of different types, such as integers, floats, strings, and even other tuples. This makes tuples versatile for organizing and representing structured data.

* Returning Multiple Values: Tuples are often used to return multiple values from a function. Instead of returning individual values, you can pack them into a tuple and unpack the tuple when receiving the return values.

* Unpacking and Packing: Tuples support unpacking, which allows you to assign multiple variables at once by unpacking a tuple into individual elements. Packing is the process of creating a tuple by grouping multiple values together.

Here are some examples that demonstrate the power and versatility of tuples.

```python
# Creating a tuple
my_tuple = (1, 2, 3, 'hello', 4.5)

# Accessing elements
print(my_tuple[0])  # Output: 1
print(my_tuple[3])  # Output: 'hello'

# Unpacking a tuple
a, b, c, d, e = my_tuple
print(a, b, c, d, e)  # Output: 1 2 3 'hello' 4.5

# Returning multiple values from a function
def get_info():
    name = 'Renato Lins'
    country = 'Brazil'
    return name, country

info_tuple = get_info()
print(info_tuple)  # Output: ('Renato Lins', 'Brazil')

# Using tuples as keys in dictionaries (since they are immutable)
my_dict = {(1, 2): 'value', (3, 4): 'another value'}
print(my_dict[(1, 2)])  # Output: 'value'
```

__Understanding Unpacking and Packing Better__:

1) Unpacking: 

Unpacking refers to the process of extracting individual elements from a tuple and assigning them to multiple variables simultaneously. This is particularly useful when a tuple contains multiple values that you want to use independently. Here's an example:

```python
my_tuple = (1, 2, 3)
a, b, c = my_tuple  # Unpacking the tuple into variables a, b, and c
print(a)  # Output: 1
print(b)  # Output: 2
print(c)  # Output: 3
```

In this example, the values (1, 2, 3) from my_tuple are unpacked into variables a, b, and c, respectively.

2) Packing:

Packing is the reverse process of unpacking. It involves grouping multiple values or variables together to create a tuple. This can be done explicitly by using parentheses `()` or implicitly in certain contexts. Here's an example:

```python
x = 10
y = 20
z = 30
my_packed_tuple = (x, y, z)  # Packing values into a tuple
print(my_packed_tuple)  # Output: (10, 20, 30)
```

In this example, the values `x`, `y`, and `z` are packed into `my_packed_tuple` using parentheses `()`.

3) Combining Unpacking and Packing:

You can also combine unpacking and packing in various ways to manipulate tuples. For instance:

```python
# Example combining unpacking and packing
original_tuple = (1, 2, 3, 4, 5)
a, *b, c = original_tuple  # Unpacking with * operator to capture multiple elements
print(a)  # Output: 1
print(b)  # Output: [2, 3, 4]
print(c)  # Output: 5

# Packing into a new tuple
new_tuple = (a, *b, c)
print(new_tuple)  # Output: (1, 2, 3, 4, 5)
```

In this example, the `*` operator is used during unpacking to capture multiple elements into variable `b`, and then these elements are packed back into `new_tuple`.

Unpacking and packing are fundamental concepts in working with tuples and are often used to handle multiple values efficiently and effectively in Python.

---

### 19. Objects and Common Object Methods in Python

In Python, objects are collections of key-value pairs. Each key must be an immutable type (e.g., strings, numbers, tuples), and values can be any data type, including integers, strings, booleans, other objects, or functions. Python objects can be created using dictionaries (`dict`) or classes. 

```python
# Creating a dictionary with key-value pairs
person = {
    'name': 'John',        
    'age': 30,             
    'address': {           
        'city': 'New York',
        'country': 'USA'
    }
}

# Accessing values using keys
print(person['name'])           # Output: John
print(person['address']['city']) # Output: New York
```

__Object Creation Using Classes:__

Python classes allow you to define blueprints for objects with specific structures and behavior:

```python
# Defining a class called 'Person'
class Person:
    # The constructor method (__init__) is called when a new object is created from the class. 
    # It initializes the object's attributes with the value passed during object creation.
    def __init__(self, name):
        self.name = name  # Assigns the provided 'name' argument to the 'name' attribute of the object
    
    # Defining a method called 'greet' that prints a greeting message including the person's name.
    def greet(self):
        # Using an f-string to include the 'name' attribute in the printed message.
        print(f"Hello, my name is {self.name}.")


# Creating an instance of the class
person1 = Person("John")

# Calling the greet method
person1.greet()  # Output: Hello, my name is John.
```

Python supports inheritance, allowing classes to share behavior through a mechanism called the "method resolution order" (MRO):

```python
# Example of inheritance
class Person:
    def __init__(self, name):
        self.name = name

class Employee(Person):
    def greet(self):
        print(f"Hello, I am {self.name}, and I work here!")

employee = Employee("Alice")
employee.greet()  # Output: Hello, I am Alice, and I work here!
```

__Common Object Methods in Python:__

**`dict.fromkeys()` Method**: This method creates dictionaries from keys with default values:

```python
keys = ['name', 'age', 'city']
person = dict.fromkeys(keys, None)
print(person)  # Output: {'name': None, 'age': None, 'city': None}
```

__Built-in Dictionary Methods:__

**`copy()`**: Creates a shallow copy of a dictionary.

```python
source = {'foo': 1, 'bar': 2}
target = source.copy()
print(target)  # Output: {'foo': 1, 'bar': 2}
```

**`update()`**: Merges properties from one dictionary into another.

```python
target = {'number': 10}
source = {'foo': 1, 'bar': 2}
target.update(source)
print(target)  # Output: {'number': 10, 'foo': 1, 'bar': 2}
```

**`setdefault()`**: Inserts a key with a default value if the key is not already present.

```python
person = {'name': 'John'}
person.setdefault('age', 30)
print(person)  # Output: {'name': 'John', 'age': 30}
```

__Dictionary Iteration:__

**`for` Loop**: Iterate over dictionary keys.

```python
person = {'name': 'John', 'age': 30}
for key in person:
    print(key, person[key])  # Output: name John, age 30
```

**`keys()` Method**: Returns the dictionary's keys.

```python
print(person.keys())  # Output: dict_keys(['name', 'age'])
```

**`values()` Method**: Returns the dictionary's values.

```python
print(person.values())  # Output: dict_values(['John', 30])
```

**`items()` Method**: Returns key-value pairs as tuples.

```python
print(person.items())  # Output: dict_items([('name', 'John'), ('age', 30)])
```

__Dictionary Unpacking:__ Python allows dictionary unpacking, similar to destructuring.

```python
person = {'name': 'John', 'age': 30, 'city': 'New York'}
name, age, city = person.values()

print(name)  # Output: John
print(age)   # Output: 30
print(city)  # Output: New York
```

__Merging Dictionaries:__ You can merge dictionaries using the `**` (double asterisk) operator:

```python
dict1 = {'a': 1, 'b': 2}
dict2 = {'c': 3, 'd': 4}

merged_dict = {**dict1, **dict2}
print(merged_dict)  # Output: {'a': 1, 'b': 2, 'c': 3, 'd': 4}
```

__Working with JSON in Python:__

Python's `json` module provides tools for serializing and deserializing JSON data.

**`json.dumps()`**: Converts a Python dictionary into a JSON string.

```python
import json
person = {'name': 'John', 'age': 30}
json_data = json.dumps(person)
print(json_data)  # Output: '{"name": "John", "age": 30}'
```

**`json.loads()`**: Parses a JSON string into a Python dictionary.

```python
json_data = '{"name": "John", "age": 30}'
person = json.loads(json_data)
print(person['name'])  # Output: John
```

---

### 20. A better understanding of `None` and missing values

In Python, `None` is used to represent the absence of a value. It is the default value for variables and object attributes when they are not explicitly initialized with a value. Assigning `None` to a variable signifies that it holds no value intentionally.

For example:

```python
# Variable with no value
user_name = None

if user_name is None:
    print("No username provided")  # Output: No username provided
```

Dealing with `None` in Python:

When working with objects or dictionaries, you may encounter cases where a value is `None`. Python offers several ways to handle this safely, such as using the `.get()` method for dictionaries or conditional expressions to provide default values.

Example using dictionary and `.get()` method for default values:

The `.get()` method allows for safe access to a key without causing an error if the key doesn't exist or holds a `None` value. You can also specify a default value to return if the key is missing or `None`.

```python
user = {
    "address": {
        "city": "New York"
    }
}

# Accessing city property safely
city = user.get("address", {}).get("city", "Unknown City") 
# If "address" doesn't exist, an empty dictionary {} is returned as a default.

print("City:", city)  # Output: 'New York'
```

If the `address` key or the `city` within `address` is missing or holds `None`, the default `"Unknown City"` will be returned.

Using conditional expressions (ternary operators):

Another approach in Python is using conditional expressions to check for `None` and provide default values:

```python
# Checking for None and providing a default value
postal_code = user.get("address", {}).get("postalCode", None)
postal_code = postal_code if postal_code is not None else "N/A"
print("Postal code:", postal_code)  # Output: 'N/A'
```

Checking for `None`:

In Python, the recommended way to check for `None` is using `is None` or `is not None`. This is a clear and explicit way to determine if a variable or value is `None`.

```python
# Recommended way to check for None
postal_code = user.get("address", {}).get("postalCode", None)
is_postal_code_none = postal_code is None
print("Is postal code None?", is_postal_code_none)  # Output: True
```

Handling default values with logical OR (`or`):

Python’s `or` operator can be used to provide default values when a variable or dictionary key holds a falsy value (e.g., `None`, `0`, `False`, or an empty string).

```python
user = {"name": "John", "city": None}

# Logical or for default values
name = user.get("name") or "Anonymous"  # Output: 'John'
city = user.get("city") or "Unknown City"  # Output: 'Unknown City'
print(f"Name: {name}, City: {city}")
```

In this case, the right-hand side of the `or` expression is returned if the left-hand side is falsy.

Type and Boolean Values of `None`:

The `None` value in Python is of type `NoneType`. In boolean contexts, `None` behaves like a falsy value.

```python
# Checking type of None
print(type(None))  # Output: <class 'NoneType'>

# Boolean opposite of None is True
print(not None)  # Output: True
```

However, it’s best to avoid using `not` for checking `None` and use explicit comparisons (`is None`) for clarity.

---

### BONUS - Installing and running Python on your machine

Installing Python on your machine provides offline access, improved performance, efficient resource utilization, customization, seamless integration with local tools, and the flexibility to run any desired version on your preferred machine. Moreover, it unlocks powerful capabilities such as automating tasks, creating servers, controlling devices connected to the PC, etc., expanding the possibilities provided by browser interpreters in countless ways. Now, let's explore how we can run Python on our machines, unlocking its full potential for use.

1. __Installing Python__

To start, you need to install Python on your computer. Follow the steps below:

a. Go to the official Python website at __python.org/download__.

b. Click on the download button for the latest version of Python compatible with your operating system (Windows, macOS, or Linux).

c. Run the downloaded installer and follow the on-screen instructions to complete the installation. Make sure to check the option "Add Python X.X to PATH" to easily access Python from the terminal.

d. After installation, open the terminal (Command Prompt on Windows, Terminal on macOS and Linux) and type `python --version` to verify if Python was installed correctly and which version is being run.

By now, we can run Python directly from the command line by using the python command. This opens the Python interpreter, indicated by the `>>>` prompt. From here, we can execute Python commands. For example, typing `2 + 3` will display `5` in the terminal. To exit the Python interpreter, we can type `ex()` or press Ctrl + Z followed by ENTER.

2. __Installing Visual Studio Code and Essential Plugins for Python Development__

Visual Studio Code (VS Code) is a powerful code editor developed by Microsoft, known for its versatility and lightweight design. To install VS Code, visit __code.visualstudio.com__, download and run the installer for your operating system, then follow the on-screen instructions to complete the installation process.

- Essential VS Code plugin for Python development:

__Python (by Microsoft)__: Boost your Python development with Microsoft's VS Code extension. Access IntelliSense, linting, debugging, navigation, testing, Jupyter support, and code refactoring in a single, professional package. 

__autopep8 (by Microsoft)__: The Autopep8 VS Code plugin automatically formats Python code to adhere to the PEP 8 style guide within Visual Studio Code. It provides on-the-fly feedback, customizable formatting options, and seamless integration with VS Code, promoting consistent and standardized code formatting.

__Code Spell Checker(by Street Side Software)__:  This extension helps maintain clean and error-free code by highlighting spelling mistakes in comments and strings. It assists in avoiding typos and ensuring code professionalism.

__General Configuration__: VS Code allow you to customize settings, keybindings, and themes according to your preferences. Explore the features provided by VS Code and its plugins to maximize productivity and efficiency in Python development.

NOTE: To enable automatic code formatting with __autopep8__ when saving Python files, create a folder named __.vscode__ in the root directory where your Python scripts are located. Inside this folder, include a file named __settings.json__ with the following configuration:

```json
{
  "[python]": {
    "editor.defaultFormatter": "ms-python.autopep8",
    "editor.formatOnSave": true
  }
}
```

After configuring this, you'll notice that Python's coding style guidelines are automatically applied. This includes maintaining a two-line distance between function definitions, adding spaces around operators, and after commas in function arguments, etc. These automated adjustments can save us a lot of time by eliminating the need to manually adhere to PEP 8.

3. __Running Python files__

With VS Code open, navigate to the desired folder (where your project will be), right-click, and select 'New File'. Name it with a .py extension (e.g., my_script.py). Inside this file, you can write a test code, like the following:

```python
num1 = 10
num2 = 20
result = num1 + num2
print("The sum of", num1, "and", num2, "is:", result)
```

Once you're in the directory containing your Python file, you can run it by typing `python my_script.py`.

4. __Understanding and installing Python packages__

A Python package is a collection of modules, functions, classes, and other resources that can be easily distributed and reused in Python projects. Packages help organize and manage Python code by providing a structured way to group related functionality together. We have official and Non-official Packages:

__Official Packages__: These are packages that are officially maintained and distributed by the Python Software Foundation or other recognized organizations. They undergo rigorous testing and adhere to Python's standards and best practices. Examples include packages like requests, numpy, and matplotlib.

__Non-official Packages__: These are packages developed and maintained by individual developers or third-party organizations. While they may not be officially endorsed by Python, they can still be valuable and widely used in the Python community. Examples include packages like django, flask, and tensorflow.

 Benefits of Installing Packages:

* Code Reusability: Packages provide pre-written code that you can reuse in your projects, saving time and effort in development.

* Enhanced Functionality: Packages often offer specialized functionality that extends Python's core capabilities. For example, packages like requests make it easy to work with HTTP requests, while numpy provides efficient array operations.

* Community Support: Many packages have active communities of developers who contribute improvements, bug fixes, and documentation, providing valuable support for users.

* Increased Productivity: By leveraging existing packages, developers can focus on solving higher-level problems rather than reinventing the wheel for common tasks.

* Ecosystem Growth: Installing and using packages contributes to the growth of Python's ecosystem, fostering innovation and collaboration within the community.

__Installing packages with PIP__: Pip is a package manager for Python that simplifies the process of installing, managing, and uninstalling Python packages. It stands for "Pip Installs Packages" or "Pip Installs Python". It typically comes pre-installed with most Python distributions. Pip is the default and most common way to install Python packages due to its ease of use, large package repository, widespread adoption within the Python community, integration with virtual environments, and active development and maintenance. To check the version of Pip installed on your system, you can use the following command in your terminal or command prompt: `pip --version`. 

Installing and using a package:

Once PIP is installed, you can use it to install any package from __pypi.org__, the official repository for Python packages. For example, to install __numpy__, use the following command: `pip install numpy`. After installation, you can optionally verify its success by checking the package details.: `pip show numpy`. With the new package installed, we can make use of it as per the example:

```python
# Import the NumPy library and alias it as np
import numpy as np

# Create an array using NumPy's array function
my_array = np.array([1, 2, 3, 4, 5])

# Print the array
print(my_array)
```

If you want to check all Python packages that have been installed, you can simply use the command `pip freeze`.

NOTE: Use `pip2` when you want to specifically install packages for Python 2.x versions. Use `pip3` when you want to specifically install packages for Python 3.x versions. However, if you're working in an environment where only one version of Python is installed or if you're working within a virtual environment (that we will cover next), you can use `pip`, and it will operate based on whichever Python version is appropriate to the context.

5. __Installing Python and packages in virtual environments - for serious and collaborative development__

In Python, an "environment" is the context in which a Python program runs. It includes an interpreter and any installed packages. Virtual environments allow developers to create isolated coding environments for projects, managing dependencies separately. Here's an overview on how it works:

* Isolation: Virtual environments segregate packages from the system-wide Python installation, preventing conflicts. Consequently, we don't need to concern ourselves with varying Python versions installed on individual developers' machines.

* Reproducibility: Dependencies are recorded for consistent environment recreation across machines.

* Portability: Environments can be easily shared, ensuring consistent setups for collaborators.

* Python Version Management: Different Python versions and packages can be used for each project, ensuring granular control and preventing conflicts.

* Activation/Deactivation: Environments can be activated or deactivated as needed, facilitating seamless switching between projects and related dependencies.

If you intend to use virtual environments to manage Python packages, it's best to avoid Python and associated packages that are globally installed on your machine. This keeps things separate between your system-wide Python setup and the isolated environments. Next we will check two common ways to do this.

__Method 1: Using Pip + Virtual environments:__ 

With this method, we manually create virtual environments and specify the dependencies they will hold to run our project. Here's how it's done:

1) Uninstall globally installed packages from your machine, for example: `pip uninstall numpy`. Hit 'Y' if confirmation is required. Optional: Reinstall the globally installed Python, so you get the latest version of PIP. For Windows: Open the Control Panel, go to "Programs" or "Programs and Features", find Python in the list of installed programs, select it, and choose "Uninstall". If you use Linux, you can use a command like `sudo apt-get purge python3`. This will uninstall both Python and PIP. Restart your PC and install Python again going to __python.org/downloads__.

2) Create a Virtual Environment: To create a virtual environment, navigate to your project directory in the terminal and run the following command: `python -m venv myenv`. This command will create a virtual environment named 'myenv' using the venv module in Python. The `-m venv` command is a module invocation. The `-m` flag in Python allows you to run a Python module as a script. In this case, we're running the venv module, which is a built-in module in Python for creating virtual environments. This environment is isolated from the system-wide Python installation and other virtual environments, allowing you to install and manage packages specific to your project.

3) Activate Virtual Environment: After creating the virtual environment, you need to activate it. On Windows, run: `myenv/Scripts/activate`. If you're using Bash, you can run source `source myenv/bin/activate` or `source myenv/Scripts/activate` (open your myenv folder to check the patch of 'activate' script). After your virtual environment has been activated, you'll see it's name on terminal, e.g. (myenv).

4) Install Packages on your virtual environment: Now that your virtual environment is activated, you can use it's own PIP to install Python packages just like you would in a global Python installation. For example, to install numpy, run `pip install numpy`. This will install the numpy package into your virtual environment only. Now you can run and test any script that makes usage of the numpy package.

5) Deactivate Virtual Environment: When you're done working on your project, you can deactivate the virtual environment by running: `deactivate`. In this scenario, numpy is installed only within our virtual environment. Consequently, attempting to execute scripts dependent on numpy outside of this environment will fail.

6) Generate the requirements.txt File: A requirements.txt file is commonly used in Python projects to specify the project's dependencies, including the required packages and their respective versions. Once the virtual environment is activated, use the `pip freeze` command to generate a list of installed packages on that virtual environment and their versions. Then, redirect the output to a requirements.txt file: `pip freeze > requirements.txt`. It's important to note that after installing new packages in our virtual environment, the requirements.txt file will not be automatically updated. For each new package installed (that will actually be part of our project), we need to update requirements.txt by running the command `pip freeze > requirements.txt` again. Another point to consider is that when uninstalling a package, we also need to manually uninstall any related packages that may have been installed along with it.

7) Document how others will run your project: After working on your project and installing necessary packages in its virtual environment, you won't share the 'myenv' folder or its contents. If you're uploading your project to GitHub, for instance, the 'myenv' folder will have to be ignored. You'll need to instruct others to:

* Download or clone the project.
* Ensure Python and PIP are installed on their machines.
* Create a virtual environment using the command `python -m venv myenv`.
* Activate the virtual environment using `myenv/Scripts/activate` (Windows) or `source myenv/bin/activate` (Bash).
* Install required packages listed in 'requirements.txt' using `pip install -r requirements.txt`.
* Execute your project's entry point, for example `python main.py`.

Following these steps, other developers can work in virtual environments with the same packages and versions specified in your project.

NOTE: The `-r` flag stands for "read" and is used to specify that pip should read the list of package names and versions from the requirements.txt 

Pip and virtual environments are essential for managing Python projects, reducing inconsistencies and challenges, especially in collaborative projects. However, manual management of dependencies can result in inconsistencies and challenges, particularly in larger projects. Therefore, it's worth considering a tool like __Pipenv__.

__Method 2: Using Pipenv (An even better solution):__ 

Pipenv is a tool designed to address the challenges of dependency management in Python projects. It allows us to create virtual environments for projects, ensuring that dependencies are isolated and specific to each project. By consolidating features from Pip and virtualenv, Pipenv simplifies the development process and enhances collaboration on projects. Key Features and Benefits of Pipenv:

* Virtual Environment Management: Automatically creates and manages virtual environments for projects, eliminating the need to manage them separately using tools like virtualenv.

* Holistic Dependency Management: When uninstalling a package with Pipenv, it automatically removes related and unused dependencies, offering a more comprehensive approach compared to traditional methods like virtual environments and requirements.txt. This ensures a cleaner environment with only necessary dependencies installed.

* Deterministic Builds: Generates a Pipfile.lock file that records exact versions of dependencies, ensuring consistent builds across environments and preventing unexpected behavior due to automatic upgrades.

* Package Distribution: Provides features for distributing code as a package, enhancing the development workflow for both personal projects and collaborations.

* Ease of Use: Simplifies the workflow by consolidating common tasks into a single command-line tool, streamlining dependency management and project setup.

As seen above, Pipenv simplifies Python dependency management, particularly for collaborative projects. 

Now we will start using Pipenv by following these steps:

1) Uninstall virtual env with `pip uninstall virtualenv` then remove your virtual environment files like 'myenv' folder and 'requirements.txt'. This prevents conflicts and ensures Pipenv manages dependencies smoothly. 

2) Install Pipenv on your machine with: `pip install pipenv`. 

3) Create the virtual environment: A virtual environment will be created by running `pipenv --python <python_version>`. For instance, `pipenv --python 3` will consider the latest version of Python 3 that is installed on your machine. By using `pipenv --python 3.8` for example, Pipenv will select Python 3.8 if it's installed on your machine. After creating the virtual environment, Pipenv will also generate the 'Pipfile' used to specify the project's packages/dependencies.

Note 1: If the specified version is not available, pipenv will select the closest version installed on your machine. It's important to note that Python doesn't include a built-in version manager. To use a specific Python version, you must manually install it and update the system's PATH, or utilize tools like __pyenv__ or __pyenv-win__.

Note 2: By default, Pipenv creates virtual environments in your system, usually within the '.virtualenvs' folder under your user directory. While creating a '.virtualenv' folder in your project directory can be beneficial, it's not mandatory, so this tutorial won't cover this type of configuration.

4) Activate the virtual environment by using the command `pipenv shell`. After this step, you may notice that the title of your terminal has changed to 'pipenv'.

5) Confirm that a virtual environment associated with your project has been created: `pipenv --venv`. This command will display the path of the virtual environment created on your machine.

6) Install dependencies as needed: Install any package that is to be used with `pipenv` command, for example: `pipenv install numpy`. Note that this will generate a Pipfile.lock file as well, which aids in internal tracking of dependency relationships. Once packages are installed within a virtual environment context, they will belong to that environment only. It is important to mention that some packages assist developers in tasks like code linting and testing, while others are essential for the application's functionality, like a math library in a math application. To install a package for development purposes, use the `--dev` flag or its shorthand `-D`. For instance: `pipenv install pytest -D`.

7) Uninstall dependencies as needed: To do this, you can execute the command `pipenv uninstall <package_name>`, for example: `pipenv uninstall numpy`.

8) Feel free to manage environments and dependencies: When you're finished working on the project and wish to exit its corresponding virtual environment, you can do so with the `exit` command. To reactivate the virtual environment, simply use the `pipenv shell` command again. If you need to recreate your virtual environment or have downloaded someone's project without an associated virtual environment, you can run `pipenv install` where the Pipfile resides. This command will both create the virtual environment on your machine and download the necessary packages. Afterwards, running the `pipenv shell` command will have you ready code on that project's virtual environment. By doing so, the Pipfile will place development dependencies under the [dev-packages] section. 

NOTE 1: Although the Pipfile itself does not explicitly specify the location of the virtual environment, Pipenv uses the information in the Pipfile to determine the Python version and dependencies for the project and then locates or creates the associated virtual environment accordingly.

NOTE 2: If you're working on a project that requires a Python version you don't have installed, you'll need to manually install that version and update the system's PATH, as previously mentioned. It's advisable to do this before executing `pipenv install`, which sets up the virtual environment.

9) Document how others will run your project: If you plan to upload your project to a Git platform, you'll need to instruct others to:

* Download or clone the project.
* Have Python and PIP installed on their machines.
* Install Pipenv with `pip install pipenv`.
* Install dependencies while creating a virtual environment: `pipenv install` (This step relies on the Pipfile).
* Activate project's virtual environment with `pipenv shell` and exit it with the `exit` command.
* Execute your project's entry point, for example `python main.py`.

NOTE: As you may have noticed, Pipfile and Pipfile.lock are crucial for maintaining consistency in dependency management within collaborative projects. These files are important for your project and must be included when pushing code to a repository.

In summary:

* Install Pipenv on your machine with `pip install pipenv`.
* Create a virtual environment with `pipenv --python 3`.
* Activate/reactivate a virtual environment  with `pipenv shell`.
* Confirm virtual environment creation path with `pipenv --venv`.
* Install regular dependencies using `pipenv install <package_name>`.
* Install development dependencies using `pipenv install <package_name> --dev` or `pipenv install <package_name> -D`.
* Uninstall dependencies with `pipenv uninstall <package_name>`.
* Exit virtual environments with `exit`. 
* Run `pipenv install` in the project directory to establish a virtual environment and download project's dependencies.

10) Using `requirements.txt` alongside Pipenv:

Although your project is managed with Pipenv, you may still want to run `pip freeze > requirements.txt` to export the current list of installed packages along with their versions to a __requirements.txt__ file. This can be beneficial for sharing your project with individuals who do not use Pipenv or for deployment on platforms that rely on __requirements.txt__ for package installation. 

It's possible for your virtual environment created with Pipenv to have 'ghost dependencies,' which can lead to unnecessary entries in the requirements.txt file. If you encounter this issue, you can take the following steps:

* Save your `Pipfile` (or its content) in a safe location to preserve your project's dependencies.
* Exit the virtual environment using `exit`, and delete it with `pipenv --rm` to remove the existing environment entirely.
* Create and activate a new virtual environment with Pipenv using `pipenv --python 3` followed by `pipenv shell`.
* Update the Pipfile with any specific package versions or configurations required for your project.
* Install the dependencies specified in the updated Pipfile using `pipenv install`.
* Finally, generate a clean __requirements.txt__ file by running `pip freeze > requirements.txt` to reflect the current state of your dependencies in the new virtual environment.

Following these steps helps ensure that you start with a clean and well-defined virtual environment, without any unnecessary or unwanted dependencies, and generate an accurate __requirements.txt__ file for sharing or deployment purposes.
