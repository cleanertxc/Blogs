# Lesson 6: Scripting
## 6.1 Scripting With Raw Input
1. `input` method

```python
name = input("Enter your name: ")
print("Hello there, {}!".format(name.title()))

num = int(input("Enter an integer"))
print("hello" * num)

result = eval(input("Enter an expression: "))
print(result)
#interpret user input as a Python expression using the built-in function eval
```
## 6.2 Errors and Exceptions
- **Syntax errors** occur when Python can’t interpret our code, since we didn’t follow the correct syntax for Python. 
- **Exceptions** occur when unexpected things happen during execution of a program, even if the code is syntactically correct. 
## 6.3 Handling Errors
1. Try Statement
- `try` This is the only mandatory clause in a try statement. The code in this block is the first thing that Python runs in a try statement.
- `except` If Python runs into an exception while running the try block, it will jump to the except block that handles that exception.
- `else` If Python runs into no exceptions while running the try block, it will run the code in this block after running the try block.
- `finally` Before Python leaves this try statement, it will run the code in this finally block under any conditions, even if it's ending the program.

```python
try:
    # some code
except (ValueError, KeyboardInterrupt):
    # some code

try:
    # some code
except ValueError:
    # some code
except KeyboardInterrupt:
    # some code
```
## 6.4 Accessing Error Messages

```python
try:
    # some code
except ZeroDivisionError as e:
   # some code
   print("ZeroDivisionError occurred: {}".format(e))
>>ZeroDivisionError occurred: integer division or modulo by zero
```
## 6.5 Reading and Writing Files
1. Reading a File

```python
f = open('my_path/my_file.txt', 'r')
file_data = f.read()
f.close()
```
2. Writing to a File
- If the file does not exist, Python will create it for you. If you open an existing file in writing mode, any content that it had contained previously will be deleted. 
- If you're interested in adding to an existing file, without deleting its content, you should use the append ('a') mode instead of write.
```python
f = open('my_path/my_file.txt', 'w')
f.write("Hello there!")
f.close()
```
3. `with` method
auto-closes a file
```python
camelot_lines = []
with open("camelot.txt") as f:
    for line in f:
        camelot_lines.append(line.strip())
#using .strip() to remove \n
print(camelot_lines)
```
## 6.6 Importing Local Scripts

```python
import useful_functions as uf
uf.add_five([1, 2, 3, 4])
```
1. To import an individual function or class from a module:

```python
from module_name import object_name
```
2. To import multiple individual objects from a module:
```python
from module_name import first_object, second_object
```
3. To rename a module:
```python
import module_name as new_name
```
4. To import an object from a module and rename it:
```python
from module_name import object_name as new_name
```
5. To import every object individually from a module (DO NOT DO THIS):
```python
from module_name import *
```
6. If you really want to use all of the objects from a module, use the standard import module_name statement instead and access each of the objects with the dot notation.
```python
import module_name
```
