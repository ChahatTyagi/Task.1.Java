# Task.1.Java
import java.util.*;
import java.util.Random;
public class NumberGuessingGame
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        Random random=new Random();
        int min=1;
        int max=100;
        System.out.println("Enter the number of attempts: ");
        int maxAttempts=sc.nextInt();
        int totalRounds=0;
        int totalAttempts=0;
        while(totalRounds<maxAttempts)
        {
            int generatedNumber=random.nextInt(max-min+1)+min;
            int attempts=0;
            while(true)
            {
                System.out.println("Guess the number between 1 and 100: ");
                int userGuess=sc.nextInt();
                attempts++;
                if(userGuess == generatedNumber)
                {
                    System.out.println("Congratulations! Guessed correctly.");
                    totalRounds++;
                    totalAttempts += attempts;
                    break;
                }
                else if(userGuess > generatedNumber)
                {
                    System.out.println("Too high. Try again.");
                }
                else
                {
                    System.out.println("Two low. Try again.");
                }
                }
            }
        System.out.println("User's Score:");
        System.out.println("Total attempts taken: "+totalAttempts);
        System.out.println("Total rounds won: "+totalRounds);
        sc.close();
        }
    }


       
