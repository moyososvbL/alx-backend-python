In Python, variable annotations allow you to provide additional type information about variables. Variable annotations were introduced in Python 3.6 as a way to add type hints to your code without affecting the runtime behavior. Here's an example of how you can use variable annotations in Python:

```python
# Variable annotation
name: str = "John"

# Multiple variable annotations
age: int = 30
height: float = 175.5

# Annotations can be used with different data types
is_student: bool = True
grades: List[float] = [85.5, 90.0, 78.5]

# Annotations can also be used with custom classes
class Person:
    pass

    person: Person = Person()
    ```

    In the above example, the variables `name`, `age`, `height`, `is_student`, and `grades` have type annotations assigned to them. These annotations provide information about the expected types of the variables.

    It's important to note that variable annotations in Python are optional and do not enforce any type checking at runtime. They serve as a form of documentation and can be used by static type checkers and linters, such as `mypy`, to analyze your code for potential type errors.

    Variable annotations are stored as metadata in the `__annotations__` dictionary of the module or function where they are defined. You can access this dictionary to retrieve the annotations programmatically, like this:

    ```python
    print(__annotations__)
    # Output: {'name': <class 'str'>, 'age': <class 'int'>, 'height': <class 'float'>, 'is_student': <class 'bool'>, 'grades': typing.List[float]}
    ```

    Note that variable annotations do not affect the actual runtime behavior of your code. They are purely informational and can be used by external tools or static type checkers to analyze your code for potential type errors.
