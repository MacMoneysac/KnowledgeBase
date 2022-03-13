# Strings

kann man auf zwei Arten erzeugen: Feld, oder Pointer auf Feld. Ein Feld ist ein auch ein Pointer

Der Pointer selbst ist im Stack, während der Inhalt des Pointers im Heap ist.

```c
char *b = "Hallo";
 // ohne * ungültige Eingabe 
```

will place "Hallo" as an **array** in the read-only parts of the memory (const, because it isn't stored in a variable)

b is a pointer to that will make any writing operation on this memory illegal.

```c
// change content
b = "Tschüss";
// der Zeiger (Memory Address) kann geändert werden (auf anderen String)
b = s + 3;
```

```c
// DO NOT
b = "Tschüss";
b[2] = 'e';     

// es zeigt auf einen Array mit const content

```

```c

// ONLY WHEN
b = a;
b[0] = '\n';    

// a ist kein const array


```

```c
  char a[] = "AVENGERS";
  
  char *ptr_a;
  ptr_a = a;
```

a ist die "Memory Address" vom ersten Zeichen;

```c
    a[0]    == A
    *a      == A
    
    *(a+1)  == V
    a[1]    == V
    
    *ptr_a  == A
```

## Array

Jedes Feld ist ein Pointer

```c
char a[x] = {'A', 'V', 'E', 'N', 'G', 'E', 'R', '\0'} 
// only init once

char a[] = "AVENGERS";
char a[32];
```

Die Größe muss festgelegt werden

puts the literal string "`AVENERGS`" in read-only part of the memory and **copies** the string to newly allocated memory on the stack. Thus making that legal:

```c
// change content
a[2] = 'A';
```

```c
// DO NOT RENAME
a = "DC COMICS"; // only init once
a = a + 3;
