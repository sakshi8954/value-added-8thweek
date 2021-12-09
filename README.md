#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
    int prime(int num)
    {
         int count=0;
         for(int i=1;i<=num/2;i++){
             if(num%i==0)
                 count++;
         }      
        if(count==1)
            return 1;
         else
        return 0;
    }
    int main() {
        int t;
        scanf("%d",&t);
        while(t--){
            int rev=0;
            int n;
            scanf("%d",&n);
            for(int i=2;i<=n;i++){
                if((prime(i)==1)&&(prime((2*i)+1)==1)){
                    rev=rev+i;
                }
            }
            printf("%d\n",rev);
            
    }
 
    
    return 0;
}
