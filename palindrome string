#include<stdio.h>
#include<ctype.h>
#include<string.h>

int comp(char s1[],char s2[])
{
	int i1=0,i2=0;
    while (i1<strlen(s1))
	 {
	 	while ( i1 < strlen(s1) && !isalpha(s1[i1]) )
	 	i1++;
	 	if (s1[i1] != s2[i2])
	 	{
	 	    return 0;
	 	}
		i1++;
		i2++;
	 }	
	 return 1;
}


int main ()
{
	int l1;
	printf("Enter the length of the string :") ;
	scanf("%d",&l1);
	char str[l1+1],rev_str[l1+1];
	getchar();
	printf("\nEnter the string :");
	fgets(str, sizeof(str), stdin);
	int i1=strlen(str)-1,i2=0;
    while (i1>=0)
	 {
	 	while ( i1 >= 0 && !isalpha(str[i1]) )
	 	i1--;
	 	rev_str[i2] = str[i1];
		i1--;
		i2++;
	 } 
	
	if (comp(str,rev_str) == 1) 
	printf("\nThe given string '%s' is a palindrome",str);
	else 
	printf("\nThe given string '%s'is not a palindrome",str);
	return 0;	
}
