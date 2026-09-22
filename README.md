#include <stdio.h>
int linearSearch(int arr[], int size, int target);
int main() {
    int data[] = {11, 71, 6, 80, 45, 23};
    int size = sizeof(data) / sizeof(data[0]);
    int target;
    printf("Enter the number to search: ");
    scanf("%d", &target);
    int resultIndex = linearSearch(data, size, target);
    if (resultIndex != -1) {
        printf("Element found at Index: %d\n", resultIndex);
    } else {
        printf("Element not found.\n");
    }
    return 0;
}
int linearSearch(int arr[], int size, int target) {
    for (int i = 0; i < size; i++) {
        if (arr[i] == target) {
            return i; // Element found, return its index
        }
    }
    return -1; // Element not found after checking the entire array
}
