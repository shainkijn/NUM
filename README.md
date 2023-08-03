# guessnum
import java.util.Random;
import java.util.Scanner;

public class NumberGuessingGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        int correctNumber = random.nextInt(100) + 1;
        int attempts = 0;
        int guess;

        System.out.println("Welcome to the Number Guessing Game!");
        System.out.println("I have selected a number between 1 and 100. Can you guess it?");

        while (true) {
            System.out.print("Enter your guess: ");
            guess = scanner.nextInt();
            attempts++;

            if (guess == correctNumber) {
                System.out.println("Congratulations! You guessed the number " + correctNumber + " correctly in " + attempts + " attempts.");
                break;
            } else if (guess < correctNumber) {
                System.out.println("Too low. Try again.");
            } else {
                System.out.println("Too high. Try again.");
            }
        }

        scanner.close();
    }
}
