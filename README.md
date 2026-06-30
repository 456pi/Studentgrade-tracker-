# Studentgrade-tracker-
A Student Grade Tracker is a software program that helps teachers and students keep track of academic performance. It stores student details, subject-wise marks, calculates total marks, percentage, and grade, and displays the final result.
import java.util.ArrayList;
import java.util.Scanner;
import java.util.Collections;

public class GradeTracker {
public static void main(String[] args) {
Scanner scanner = new Scanner(System.in);
ArrayList<Double> grades = new ArrayList<>();

System.out.println("--- Student Grade Tracker ---");  
    System.out.println("Enter grades (type -1 to finish):");  

    while (true) {  
        System.out.print("Enter grade: ");  
        double grade = scanner.nextDouble();  
        if (grade == -1) break;  
        if (grade >= 0 && grade <= 100) {  
            grades.add(grade);  
        } else {  
            System.out.println("Please enter a valid grade between 0 and 100.");  
        }  
    }  

    if (grades.isEmpty()) {  
        System.out.println("No grades were entered.");  
    } else {  
        displaySummary(grades);  
    }  
    scanner.close();  
}  

public static void displaySummary(ArrayList<Double> grades) {  
    double sum = 0;  
    double highest = Collections.max(grades);  
    double lowest = Collections.min(grades);  

    for (double g : grades) {  
        sum += g;  
    }  

    double average = sum / grades.size();  

    System.out.println("\n--- Summary Report ---");  
    System.out.println("Total Students: " + grades.size());  
    System.out.printf("Average Score: %.2f\n", average);  
    System.out.println("Highest Score: " + highest);  
    System.out.println("Lowest Score:  " + lowest);  
}

}

Make .Java file for download
