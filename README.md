# FinalProjectUSCrime
My final project for the class

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
