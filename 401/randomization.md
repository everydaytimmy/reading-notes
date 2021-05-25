## Random Module

```
import random
print random.randint(0, 5)
```


If you want a larger number
For example, a random number between 0 and 100:

```
import random
random.random() * 100

```

Generate a random value from the sequence sequence.

```
random.choice( ['red', 'black', 'green'] ).
```

The choice function can often be used for choosing a random element from a list.

```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```

The shuffle function, shuffles the elements in list in place, so they are in a random order.

```
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)

```

#### Randrange
Generate a randomly selected element from range(start, stop, step)

```
random.randrange(start, stop[, step])
```

```
import random
for i in range(3):
    print random.randrange(0, 101, 5)
```

### Risk Analysis

List of possible risks:

1) Use of new hardware
2) Use of new technology
3) Use of new automation tool
4) The sequence of code
5) Availability of test resources for the application
