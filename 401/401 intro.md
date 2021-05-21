Some of the Python standard library's useful modules include string, re, datetime, math, random, os, multiprocessing, subprocess, socket, email, json, doctest, unittest, pdb, argparse and sys.

Different exceptions are raised for different reasons.
Common exceptions:
ImportError: an import fails;
IndexError: a list is indexed with an out-of-range number;
NameError: an unknown variable is used;
SyntaxError: the code can't be parsed properly;
TypeError: a function is called on a value of an inappropriate type;
ValueError: a function is called on a value of the correct type, but with an inappropriate value.

Try - Except - Finally

Readlines?


Python supports the following data structures: **lists, dictionaries, tuples, sets**.

**When to use a dictionary:**
- When you need a logical association between a **key:value** pair.
- When you need fast lookup for your data, based on a custom key.
- When your data is being constantly modified. Remember, dictionaries are mutable.

**When to use the other types:**
- Use **lists** if you have a collection of data that does not need random access. Try to choose lists when you need a simple, iterable collection that is modified frequently.
- Use a **set** if you need uniqueness for the elements.
- Use **tuples** when your data cannot change.

Many times, a tuple is used in combination with a dictionary, for example, a tuple might represent a key, because it's immutable.

### Sets

Sets can be combined using mathematical operations.
The **union** operator **|** combines two sets to form a new one containing items in either.
The **intersection** operator **&** gets items only in both.
The **difference** operator **-** gets items in the first set but not in the second.
The **symmetric** difference operator **^** gets items in either set, but not both.

### itertools


There are many functions in **itertools** that operate on iterables, in a similar way to map and filter.
Some examples:
**takewhile** - takes items from an iterable while a predicate function remains true;
**chain** - combines several iterables into one long one;
**accumulate** - returns a running total of values in an iterable.

More magic methods for common operators:
__sub__ for -
__mul__ for *
__truediv__ for /
__floordiv__ for //
__mod__ for %
__pow__ for **
__and__ for &
__xor__ for ^
__or__ for |
