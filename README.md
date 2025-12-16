# java1
package Arrays;
import java.util.Scanner;
public class MiniProjCal {
	private static final int case1 = 0;
	static double add(double a,double b)
	{
		return a+ b;
		
	}
	static double subtract(double a,double b)
	{
		return a-b;
	}
	static double mult(double a,double b)
	{
		return a*b;
		
	}
	static double div(double a ,double b) {
		if(b==0) {
			System.out.println("Error:div by b");
			return 0;
		}
		return a/b;
	}
	static double modulus(double a,double b)
	{
		return a%b;
	}
	public static void main(String[]args)
	{
		Scanner sc=new Scanner(System.in);
		int choice;
		do {
			System.out.println("\n=== MENU DRIVEN CALCULATOR ===");
            System.out.println("1. Addition");
            System.out.println("2. Subtraction");
            System.out.println("3. Multiplication");
            System.out.println("4. Division");
            System.out.println("5. Modulus");
            System.out.println("6. Exit");
            
            System.out.println("Enter your choice");
            choice=sc.nextInt();
            if (choice>=1&&choice<=5) {
            	System.out.println("Enter your first number:");
            	double n=sc.nextDouble();
            	
            	System.out.println("Enter your second number");
            	double m=sc.nextDouble();
            	
            	switch(choice) {
            	case 1:
            		System.out.println("Result="+add(n,m));
            	break;
            	case 2:
            		System.out.println("Result="+subtract(n,m));
            		break;
            	case 3:
            		System.out.println("Result="+mult(n,m));
            		break;
            	case 4:
            		System.out.println("Result="+ div(n,m));
            		break;
            	case 5:
            		System.out.println("Result="+modulus(n,m));
            		break;
            	}
            }else if(6!=choice) {
            	System.out.println("Invalid choice");
            }
		}while(6!=choice);
		System.out.println("Close calucator ");
		sc.close();
	}

}
