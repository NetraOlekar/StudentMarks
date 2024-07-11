# StudentMarks
import java.util.Scanner;

public class StudentMarks {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the Total number of subjects: ");
        int numofSubjects = sc.nextInt();

        int TotalMarks = 0;
        for (int i = 1; i <= numofSubjects; i++) 
        {
            System.out.print("Enter the marks for Subject " + i + ": ");
            int Marksofsubject= sc.nextInt();
            TotalMarks += Marksofsubject;
        }

        float AveragePercentage = (float) TotalMarks / numofSubjects;
        char grade = calculateStudentGrade(AveragePercentage);
        System.out.println("\nResults of Student:");
        System.out.println("Totalnumber of Marks: " + TotalMarks);
        System.out.println("Average Percentage of Student: " + AveragePercentage + "%");
        System.out.println("Student Grade: " + grade);

        sc.close();
    }
    private static char calculateStudentGrade(float AveragePercentage) {
        if (AveragePercentage >= 90)
        {
            return 'A';
        } else if (AveragePercentage >= 80) 
        {
            return 'B';
        } else if (AveragePercentage >= 70)
        {
            return 'C';
        } else if (AveragePercentage >= 60)
         {
            return 'D';
        } 
        else
         {
            return 'F';
        }
    }
}

    
   
    
    

