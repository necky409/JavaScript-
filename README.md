staticArrayDemo.java 
import java.util.Scanner; // Import the Scanner class

public class StaticArrayDemo {

    public static void main(String[] args) {
        // Declare a static array of size 10 to hold integers
        int[] numbers = new int[10];

        // Create a Scanner object to read user input
        Scanner inputScanner = new Scanner(System.in);

        System.out.println("--- Java Array Example ---");
        System.out.println("Please enter 10 integer values:");

        // Populate the array with user input
        for (int i = 0; i < numbers.length; i++) {
            System.out.print("Enter value for element " + (i + 1) + ": ");
            // Use a try-catch block for robust input handling (optional but good practice)
            try {
                numbers[i] = inputScanner.nextInt();
            } catch (java.util.InputMismatchException e) {
                System.out.println("Invalid input. Please enter an integer. Exiting for simplicity.");
                inputScanner.close(); // Close the scanner before exiting
                return; // Exit the program if input is not an integer
            }
        }

        // Print all values in the array
        System.out.println("\nValues in the array:");
        for (int i = 0; i < numbers.length; i++) {
            System.out.println("Element " + (i + 1) + ": " + numbers[i]);
        )




statisaArrayDemo.cpp
int main() {
    // Declare a static array of size 10 to hold integers
    // For C-style arrays, the size must be a compile-time constant.
    const int ARRAY_SIZE = 10;
    int numbers[ARRAY_SIZE];

    std::cout << "--- C++ Array Example ---" << std::endl;
    std::cout << "Please enter " << ARRAY_SIZE << " integer values:" << std::endl;

    // Populate the array with user input
    for (int i = 0; i < ARRAY_SIZE; ++i) {
        std::cout << "Enter value for element " << (i + 1) << ": ";
        // Basic input validation: check if the input was an integer
        while (!(std::cin >> numbers[i])) {
            std::cout << "Invalid input. Please enter an integer: ";
            std::cin.clear(); // Clear the error flags
            // Ignore the rest of the invalid input line
            std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        }
    }

    // Print all values in the array
    std::cout << "\nValues in the array:" << std::endl;
    for (int i = 0; i < ARRAY_SIZE; ++i) {
        std::cout << "Element " << (i + 1) << ": " << numbers[i] << std::endl;
    }

    

     
   
