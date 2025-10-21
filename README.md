# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    float length, breadth, area;
    float *ptrLength, *ptrBreadth;
    
    ptrLength = &length;
    ptrBreadth = &breadth;
 
    printf("Enter the length of the rectangle: ");
    scanf("%f", ptrLength);

    printf("Enter the breadth of the rectangle: ");
    scanf("%f", ptrBreadth);
   
    area = (*ptrLength) * (*ptrBreadth);
   
    printf("Area of the rectangle = %.2f\n", area);

    return 0;
}


## OUTPUT
<img width="623" height="665" alt="Screenshot 2025-10-21 170705" src="https://github.com/user-attachments/assets/3faec34e-780c-483a-8830-e44982c1ca54" />
		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    char *str;

    str = (char *)malloc(8 * sizeof(char)); 

    strcpy(str, "WELCOME");

    printf("%s\n", str);

    free(str);

    return 0;
}


## OUTPUT
<img width="497" height="549" alt="Screenshot 2025-10-21 170719" src="https://github.com/user-attachments/assets/fd4d9920-dc43-4b4a-a2e9-76fa74d0351e" />



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
#include <stdio.h>

struct Student {
    char name[50];
    int rollNumber;
    float marks;
};

int main() {
    struct Student s;

    printf("Enter student name: ");
    fgets(s.name, sizeof(s.name), stdin); 

    printf("Enter roll number: ");
    scanf("%d", &s.rollNumber);

    printf("Enter marks: ");
    scanf("%f", &s.marks);

    
    printf("\n--- Student Information ---\n");
    printf("Name       : %s", s.name);
    printf("Roll Number: %d\n", s.rollNumber);
    printf("Marks      : %.2f\n", s.marks);

    return 0; 
}



## OUTPUT
<img width="639" height="884" alt="Screenshot 2025-10-21 170739" src="https://github.com/user-attachments/assets/73d7fad5-c10b-4c70-a6a7-19f0ff49d520" />


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
#include <stdio.h>

struct Employee {
    char name[50];
    int id;
    float basicSalary;
    float hra;  
    float da;   
    float grossSalary;
};
int main() {                                                                       
    struct Employee emp[3];                                                           
    for (int i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d:\n", i + 1);                           
        printf("Name: ");
        scanf(" %[^\n]", emp[i].name);
        printf("ID: ");
        scanf("%d", &emp[i].id);
        printf("Basic Salary: ");
        scanf("%f", &emp[i].basicSalary);
        printf("HRA: ");
        scanf("%f", &emp[i].hra);
        printf("DA: ");
        scanf("%f", &emp[i].da);
        emp[i].grossSalary = emp[i].basicSalary + emp[i].hra + emp[i].da;
    }
    printf("\n--- Employee Salary Details ---\n");
    for (int i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("Name        : %s\n", emp[i].name);
        printf("ID          : %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basicSalary);
        printf("HRA         : %.2f\n", emp[i].hra);
        printf("DA          : %.2f\n", emp[i].da);
        printf("Gross Salary: %.2f\n", emp[i].grossSalary);
    }
    return 0; 
}


 ## OUTPUT
<img width="882" height="883" alt="Screenshot 2025-10-21 170835" src="https://github.com/user-attachments/assets/3e20c613-53a2-41c7-997a-a0e717317a30" />
<img width="421" height="862" alt="Screenshot 2025-10-21 170947" src="https://github.com/user-attachments/assets/94d42bdb-e5a1-47b7-b5c9-ec0ff0e221e2" />

 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
#include <stdio.h>

struct student {
    char name[10];       
    int rollno;         
    int subject[5];     
    int total;           
    float average;       
};

int main() {
    struct student s[2]; 
    int i, j;
    for (i = 0; i < 2; i++) {
        printf("Enter marks for Student %d (5 subjects):\n", i + 1);
        for (j = 0; j < 5; j++) {
            printf("Subject %d: ", j + 1);
            scanf("%d", &s[i].subject[j]);
        }
    }
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
    }
    printf("\nStudent Results:\n");
    for (i = 0; i < 2; i++) {
        printf("Student %d - Total: %d, Average: %.2f\n", i + 1, s[i].total, s[i].average);
    }

    return 0;
}


## OUTPUT
<img width="973" height="689" alt="Screenshot 2025-10-21 171006" src="https://github.com/user-attachments/assets/b5b609ff-2441-41a4-b84e-15abec9b7fdc" />
<img width="462" height="371" alt="Screenshot 2025-10-21 171025" src="https://github.com/user-attachments/assets/a43d9214-4b7b-4100-98a1-8ba9db091295" />

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


