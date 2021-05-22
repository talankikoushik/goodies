#include <stdio.h>

int main()
{
    int n;
    
   
   char* a[10]={"Fitbit Plus: 7980","IPods: 22349","MI Band: 999","Cult Pass: 2799","Macbook Pro:229900","Digital Camera: 11101","Alexa: 9999","SandwichToaster: 2195","Microwave Oven: 9800","Scale: 4999"};
   printf("number of employees:");
   scanf("%d",&n);
   int b[10]={7980,22349,999,2799,229900,11101,9999,2195,9800,4999};
   int d[10];
   
    printf(" Here the goodies that are selected for distribution are:");
    int c[n];
    
   for(int i=0;i<n;i++)
   {
    scanf("%d ",&c[i]);
   }
   for(int i=0;i<n;i++)
   {
       printf("%s ",a[c[i]]);
   }
   int k=0;
   for(int i=0;i<n;i++)
   {
       for(int j=i+1;j<n;j++)
       {
    
       
       if(b[c[i]]<b[c[j]])
       {
           int t;
           t=b[c[i]];
           b[c[i]]=b[c[j]];
           b[c[j]]=t;
       }
       
       
       }
       d[k]=b[c[i]];
       k++;
       
   }
   int s=d[0]-d[k-1];
   printf("And the difference between the chosen goodie with highest price and the lowest price is %d",s
    return 0;
}
