# pythonSets

An introduction to sets

## Objectives:

1. Define a set
2. Learn why sets are userful

It’s back to school time! You spend a few minutes making a list of all the supplies that you need to pick up before your first day. Do you need pens? Check! Do you need some notebooks? Some graph paper?

Let’s make a shopping list!

```python
shopping_list = [“pens“, “notebooks”, “graph paper”]
```

We know what we need now, but what if you need to add something more to the list? You already know that since we are using a list, all we need to do is add something to the list is:

```python
shopping_list.append(“pencils”)
print(shopping_list)

> [“pens“, “notebooks”, “graph paper”, “pencils”]
```

Lists are great for storing ordered information. And if we want to index information we can use dictionaries to store values that are indexed with specific keys so we can access that information quickly.

While lists and dictionaries are useful data structures to manage your information, they have two minor downsides. The first one is mutability- Lists and dictionaries can be changed(or rather, their elements can be) by using any of their numerous built in functions. The other problem you may encounter with lists, is that they can also contain duplicate values.

“Here sets come to save the day”

So what if you want to store information unordered, but still be able to find a specific element quickly? We use SETS

Sets are used to store unique information, in an unordered list. The values in a set are immutable, which means that you can’t change individual values like you can with a list or dict.

```python
v = set(“hello”)
[“h”,”e”,”l”,”o”]
v[0]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'set' object does not support indexing
```

You will notice a couple of interesting behaviors of sets here:
All of the values are unique. So when we created our set from the str(“hello”), it removed the second “l” from the set
We are unable to

If you haven’t heard of them, we can also use tuples to store information that can’t be changed, so if you are working with information that you only want to read, but not change, tuples may be useful, but we will cover that later.
