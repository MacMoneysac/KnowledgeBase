# Lists

## Declaration

### bei bestimmten Datentypen

```java
public class SLLInt {
    public int value;
    public SLLInt next;

    public SLLInt(int value, SLLInt next){
        this.value = value;
        this.next = next;
    }

    public SLLInt(int value){
        this.value = value;
        this.next = null;
    }
}
```

### bei beliebigen Datentypen

```java
public class SLL {
    public Object value;
    public SLL next;
  
    SLL(Object value, SLL next) {
        this.value = value;
        this.next = next; 
    }
}
```

### Kurzschreibweise

```java
public class SLL<E> { 
    SLL.java E value;
    SLL<E> next;
    SLL(E value, SLL<E> next) {
        this.value = value;
        this.next = next; 
    }
}
```

### Toolbox

```java
    // Bei Listen können nur die nachfolgenden Objekte abgerufen werden
    
    
    // Vorne anfügen - neues Kettenglied
    
    head = new SLL(elememt, head)


    // Erstes Element entferen
    
    head = head.next
    
    
    // tail: wenn das Ende abgerufen werden soll (head.next.next...)
    
    if(head == null){
    
        head = new SLL(element, head); //head ist null
        tail = head;
        
    } else {
    
        tail.next = new SLL(element, null);
        tail = tail.next;
        
    }
```

### in der Mitte entfernen

```java

        // Rekursiv: neue Liste erzeugen
            
            
public static SLLChar removeRekursiv(SLLChar list, char delete){
    if(list == null){
        return null
    }
    
    else if(list.value == delete){
        return removeRekursiv(list.next, delete) //?
    }
    
    else {
        return new SLLChar(
            list.value, removeRekursiv(next.element, delete)
        ) //?, Problem wird nach hinten verschoben
    }
}
```

```java
        // Iterativ: Liste muss verändert werden
            
public static SLLChar removeIterativ(SLLChar list, char delete){

    SLLChar head = null;  //head als Rückgabewert
    SLLChar tail = null;
    
    while(list != null){            // list als Durchlaufvariable
    
        if(list.value != delete){       // nicht löschen
            SLLChar neu = new SLLChar(list.value, null);        // "neu" als temporäre SLL, warum null??
            
            if(head == null){
                head = neu;
                tail = neu;
            }
            
            else{       // löschen
                tail.next = neu;
                tail = tail.next;
            }
            
        }
        list = list.next;
        
    }
    return head;
}
```
