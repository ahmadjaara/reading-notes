# List Comprehensions in Python

In order to keep your code elegant and readable, it’s recommended that you use Python’s comprehension features it's a powerful and concise method for creating lists in Python

## Syntax

my_new_list = [ `expression` **for** `item` **in** `list` ]

- you’re going to perform an expression on each item in the list. The expression will determine what item is eventually stored in the output list

Ex:

digits = [x for x in range(10)]
print(digits)
output: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

- here the expresion dont do anything just store the value of x in the range
- you can also add a condition for the x

## Decorators

the decorators are used to modify the behaviour of function or class. In Decorators, functions are taken as the argument into another function and then called inside the wrapper function.

### Syntax for Decorator

    @gfg_decorator
    def hello_decorator():
        print("Gfg")

    '''Above code is equivalent to -

    def hello_decorator():
        print("Gfg")
        
    hello_decorator = gfg_decorator(hello_decorator)'''
