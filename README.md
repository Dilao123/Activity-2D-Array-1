import java.util.Scanner;

public class Main{
    public static void main(String[] args) {
        // Create a scanner object to read input from the user
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to input the number of rows and columns
        System.out.print("Enter the number of rows: ");
        int rows = scanner.nextInt();

        System.out.print("Enter the number of columns: ");
        int columns = scanner.nextInt();

        // Create a 2D array with the given dimensions
        int[][] array = new int[rows][columns];

        // Populate the array using a nested for loop
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                array[i][j] = i * j;
            }
        }

        // Print the array in a table format
        System.out.println("Multiplication Table:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                System.out.print(array[i][j] + "\t");  // \t is for tab spacing
            }
            System.out.println();  // Move to the next line after each row
        }

        // Close the scanner
        scanner.close();
    }
}
