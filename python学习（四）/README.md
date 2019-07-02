# Lesson 5：Function
## 5.1 Defining Functions
1. function header
>`def`+`function name`+`parentheses that may include arguments separated by commas` + `:`
2. function body
> 1.indented after the header line
> 2.return (not necessary)
3. Default Arguments

```python
def cylinder_volume(height, radius=5):
    pi = 3.14159
    return height * pi * radius ** 2
```
It is possible to pass values in two ways - by position and by name. Each of these function calls are evaluated the same way.

```python
cylinder_volume(10, 7)  # pass in arguments by position
cylinder_volume(height=10, radius=7)  # pass in arguments by name
```
## 5.2 Variable Scope
1. If a variable is created inside a function, it can only be used within that function.
2. Variables defined outside functions, can still be accessed within a function. 
3. However, the value of a global variable can not be modified inside the function.
## 5.3 Documentation
1. Docstrings are surrounded by triple quotes.

```python
def population_density(population, land_area):
    """Calculate the population density of an area.

    INPUT:
    population: int. The population of that area
    land_area: int or float. This function is unit-agnostic, if you pass in values in terms
    of square km or square miles the function will return a density in those units.

    OUTPUT: 
    population_density: population / land_area. The population density of a particular area.
    """
    return population / land_area
```
## 5.4 Lambda Expressions
1. You can use lambda expressions to create anonymous functions. 

```python
multiply = lambda x, y: x * y
multiply(4, 7)
>>28
```
