
``` c

#include <stdio.h>
int main()
{
    int a,b;
    scanf("%d %d", &a, &b);

    while(a != 0) {
        int rem = b % a;
        b = a;
        a = rem;
    }
    printf("%d\n", b);
    return 0; 
}

/*
euclid algorithm ->

    a       b       reminder
    30      42      b % a == 12
    12      30      b % a == 6
    6       12      b % a == 0

    euclid algorithm -> C Programing Implement

    while(a != 0) {

        int rem = b % a;
        b = a;
        a = rem;

    }

    // How to Working Euclid Algorithm 

    input: a = 30, b = 42;

    step : 1
    _______________________________________________

    rem = b % a (12) ;
    b = a (30);
    a = rem (12);
    loop: a != 0 (true)
     _________________________________________________

     step : 2
    _______________________________________________

    rem = b % a (6) ;
    b = a (12);
    a = rem (6);
    loop : a != 0 (true)
     _________________________________________________

     step : 3
    _______________________________________________
    
    rem = b % a (0) ;
    b = a (6);
    a = rem (0);
    loop: a != 0 (false) -> loop Stop

     _________________________________________________

     Output : printf("%d",b); (6)
*/
```
