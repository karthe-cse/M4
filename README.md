# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    // Step 1 & 2: Assign values
    int a = 44, b = 3;

    // Step 3: Left shift a by 3 times
    int result = a << b;  // same as a << 3

    // Step 4: Display the result
    printf("Result of %d << %d is: %d\n", a, b, result);

    // Step 5: Stop the program
    return 0;
}

## OUTPUT
Result of 44 << 3 is: 352









## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    int num1, num2;

    // Step 2: Read two numbers
    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    // Step 3 & 4: Compare and display result
    if (num1 == num2) {
        printf("Both are equal.\n");
    } else {
        printf("Both are not equal.\n");
    }

    // Step 5: Stop the program
    return 0;
}


## OUTPUT

Enter two numbers: 10 10
Both are equal.

           
## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM
#include <stdio.h>
#include <ctype.h>  // for tolower()

int main() {
    char str[100];

    // Step 2: Read a string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // safer than gets()

    // Step 3: Convert string to lowercase
    for (int i = 0; str[i] != '\0'; i++) {
        str[i] = tolower(str[i]);
    }

    // Step 4: Display the result
    printf("Lowercase string: %s", str);

    // Step 5: Stop the program
    return 0;
}


## OUTPUT
Enter a string: Hello World!
Lowercase string: hello world!




## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    char str[100];
    int count = 0;

    // Step 2: Read a string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Step 3 & 4: Loop through string and count spaces
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == ' ') {
            count++;
        }
    }

    // Step 5: Display the result
    printf("Number of spaces: %d\n", count);

    // Step 6: Stop the program
    return 0;
}

## OUTPUT
Enter a string: Hello there, how are you?
Number of spaces: 4





## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM
#include <stdio.h>

int main() {
    // Step 2: Declare variables
    char c1[100], c2[100];
    int flag = 0, i = 0;

    // Step 3: Read the first string including spaces until newline
    printf("Enter first string (can include spaces): ");
    scanf("%[^\n]", c1);

    // Consume leftover newline after first scanf
    getchar();

    // Step 4: Read the second string without spaces
    printf("Enter second string (no spaces): ");
    scanf("%s", c2);

    // Step 5 & 6: Compare character by character
    while (c1[i] != '\0' && c2[i] != '\0') {
        if (c1[i] != c2[i]) {
            flag = 1;  // Strings differ
            break;
        }
        i++;
    }

    // Also check if both strings ended simultaneously
    if (c1[i] != '\0' || c2[i] != '\0') {
        flag = 1;  // Length mismatch
    }

    // Step 7: Print result based on flag
    if (flag == 0) {
        printf("strings are same\n");
    } else {
        printf("strings are not same\n");
    }

    // Step 8: End program
    return 0;
}


## OUTPUT
Enter first string (can include spaces): hello
Enter second string (no spaces): hello
strings are same

 

## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

