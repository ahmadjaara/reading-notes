# class 4

## OOP

Objects are an encapsulation of variables and functions into a single entity.
Objects get their variables and functions from classes. Classes are essentially a template to create your objects.
init()

The __init__() function, is a special function that is called when the class is being initiated. It's used for asigning values in a class.

A recursive function is a function defined in terms of itself via self-referential expressions.

## pytest

### Fixtures

You'll want to have some objects available to all of your tests. Those objects might contain data you want to share across tests, or they might involve the network or filesystem. These are often known as "fixtures" in the testing world, and they take a variety of different forms.
you define fixtures using a combination of the `pytest.fixture` decorator

### Coverage

let's say you've written five functions, and that you've written tests for all of them. Can you be sure you've actually tested all of the possible paths through those functions
That where you want to have "code coverage", checking that your tests have run all of the code

## recursive function

function that continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: `base case` and `recursive case`

Each recursive call adds a stack frame (containing its execution context) to the call stack until we reach the base case. Then, the stack begins to unwind as each call returns its results
