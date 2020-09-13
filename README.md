#include<stdio.h>
#include<stdlib.h>
int maximum_sum(int *arr,int n)
{
    int i,max=arr[0],current_max=0;
    for(i=0;i<n;i++)
    {
        current_max+=arr[i];
        if(max<current_max)
            max=current_max;
        else if(current_max<0)
            current_max=0;
    }
    return max;
}
int main()
{
    int n,i;
    scanf("%d",&n);
    int *arr=(int *)malloc(n*sizeof(int));
    for(i=0;i<n;i++)
        scanf("%d",&arr[i]);
    printf("%d",maximum_sum(arr,n));
}
