# Astro-Instruments-101




you should remove  my code.
#include <stdio.h>
#include <math.h>
void prnt(int*A,int N)
{
    for(int i=0;i<N;i++)
    {
        A[i]='O'+A[i];
     printf("%c",A[i]);
    }
     printf("\n");
}
int main()
{
    int i,n1,N;
    scanf("%d",&n1);
    N=2*n1;
    int a=0,b=0,n,m,c;
    for(int j=0;j<N;j++)
    {
      if(j%2==0)a=2*a+1;
      else a=2*a+0;
      if(j>=n1)b=b+pow(2,j);
    }
    n=pow(2,N-1);
    //printf("%d %d %d\n",a,b,n);
    for(;a<=b;a++)
    {
        c=a;m=n;
        int c1=0,c2=0,A[N],f=0;
      for(i=0;i<N;i++)
      {
       A[i]=c/m;
       c=c%m;m=m/2;
       if(A[i]==1){c1++;}
       if(A[i]==0){c2++;}
       if(c2>c1){f=1;break; }
      }
      if(f==1 ||c1>n1 || c2>n1){ continue; }
      else prnt(A,N);
     
    }
    return 0;
} 
