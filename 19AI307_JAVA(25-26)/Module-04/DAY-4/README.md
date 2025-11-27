# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create an MVC program for a School System where the DAO stores student info, controller fetches it, and view displays it.

## AIM:
To implement the MVC and DAO design patterns to store student details and display a specific student based on roll number.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Student model class with name, age, and roll number.
4.	Define a StudentDAO interface with methods to add and retrieve students.
5.	Implement StudentDAOImpl to store students in a list and retrieve them by roll number.
6.	Create a StudentView class to display student details.
7.	Create a StudentController to connect DAO and View, handling add and display operations.
8.	In main, input student details, store them using the controller, then input a roll number and display the matching student.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: AMURTHA VAAHINI KN
RegisterNumber:  212222240008
*/
```

## SOURCE CODE:


```
import java.util.*;

// Model
class Student {
    private String name;
    private int age;
    private String rollNo;

    public Student(String name, int age, String rollNo) {
        this.name = name;
        this.age = age;
        this.rollNo = rollNo;
    }

    public String getName() { return name; }
    public int getAge() { return age; }
    public String getRollNo() { return rollNo; }
}

// DAO Interface
interface StudentDAO {
    void addStudent(Student student);
    Student getStudentByRollNo(String rollNo);
}

// DAO Implementation
class StudentDAOImpl implements StudentDAO {
    private List<Student> students = new ArrayList<>();

    public void addStudent(Student student) {
        students.add(student);
    }

    public Student getStudentByRollNo(String rollNo) {
        for (Student s : students) {
            if (s.getRollNo().equals(rollNo)) {
                return s;
            }
        }
        return null;
    }
}

// View
class StudentView {
    public void displayStudent(Student student) {
        if (student != null) {
            System.out.println("Student Details:");
            System.out.println("Name    : " + student.getName());
            System.out.println("Age     : " + student.getAge());
            System.out.println("Roll No : " + student.getRollNo());
        } else {
            System.out.println("Student not found.");
        }
    }
}

// Controller
class StudentController {
    private StudentDAO dao;
    private StudentView view;

    public StudentController(StudentDAO dao, StudentView view) {
        this.dao = dao;
        this.view = view;
    }

    public void addStudent(Student student) {
        dao.addStudent(student);
    }

    public void showStudent(String rollNo) {
        Student student = dao.getStudentByRollNo(rollNo);
        view.displayStudent(student);
    }
}

// Main class
public class SchoolSystemMVC {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine().trim());

        StudentDAO dao = new StudentDAOImpl();
        StudentView view = new StudentView();
        StudentController controller = new StudentController(dao, view);

        // Input students
        for (int i = 0; i < n; i++) {
            String name = sc.nextLine().trim();
            int age = Integer.parseInt(sc.nextLine().trim());
            String rollNo = sc.nextLine().trim();
            controller.addStudent(new Student(name, age, rollNo));
        }

        // Input roll number to display
        String searchRoll = sc.nextLine().trim();
        controller.showStudent(searchRoll);

        sc.close();
    }
}
```




## OUTPUT:

<img width="602" height="503" alt="image" src="https://github.com/user-attachments/assets/ec6621fa-c455-4097-b8f5-b139a951db54" />


## RESULT:

The program successfully stores student details and retrieves and displays a student using MVC and DAO patterns.
