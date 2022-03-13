# Stack implementations

## StackByArray

```java
public class StackByArray{

    private Object elements = new Object[Zahl];
    private int pegel = 0;
    
    public void push(Object value){
        elements[pegel++] = value;
    }
    
    public Object pop(){
        Object speicher = elements[pegel-1];
        elements[pegel-1] = null;
        pegel--;
        return speicher;
    }
    
    public Object peek(){
        return elements[pegel-1];
    }
    
    public boolean isEmpty(){
        return pegel == 0;
    }
}
```

## StackByList

```java
public class StackByList{

    private SLL head = null;
    
    public void push(Object value){
        head = new SLL(value, head);
    }
    
    public Object pop(){
        Object speicher = head.value;
        head = head.next;
        return speicher;
    }
    
    public Object peek(){
        return head.value;
    }
    
    public boolean isEmpty(){
        return head == null;
    }
}
```

## QueueByList

```java
    public class QueueByList{
        private SLL head = null;
        private SLL tail = null;
        
        public void enqueue (Object element){
            if(head == null){
                head = new SLL(element, head) //head ist null
                tail = head;
            } else {
                tail.next = new SLL(element, null);
                tail = tail.next;
            }
        }
        
        public Object deq(){
            Object r = head.value;
            head = head.next;
            return r;
        }
        
        public Object first(){
            return head.value;
        }
        
        public boolean isEmpty(){
            return (head == null); 
        }
    }

```

## toInfix

```java
public static String toInfix(String postfix){
    StackBy... stack = new StackBy...(){
        while(!postfix.isEmpty())
            char c = postfix.charAt(0);
            
            switch(c){
                case '+': \n 
                case '-': \n
                case '*': \n
                case '/': 
                    String second = (String) stack.pop();
                    String first = (String) stack.pop();
                    String result = "(" + first + c + second + ")";
                    stack.push(result);
                    postfix = postfix.substring(1);
                    break;
                
                default:
                    int indexSep = postfix.indexOf('|');
                    String zahl = postfix.substring(0, indexSep);
                    stack.push(zahl);
                    postfix = postfix.substring(indexSep +1);
            }
        }
    }
    return (String) stack.pop();
}
```

## toPrefix

```java
public static String toPrefix(String postfix){

    // siehe postfix
    
    case '/':
        String result = c + first + second;
    
    default:
        String zahl = postfix.substring(0, indexSep+1);
}
```
