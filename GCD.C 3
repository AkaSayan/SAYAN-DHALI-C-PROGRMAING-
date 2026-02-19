#include <stdio.h>

int main() {
    int a[] = {10, 12, 15};
    int n = 3;

    int subset[100][10];   
    int subsetSize[100];   

    int total = 1;   

    subsetSize[0] = 0;   

    for(int i = 0; i < n; i++) {
        int currentTotal = total;

        for(int j = 0; j < currentTotal; j++) {
            
            for(int k = 0; k < subsetSize[j]; k++) {
                subset[total][k] = subset[j][k];
            }

            
            subset[total][subsetSize[j]] = a[i];

            subsetSize[total] = subsetSize[j] + 1;
            total++;
        }
    }

    
    for(int i = 0; i < total; i++) {
        printf("{ ");
        for(int j = 0; j < subsetSize[i]; j++) {
            printf("%d ", subset[i][j]);
        }
        printf("}\n");
    }

    return 0;
}
