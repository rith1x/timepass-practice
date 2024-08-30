# Armstrong Number

```c
// Online C compiler to run C program online
#include <stdio.h>
int isArmstrong(int n){
    int cpy = n;
    int len = 0;
    while (n!=0){
        len++;
        n/=10;
    }
    int x=cpy;
    int val = 0;
    
    while (x!=0){
        int acc = 1;
        for(int i=0; i<len; i++){
            acc*=x%10;
        }
        val+=acc;
        x/=10;
    }
    return val == cpy ? 1 : 0;
}
int main() {
    int n;
    scanf("%d",&n);
    int s = isArmstrong(n);
    if(s)
    printf("Yes");
    else
    printf("No");
    return 0;
}

```
