import java.util.Scanner;

class School {
    private int rollNo;
    private String name;
    private String address;
    private String branch;
    private double[] marks = new double[4];
    private double percentage;
    private char grade;

    // Constructor to initialize the student's information
    public School(int rollNo, String name, String address, String branch, double[] marks) {
        this.rollNo = rollNo;
        this.name = name;
        this.address = address;
        this.branch = branch;
        this.marks = marks;
        this.calculatePercentageAndGrade();
    }

    // Calculate percentage and grade based on marks
    private void calculatePercentageAndGrade() {
        double totalMarks = 0.0;
        for (double mark : marks) {
            totalMarks += mark;
        }
        percentage = totalMarks / (marks.length * 100.0) * 100;

        if (percentage >= 90) {
            grade = 'A';
        } else if (percentage >= 80) {
            grade = 'B';
        } else if (percentage >= 70) {
            grade = 'C';
        } else if (percentage >= 60) {
            grade = 'D';
        } else {
            grade = 'F';
        }
    }

    // Display student information
    public void displayStudentInfo() {
        System.out.println("Roll No: " + rollNo);
        System.out.println("Name: " + name);
        System.out.println("Address: " + address);
        System.out.println("Branch: " + branch);
        System.out.println("Marks in 4 subjects: ");
        for (int i = 0; i < marks.length; i++) {
            System.out.println("Subject " + (i + 1) + ": " + marks[i]);
        }
        System.out.println("Percentage: " + percentage + "%");
        System.out.println("Grade: " + grade);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the number of students: ");
        int numStudents = scanner.nextInt();

        // Create an array to store student objects
        School[] students = new School[numStudents];

        for (int i = 0; i < numStudents; i++) {
            System.out.println("Enter Student " + (i + 1) Details: ");
            System.out.print("Roll No: ");
            int rollNo = scanner.nextInt();
            scanner.nextLine();  // Consume newline
            System.out.print("Name: ");
            String name = scanner.nextLine();
            System.out.print("Address: ");
            String address = scanner.nextLine();
            System.out.print("Branch: ");
            String branch = scanner.nextLine();
            double[] marks = new double[4];
            for (int j = 0; j < 4; j++) {
                System.out.print("Enter Marks for Subject " + (j + 1) + ": ");
                marks[j] = scanner.nextDouble();
            }

            students[i] = new School(rollNo, name, address, branch, marks);
        }

        System.out.print("Enter the student number to display details: ");
        int studentNumber = scanner.nextInt();

        if (studentNumber > 0 && studentNumber <= numStudents) {
            System.out.println("Student " + studentNumber + " Details: ");
            students[studentNumber - 1].displayStudentInfo();
        } else {
            System.out.println("Invalid student number.");
        }
    }
}
