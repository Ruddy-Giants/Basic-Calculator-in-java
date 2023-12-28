# java basic calculator

//stating the programm
import java.util.Scanner;

public class BasicCalculator {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        double num1, num2, result;
        char operator;

        //taking first number as a input

        System.out.print("Enter first number: ");
        num1 = input.nextDouble();

        //taking second number as a input

        System.out.print("Enter second number: ");
        num2 = input.nextDouble();

        //taking the operator as a input by user

        System.out.print("Enter an operator (+, -, *, /): ");
        operator = input.next().charAt(0);

        //using switch-case
        switch (operator) {
            case '+':
                result = num1 + num2;
                break;
            case '-':
                result = num1 - num2;
                break;
            case '*':
                result = num1 * num2;
                break;
            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                } else {
                    System.out.println("Error: Division by zero is not allowed.");
                    return;
                }
                break;
            default:
                System.out.println("Error: Invalid operator.");
                return;
        }
        System.out.println("Result: " + result);
    }
}

