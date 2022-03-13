### Exceptions

```python
print("Starting ...")
try:
    age = int(input("Enter age: "))
    
except ValueError:
    print("not valid age")
    
else:
    print("That's perfect!")
# else block will only be activated when try is complete pass through (with no exceptions!)
    
finally:
    print("Disconnect from Server")

print("Bumm")
```
