### Learning Objectives for the Week

1. **Student will be able to design and implement Python classes that use object-oriented principles such as inheritance, encapsulation, and polymorphism.**
2. **Student will be able to apply and understand the concept of method overriding and how it is used in subclassing to extend or modify behavior of parent classes.**
3. **Student will be able to explain and implement polymorphism and duck typing to make their code more modular and flexible.**
4. **Student will be able to utilize magic methods to customize object behavior, such as overloading operators and defining custom string representations.**
5. **Student will be able to differentiate between inheritance, composition, and aggregation, and apply them appropriately in Python class design.**
6. **Student will be able to use dataclasses and named tuples to efficiently handle simple data structures in Python.**

---

### Questions to Assess Understanding (with Answers)

1. **What is the difference between inheritance and composition in object-oriented design? Provide an example of when you would use one over the other.**

   - **Answer**: Inheritance creates an "is-a" relationship between classes (e.g., a `Dog` is an `Animal`), where a subclass inherits attributes and methods from a parent class. Composition, on the other hand, creates a "has-a" relationship (e.g., a `Car` has an `Engine`), where an object contains other objects as parts of its structure. Inheritance is used when you want to extend or modify the behavior of a base class, while composition is used when objects are built by combining simpler objects.

2. **How does polymorphism contribute to code flexibility in Python? Provide an example.**

   - **Answer**: Polymorphism allows different classes to be used interchangeably if they share the same interface, enabling flexible and reusable code. For example, if two classes `Dog` and `Cat` both implement a `speak()` method, we can use them interchangeably in a function that calls `speak()` on an object, without needing to know the object's specific class.

3. **What is method overriding, and why is it useful in subclassing? Provide an example.**

   - **Answer**: Method overriding allows a subclass to provide a specific implementation of a method that is already defined in its parent class. This is useful when the subclass needs to alter or extend the functionality of the parent class's method. For example, a parent class `Animal` may have a `move()` method, and a subclass `Bird` can override this method to provide flying behavior, rather than the default walking behavior.

4. **What is duck typing, and how does it differ from traditional polymorphism in Python?**

   - **Answer**: Duck typing is a concept in Python where an object's suitability for use is determined by the presence of certain methods and properties, rather than the object's class type. The phrase "if it looks like a duck and quacks like a duck, it's a duck" summarizes the idea. Traditional polymorphism often relies on class hierarchies, while duck typing focuses on behavior. For example, if an object has a `speak()` method, it can be used in a context that expects any object with a `speak()` method, regardless of its class.

5. **Explain the purpose of magic methods in Python. Provide an example of how you would use `__eq__` and `__repr__` in a class.**

   - **Answer**: Magic methods in Python (also called dunder methods) allow customization of built-in behavior for objects, such as how they respond to operators or how they are represented as strings. For example, `__eq__` is used to define equality behavior between objects:
     ```python
     class Point:
         def __init__(self, x, y):
             self.x = x
             self.y = y
         def __eq__(self, other):
             return self.x == other.x and self.y == other.y
         def __repr__(self):
             return f"Point({self.x}, {self.y})"
     ```
     Here, `__eq__` allows comparing two `Point` objects based on their coordinates, and `__repr__` defines how the object is printed.

6. **What are the benefits of using dataclasses in Python? Provide a simple example.**

   - **Answer**: Dataclasses reduce the amount of boilerplate code needed for simple classes that primarily store data, automatically generating methods like `__init__`, `__repr__`, and `__eq__`. For example:
     ```python
     from dataclasses import dataclass
     @dataclass
     class Person:
         name: str
         age: int
     ```
     This automatically generates an initializer, a string representation, and equality comparison based on the `name` and `age` attributes.

7. **What is the significance of properties in Python? How do they contribute to encapsulation?**

   - **Answer**: Properties in Python allow for controlled access to instance attributes by defining getter, setter, and deleter methods, without changing the interface of the class. This helps maintain encapsulation by controlling how attributes are accessed or modified, while still allowing external code to interact with them as if they were normal attributes. For example:
     ```python
     class Temperature:
         def __init__(self, celsius):
             self._celsius = celsius
         @property
         def celsius(self):
             return self._celsius
         @celsius.setter
         def celsius(self, value):
             if value < -273.15:
                 raise ValueError("Temperature below -273.15 is not possible")
             self._celsius = value
     ```

8. **In Python, when would you use a static method over a class method? Provide an example of each.**

   - **Answer**: A static method is used when a method does not need to access or modify instance or class state, while a class method operates on the class itself rather than instances. A static method is typically used for utility functions related to the class, whereas a class method often serves as an alternative constructor. Example:
     ```python
     class Math:
         @staticmethod
         def add(a, b):
             return a + b
         @classmethod
         def from_string(cls, s):
             a, b = map(int, s.split(","))
             return cls.add(a, b)
     ```
     Here, `add()` is a static method for addition, while `from_string()` is a class method for creating an object from a string input.