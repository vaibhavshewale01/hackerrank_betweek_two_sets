// C program for hackerrank_Subarray_Division

#include<stdio.h>

int main()
{
    int n,i,d,m,j;
    scanf("%d",&n);
    int s[n];
    for(i=0;i<n;i++)
    {
        scanf("%d",&s[i]);
    }
    scanf("%d",&d);
    scanf("%d",&m);
    int sum=0,flag=0,k;
        for(i=0;i<n;i++)
        {
            k=i;
            for(j=0;j<m;j++)
            {
                sum = sum + s[k];
                k++;
            }
            if(sum==d)
            {
                flag++;
            }
            sum=0;
        }
        printf("%d",flag);
        return 0;
}

