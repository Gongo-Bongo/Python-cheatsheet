### Python Cheat Sheet

#### 1. Basic Syntax

```python
print("Hello, Python!")
```

- **print()**: Prints text to the console.

#### 2. Variables and Data Types

```python
x = 10            # Integer
y = 10.5          # Float
name = "Python"   # String
is_valid = True   # Boolean
```

- Variables are dynamically typed (no need to declare types).

#### 3. Data Structures

- **List**: Ordered, mutable collection.
  
```python
my_list = [1, 2, 3]
my_list.append(4)  # Add to list
print(my_list[0])  # Access first item
```

- **Tuple**: Ordered, immutable collection.
  
```python
my_tuple = (1, 2, 3)
```

- **Set**: Unordered collection with no duplicates.
  
```python
my_set = {1, 2, 3}
my_set.add(4)
```

- **Dictionary**: Key-value pairs.
  
```python
my_dict = {"name": "John", "age": 30}
print(my_dict["name"])   # Access value by key
```

#### 4. Conditionals

```python
a = 10
b = 20
if a > b:
    print("a is greater")
elif a == b:
    print("a equals b")
else:
    print("b is greater")
```

- **if-elif-else**: Conditional statements.

#### 5. Loops

- **For Loop**: Iterating over a sequence.

```python
for i in range(5):
    print(i)   # Prints 0 to 4
```

- **While Loop**: Repeat as long as the condition is true.

```python
x = 0
while x < 5:
    print(x)
    x += 1
```

#### 6. Functions

```python
def add(a, b):
    return a + b
```

- **def**: Defines a function.
- **return**: Returns a value from a function.

#### 7. Lambda Functions

```python
sum = lambda a, b: a + b
print(sum(3, 5))  # Output: 8
```

- Anonymous functions defined with the **lambda** keyword.

#### 8. List Comprehensions

```python
squares = [x**2 for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```

- Concise way to create lists.

#### 9. Error Handling

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("This will always execute")
```

- **try-except-finally**: Handles exceptions.
- **finally**: Always executes, useful for cleanup.

#### 10. Classes and Objects

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello, my name is {self.name}")

person = Person("Alice", 30)
person.greet()  # Output: Hello, my name is Alice
```

- **class**: Defines a class.
- **__init__**: Constructor method.
- **self**: Refers to the instance of the class.

#### 11. Inheritance

```python
class Animal:
    def sound(self):
        print("Some sound")

class Dog(Animal):
    def sound(self):
        print("Bark")

dog = Dog()
dog.sound()  # Output: Bark
```

- **Inheritance**: Enables a class to inherit properties and methods from another class.

#### 12. Modules and Importing

```python
import math
print(math.sqrt(16))  # Output: 4.0
```

- **import**: Imports a module.

#### 13. File I/O

- **Reading Files**:

```python
with open("file.txt", "r") as file:
    content = file.read()
    print(content)
```

- **Writing Files**:

```python
with open("file.txt", "w") as file:
    file.write("Hello, File!")
```

#### 14. List, Set, and Dictionary Methods

- **List Methods**:

```python
my_list = [1, 2, 3]
my_list.append(4)  # Adds an item
my_list.remove(2)  # Removes an item
```

- **Set Methods**:

```python
my_set = {1, 2, 3}
my_set.add(4)      # Adds an item
my_set.remove(2)   # Removes an item
```

- **Dictionary Methods**:

```python
my_dict = {"name": "John", "age": 30}
my_dict["age"] = 31  # Update value
print(my_dict.keys())  # Get all keys
```

#### 15. Slicing

```python
my_list = [1, 2, 3, 4, 5]
print(my_list[1:4])  # Output: [2, 3, 4]
```

- **Slicing**: Extracts a portion of a list or string using `start:stop`.

#### 16. Map, Filter, and Reduce

- **map()**: Applies a function to all items in an iterable.

```python
numbers = [1, 2, 3, 4]
squared = list(map(lambda x: x**2, numbers))
print(squared)  # Output: [1, 4, 9, 16]
```

- **filter()**: Filters items based on a condition.

```python
even = list(filter(lambda x: x % 2 == 0, numbers))
print(even)  # Output: [2, 4]
```

- **reduce()** (from **functools** module): Reduces a list to a single value.

```python
from functools import reduce
result = reduce(lambda x, y: x + y, numbers)
print(result)  # Output: 10
```

#### 17. Decorators

```python
def decorator(func):
    def wrapper():
        print("Before function")
        func()
        print("After function")
    return wrapper

@decorator
def greet():
    print("Hello!")

greet()
```

- **@decorator**: Adds functionality to an existing function.

#### 18. Generators

```python
def count_up_to(max):
    count = 1
    while count <= max:
        yield count
        count += 1

for num in count_up_to(5):
    print(num)  # Outputs 1 to 5
```

- **yield**: Returns a value and pauses the function’s state, allowing it to resume later.

#### 19. Comprehensions

- **Dictionary Comprehension**:

```python
squared = {x: x**2 for x in range(5)}
print(squared)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

- **Set Comprehension**:

```python
squared_set = {x**2 for x in range(5)}
print(squared_set)  # Output: {0, 1, 4, 9, 16}
```

#### 20. Working with Dates

```python
from datetime import datetime
now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M:%S"))
```

- **datetime** module: For working with dates and times.

---

This Python cheat sheet provides an overview of key concepts and syntax for quick reference.