# Lesson7: Advanced topics
## 7.1 Iterators and Generators
 1. example of a generator function called my_range, which produces an iterator that is a stream of numbers from 0 to (x - 1).

```python
def my_range(x):
    i = 0
    while i < x:
        yield i
        i += 1
# This yield keyword is what differentiates a generator from a typical function.
```
## 7.2 Generator Expressions

```python
sq_list = [x**2 for x in range(10)]  # this produces a list of squares

sq_iterator = (x**2 for x in range(10))  # this produces an iterator of squares
```

好了，以后就不是python小白了~~

