# Classes

```java


public class Point {
    int x, int y;

    // Class Method
    public int[] draw() {
        int[] output = [x, y]
        return output;
    }

    // Constructor
    public Point(int x, int y) {
        this.x = x;
        this.y = y;
    }
}


public static void main() {

    Point A = new Point(1, 2);
}
```

## Zugriffrechte

```text
static:     Klassen oder Objektbezogen

public:     jeder kann darauf zugreifen
private:     nur in der Klasse
protected:    nur selbst und die "Unterklassen", stay away, it's confusing "Mosh"

"nothing":    package private, nur im package zugreifbar

final:      nicht veränderbar

```

## Abstract Classes

You want to share code among several closely related classes.

## Interfaces

You expect that unrelated classes would implement your interface. For example, the interfaces Comparable and Cloneable are implemented by many unrelated class
