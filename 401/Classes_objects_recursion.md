## Classes and Objects

Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes

You can create multiple different objects that are of the same class(have the same variables and functions defined). However, each object contains independent copies of the variables defined in the class.


```
# define the Vehicle class
class Vehicle:
    name = ""
    kind = "car"
    color = ""
    value = 100.00
    def description(self):
        desc_str = "%s is a %s %s worth $%.2f." % (self.name, self.color, self.kind, self.value)
        return desc_str

# your code goes here
car1 = Vehicle()
car1.name = "Fer"
car1.color = "red"
car1.kind = "convertible"
car1.value = 60000.00

car2 = Vehicle()
car2.name = "Jump"
car2.color = "blue"
car2.kind = "van"
car2.value = 10000.00

# test code
print(car1.description())
print(car2.description())
```
### Thinking Recursively

https://realpython.com/python-thinking-recursively/

A recursive function is a function defined in terms of itself via self-referential expressions.

This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.

#### Maintaining State

When dealing with recursive functions, keep in mind that each recursive call has its own execution context, so to maintain state during recursion you have to either:

 - Thread the state through each recursive call so that the current state is part of the current call’s execution context
 - Keep the state in global scope

Here’s how you maintain the state by keeping it in global scope:

```
# Global mutable state
current_number = 1
accumulated_sum = 0


def sum_recursive():
    global current_number
    global accumulated_sum
    # Base case
    if current_number == 11:
        return accumulated_sum
    # Recursive case
    else:
        accumulated_sum = accumulated_sum + current_number
        current_number = current_number + 1
        return sum_recursive()

```

*lru_cache* is a *decorator* that caches the results. Thus, we avoid recomputation by explicitly checking for the value before trying to compute it. One thing to keep in mind about lru_cache is that since it uses a dictionary to cache results, the positional and keyword arguments (which serve as keys in that dictionary) to the function must be hashable.
