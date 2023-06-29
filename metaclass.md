- In Python, the `object` class is the base class for all other classes. It is the ultimate parent class from which all classes inherit by default.
- A metaclass is the class of the class.
- python has built-in type metaclass.
- Metaclasses provide a way to customize the creation and behavior of class objects.
- Every class is an instance of its metaclass.
- If we don't specify the metaclass for our class, then default metaclass will be `type`.
`type(classname, superclasses, attributes)`

#### type is also a function in python
```
type(classname, superclasses, attributes)
```

#### Custom meta class in python

```
class MyMetaclass(type):
    def __init__(cls, name, bases, attrs):
        print(f"Creating class {name} using MyMetaclass")

class MyClass(metaclass=MyMetaclass):
    pass
```

- To customize the creation of objects using a metaclass in Python, you can override the __call__() method in the metaclass. The __call__() method is invoked when an instance of a class is created.
```
  class CustomMeta(type):
    def __call__(cls, *args, **kwargs):
        # Custom logic before object creation
        print("Before object creation")

        # Create the object
        obj = super().__call__(*args, **kwargs)

        # Custom logic after object creation
        print("After object creation")

        return obj


class MyClass(metaclass=CustomMeta):
    def __init__(self, value):
        self.value = value


obj = MyClass(10)
# Output
# Before object creation
# After object creation
```
#### The execution order of methods when an instance of a class is created.
__call__ => __new__ => __init__
- call method creates the object
- new method allocates the memory
- init method initialises the object.





 
