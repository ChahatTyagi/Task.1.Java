# Task.1.Java
import java.util.*;
class nogame
{
    static void main( )
    {   
        Scanner sc=new Scanner(System.in);
        System.out.println("enter the no. of attempts the user has to guess the number");
        int t=sc.nextInt();
        Random random=new Random();
        int a= random.nextInt(100)+1;
        int b=a;int f=0,g=0,h=0,count=0,won=0;
         for(int j=1;j<=t;j++)
         {
             System.out.println("enter the guessed no");
             int s=sc.nextInt();
              if(a==s)
           {
             System.out.println("guessed no is correct");
             f++;
             count++;
             won++;
            }
          else if(s%2>a)
          {
           System.out.println("guessed no is too high");
           g++;
          }
          else if(s%2<a)
          {
           System.out.println("guessed no is low");
           h++;
          }
          System.out.println("no of right:"+ f);
          System.out.println("no of guessed no is high:"+g);
          System.out.println("no of guessed no is low:"+h);
          s=0;
         }
         System.out.println("random no:"+a);
         if(count==0)
         {
             System.out.println("user was not able to guess in "+t+" chances");
         }
         System.out.println("User's Score:");
         System.out.println("No. of attempts taken by the user:"+t);
         System.out.println("No. of rounds won by the user:"+won);
        }
         }
