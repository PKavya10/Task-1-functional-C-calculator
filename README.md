#include <iostream>

using namespace std;

int main() {
    double num1, num2, result;
    char operation;

    // Get user input
    cout << "Enter first number: ";
    cin >> num1;

    cout << "Enter operator (+, -, *, /): ";
    cin >> operation;

    cout << "Enter second number: ";
    cin >> num2;

    // Perform calculation based on the chosen operation
    switch (operation) {
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
            // Check for division by zero
            if (num2 != 0) {
                result = num1 / num2;
            } else {
                cout << "Error: Division by zero is not allowed." << endl;
                return 1;  // Exit program with an error code
            }
            break;
        default:
            cout << "Error: Invalid operator." << endl;
            return 1;  // Exit program with an error code
    }

    // Display the result
    cout << "Result: " << result << endl;

    return 0;  // Exit program successfully
}
