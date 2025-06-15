# 5 Tips To Organize Python Code

## 1. Use Modules and Packages

A **Module** is a individual python file
A **Package** is a directory containing multiple python modules

Packages have \__init__.py inside the directory!

> Don't be afraid of **separating your code our**!

### imports

Run main.py command: ```python '.\videos\003-2025-06-14-5 Tips To Organize Python Code\code\main.py'```

When imported, the \__init__.py file will be called once.
Initialization code can be written in the \__init__.py!

#### Example 1 - Import Package

main.py
```python
import physics
```

physics/\__init__.py
```python
print("Hello world")
```

RUN python main.py:
```
Hello world
```

> When physics is imported in main.py, the \__init__.py prints "Hello world""

#### Example 2 - Wrong Package Import 

main.py
```python
from physics import Forces
```

physics/\__init__.py
```python
print("Hello world")
```

RUN python main.py:
```
ImportError: cannot import name 'Forces' from 'physics'
```

> physics package do not know Forces, because Forces is inside forces.py module!


#### Example 2.1 - Wrong Package Import RESOLVED

main.py
```python
from physics import Forces
```

physics/\__init__.py
```python
from .forces import Forces
print("Hello world")
```

RUN python main.py:
```
Hello world
```

> physics \__init__.py imports Forces from forces.py module using relative imports (.forces). Letting physics package know that Forces exists

## 2. One class = One file

Use that for Object Oriented projects.

Follow best practice:
* **file name in snake_case**
* **class in PascalCase**

# 3. Group related functionality togheter

Use src, docs, tests, utils...

Unrelated to the main project functionalities files can be under the root.

Good to have a cli.md to show how to run the code.

Example: [Tech-With-Tm/api](https://github.com/Tech-With-Tim/API)
![Alt text](images\image.png)

# 4. Separate Utility & Helper Functions

put in a module or file all the functions that don't belong in a class.

Examples:
* Converting a time variable to another format
* Funcitons that are used in multiple classes

# 5. Organize imports

Use:
> 1. **Third-party imports**
> 2. **Built in imports**
> 3. **Local files or relative imports** 
> 
> Order the imports in each group alphabetically

