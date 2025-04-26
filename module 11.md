

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
//type your code here
#include <stdio.h>

int max_of_four(int n1, int n2, int n3, int n4) {
    int max = n1;
    if (n2 > max) max = n2;
    if (n3 > max) max = n3;
    if (n4 > max) max = n4;
    return max;
}

int main() {
    int n1, n2, n3, n4;
    printf("Enter four integers: ");
    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);

    int greater = max_of_four(n1, n2, n3, n4);
    printf("The greatest number is: %d\n", greater);

    return 0;
}

Output:
//paste your output here
<img width="252" alt="image" src="https://github.com/user-attachments/assets/bb558a76-8494-4838-b793-baa6ac66ee28" />

Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
//type your code here
#include <stdio.h>

void calculate_the_max(int n, int k) {
    int a = 0, o = 0, x = 0;

    for (int i = 1; i <= n; i++) {
        for (int j = i + 1; j <= n; j++) {
            if ((i & j) < k && (i & j) > a) {
                a = i & j;
            }
            if ((i | j) < k && (i | j) > o) {
                o = i | j;
            }
            if ((i ^ j) < k && (i ^ j) > x) {
                x = i ^ j;
            }
        }
    }

    printf("Maximum AND value: %d\n", a);
    printf("Maximum OR value: %d\n", o);
    printf("Maximum XOR value: %d\n", x);
}

int main() {
    int n, k;
    printf("Enter n and k: ");
    scanf("%d %d", &n, &k);

    calculate_the_max(n, k);

    return 0;
}

Output:
//paste your output here
<img width="178" alt="image" src="https://github.com/user-attachments/assets/48d00f95-062f-4b1d-909a-b3c2912fc4ba" />

Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
//type your code here
#include <stdio.h>

int main() {
    int noshel, noque, k, c;

    printf("Enter number of shelves and queries: ");
    scanf("%d %d", &noshel, &noque);

    int shelarr[noshel][100];
    int nobookarr[noshel];

    for (int i = 0; i < noshel; i++) {
        nobookarr[i] = 0;
    }

    for (int i = 0; i < noque; i++) {
        int choice, shelf, book;
        printf("Enter query type (1 for adding book, 2 for retrieving book): ");
        scanf("%d", &choice);

        if (choice == 1) {
            printf("Enter shelf number and book ID to add: ");
            scanf("%d %d", &shelf, &book);

            shelarr[shelf-1][nobookarr[shelf-1]] = book;
            nobookarr[shelf-1]++;

        } else if (choice == 2) {
            printf("Enter shelf number and book index to retrieve: ");
            scanf("%d %d", &shelf, &k);

            if (k < nobookarr[shelf-1]) {
                printf("Book ID: %d\n", shelarr[shelf-1][k]);
            } else {
                printf("Invalid index.\n");
            }
        } else {
            printf("Invalid choice.\n");
        }
    }

    return 0;
}

Output:
//paste your output here

<img width="547" alt="image" src="https://github.com/user-attachments/assets/59cab584-7315-48d6-a1ac-a276669ab7e4" />

Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
//type your code here
#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter the number of integers: ");
    scanf("%d", &n);

    int a[n];

    for (int i = 0; i < n; i++) {
        printf("Enter integer %d: ", i + 1);
        scanf("%d", &a[i]);
        sum += a[i];
    }

    printf("Sum of the integers: %d\n", sum);

    return 0;
}

Output:
//paste your output here

 
<img width="260" alt="image" src="https://github.com/user-attachments/assets/771b6b5f-5b46-4306-9049-a691c0c32f54" />


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
//type your code here
#include <stdio.h>
#include <ctype.h>

int main() {
    char sentence[1000];
    int count = 0, i = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);

    while (sentence[i]) {
        if (isalpha(sentence[i])) {
            if (i == 0 || !isalpha(sentence[i - 1])) {
                count++;
            }
        }
        i++;
    }

    printf("Number of words: %d\n", count);

    return 0;
}

Output:
//paste your output here

<img width="250" alt="image" src="https://github.com/user-attachments/assets/5435b1bd-f236-4524-a65f-a3519ceaf99d" />


Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
