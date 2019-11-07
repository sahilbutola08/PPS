# **PPS ASSIGNMENT**
---

#### _Submitted By : Sahil Butola_
#### _Submitted To : Mrs. Jasmine Kaur_
 
---
 ## 1. Write a Program to add two numbers.

```c
#include<stdio.h>

int main()
{
	int num1,num2,sum;
	printf("Enter the first number : ");
	scanf("%d",&num1);
	printf("\nEnter the second number : ");
	scanf("%d",&num2);
	sum=num1+num2;
	printf("\nSum of the two number is %d\n",sum);
	return 0;
}
 ```
  
  #### Output : 
    Enter the first number : 5
    Enter the seconf number : 6
    Sum of the two number is 11
  ---  
 ## 2.Write a program to find average of n numbers.

```c
#include<stdio.h>
  int main()
{
	float arr[20],avg,sum=0;
	int N,i;
	printf("\n How many numbers you want to enter : ");
	scanf("%d",&N);
	printf("\nEnter The Numbers : \n");
	for(i=0;i<N;i++)
	{
		scanf("%f",&arr[i]);
		sum+=arr[i];
	}
	printf("\n Average of the numbers is %3.f",sum/N);
	return 0;
}
```

#### Output : 
    How many numbers you want to enter : 5
    Enter The Numbers : 1 2 3 4 5
    Average of the numbers is 3.000
---
 ## 3. Write a program to print Weekdays using switch statement.

```c
#include<stdio.h>
int main()
{
	int week;
	printf("\nEnter Week Number : ");
	scanf("%d",&week);
	switch(week){
		case 1 : printf("\nMonday.");
		break;
		case 2 : printf("\nTuesday");
		break;
		case 3 : printf("\nWednesday");
		break;
		case 4 : printf("\nThursday");
		break;
		case 5 : printf("\nFriday");
		break;
		case 6 : printf("\nSaturday");
		break;
		case 7 : printf("\nSunday");
		break;
		default : printf("\nYou have entered wrong week number!");
		break;
	}
	return 0;
}
```

### Output : 
    Enter Week number : 3
    Wednesday
---    
## 4. Write a program to find whether the number is even or odd.

```c
#include<stdio.h>
int main()
{
	int num;
	printf("\n Enter an Integer : ");
	scanf("%d",&num);
	if(num%2==0)
	{
		printf("\n The integer %d is Even.",num);
	}
	else
	{
		printf("\n The integer %d is Odd.",num);
	}
	return 0;
}
```

### Output : 
    Enter an Integer : 5
    The integer 5 is Odd.
---
 ## 5. Write a program to print the table using for loop.

```c
#include<stdio.h>
int main()
{
 int i,num;
 printf("\nEnter the number for which\
           you want the table : ");
 scanf("%d",&num);
 printf("\nTable of %d :-",num);
 for(i=1;i<=10;i++)
  {
    printf("\n%d X %d = %d",num,i,num*i);
	}
  return 0;
}
``` 

#### Output : 
    Enter the number for which you want the table : 6
    Table of 6 :-
    6 X 1 = 6
    6 X 2 = 12
    6 X 3 = 18
    6 X 4 = 24
    6 X 5 = 30
    6 X 6 = 36
    6 X 7 = 42
    6 X 8 = 48
    6 X 9 = 54
    6 X 10 = 60
 ---   
 ## 6. Write a program to check whether the number is armstrong or not.

```c
#include<stdio.h>
int main( )
{
 int num,sum=0,digit;
 printf("Enter a Number : ");
 scanf("%d",&num);
 int temp=num;
 while(temp!=0)
  {
    digit=temp%10;
    temp/=10;
    sum+=(digit*digit*digit);
  }
if(sum==num)
{
 printf("The number %d is an armstrong number.\n",num);
}
else
  printf("The number %d is not an armstrong.\n",num);
return 0;
}
```
#### Output : 
     Enter a Number : 371
     The number 371 is an armstrong number.
---
## 7. Write a program to print Calculator using puts.

```C
#include<stdio.h>
void main()
{
puts(" ------------------ ");
puts("|                  |");
puts(" __________________ ");
puts("|____|____|____|___|");
puts("|____|____|____|___|");
puts("|____|____|____|___|");
puts("|____|____|____|___|");
puts("|__________________|");
}
```
---
## 8. Write a program for Bubble sort.

