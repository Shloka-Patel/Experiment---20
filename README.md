# Experiment---20 

### Aim 
To study and implement Sorting Algortithm in C++ <ol><li>Selection Sort</li> <li>Insertion Sort</li> <li>Bubble Sort</li></ol> 

### Software 
Visual Studio Code 

### Theory 

### Code 
(A) 
```
// NAME - SHLOKA PATEL 
// PRN - 23070123120 
// EXPERIMENT - 20(A) 

#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void s_sort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;
    int arr[no_el];

    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    s_sort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    return 0;
} 
```

(B) 
```
```

(C) 
```
```

### Output 
(A) 
![]() 

(B) 
![]() 

(C) 
![]() 

### Conclusion 

