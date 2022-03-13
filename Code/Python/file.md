# Open files

```python
try:
    with open("app.py") as file, open("another.txt") as config:
        print("file opended")
    # python will close these file automatically whenn programm crashed. No finally needed
```
