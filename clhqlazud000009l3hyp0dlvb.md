---
title: "Three Helpful Python Functions to Know"
seoTitle: "Transform your data with Python's Map, Filter, and Sorted Functions"
datePublished: Tue May 16 2023 18:10:51 GMT+0000 (Coordinated Universal Time)
cuid: clhqlazud000009l3hyp0dlvb
slug: three-helpful-python-functions-to-know
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684262694592/b359675e-1011-4301-a9d8-d20e02a57c6f.png
tags: python, python-beginner, codingnewbies

---

In Python, there is a large collection of built-in functions that are frequently used to enhance the efficiency and readability of our source code. Among this vast collection, I have found the `map`, `filter` and `sorted` functions to be very useful, especially working with datasets.

### Map:

The `map` function can be used to transform data by applying any given operation to each element in an iterable. It requires two arguments: a function and an iterable, such as a list. The following is an example of the `map` function:

```python
map(func_name, iterable)
```

When the `map` function is called, the specified function is applied to each item in the iterable. This results in a new iterable containing the transformed values. This enables us to perform operations on each element of an iterable, greatly simplifying and optimizing our code.

For example, suppose we had a list of integers that we needed to double in value. We could accomplish this by executing the code below.

```python
def addition(n):
	return n + n

numbers = (1, 2, 3, 4)
result = map(addition, numbers)
print(list(result)) # Output: [2,4,6,8]
```

### Filter:

The filter function operates similarly to that of the map function in the sense that it will iterate over a data type, such as a list, but differs in the purpose of the operation performed. This function will selectively extract elements given the provided condition. This function again takes a function as well as an iterable as parameters.

```python
filter(func_name, iterable)
```

When the passed-in function executes, it returns a boolean value. The `filter` function will return an iterable containing only values that evaluates to `True`. By leveraging the `filter` function, we can extract desired subsets of data from a larger dataset.

For example, suppose we have a list of numbers and want to select only the even numbers. We can achieve this using the following code:

```python
def is_even(n):
	if number % 2 == 0:
          return True  
    return False

numbers = (1, 2, 3, 4)
result = map(is_even, numbers)
print(list(result)) # Output: [2,4]
```

### Sorted:

A third function that proves valuable when working with datasets is the `sorted` function. As the name suggests, this function is going to perform a sorting algorithm on the provided dataset and return the sorted result. By default, it will sort the items of the provided dataset in ascending order, but this can be changed by providing additional parameters.

For example, suppose we had a tuple containing letters in random order and we wanted them sorted. We could accomplish this using the following code:

```python
a = ("b", "g", "a", "d", "f", "c", "h", "e")
a_sorted = sorted(a, reverse=True)
a_reverse_sorted = sorted(a)

print(a_sorted) #Output: ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']
print(a_reverse_sorted) #Output: ['h', 'g', 'f', 'e', 'd', 'c', 'b', 'a']
```

Python's large collection of built-in functions helps make our life as developers easier when writing efficient code. When dealing with datasets, the `map`, `filter`, and `sorted` functions can be a huge lift. They enable us to write clean concise code to perform actions over any provided dataset.

I hope you found this helpful. Thanks for visiting!