```C
#include <stdio.h>
 
int main()
{
  int array[100], n, c, d, swap;
 
  printf("Enter number of elements\n");
  scanf("%d", &n);
 
  printf("Enter %d integers\n", n);
 
  for (c = 0; c < n; c++)
    scanf("%d", &array[c]);
 
  for (c = 0 ; c < n - 1; c++)
  {
    for (d = 0 ; d < n - c - 1; d++)
    {
      if (array[d] > array[d+1]) 
      {
        swap       = array[d];
        array[d]   = array[d+1];
        array[d+1] = swap;
      }
    }
  }
 
  printf("Sorted list in ascending order:\n");
 
  for (c = 0; c < n; c++)
     printf("%d\n", array[c]);
 
  return 0;
}
```
#### Output : 
    Enter number of elements : 5
    Enter 5 integers : 5 4 6 9 8 3
    Sorted list in ascending order : 3 4 5 6 8 9
___

## 9. Write a program for Binary search.

```C
#include <stdio.h>

int main()
{
   int c, first, last, middle, n, search, array[100];

   printf("Enter number of elements\n");
   scanf("%d",&n);

   printf("Enter %d integers\n", n);

   for (c = 0; c < n; c++)
      scanf("%d",&array[c]);

   printf("Enter value to find\n");
   scanf("%d", &search);

   first = 0;
   last = n - 1;
   middle = (first+last)/2;

   while (first <= last) {
      if (array[middle] < search)
         first = middle + 1;
      else if (array[middle] == search) {
         printf("%d found at location %d.\n", search, middle+1);
         break;
      }
      else
         last = middle - 1;

      middle = (first + last)/2;
   }
   if (first > last)
      printf("Not found! %d isn't present in the list.\n", search);

   return 0;
}
```
#### Output : 
      Enter number of elements : 4
      Enter 4 integers : 5 2 7 6
      Enter value to find : 6
      6 is found at location 4
---
## 10. Write a program to find factorial of a number : 
```C
#include <stdio.h>
 
int main()
{
  int i, Number; 
   
  printf("\n Enter any number to Find Factors : \n");
  scanf("%d", &Number);
 
  printf("\n Factors of the Given Number are :\n");
  for (i = 1; i <= Number; i++)
   {
     if(Number%i == 0)
        {
		 printf(" %d  ", i);
		}
   }
 
  return 0;
}
```
#### Output : 
    Enter any number to Find Factors : 3
    Factors of the Given Number are : 6
    
---

## 11. Write a program for fizzbuzz.
```C
#include<stdio.h>

int main()
{
 for(int i=1;i<=30;i++)
{
 if(i%3==0 && i%5==0)
{
 printf("fizzBuzz\t");
}
else if(i%3==0)
{
 printf("fizz\t");
}
else if(i%5==0)
{
 printf("Buzz\t");
}
else{
printf("%d\t",i);
}
}return 0;
}
```
#### Output : 
      1 2 fizz 4 buzz fizz 7 8 fizz buzz 11 fizz 13 14 fizzBuzz
---

## 12. Write a program to find sum of first 100 integers.

```C
#include<stdio.h>

int main()
{
	int sum=0;
	for(int i=1;i<=100;i++)
	{
		sum+=i;
	}
	printf("%d",sum);
	return 0;
}
```
#### Output : 
    5050
---
## 13. Write a Program to fine greater of two numbers : 
```C
#include<stdio.h>
int main()
{
	int a,b,max;
	printf("Enter two numbers : ");
	scanf("%d %d",&a,&b);
	max=a;
	if(b>max)
	{
		max=b;
	}
	printf("The greater number is : %d ",max);
	return 0;
}
```
#### Output : 
     Enter two numbers : 4 5
     The greater number is 5
---
## 14. Write a Program to find the greater of three numbers : 
```C
#include<stdio.h>
int main()
{
	int a,b,c,max;
	printf("Enter three numbers : ");
	scanf("%d %d %d",&a,&b,&c);
	if(a>b&&a>c)
	{
		max =a ;
	}
	else if(b>c)
	{
		max=b;
	}
	else max=c;
	printf("The greatest number is : %d\n",max);
	return 0;
}
```
#### Output : 
     Enter three numbers : 3 4 5
     The greatest numbers is : 5
