#include<stdio.h>
int main()
{
   int a=0, b=1, range, c, sum=0;

   printf("Enter the range of Fibonacci series: ");
   scanf("%d",&range);

   printf("The fibonacci series is: \t");
   while( a <= range )
   {
      printf("%d\t",a);
      sum += a;
      c = a + b;
      a = b;
      b = c;
   }

   printf("\nTheir sum is = %d", sum);

   return 0;
}
