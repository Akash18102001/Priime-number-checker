#include <stdio.h>
int prime(int,int);							//function prototype
main()
{
	int n, a;
	printf(" Enter any number : ");
	scanf("%d",&n);							//Scanning and storing the input
	if(n==1)
	{
	printf("\n 1 is not a Prime number.");	//Since 1 is not a prime number
	}
	else
	{
		a=prime(n,n/2);						//call to function prime
		if(a==1)
		{
			printf("\n %d is a Prime number.",n);
		}
		else
		{
			printf("\n %d is not a Prime number.",n);
		}
	}
}

int prime(int n,int k)						//Definition of Recursive function prime
{
	if(k==1)
	{
		return 1;
	}
	else
	{
		if(n % k == 0)
		{
			return 0;
		}
		else
		{
			return prime( n , k - 1);
		}
	}
}