---
## 15. Write a Program to find gcd of two number.
```C
#include<stdio.h>
int main()
{
int n1,n2,remainder=1;
printf("\n Enter value for n1 and n2 : ");
scanf("%d%d",&n1,&n2);
while(remainder!=0)
{
remainder=n2%n1;
n2=n1;
n1=remainder;
}
printf("\n GCD : %d \n",n2);
return 0;
}
```
#### Output : 
     Enter value for n1 and n2 : 36 24
     GCD : 12
---
## 16. Write a Program to find whether he tear is leap year or not.
```C
#include<stdio.h>

int main()
{
 int year;
 puts("Enter A Year : ");
 scanf("%d",&year);
 if(year%4==0)
{
 puts("This year is leap year.");
}
else
 puts("This year is not a leap year.");
return 0;
}
```
   #### Output :  
    Enter a Year : 2002
    This year is not a leap year.
---
## 17. Write a Program for Linear Search.
```C
#include <stdio.h>
 
int main()
{
  int array[100], search, c, n;
 
  printf("Enter number of elements in array : ");
  scanf("%d", &n);
 
  printf("Enter %d integer(s) : ", n);
 
  for (c = 0; c < n; c++)
    scanf("%d", &array[c]);
 
  printf("Enter a number to search : ");
  scanf("%d", &search);
 
  for (c = 0; c < n; c++)
  {
    if (array[c] == search)    
    {
      printf("\n%d is present at location %d.\n", search, c+1);
      break;
    }
  }
  if (c == n)
    printf("%d isn't present in the array.\n", search);
 
  return 0;
```
#### Output : 
    Enter number of elements in array : 5
    Enter 5 integer(s) : 1 3 6 7 3
    Enter a number to search : 5
    5 isn't present int the array.
---
## 18. Write a Program for Matrix addition.
```C
    #include <stdio.h>
     
    int main()
    {
       int m, n, c, d, first[10][10], second[10][10], sum[10][10];
     
       printf("Enter the number of rows and columns of matrix\n");
       scanf("%d%d", &m, &n);
       printf("Enter the elements of first matrix\n");
     
       for (c = 0; c < m; c++)
          for (d = 0; d < n; d++)
             scanf("%d", &first[c][d]);
     
       printf("Enter the elements of second matrix\n");
     
       for (c = 0; c < m; c++)
          for (d = 0 ; d < n; d++)
             scanf("%d", &second[c][d]);
       
       printf("Sum of entered matrices:-\n");
       
       for (c = 0; c < m; c++) {
          for (d = 0 ; d < n; d++) {
             sum[c][d] = first[c][d] + second[c][d];
             printf("%d\t", sum[c][d]);
          }
          printf("\n");
       }
     
       return 0;
    }
```
#### Output : 
    Enter the number of rows and columns of matrix : 2 2
    Enter the elements of first matrix : 1 2 1 3
    Enter the elements of second matrix :1 4 2 5
    Sum of entered matrices : 
    2 6 
    3 8
---
## 19. Write a Program to find transpose of a Matrix.
```C
#include<stdio.h>
 void main()
{
 int a[10][10],b[10][10],m,n,i,j;
 printf("Enter rows and coulmn : ");
 scanf("%d %d",&m,&n);
 printf("Enter the matrix : ");
 for(i=0;i<m;i++)
{
 for(j=0;j<n;j++)
{
  scanf("%d",&a[i][j]);
}
}
for(i=0;i<m;i++)
{ for(j=0;j<n;j++)
 { b[j][i]=a[i][j];
}
}
printf("\nTranspose : \n");
for(i=0;i<m;i++)
{
 for(j=0;j<n;j++)
{
 printf("%d\t",b[i][j]);
}
puts("\n");
}
```
#### Output : 
    Enter rows and column : 2 2
    Enter the matrix : 1 3 5 6
    
    Transpose : 
    1      5
    3      6
---
## 20. Write a Program to find the sum of digits of a number :
  ```C
  #include<stdio.h>

void main()
{
 int digit,sum=0,i;
 puts("Enter 3 digit integer : ");
 scanf("%d",&digit);
 while(digit>0)
{
 i=digit%10;
 digit=digit/10;
sum=sum+i;
 }
 printf("\nSUM OF DIGITS : %d\n",sum);
}
  ```
  #### Output : 
       Enter 4 digit number : 342
       SUM OF THE DIGITS : 9
