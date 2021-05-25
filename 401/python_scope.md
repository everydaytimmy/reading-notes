### Scope

The Python scope concept is generally presented using a rule known as the **LEGB rule**.

The letters in the acronym LEGB stand for **Local, Enclosing, Global, and Built-in** scopes. 

**Global scope:** The names that you define in this scope are available to all your code.

**Local scope:** The names that you define in this scope are only available or visible to the code within the scope.

Python resolves names using the so-called LEGB rule

**Local (or function) scope** is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. It’s created at function call, not at function definition, so you’ll have as many different local scopes as function calls. *This is true even if you call the same function multiple times, or recursively. Each call will result in a new local scope being created.*

**Enclosing (or nonlocal)** scope is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

**Global (or module) scope** is the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.

**Built-in scope** is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.

Python provides two keywords that allow you to modify the content of global and nonlocal names. These two keywords are:

1) global
2) nonlocal

fails:
```
>>> counter = 0  # A global name
>>> def update_counter():
...     counter = counter + 1  # Fail trying to update counter
```

works:

```
>>> counter = 0  # A global name
>>> def update_counter():
...     global counter  # Declare counter as global
...     counter = counter + 1  # Successfully update the counter
...
```

Note: The use of global is considered bad practice in general. If you find yourself using global to fix problems like the one above, then stop and think if there is a better way to write your code.

This is better - note 'counter' being defined as a parameter
```
>>> global_counter = 0  # A global name
>>> def update_counter(counter):
...     return counter + 1  # Rely on a local name
```

This implementation of update_counter() defines counter as a parameter and returns its value augmented by 1 unit every time the function is called. This way, the result of update_counter() depends on the counter you use as an input and not on the changes that other functions (or pieces of code) can perform on the global variable, global_counter.

Avoid lazy global names (global names that are declared inside of a function)

### The nonlocal Statement

Similarly to global names, nonlocal names can be accessed from inner functions, but not assigned or updated. If you want to modify them, then you need to use a nonlocal statement. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.

Unlike global, you can’t use nonlocal outside of a nested or enclosed function. To be more precise, you can’t use a nonlocal statement in either the global scope or in a local scope.


