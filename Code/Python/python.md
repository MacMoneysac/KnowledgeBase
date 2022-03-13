# Python Basics

## For Loops

```python
for x in range(5):
    print(x)
    if x == 1:
        break
else:
    print("else-breakpoint passed!")
# else block will only be activated when for-loop is completed (with no break!)

print("Terminate")
    
```

## Define Functions

```python
def calculate_xfact(age):
    if age < 1:
        raise ValueError("Age cannot be 0 or less)
    
```

Note: Only raise exception, when necessary. It's take 4 times longer than usual.

## Main Function

```python
    if __name__ == "__main__":
```
