 #include <stdio.h>

int main(void) {
    int score[3][2][3] = {
        {{10, 20, 30}, {40, 50, 60}},
        {{70, 80, 90}, {15, 25, 35}},
        {{45, 55, 65}, {75, 85, 95}}
    };

    int size = sizeof(score) / sizeof(score[0]);

    for (int i = 0; i < size; i++) {
        printf("Block %d:\n", i);
        for (int j = 0; j < 2; j++) {
            for (int k = 0; k < 3; k++) {
                printf("%d ", score[i][j][k]);
            }
            printf("\n");
        }
    }

    printf("\nsize = %d\n", size);
    printf("First value of block 1 using score + 1: %d\n", (*(score + 1))[0][0]);

    return 0;
}
