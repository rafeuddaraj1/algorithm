# Prime Number Algorithm 

__Algorithm__
______
```txt 
 
Step 1: Read number X in any integer variable, let that variable is “NumX”. 
Step 2: Read second number y in another integer variable let say “NumY”. 
Step 3: Finding prime number between NumX and NumY: In order to find all the prime number present between two number NumX and NumY , we need to run a nested loop along with if statement as follows: 
   Step 3.1) Run a loop from Index = NumX to Index <= NumY 
       step 3.2) Run a nested loop from Index_1 = 2 to Index_1< Index 
                step 3.3) check if Index % Index_1 == 0, then 
							set Flag = 0 and break the loop 3.3 
				    But if condition is not true, then set Flag = 1. 
				End of step 3.3 
		End of step 3.2 
		check if Flag == 1 , then print “Prime Number is ”, Index; 
	End of step 3.1 
Step 4: End. 
```

__impalement c program__

```c
// C program to find prime number between two number X and Y 
// Rafe Uddaraj 
#include<stdio.h> 
int main() 
{ 
    int NumX, NumY, Flag =0;  //to store two number 
    int i,j; // for running nested loop 
 
    printf("Enter two number :\n"); 
    scanf("%d%d",&NumX,&NumY); 
 
    for(i=NumX; i<=NumY;i++) 
    { 
        for(j=2;j<i;j++) 
        { 
            if(i%j == 0) 
            { 
                Flag = 0; 
                break; 
            } 
            Flag = 1; 
        } 
        if(Flag == 1) 
            printf("Prime number: %d\n",i); 
    } 
 
} 
```