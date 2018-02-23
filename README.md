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

So what if you want to store information unordered, but still be able to find a specific element quickly?
We use SETS

```python
v = set(“hello”)
print(v)
>> set([“h”,”e”,”l”,”o”])
v[0]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'set' object does not support indexing
```

You will notice a couple of interesting behaviors of sets here:

1. Sets are used to store unique information, in an unordered list, so all of the values are unique. So when we created our set from the str(“hello”), it removed the second “l” from the set.
2. The other behavior is the lack of indexing. In a list `v[0]` would normally access the list at the first position, but sets do not act this way!

So let's try to make our shopping list with a set instead of a list:

we can use the set() constructor to create a set with predefined information

```python
shopping_list_set = set("pens", "notebooks", "graph paper")
```

What if we need to add something?

```python
shopping_list_set.add("pencils")
print(shopping_list_set)
>> set(["pens", "notebooks", "graph paper", "pencils"])
```

Great! Now we have our shopping list all ready to go!

When we are shopping, we can print the list, or we can see if something is in the list:

```python
"pens" in shopping_list_set
>> True
```

And when we put the pens in our shopping basket, we can go ahead and remove it from our list:

```python
shopping_list.set.remove("pens")
print(shopping_list_set)
>> set(["notebooks", "graph paper", "pencils"])
```

And how about this fancy move when we grab our notebooks:

```python
for word in shopping_list_set:
    if word == "notebooks":
        shopping_list_set.remove(word)
```

And now notebooks are off of the list!

# Summary

Lists are great for storing information that we need to keep ordered, but when we need to find something in a list, we have to go through each index to check for a match. With sets we are able to find individual elements more quickly. Besides that, sets also include some handy built-in functions to compare between sets and preform arithmetic operations on your sets.

When deciding whether to use a set of list, think about this:
Iterating through lists is faster than iterating through a set because lists are indexed. But if order isn't important, sets are better at storing unique information, especially if you are solely looking to check if something exists.
