# Number_Guessing_Game<br>
Hi i am krish !! <br>
This gonna be my first code that i publish !! <br>

A simple Python program where the computer randomly picks a number between 1 and 100, and the player has to guess it. The game provides hints whether the guess is too high or too low until the correct number is guessed. <br>

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int number, guess, attempts = 0;

    // Seed random number generator
    srand(time(0));
    number = rand() % 100 + 1; // random number between 1 and 100

    printf("Welcome to Number Guessing Game!\n");
    printf("Guess the number (between 1 and 100):\n");

    do {
        printf("Enter your guess: ");
        scanf("%d", &guess);
        attempts++;

        if (guess > number) {
            printf("Too high! Try again.\n");
        } else if (guess < number) {
            printf("Too low! Try again.\n");
        } else {
            printf("🎉 Correct! You guessed it in %d attempts.\n", attempts);
        }
    } while (guess != number);

    return 0;
}

