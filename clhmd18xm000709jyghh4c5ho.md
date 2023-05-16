---
title: "What are Python Lambdas? How do I use them?"
datePublished: Sat May 13 2023 19:08:14 GMT+0000 (Coordinated Universal Time)
cuid: clhmd18xm000709jyghh4c5ho
slug: what-are-python-lambdas-how-do-i-use-them
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684262820882/097c38ff-b6b7-4704-8d7e-ffa5b20d64ca.png
tags: lambda, python, python-beginner

---

## What are lambda functions?

A lambda function is a small function that can be defined inline without a formal function definition. This means that it can be created and used immediately without needing to be defined beforehand.

Here's a simple example:

```python
add = lambda x, y: x + y
```

In this example, we've defined a lambda function called `add` that takes two arguments, `x` and `y`, and returns their sum. This lambda function can be called just like any other function:

```plaintext
result = add(2, 3)
print(result)  # Output: 5
```

Lambda functions are often used for simple, one-off operations that don't need to be defined as a full function. They're particularly useful for operations that are used as arguments to other functions, such as sorting or filtering.

## Using lambda functions for sorting

Sorting is a common operation in programming, and Python has a built-in `sorted()` function that can be used to sort lists and other iterable objects. One of the powerful features of the `sorted()` function is that it can take a key function as an argument, which is used to determine the value to sort on.

For example, let's say we have a list of dictionaries representing people, with each dictionary containing a name and an age:

```python
people = [
    {'name': 'Alice', 'age': 25},
    {'name': 'Bob', 'age': 20},
    {'name': 'Charlie', 'age': 30},
]
```

If we want to sort this list by age, we can use a lambda function as the key function:

```python
sorted_people = sorted(people, key=lambda person: person['age'])
```

In this example, the lambda function `lambda person: person['age']` is used as the key function for sorting. It takes a single argument, `person`, which is one of the dictionaries in the `people` list, and returns the value of the `'age'` key. This lambda function is used to determine the value to sort on, so the resulting `sorted_people` list will be sorted by age.

## Using lambda functions for filtering

Filtering is another common operation in programming, and Python has a built-in `filter()` function that can be used to filter iterable objects based on a given condition. Like the `sorted()` function, the `filter()` function can take a function as an argument to determine the condition to filter on.

For example, let's say we have a list of numbers:

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

If we want to filter this list to only include even numbers, we can use a lambda function as the filtering condition:

```python
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
```

In this example, the lambda function `lambda x: x % 2 == 0` is used as the filtering condition. It takes a single argument, `x`, which is one of the numbers in the `numbers` list, and returns `True` if the number is even and `False` otherwise. This lambda function is used as the filtering condition, so the resulting `even_numbers` list will only

## Using lambda functions for more complex business logic

In some scenarios, we may want to use a lambda function to apply more complex business logic to our data. However, in these cases, an inline function definition can be extensive and difficult to read for other developers. To address this issue, we can reference a pre-defined method if necessary.

For example, let's say we have a list of numbers:

```python
numbers = [.454,.627,.751,.995,.892,.583,.232,.346,.769,.906]
```

If we want to apply a function to manipulate this list, we can use a lambda function:

```python
def calc_percentage(x):
    percentage = format(x * 100, '.1f')
    return str(percentage) + '%'

percent_arr = list(map(lambda x: calc_percentage(x), numbers))
```

In this example, the lambda function `lambda x: calc_percentage(x)` is used to apply the `calc_percentage()` function to each number in the `numbers` list. The resulting `percent_arr` list will contain each number in `numbers` with the values converted to percentages.

By referencing a pre-defined method in a lambda function, we can apply more complex business logic to our data without sacrificing readability.