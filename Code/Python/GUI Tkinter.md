# GUI TKinter

## General

```python
from tkinter import *
root = Tk()
...
root.mainloop()
```

```python
root.title("Fanstatisches Fenster")
root.minsize(width=300, height=300)

```

## Widgets

### Labels

```python
l = Label(root, text="Schnauze", borderwith=3)
```

### Buttons

```python
b = Button(root, text="Launch", command = myClick)
```

### Text Field

```python
e = Entry(root, width = 50)
e.insert(0, "Enter target: ")
```

### Command

```python
def myClick:
    greeting = "Hello " + e.get()
    
```

## Layout Management

### Pack

```python

```

### Grid

```python
something.grid(row=0, column=0, columnspan=3, padx=0, pady=0)
```

### Place

```python

```

## Websites

API:
<http://www.tcl.tk/man/tcl8.5/TkCmd/contents.htm>

Python Docs: <https://docs.python.org/3/library/tkinter.html>

German:
<https://www.python-kurs.eu/python_tkinter.php>

Effbot: <https://effbot.org/tkinterbook/grid.htm>

More Tutorials: <https://wiki.python.org/moin/TkInter>
