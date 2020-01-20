#include<stdio.h>
#include<math.h>

#define k_max 5

long long fact(long x) {
if(x == 0)
return 1;

long long res = x;
while(--x > 1) {
res *= x;
}

return res;
}

double _cos(double x) {
x *= -1;
double eit = 0;
for(int k = 0; k < k_max; k++) {
double eres = (pow(-1,k)*pow(x,k))/fact(2*k);
eit += eres;

if(k == k_max - 2)
printf("Iepriekspedejais: %.24lf\n", eres);
else if(k == k_max - 1)                                                                                                 
printf("Pedejais: %.24lf\n", eres);                                                                                     
}

return eit;
}

void main() {
double x;
printf("Ievadiet x ");
scanf("%lf", &x);
x = sqrt(x);
printf(
"                          500  " "\n"
"                         ----- " "\n"
"                          \\   " "\n"
"                           \\    "      " (-1)^k * x^k      " "\n"
" cos((sqrt)x) =           = >   "    " -----------------  "  "\n"
"                          /      "      "   (2*k)!          " "\n"
"                         /    " "\n"
"                         ----- " "\n"
"                          k=0  " "\n"
"" "\n"
"" "\n"
"\n");

printf("C    cos(%lf) = %lf\n\n", x, cos(x));
printf("Mans cos(%lf) = %lf\n", x, _cos(x));
}
