# CalorieCountPrj1
import java.util.Scanner;

public class CalorieCount{
  public static void main(String[] args){
    System.out.println("Fall 2023 - CS1083 - Section 006 - Project 1 - CaloriesCount - written by Aishat Kolawole");
    Scanner scnr = new Scanner(System.in);

   /* It will start asking the value of calories burnt for Monday and will continue asking the values until getting the value corresponding to
Sunday*/
    System.out.println(); //space needed 
    System.out.print("Calories burnt on Monday: ");
    int c1 = scnr.nextInt(); //monnday starts at 1
    
    System.out.print("Calories burnt on Tuesday:");
    int c2 = scnr.nextInt();

    System.out.print("Calories burnt on Wednesday: ");
    int c3 = scnr.nextInt();

    System.out.print("Calories burnt on Thursday: ");
    int c4 = scnr.nextInt();
   
    System.out.print("Calories burnt on Friday: ");
    int c5  = scnr.nextInt();
    
    System.out.print("Calories burnt on Saturday: ");
    int c6 = scnr.nextInt();

    System.out.print("Calories burnt on Sunday: ");
    int c7 = scnr.nextInt();
    
    int i;
    int countDays = 1; //the counter to see which value is the day (1-Mon, 2-Tues..)
    
    //first read the average calorie count burnt for every day of the week
    int sumWeek = (c1 + c2 +c3 + c4 + c5 + c6 + c7);
    
    System.out.println("Week \tMonday \tTuesday \tWednesdayThursday\tFriday \tSaturday\tSunday \tTotal/Week");
    //outer loop columns /* first column is Week with 1-5 below (6 rows total)
    for(i = 1; i <= 5; i++){
      System.out.print(i + " \t");
      //inner loop rows -->
    for(int j = 1; j < 8 ; j++){ //j will start from 1 to 7 *rows 2 to 8 correspond to the days of the week from Monday to Sunday
      System.out.print(countDays + "-");
      if(j == 1){ //*It starts with a Monday as day 1 of the month
        System.out.print(c1 +" \t"); //\t tab per day column
      }
      if(j == 2){
        System.out.print(c2 +" \t");
      }
      if(j == 3){
        System.out.print(c3 +" \t ");
      }
      if(j == 4){
        System.out.print(c4 +" \t ");
      }
      if(j == 5){
        System.out.print(c5 +" \t ");
      }
      if(j == 6){
        System.out.print(c6 +" \t ");
      }
      if(j == 7){
        System.out.print(c7 +" \t ");
      }
      countDays++; //counting the days
      if(countDays > 30) 
        break; //this breaks out of the inner loop
      }
    if(countDays > 30){
      break; //breaks out of outermost loop 
      }
    System.out.println(" W" + i + "-" + sumWeek); //*The program needs to print a total per week as the last column.
    }
    for(i = 0; i < 5; i++) //print for 0-0 after breaking out of the loops above 1
    {
      System.out.print("0-0 \t ");
    }
    System.out.println(" W" + i + "-" + (c1+c2)); //c1+c2 = sum of two days not 7 
    
    System.out.println("Total Calories: " + ((sumWeek * 4) + (c1+c2))); 
  }
}

  
