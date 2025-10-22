# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM
'''
#include <stdio.h>
#include <math.h>

// Function to calculate EMI
void calculateEMI(float principal, float rate, int time) {
    float monthlyRate = rate / (12 * 100); // Convert annual rate to monthly
    int months = time * 12;

    float emi = (principal * monthlyRate * pow(1 + monthlyRate, months)) /
                (pow(1 + monthlyRate, months) - 1);

    printf("\nEMI for the loan is: ₹%.2f\n", emi);
}

int main() {
    float principal, rate;
    int time;

    // Input from user
    printf("Enter loan amount (₹): ");
    scanf("%f", &principal);

    printf("Enter annual interest rate (%%): ");
    scanf("%f", &rate);

    printf("Enter loan tenure (in years): ");
    scanf("%d", &time);

    // Call the function
    calculateEMI(principal, rate, time);

    return 0;
}
'''

## OUTPUT

![Image](https://github.com/user-attachments/assets/8fd97d37-c4da-4e1d-87af-fbd1851fd3cd)

## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
'''
#include <stdio.h>

int main() {
    int n = 6; // Number of terms
    int first = 0, second = 1, next;

    printf("Fibonacci series up to %d terms:\n", n);

    for (int i = 0; i < n; i++) {
        if (i <= 1)
            next = i;
        else {
            next = first + second;
            first = second;
            second = next;
        }
        printf("%d ", next);
    }

    return 0;
}
'''

## OUTPUT

![Image](https://github.com/user-attachments/assets/4246dbd1-600c-44d9-9e6c-8d6c75457939)


## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM
'''
#include <stdio.h>

int main() {
    int n;

    // Ask user for number of elements
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n]; // Declare array of size n

    // Read elements into the array
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Print the last element
    printf("The last element is: %d\n", arr[n - 1]);

    return 0;
}
'''

## OUTPUT


![Image](https://github.com/user-attachments/assets/8eecba27-180f-407c-bd88-b7d7fe2f595f)


## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM
'''
#include <stdio.h>

int main() {
    int n, count = 0;

    // Ask user for number of elements
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

    // Read elements into the array
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        if (arr[i] > 0) {
            count++;
        }
    }

    // Print the count of positive elements
    printf("Total number of positive elements: %d\n", count);

    return 0;
}
'''


## OUTPUT

![Image](https://github.com/user-attachments/assets/e22f6d31-0b80-4713-89f5-175fae71203e)

## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
'''
#include <stdio.h>

int main() {
    int n;

    // Ask user for number of elements
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];
    char result[n];

    // Read elements into the array
    printf("Enter %d elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);

        // Replace even numbers with 'E', else store '*'
        if (arr[i] % 2 == 0)
            result[i] = 'E';
        else
            result[i] = '*'; // Placeholder for non-even values
    }

    // Display the result
    printf("Modified array:\n");
    for (int i = 0; i < n; i++) {
        if (result[i] == 'E')
            printf("%c ", result[i]);
        else
            printf("%d ", arr[i]);
    }

    return 0;
}
'''

## Output:
 
![Image](https://github.com/user-attachments/assets/979a09b3-8027-4d6c-9192-7a697dd1b0d6)

## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



