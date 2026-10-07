// WAP IN C TO FIND PRIME NO. OR NOT USING IF ELSE

#include <stdio.h>
int main() {
    int n, i, f = 0;

    printf("Enter a positive integer: ");
    scanf("%d", &n);

    // Numbers less than or equal to 1 are not prime
    if (n <= 1) {
        f = 1; 
    } else {
        // Loop to check divisibility from 2 up to n/2
        for (i = 2; i <= n / 2; i++) {
            if (n % i == 0) {
                f = 1; // It has a divisor, so it's not prime
                break; // Exit loop early
            } else {
                // Nested else: explicitly do nothing and continue checking
                continue; 
            }
        }
    }

    // Final evaluation using if-else
    if (f == 0) {
        printf("%d is a Prime Number.\n", n);
    } else {
        printf("%d is Not a Prime Number.\n", n);
    }

    return 0;
}
