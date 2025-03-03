# 2-2-matrix-input-promp.cpp
Assignment
BBIT-01-0170/2024
Tom Aguko


#include <stdio.h>

#define SIZE 2  // Macro for matrix size

int main() {
    int matrix[SIZE][SIZE];

    // Predefined values for reference
    int defaultValues[SIZE][SIZE] = {{50, 29}, {45, 91}};

    // Prompt user to enter values one by one
    printf("Enter values for a %dx%d matrix (one by one):\n", SIZE, SIZE);
    
    for (int i = 0; i < SIZE; i++) {
        for (int j = 0; j < SIZE; j++) {
            printf("Enter value for matrix[%d][%d] (Suggested: %d): ", i, j, defaultValues[i][j]);
            scanf("%d", &matrix[i][j]);
        }
    }

    // Display the entered matrix
    printf("\nThe entered matrix is:\n");
    for (int i = 0; i < SIZE; i++) {
        for (int j = 0; j < SIZE; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}

