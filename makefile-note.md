# About gcc compile cmd
To compile the source file main.c containing *main() func*, you should put all related file together.
It consists of two important components:
- The .h file:
	- It indicates which functions and feilds the main function will use.
- The .c file:
	- It actually defines the function and the varibles. 

*./main.c*
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

# Simple Makefile

```
CC=gcc
OBJS=csapp.o echo.o select.o
SRC=../src/csapp.c ../netp/echo.c select.c
INCLUDE=../include/ 
CFLAGS=-I$(INCLUDE) -pthread

GEN : $(OBJS)
	$(CC) -o $@ $^ $(CFLAGS)
# secondly execute gcc -o GEN csapp.o echo.o select.o -I../include/  -pthread

$(OBJS) : $(SRC)
	$(CC) -c $^ $(CFLAGS)
# firstly execute: gcc -c ../src/csapp.c ../netp/echo.c select.c -I../include/  -pthread
clean :
	rm -rf *.o
```
