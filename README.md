# SecondLargestElementInAnArray
Includes Finding Second Largest Element In An Array
#include<stdio.h>

int main(){
int numbers[100];
int i;
int n;
int max;
int min;
int smax;
int temp;
printf("enter number of elements:");
scanf("%d", &n);
for(int i=0;i<n;i++){
printf("enter elements%d:", i+1);
scanf("%d", &numbers[i]);
}
if(numbers[0]>numbers[1])
{
max=numbers[0];
smax=numbers[1];}
else{
max=numbers[1];
smax=numbers[0];}

for(int i=2;i<n;i++){
if((numbers[i]>max) && (numbers[i]>smax)){
temp=max;
max=numbers[i];
smax=temp;
}
else{
if(numbers[i]>smax){
smax=numbers[i];
}
}
}

printf("maximum=%d",max);
printf("second max %d", smax);
return 0;
}
