# Python Scope:
scope rules teall you how variables and names are looked up in your code. It determines the visibility of a variable within the code. The scope of a name or variable depends on the place in your code where you create that variable.

## scope
Most commonly, you’ll distinguish two general scopes :

- Global scope: The names that you define in this scope are available to all your code.

- Local scope: The names that you define in this scope are only available or visible to the code within the scope.

## Using the LEGB Rule for Python Scope

LEGB rule is a kind of name lookup procedure, which determines the order in which Python looks up names,
if you reference a given name, then Python will look that name up sequentially in the local, enclosing, global, and built-in scope

- `Local` (or function) scope is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. 

- `Enclosing` (or nonlocal) This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

- `Global` (or module)  This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.

- `Built-in` scope  This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.

# Big o
Big O notation describes the complexity of your code using algebraic terms.
![big o](/pic/bigo2.jpeg "1")