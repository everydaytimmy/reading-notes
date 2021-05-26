## List Comprehensions

https://www.pythonforbeginners.com/basics/list-comprehensions-in-python

List comprehensions provide a concise way to create lists.

It consists of brackets containing an expression followed by a for clause, then
zero or more for or if clauses. The expressions can be anything, meaning you can
put in all kinds of objects in lists.

```
new_list = [expression(i) for i in old_list if filter(i)]
```

```
[ expression for item in list if conditional ]
```
is eqivalent to 
```
for item in list:
    if conditional:
        expression
```

another example
```
squares = [x**2 for x in range(10)]

print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

#### Show the first letter of each word
We will take the first letter of each word and make a list out of it.
```
listOfWords = ["this","is","a","list","of","words"]

items = [ word[0] for word in listOfWords ]

print items
```
The output should be: [‘t’, ‘i’, ‘a’, ‘l’, ‘o’, ‘w’]
