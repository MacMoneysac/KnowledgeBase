# binary Search

## Binäre Suche iterativ

```java
public static int getIndex(int[] x, int value){
    int links = 0;
    int rechts = x.length-1;
    
    while (links < rechts){
        int mitte = (links + rechts) /2;
        
        if(x[mitte] == value)
            return mitte;
        
        else if(x[mitte] < value)
            links = mitte +1;
        else
            rechts = mitte -1;
    }
    return -1;
}       
```

## Binäre Suche rekursiv

```java
public static getIndex(int[] x, int value, int links, int rechts){
    if(x == null)
        return -1;
    
    if(rechts < links)
        return -1;
    
    int mitte = (rechts + links)/2;
    if(x[mitte] == value)
        return mitte;
    else if(x[mitte] < value)
        return getIndex(x, value, mitte+1, rechts);
    else
        return getIndex(x, value, links, mitte-1);
}
```

## Selection Sort

```java
public static void selectionSort(double[] a){
    
    for (int i = 0; i < a.length-1; i++){
        int index = i; // char temp = a[i];
        
        for(int j = i + 1; j < a.length; j++){
            if(a[j] < a[index])
                index = j;
        }
        
        if(index != i){
            double temp = a[index];
            a[index] = a[i];
            a[i] = temp;
    
        }
    }
}
```
