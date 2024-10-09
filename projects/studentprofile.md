---
layout: project
type: project
image: img/cotton/cotton-square.png
title: "Student Profile"
date: 2024-05-26
published: true
labels:
  - C
  - Student Project
  - GitHub
summary: "A student profile system that I developed for ICS 211."
---

This C program manages student data by creating, reading, writing, and editing records stored in a binary file called students.data. 
It defines a Student struct that holds information such as student number, first and last name, age, and GPA. 
The program features functions to handle various tasks: createFile initializes the file with 20 blank student records; 
writeFile allows users to add or update a student's data; readFile retrieves and displays all student records; and editFile enables the user to modify a specific student's information. 
The main function presents a menu that lets users choose between creating the file, writing to it, reading records, editing records, or exiting the program. 
The program uses binary file operations (fwrite, fread, fseek) to manage the student data and ensures input validation, 
such as restricting the size of names and checking valid record numbers. 
Through a simple console-based interface, users can efficiently manage student information. does this show!!!!!!

```cpp
typedef struct {
    int number;
    char first[MAX_STRING];
    char last[MAX_STRING];
    int age;
    double gpa;
} Student;

// Function structs
double getdouble();
int getstring(char *str, int size);
void printStudent(Student);
void createFile();
void writeFile();
void readFile();
void editFile();
```
<hr>

<pre>

</pre>

<hr>

<a href="https://github.com/jogarces/ics-313-text-game">
  <i class="large github icon" style="font-size: 200px; width: 200px; height: 200px;"></i> jogarces/ics-313-text-game
</a>
