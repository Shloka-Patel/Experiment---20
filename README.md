# Experiment---20 

### Aim 
To study and implement Sorting Algortithm in C++ <ol><li>Selection Sort</li> <li>Insertion Sort</li> <li>Bubble Sort</li></ol> 

### Software 
Visual Studio Code 

### Theory 
<b> (1) Selection Sort </b> <br> 
<ul><li>Finds the minimum element in the unsorted array.</li> <li>Swaps it with the elementt at the beginning.</li> <li>Repeats the process for the rest of the unsorted array.</li></ul> 

<b>(2) Insertion Sort</b> <br> 
<ul><li>Starts from the second element, and compare it with previous elements.</li> <li>Moves larger elements one position to the right to make space for the current element.</li> <li>Insert the current element in its correct position.</li></ul>

<b> (3) Bubble Sort </b> <br> 
<ul><li>Repeatedly compares adjacent elements.</li> <li>Swap them if they are in the wrong order.</li> <li>The largest (or smallest) element "bubbles up" to its correct position.</li></ul> 

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
// NAME - SHLOKA PATEL 
// PRN - 23070123120 
// EXPERIMENT - 20(B) 

#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void bubbleSort(int *a, int elements) {
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

    bubbleSort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    return 0;
}  
```

(C) 
```
// NAME - SHLOKA PATEL 
// PRN - 23070123120 
// EXPERIMENT - 20(C) 

#include<iostream>
using namespace std;

void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        // Move elements of arr[0..i-1], that are greater than key, to one position ahead of their current position
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

int main() {
    int n;
    cout << "How many elements in your array?" << endl;
    cin >> n;
    
    int arr[n];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    insertionSort(arr, n);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    
    return 0;
} 
```

### Output 
(A) 
![](https://github.com/Shloka-Patel/Experiment---20/blob/main/Output_20A.png) 

(B) 
![](https://github.com/Shloka-Patel/Experiment---20/blob/main/Output_20B.png) 

(C) 
![](https://github.com/Shloka-Patel/Experiment---20/blob/main/Output_20C.png) 

### Conclusion 
<ul><li><b>Selection Sort:</b> Selects the smallest element and swaps it; siple but inefficient for large arrays.</li><br> 
<li><b>Insertion Sort:</b> Efficient for small or nearly sorted arrays; it inserts elements in their correct position.</li><br> 
<li><b>Bubble Sort:</b> Repeatedly swaps adjacentn elements; easy to understand but inefficient for large datasets.</li> <br> 

