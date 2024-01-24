//Using Switch Case
import java.util.Scanner;
 
public class SimpleCalculator {
    public static void main(String[] args)
    {
        try (Scanner sc = new Scanner(System.in)) {
            // Enter the first number
            System.out.print("Enter the first number: ");
            int firstNumber = sc.nextInt();

            
            // Enter the first number
            System.out.print("Enter the second number: ");
            int secondNumber = sc.nextInt();
 
            //  User to enter their choice of operation
            System.out.print("Enter the type of operation you want to perform (+, -, *, /, %): ");
            String operation = sc.next();
            int result = performOperation(firstNumber, secondNumber, operation);
            
            System.out.println("Your answer is: " + result);
        }
    }
 
    public static int performOperation(int firstNumber, int secondNumber, String operation)
    {
        int result = 0;
        switch (operation) {
            // perform addition operation
            case "+":
                result = firstNumber + secondNumber;
                break;
                // perform subtraction operation
            case "-":
                result = firstNumber - secondNumber;
                break;
                // perform multiplication operation
            case "*":
                result = firstNumber * secondNumber;
                break;
                // perform remainder operation
            case "%":
                result = firstNumber % secondNumber;
                break;
                // perform deivider operation
            case "/":
                result = firstNumber / secondNumber;
                break;
            default:
                // invalid operation
                System.out.println("Invalid operation");
                break;
        }
        return result;
    }
}
