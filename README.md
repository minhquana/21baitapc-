# 21baitapc-
#include <iostream>

void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }

        arr[j + 1] = key;
    }
}

int main() {
    int arr[] = {41, 23, 4, 14, 56, 1};
    int n = sizeof(arr) / sizeof(arr[0]);

    insertionSort(arr, n);

    std::cout << "Mãng đã sắp xếp : ";
    for (int i = 0; i < n; i++) {
        std::cout << arr[i] << " ";
    }

    return 0;
}
