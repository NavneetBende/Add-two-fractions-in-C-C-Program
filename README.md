# Add-two-fractions-in-C-C-Program

Add two fractions in C
Here, in this page we will discuss program for add two fractions in C. For this purpose we need to ask the user to enter two fractional values where each fraction must consist a Numerator and a Denominator.

Add two fractions in C
While loop in C
Concept
 For understanding this in a better way lets suppose an example :

 Suppose, First fraction consist of 1 as numerator and 3 as denominator, and Second fraction consist of 3 as numerator and 9 as denominator.

 (1 / 3) + (3 / 9) = (6 / 9) = (2 / 3)

Find LCM of 3 and 9 and the result will be 9.
Multiply 3 in first fraction : (3 / 9) + (3 / 9)
Add both fractions and then the result will be : (6 / 9)
Now simplify it by finding the HCF of 6 and 9 and the result will be 3.
So divide 6 and 9 by 3 and then the result will be : (2 / 3)
This will be your simplified answer for the given problem.
Algorithm
Initialize variables of numerator and denominator
Take user input of two fraction
Find numerator using this condition (n1*d2) +(d1*n2 ) where n1,n2 are numerator and d1 and d2 are denominator
Find denominator using this condition (d1*d2) for lcm
Calculate GCD of a this new numerator and denominator
Display a two value of this condition x / gcd, y/gcd
Related Pages
Permutations in which n people can occupy r seats in a classroom
 
Maximum number of handshakes
 
Calculate the area of a circle

Can a number be expressed as a sum of two prime numbers

Count possible decoding of a given digit sequence


C code
Run
#include<stdio.h>
int main()
{
    //for initialize variables
    int numerator1, denominator1, numerator2, denominator2, x, y, c, gcd_no;
    
    //To take user input of numerators and denominators
    printf("Enter the numerator for 1st number   : ");
    scanf("%d",&numerator1);
    printf("Enter the denominator for 1st number : ");
    scanf("%d",&denominator1);
    printf("Enter the numerator for 2nd number   : ");
    scanf("%d",&numerator2);
    printf("Enter the denominator for 2nd number : ");
    scanf("%d",&denominator2);
    
    //numerator
    x=(numerator1*denominator2)+(denominator1*numerator2); 
    
    //denominator
    y=denominator1*denominator2; 
    
	// Trick part. Reduce it to the simplest form by using gcd.
    for(c=1; c <= x && c <= y; ++c)
    {
       if(x%c==0 && y%c==0)
          gcd_no = c;
    }
    
    //To display fraction of givien numerators and denominators
    printf("(%d / %d) + (%d / %d) = (%d / %d)", numerator1, denominator1, numerator2, denominator2, x/gcd_no, y/gcd_no);
    
    return 0;
}
Output
Enter the numerator for 1st number   : 1
Enter the denominator for 1st number : 3
Enter the numerator for 2nd number   : 3
Enter the denominator for 2nd number : 9
(1 / 3) + (3 / 9) = (2 / 3)
