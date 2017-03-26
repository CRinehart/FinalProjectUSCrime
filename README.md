# FinalProjectUSCrime

For the USCrime class it needs to not have the main in it. With this one,
I need to bring in the data via command line like below, store the data
from the csv into arrays and then use that to do calculations for population growth
from question 1 in the test class file and pull the year from a specific array for the 
last four questions. The TestUSCrime will print out the data.

    package uscrime;

    import java.io.BufferedReader;
    import java.io.FileReader;
    import java.io.IOException;

    public class USCrime {
        String year;
        
        //default constructor
        public USCrime(){
        };
       
        public static void main(String[] args) throws IOException {
            BufferedReader br = null;
            String fileName = args[0];
            try {
                String line;
                br = new BufferedReader(new FileReader(fileName));
                while ((line = br.readLine()) != null) {
                    String[] crime_array = line.split(",");

                    System.out.println("Year: " + crime_array[0]);
                }
            }
            catch (IOException ex) {
                ex.printStackTrace();
            }
            
        public int getMaxMurderRateYear() {
            return crime_array[][];     //input the array numbers for the highest murder rate in a year
            }
            
        public int getMinMurderRateYear() {
            return crime_array[][];     //input the array numbers for the lowest murder rate in a year
            }
            
        public int getMaxRobberyRateYear() {
            return crime_array[][];     //input the array numbers for the highest robbery rate in a year
            }
            
        public int getMinRobberyRateYear() {
            return crime_array[][];     //input the array numbers for the lowest robbery rate in a year
            }
    
        }
    }
------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------

    //Filename:TestUsCrime
    //Author: Cody M Rinehart
    //Date: 25032017
    /*Purpose: The purpose of this program is to create the menu and read the user's
    input to determine what data will be printed out to the user*/

    package uscrime;

    public class TestUsCrime

      public static void promptMenu() {
        System.out.println("**********Welcome to the US Crime Statistical Application**********");
        System.out.println();
        System.out.println("Enter the number of the question you want answered. Enter 'Q' to quit the program:");
        System.out.println();
        System.out.println("1. What were the percentages in population growth for each consecutive year from 1994-2013?");
        System.out.println("2. What year was the Murder rate the highest?");
        System.out.println("3. What year was the Murder rate the lowest?");
        System.out.println("4. What year was the Robbery rate the highest?");
        System.out.println("5. What year was the Robbery rate the lowest?");
        System.out.println("Q. Quit the program.");
      }

    public static void main (String [] args) throws IOException {
      do {
        promptMenu;
        userInput = scannerIn.next();
        System.out.print("\n");

        switch (userInput) {
          case "1":
            //insert getter method for getPopGrowth()
            break;
          case "2":
            System.out.println("The Murder rate was highest in " + /*insert getter method for getMaxMurderRateYear()*/);
            break;
          case "3":
            System.out.println("The Murder rate was lowest in " + /*insert getter method for getMinMurderRateYear()*/);
            break;
          case "4":
            System.out.println("The Robbery rate was highest in " + /*insert getter method for getMaxRobberyRateYear()*/);
            break;
          case "5":
            System.out.println("The Robbery rate was lowest in " + /*insert getter method for getMinRobberyRateYear()*/);
            break;
          case "Q":
            System.out.println("Thank you for trying the US Crimes Statistics Program.");
            break;
          default:
            System.out.println(userInput + " is not a valid choice.");
        }
      } while (!userInput.equals("Q"));
    }
