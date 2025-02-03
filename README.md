# Calculator-
#include <stdio.h>

int main() {
    double num1, num2, result;
    char operator;

    // Taking user input
    printf("Enter first number: ");
    scanf("%lf", &num1);

    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator);  // Space before %c to handle newline character

    printf("Enter second number: ");
    scanf("%lf", &num2);

    // Performing the calculation based on the operator
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
            if (num2 != 0)
                result = num1 / num2;
            else {
                printf("Error! Division by zero is not allowed.\n");
                return 1;
            }
            break;
        default:
            printf("Error! Invalid operator.\n");
            return 1;
    }

    // Display the result
    printf("Result: %.2lf\n", result);
    
    return 0;
}
