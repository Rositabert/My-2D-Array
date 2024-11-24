import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Create a Scanner object for user input
        Scanner scanner = new Scanner(System.in);

        //Prompt user to enter number of rows and columns
        System.out.print("Enter the number of rows: ");
        int rows = scanner.nextInt();
        
        System.out.print("Enter the number of columns: ");
        int cols = scanner.nextInt();

        // Create a 2D array based on user input
        int[][] array = new int[rows][cols];

        // Populate the array with the product of row and column indices
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                array[i][j] = i * j;
            }
        }

        // Print the 2D array in a table-like format
        System.out.println("The generated 2D array is:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(array[i][j] + "\t"); // Print each element with tab spacing
            }
            System.out.println(); // Newline after each row
        }

        scanner.close(); // Close the scanner
    }
}
