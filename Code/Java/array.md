# Array

## Initialize Array

```java

int[] myIntArray = new int[3];
int[] myIntArray = {1, 2, 3};
int[] myIntArray = new int[]{1, 2, 3};

```

## Strings

```java

String[] myStringArray = new String[3];
String[] myStringArray = {"a", "b", "c"};
String[] myStringArray = new String[]{"a", "b", "c"};

```

### getMaximum

```java
public static double getMaximum(double[] a){
    double max = a[0];
    for(int i = 0; i < a.length; i++){
        max = (a[i] > max) ? a[i] : max;
    }
    return max;
}
```