---
title: Reference and Array Sorting Algorithms
date: 2018-06-03
---

### Pass by Reference 

```
void myswap(int &n1, int &n2) //formal parameters			/*Called Function		 Pass by Reference*/
{
	int temp=n1;
	n1=n2;
	n2=temp;
}

int main()								// Calling Function
{
	int a,b;
	cin>>a>>b;
	myswap(a,b);	//arguments or actual parameters		// Function call independent of pass method
	cout<<a<<" "<<b;

}	
```
	
	
>	- **Pass by Value** - New variables are created											
>  	- **Pass by Reference**	- New variables are _not_ created, new names are given to the existing _variables_.


### Algorithms
 	
 	1. Sorting an Array
 		a. Bubble Sort
 		b. Insertion Sort
 		c. Selection Sort