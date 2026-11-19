import java.util.Scanner;
public class StudentMarksAnalyzer{
public static void main(String args[]){
    Scanner sc = new Scanner(System.in);

    int n = 0;
    while(true){
        System.out.print("Enter number of students: ");
        try{
            n = Integer.parseInt(sc.nextLine().trim());
            if(n>0){
                break;
            }
            System.out.println("Enter a number greater than 0 :");
        } catch(NumberFormatException e){
            System.out.println("Invalid input! Please enter a whole number.");

        }
    }
    String[] names = new String[n];
    double[] marks = new double[n];

    for(int i = 0; i<n; i++){
        System.out.println("\nStudent " + (i+1) + ":");
        while(true){
            System.out.print("Enter name :");
            names[i]= sc.nextLine().trim();
            if(!names[i].isEmpty()){
                break;
            }
            System.out.println("Name can not be empty. Try again");
        }
        while(true){
            System.out.print("Enter marks for " +names[i]+ "(0 to 100): ");
            try{
                double score = Double.parseDouble(sc.nextLine().trim());
                if(score >= 0 && score <= 100){
                    marks[i]= score;
                    break;
                } else{
                    System.out.println("Invalid! Marks must be between 0 and 100.");
                }
            } catch (NumberFormatException e){
                System.out.println("Invalid! Please enter numbers only.");
            }
        }
    }
    
    double sum = 0; 
    double highest = marks[0];
    double lowest = marks[0];
    for(int i = 0; i<n; i++){
        sum += marks[i];

        if(marks[i]>highest){
            highest = marks[i];
        }
        if(marks[i]<lowest){
            lowest = marks[i];
        }
    }
    double average = sum/n;

    System.out.println("\n---Class Statistics---");
    System.out.printf("Average Marks : %.2f%n", average);
    System.out.printf("Highest Marks : %.2f%n", highest);
    System.out.printf("Lowest Marks : %.2f%n",lowest );

    System.out.print("Top Scorer(s) : ");
    boolean first = true;
    for(int i =0; i<n; i++){
        if(marks[i]==highest){
            if(!first){
                System.out.print(", ");
            }
            System.out.print(names[i]);
            first= false;
        }
    }
    System.out.println();
    sc.close();
}
}
