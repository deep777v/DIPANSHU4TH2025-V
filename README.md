import java.util.Scanner;
 
public class BankingSystem {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int[] transactionIDs = {101, 102, 103, 104, 105};
 
        try {
            System.out.print("Enter the total balance: ");
            double totalBalance = scanner.nextDouble();
 
            System.out.print("Enter the number of account holders: ");
            int numOfAccountHolders = scanner.nextInt();

            double averageBalance = totalBalance / numOfAccountHolders;
            System.out.println("Average Account Balance: " + averageBalance);
        } catch (ArithmeticException e) {
            System.out.println("Error: Division by zero. Number of account holders cannot be zero.");
        }
 
        System.out.println();
 
        try {
            System.out.print("Enter the transaction ID index to access (0-4): ");
            int index = scanner.nextInt();

            System.out.println("Transaction ID: " + transactionIDs[index]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: Invalid index. Please enter a valid index between 0 and 4.");
        }
 
        scanner.close();
    }
}
