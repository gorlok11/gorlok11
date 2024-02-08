#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    srand(time(0));

    int num = rand() % 100 + 1;
    int guess, attempts = 0;

    cout << "Welcome to the Number Guessing Game! I'm thinking of a number between 1 and 100.\n";

    do {
        cout << "Enter your guess: ";
        cin >> guess;
        attempts++;

        if (guess > num) {
            cout << "Too high. Try again.\n";
        } else if (guess < num) {
            cout << "Too low. Try again.\n";
        }

    } while (guess != num);

    cout << "Congratulations! You guessed the correct number in " << attempts << " attempts.";

    return 0;
}
