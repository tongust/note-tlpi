# About gcc compile cmd
To compile the source file main.c containing *main() func*, you should put all related file together.
It consists of two important components:
- The .h file:
	- It indicates which functions and feilds the main function will use.
- The .c file:
	- It actually defines the function and the varibles. 

## Main code
*./*
_____
```cpp
#include "foo.h"
#include "fqq.h"

/* main code */

int main() 
{
}
```

*../include/foo.h*

```cpp
void foo();
```

*../src/foo.c*
```cpp
void foo() {
	/*Do something*/
	return;
}
```

*../src/fqq.c*
```cpp
void fqq() {
	/*Do something*/
	return;
}
```
The gcc cmd should be
> gcc -o main -I../include/ ../src/foo.c ./main.c 

