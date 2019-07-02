# Lesson 3: Data structure
## 3.1.Lists and Membership Operators
1. Lists can contain any mix

```python
list_of_random_things = [1, 3.4, 'a string', True]

list_of_random_things[-1] 
#-1 in the last index
>>True
list_of_random_things[-2] 
>>a string
```
2. Slice: the `lower index` is inclusive and the `upper index` is exclusive.

```python
list_of_random_things = [1, 3.4, 'a string', True]
list_of_random_things[1:2]
>>[3.4]
list_of_random_things[:2]
>>[1, 3.4]
list_of_random_things[1:]
>>[3.4, 'a string', True]
```
3. `in` or `not in`
```python
'this' in 'this is a string'
>>True
5 in [1, 2, 3, 4, 6]
>>False
5 not in [1, 2, 3, 4, 6]
>>True
```
4. Mutability and Order
**mutable**: can be changed
**immutable**: can not be changed
**Order**: is about whether the position of an element in the object can be used to access the element. 
```python
my_lst = [1, 2, 3, 4, 5]
my_lst[0] = 'one'
print(my_lst)
>>['one', 2, 3, 4, 5]

#does not work
greeting = "Hello there"
greeting[0] = 'M'
```
5. useful function for list
 - `len()` returns how many elements are in a list.
 - `max()` returns the greatest element of the list. 
 - `min()` returns the smallest element in a list.
 - `sorted()` returns a copy of a list in order from smallest to largest, leaving the list unchanged.
 - `join` is a string method that takes a list of strings as an argument, and returns a string consisting of the list elements joined by a separator string.

```python
new_str = "\n".join(["fore", "aft", "starboard", "port"])
print(new_str)
>>fore
>>aft
>>starboard
>>port
```
-`append` adds an element to the end of a list.

```python
letters = ['a', 'b', 'c', 'd']
letters.append('z')
print(letters)
>>['a', 'b', 'c', 'd', 'z']
```

## 3.2 Tuples
> `tuple`: location = (13.4125, 103.866667) (parentheses are optional)
## 3.3 Sets
`Sets` is a data type for mutable unordered collections of unique elements.

```python
numbers = [1, 2, 6, 3, 1, 1, 6]
unique_nums = set(numbers)
print(unique_nums)
>>{1, 2, 3, 6}


fruit = {"apple", "banana", "orange", "grapefruit"}  # define a set

print("watermelon" in fruit)  # check for element

fruit.add("watermelon")  # add an element
print(fruit)

print(fruit.pop())  # remove a random element
print(fruit)

>>False
>>{'grapefruit', 'orange', 'watermelon', 'banana', 'apple'}
>>grapefruit
>>{'orange', 'watermelon', 'banana', 'apple'}
```
## 3.4 Dictionaries and Identity Operators
`dictionary ` is a mutable data type that stores mappings of unique(immutable) keys to values.

```python
elements = {"hydrogen": 1, "helium": 2, "carbon": 6}
print(elements["helium"])  # print the value mapped to "helium"
elements["lithium"] = 3  # insert "lithium" with a value of 3 into the dictionary
print("carbon" in elements)
>>True
print(elements.get("dilithium"))
>>None
```

`Identity Operators`:
|Keyword| Operator |
|--|--|
| is |  evaluates if both sides have the same identity|
|is not|evaluates if both sides have different identities|

```python
n = elements.get("dilithium")
print(n is None)
print(n is not None)
>>True
>>False
```
`get`:

```python
>>> elements.get('dilithium')
None
>>> elements['dilithium']
KeyError: 'dilithium'
>>> elements.get('kryptonite', 'There\'s no such element!')
"There's no such element!"
```
`nested dictionary`:

```python
elements = {"hydrogen": {"number": 1,
                         "weight": 1.00794,
                         "symbol": "H"},
              "helium": {"number": 2,
                         "weight": 4.002602,
                         "symbol": "He"}}
```
## 3.5 Conclusion
|Data Structure|  Ordered|Mutable|Constructor|Example
|--|--|--|--|--|
|List  | Yes |Yes|[ ] or list()|[5.7, 4, 'yes', 5.7]
|Tuple|Yes|No|( ) or tuple()|(5.7, 4, 'yes', 5.7)
|Set|No|Yes|{} or set()|{5.7, 4, 'yes'}
|Dictionary|No|No|{ } or dict()|{'Jun': 75, 'Jul': 89}
