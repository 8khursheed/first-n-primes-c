#include <stdio.h>

int test_prime(int n) {
    int i;

    if (n < 2)
        return 0;

    for (i = 2; i * i <= n; i++) {
        if (n % i == 0)
            return 0;
    }

    return 1;
}

int main() {
    int N, count = 0, number = 2;

    printf("Enter N: ");
    scanf("%d", &N);

    printf("First %d prime numbers are:\n", N);

    while (count < N) {
        if (test_prime(number)) {
            printf("%d ", number);
            count++;
        }
        number++;
    }

    return 0;
}
