#include<stdio.h>
//Program to count most occuring element
int getMaxRepeatingElement(int array[], int n) 
{
    int i, j, maxElement, count;
     int maxCount = 0;
    /* Frequency of each element is counted and checked.If it's greater than the utmost count element we found till now, then it is updated accordingly  */  
    for(i = 0; i< n; i++)   //For loop to hold each element
    {
        count = 1;
        for(j = i+1; j < n; j++)  //For loop to check for duplicate elements
        {
            if(array[j] == array[i])
            {
                count++;     //Increment  count
                /* If count of current element is more than 
                maxCount, then update maxElement */
                if(count > maxCount)
                {
                    maxElement = array[j];
                }
            }
        }
    }
    return maxElement;
}
//Driver Program
int main()
{
    int n;              //Array Size Declaration
    printf("Enter the number of elements ");
    scanf("%d",&n);    
    int array[n];      //Array Declaration
    printf("Enter the array elements");
    for(int i=0;i<n;i++)   //Initializing Array Elements
    {
        scanf("%d",&array[i]);
    } 
    int maxElement = getMaxRepeatingElement(array, n);    //Function call
    printf("\n Maximum Repeating Element : %d",maxElement);   //Prints the most occuring element 
    return 0;
}
