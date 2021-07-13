### Dunder Methods

https://dbader.org/blog/python-dunder-methods

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

#### Object Initialization: __init__

This is the constructor that lets us create objects from a class

#### Object Representation: __str__, __repr__

__repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

__str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

```
class Account:
      def __init__(self, owner, amount=0):
        self.owner = owner
        self.amount = amount
        self._transactions = []

    def __repr__(self):
        return 'Account({!r}, {!r})'.format(self.owner, self.amount)

    def __str__(self):
        return 'Account of {} with starting amount: {}'.format(
            self.owner, self.amount)
```
>>> repr(acc)
"Account('bob', 10)"

>>> str(acc)
'Account of bob with starting amount: 10'


#### teration: __len__, __getitem__, __reversed__

```
def __len__(self):
        return len(self._transactions)

    def __getitem__(self, position):
        return self._transactions[position]

```

#### Operator Overloading for Comparing Accounts: __eq__, __lt__


#### Operator Overloading for Merging Accounts: __add__

### Iterators

https://dbader.org/blog/python-iterators

Iterators use exceptions to structure control flow. To signal the end of iteration, a Python iterator simply raises the built-in StopIteration exception.

### Generators

https://dbader.org/blog/python-generators

Whereas a return statement disposes of a function’s local state, a yield statement suspends the function and retains its local state.

Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code needed when writing class-based iterators.
The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.
Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.
