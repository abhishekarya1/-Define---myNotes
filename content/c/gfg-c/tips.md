+++
title = "Useful Stuff"
date =  2019-01-27T22:27:43+05:30
weight = 1
+++

- **After the pre-processing is over, all the undefined macros are initialized with default value 0**.

### Inline Functions in C

```c
inline int square(int x) { return x*x; } 
int main() 
{ 
int x = 36/square(6); 
printf("%d", x); 
return 0; 
} 

// OUTPUT: 1 
```
- A `.i` file is generated after pre-processing of a C program.

- What is the use of `#pragma once`?

Used in a header file to avoid its inclusion more than once.

### An Interesting Case

```c
#include<stdio.h>
#define A -B
#define B -C
#define C 5

int main()
{
  printf("The value of A is %d\n", A); 
  return 0;
} 
```

Preprocessed File - 

```c


int main()
{
  printf("The value of A is %d\n", - -5);
  return 0;
}

```

**OUTPUT: 5**

-   The translator which performs macro calls expansion is called **Macro pre - processor**.
	- A **Macro processor** is a program that copies a stream of text from one place to another, making a systematic set of replacements as it does so.
	- A **Dynamic linker** is the part of an operating system that loads and links the shared libraries.
	- The C preprocessor is a micro processor that is used by compiler to transform your code before compilation. It is called **micro pre-processor** because it allows us to add macros.

### Line Splicing in C/C++

Lines terminated by a single `/` are spliced together with the next line very early in the process of translation.

```c
// C program to illustrate the concept of Line splicing. 
#include <stdio.h> 
int main() 
{ 
	// Line Splicing\ 
	printf("Hello GFG\n"); 
	printf("welcome"); 
	return (0); 
} 

```
**OUTPUT: welcome**

- Line splicing is used when defining a  macro which contains multiple lines.

```c
#include <stdio.h> 
#define MAX(a, b) \
		if(a>b) \
			printf("%d\n", a);
int main() 
{ 
	MAX(5, 2);
} 
```

**OUTPUT: 5**