# Lesson 4：Control Flow
## 4.1 Conditional Statements
 1. `if`,`else`,`elif`

```python
if season == 'spring':
    print('plant the garden!')
elif season == 'summer':
    print('water the garden!')
elif season == 'fall':
    print('harvest the garden!')
elif season == 'winter':
    print('stay indoors!')
else:
    print('unrecognized season')
```
## 4.2 Boolean Expressions for Conditions
1. Truth Value Testing
>By default, the truth value of an object in Python is considered True unless specified as False in the documentation.

>Here are most of the built-in objects that are considered False in Python:
- constants defined to be false: None and False
- zero of any numeric type: 0, 0.0, 0j, Decimal(0), Fraction(0, 1)
- empty sequences and collections: "", (), [], {}, set(), range(0)

## 4.3 Building Dictionary
1. `get` method
```python
book_title =  ['great', 'expectations','the', 'adventures', 'of', 'sherlock','holmes','the','great','gasby','hamlet','adventures','of','huckleberry','fin']
word_counter = {}
for word in book_title:
    word_counter[word] = word_counter.get(word, 0) + 1
    #use get with a default value of 0
print(word_counter)
>>{'great': 2, 'expectations': 1, 'the': 2, 'adventures': 2, 'of': 2, 'sherlock': 1, 'holmes': 1, 'gasby': 1, 'hamlet': 1, 'huckleberry': 1, 'fin': 1}
```
2. `items` method
```python
cast = {
           "Jerry Seinfeld": "Jerry Seinfeld",
           "Julia Louis-Dreyfus": "Elaine Benes",
           "Jason Alexander": "George Costanza",
           "Michael Richards": "Cosmo Kramer"
       }
for key, value in cast.items():
    print("Actor: {}    Role: {}".format(key, value))
>>Actor: Jerry Seinfeld    Role: Jerry Seinfeld
Actor: Julia Louis-Dreyfus    Role: Elaine Benes
Actor: Jason Alexander    Role: George Costanza
Actor: Michael Richards    Role: Cosmo Kramer
#items is an awesome method that returns tuples of key, value pairs, which you can use to iterate over dictionaries in for loops.
```
## 4.4 Zip and Enumerate
1. `Zip` method

```python
letters = ['a', 'b', 'c']
nums = [1, 2, 3]

for letter, num in zip(letters, nums):
    print("{}: {}".format(letter, num))
>>a: 1
b: 2
c: 3
some_list = [('a', 1), ('b', 2), ('c', 3)]
letters, nums = zip(*some_list)
#This would create the same letters and nums tuples we saw earlier. '*' is unzip.
```
2. `Enumerate` method
Enumerate is a built in function that returns an iterator of tuples containing indices and values of a list.
```python
letters = ['a', 'b', 'c', 'd', 'e']
for i, letter in enumerate(letters):
    print(i, letter)
>>0 a
1 b
2 c
3 d
4 e
```
3. Zip Lists to a Dictionary

```python
cast_names = ["Barney", "Robin", "Ted", "Lily", "Marshall"]
cast_heights = [72, 68, 72, 66, 76]

cast=dict(zip(cast_names,cast_heights))
    # replace with your code
print(cast)
>>{'Barney': 72, 'Ted': 72, 'Marshall': 76, 'Robin': 68, 'Lily': 66}
```
## 4.5 List Comprehensions

```python
capitalized_cities = []
for city in cities:
    capitalized_cities.append(city.title())
```
can be reduced to:

```python
capitalized_cities = [city.title() for city in cities]
```
Conditionals in List Comprehensions:

```python
squares = [x**2 for x in range(9) if x % 2 == 0]
# 这里if 放到for前面会报错
squares = [x**2 if x % 2 == 0 else x + 3 for x in range(9)]
print(squares)
>>[0, 4, 4, 6, 16, 8, 36, 10, 64]
```
