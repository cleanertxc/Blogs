俗话说好记性不如烂笔头，正好最近打算系统的学习一下python, 就在这里记录一下吧，也是当作第一篇博客了~~
# Lesson 2:Data type and Operator
## 2.1 Arithmetic Operators
1. `+`: Addition
2. `-`: Subtraction
3. `*`: Multiplication
4. `/`: Division
5. `%`: Mod
6. `**`: Exponentiation
7. `//`: Divides and round down to nearest integer
   
## 2.2 Variables and Assignments operator 
 x,y,z=1,2,3 $\iff$ x=1,y=2,z=3
 
 Few things to pay attention to:
 1. Only use ordinary letters, numbers and underscores in your variable names. They can’t have spaces, and need to start with a letter or underscore.
 2. **You can’t use reserved words or built-in identifiers** that have important purposes in Python.
 3. Variables better to be descriptive.
 4. The pythonic way to name variables is to use all lowercase letters and underscores to separate words.
 
## 2.3 Integers and floats
 1. check for type: type(...)
 2. int (97.5)=97
 3. Because the float, or approximation, for 0.1 is actually slightly more than 0.1 

## 2.4 Booleans, Comparison Operators, and Logical Operators
1. The bool data type holds one of the values `True` or `False`, which are often encoded as `1` or `0`, respectively.
2. `and`: Evaluates if all provided statements are True
3. `or`: Evaluates if at least one of many statements is True.
4. `not`: Flips the Bool Value

## 2.5 String
1. using a `\` in string to print `'`
2. useful operations
```python
>>> first_word = 'Hello'
>>> second_word = 'There'
>>> print(first_word + second_word)

HelloThere

>>> print(first_word + ' ' + second_word)

Hello There

>>> print(first_word * 5)

HelloHelloHelloHelloHello

>>> print(len(first_word))

5
```
3. **.format()** method
```python
print("Mohammed has {} balloons".format(27))
output:Mohammed has 27 balloons

animal = "dog"
action = "bite"
print("Does your {} {}?".format(animal, action))
output:Does your dog bite?

maria_string = "Maria loves {} and {}"
print(maria_string.format("math", "statistics"))
output:Maria loves math and statistics
```
4. **.split()** method
- The split method has two additional arguments (sep and maxsplit). 
* The sep argument stands for "**separator**". It can be used to identify how the string should be split up (e.g., whitespace characters like space, tab, return, newline; specific punctuation (e.g., comma, dashes)). If the sep argument is not provided, **the default separator is whitespace**.
- The maxsplit argument provides the **maximum number**  of splits. The argument gives maxsplit + 1 number of elements in the new list, with the remaining string being returned as the last element in the list.
```python
new_str = "The cow jumped over the moon."
new_str.split()
>>['The', 'cow', 'jumped', 'over', 'the', 'moon.']
new_str.split(' ', 3)
>>['The', 'cow', 'jumped', 'over the moon.']
new_str.split('.')
>>['The cow jumped over the moon', '']
new_str.split(None, 3)
>>['The', 'cow', 'jumped', 'over the moon.']
```
