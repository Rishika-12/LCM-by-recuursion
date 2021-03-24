# LCM-by-recuursion
#include <stdio.h>

int main()
{
    printf("Enter a & b:\n");
    int a,b,lcm;
    scanf("%d %d",&a,&b);
    lcm=find_lcm(a,b);
    printf("The lcm of %d and %d is %d",a,b,lcm);
    return 0;
}
int find_lcm(int x, int y){
    static int temp=1;
    if(temp%x==0 && temp%y==0){
        return temp;
    }
    else{
        temp++;
        find_lcm(x,y);
        return temp;
    }
}
