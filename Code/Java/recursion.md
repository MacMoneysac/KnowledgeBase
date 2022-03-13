# Recursion

```java
public static int fact(int n){

    // Abbruchbedingung
    if(n <= 1){
        return 1;
    } 
    
    // Selbstaufruf
    else{
        return fact(n - 1) * n;
    }
}

```
