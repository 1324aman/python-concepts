## str vs repr
- str returns more readable string representation of the object.
- repr returns the object representation in string format and can be used to reconstruct the object.
```
import datetime
now = datetime.datetime.now()
now.__str__()
'2020-12-27 22:28:00.324317'
```
```
now.__repr__()
'datetime.datetime(2020, 12, 27, 22, 28, 0, 324317)'

repr method can be used to reconstruct the object using eval method

print(eval(repr(now)))
datetime.datetime(2020, 12, 27, 22, 28, 0, 324317)
```
