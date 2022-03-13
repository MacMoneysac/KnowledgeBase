# Classes

## Define new Class

```python
class Point:
    default_color = "red"
    
    def __init__(self, x, y):
        self.x = x
        self.y = y
    
    def draw(self):
        print(f"Point ({self.x}, {self.y})")
```

## Factory Method \__init__

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y
    
    @classmethod # decorator
    def zero(cls): # cls -> class, only for convention
        return cls(0,0)
    
point = Point.zero()
```

## Property

### First Option

```python
class Product:
    def __init__(self, price):
        self.set_price(price)
    
    def get_price(self):
        return self.__price
        
    def set_price(self, value):
        if value < 0:
            raise ValueError("Price cannot be negative")
        self.__price = value
        
    price = property(get_price, set_price)
```

## second option

```python
class Product:
    def __init__(self, price):
        self.price = price
        
    @property
    def price(self):
        return self.__price
    
    @price.setter
    def price(self, value):
        if value < 0:
            raise ValueError("Price cannot be negative.")
        self.__price = value
```

## inheritance

```python
class Car(Vehicle):

```

## Data Classes

```python
from collections import namedtuple

Point = namedtuple("Point", ["x", "y"])
p1 = Point(x=1, y=2)

print(p1.x, p1.y)
```