---
## 21. Write a Program to check whether the number is palidrome or not :
```C
#include<stdio.h>

int main()
{
 int num,sum=0,digit,temp;
 printf("Enter a Number : ");
 scanf("%d",&num);
 temp=num;
 while(temp!=0)
  {
    digit=temp%10;
    temp=temp/10;
    sum=sum*10 + digit;
  }
 if(sum==num)
  printf("The number %d is a palindrome.\n",num);
 else
  printf("The number %d is not a palindrome.\n",num);
 return 0;
}
```
#### Output : 
      Enter a Number : 343
      The number 343 is a plaindrome.
---
## 22. Write a Program to swap two numbers using call by value method.
```C
#include<stdio.h>
 
void swap(int,int);        
 
void main( )
{
    int n1,n2;
    printf("Enter the two numbers to be swapped : ");
    scanf("%d%d",&n1,&n2);
    printf("\nValue of n1=%d and n2=%d before swapping.",n1,n2);
    swap(n1,n2);                                         }
 
void swap(int n1,int n2)                           
{ 
    int temp;
    temp=n1;
    n1=n2;
    n2=temp;
    printf("\nValue n1=%d and n2=%d after swapping.",n1,n2);
}
```
#### Output : 
     Enter the two numbers to swapped : 2 3
     Value of n1=2 and n2=3 before swapping.
     Value of n1=3 and n2=2 after swapping.
---
## 23. Write a Program to swap two numbers using call by reference method.
```C
#include<stdio.h>

int swapnum(int *num1,int *num2);

int main()
{
  int n1,n2;
  printf("Enter two integers : ");
  scanf("%d %d",&n1,&n2);
  printf("Value of n1=%d and n2=%d before swapping.",n1,n2);
  swapnum(&n1,&n2);
  printf("\nValue of n1=%d and n2=%d after swapping.",n1,n2);
  printf("%d %d",n1,n2);
 return 0;
}

int swapnum(int *num1,int *num2)
{
 int temp;
 temp=*num1;
 *num1=*num2;
 *num2=temp;
 return  0;
}
```
#### Output : 
     Enter two integers : 4 5
     Value of n1=4 and n2=5 before swapping.
     Value of n1=5 and n2=4 after swapping.
---
## 24. Write a Program to enter details of employees using structure.
```C
#include<stdio.h>

struct employee{
	int empid;
	char name[50], empdept[50];
	float salary;
};

int main()
{
	struct employee E;
	printf("\nEnter Employee Id : ");
	scanf("%d",&E.empid);
	printf("Ent Employee Name : ");
    scanf("\n%[^\n]%*c",&E.name);
    printf("Enter Employee Department : ");
    scanf("\n%[^\n]%*c",&E.empdept);
    printf("Enter Employee salary : ");
    scanf("%f",&E.salary);
    printf("\n\nEmployee Id : %d\nEmployee Name : %s\nEmployee Department : %s\nEmployee Salary : %f\n",
    E.empid,E.name,E.empdept,E.salary);
	return 0;
}
```
#### Output : 
      Enter Employee Id : 124
      Enter Employee Name : Sahil Butola
      Enter Employee Department : CSE
      Enter Employee Salary : 20000.0 
      
      Employee Id : 124
      Employee Name : Sahil Butola
      Employee Department : CSE
      Employee Salary : 20000.0
---
## 25. Write a Program to find the fractions using structures.
```C
#include<stdio.h>
struct fract{
  int n,d;
}f1,f2;
fract product(fract f1,fract f2);
int main()
{
  printf("\nEnter first number : ");
  printf("\nNumerator : ");
  scanf("%d",&f1.n);
  printf("\nDenominator : ");
  scanf("%d",&f1.d);
  printf("\nEnter Second number : ");
  printf("\nNumerator : ");
  scanf("%d",&f2.n);
  printf("\nDenominator : ");
  scanf("%d",&f2.d);
  fract result=product(f1,f2);
  printf("\nProduct : %d/%d",result.n,result.d);
  return 0;
}
fract product(fract f1,fract f2)
{
	fract result;
	result.n=f1.n*f2.n;
	result.d=f1.d*f2.d;
	return result;
}
```
#### Output : 
      Enter first number :
      Numerator : 3
      Denominator : 4
      
      Enter second number :
      Numerator : 4
      Denominator : 5
      
      Product : 12/20
-----------
