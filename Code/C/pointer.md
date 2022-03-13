# Pointer

Pointer zu andere Variable

```c
float *f;
f = &boat;

// oder verkürzt

float *f = &boat;
```

Pointer zu Data

```c
char *a = 'X';
```

## Array = Pointer

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

```c
int c[] = {5};

printf(*c) oder printf(c[0])
```

### Argv, Argc

```c
int main(int argc, char const *argv[]) {

// *argv[] == **argv    
// mehrere Zeichenketten als Parameter möglich
```

### Print String

```c
char *string = "Hallo";

printf("%s\n", string);     

// ohne "*" bei string, da der gesamte String ausgebenen werden soll und nicht nur das erste Zeichen
```

<https://stackoverflow.com/questions/859634/c-pointer-to-array-array-of-pointers-disambiguation>

<https://cdecl.org/>
