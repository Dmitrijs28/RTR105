```python
#include<stdio.h>
#include<math.h>
void main(){


 double a, b, c, x,deltax, A, B, X;
 int k;

         printf("Ievadiet vertibu a:");
         scanf("%lf", &a);
         printf("\nIevadiet vertibu b:");
         scanf("%lf", &b);
         printf("\nIevadiet vertibu c:");
         scanf("%lf", &c);
         printf("\nIevadiet precizitati:");
         scanf("%lf", &deltax);

         A = cos(sqrt(a));
         B = cos(sqrt(b));

         if((A * B)>0){
                 printf("intervalaa [%lf;%lf] cos(sqrt(x)) funkcijai nav saknu", a, b);
                }

        for(k=0;(b-a)>deltax;k++){
                x=(a+b)/2.;
        if(A*(cos(sqrt(x))-c)>0) a = x;
        else b = x;
        }
        printf("x funkcijai cos(sqrt(x))=%lf ir %lf\n", c, x);
        printf("cos(sqrt(%lf))=%lf\n", x, cos(sqrt(x)));
        printf("iterācijas lai atrastu x:%d\n",(k+1));
        }
 ```
