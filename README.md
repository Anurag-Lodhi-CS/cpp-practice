# C++ Data Structures & Algorithms Practice

A curated collection of fundamental Data Structures and Algorithms
implemented in C++ with proper edge case handling and basic optimization.

**Author:** Anurag Lodhi  
**LinkedIn:** https://linkedin.com/in/anurag-lodhi-cs

---

## Tech Stack
- Language: C++
- Concepts: Arrays, Sorting, Searching, Recursion
- Tools: GCC Compiler / VS Code

---

## Programs List

### 1. Array Operations
- Find maximum element with safety check
- Find minimum element
- Calculate sum and average  

**Time Complexity:** O(n)  
**Space Complexity:** O(1)

---

### 2. Sorting
- Bubble Sort (optimized with swapped flag)
- Selection Sort  

**Bubble Sort Complexity:**  
- Best Case: O(n)  
- Worst Case: O(n²)  
- Space Complexity: O(1)

---

### 3. Searching
- Linear Search  
- Binary Search  

**Linear Search Complexity:**  
- Time: O(n)  
- Space: O(1)

---

### 4. Functions
- Factorial using recursion  
- Fibonacci series  
- Prime number check  

**Factorial Complexity:**  
- Time: O(n)  
- Space: O(n) (recursion stack)

---

## Sample Code 1 — Array Maximum (With Edge Case Check)

```cpp
// Find largest element in array with Safety Check
// Author: Anurag Lodhi

#include <iostream>
using namespace std;

int findMax(int arr[], int n) {
    // Edge Case: Check if array is empty
    if (n <= 0) return -1;

    int maxVal = arr[0];
    for(int i = 1; i < n; i++) {
        if(arr[i] > maxVal)
            maxVal = arr[i];
    }
    return maxVal;
}

int main() {
    int arr[] = {5, 3, 8, 1, 9, 2, 7};
    int n = 7;

    int result = findMax(arr, n);

    if(result != -1)
        cout << "Maximum: " << result;
    else
        cout << "Array is empty!";

    return 0;
}


---

Sample Code 2 — Bubble Sort (Optimized)

// Bubble Sort — Optimized
// Author: Anurag Lodhi

#include <iostream>
using namespace std;

void bubbleSort(int arr[], int n) {
    for(int i = 0; i < n - 1; i++) {
        bool swapped = false;

        for(int j = 0; j < n - i - 1; j++) {
            if(arr[j] > arr[j+1]) {
                int temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
                swapped = true;
            }
        }

        // Stop if already sorted
        if(!swapped) break;
    }
}

int main() {
    int arr[] = {64, 34, 25, 12, 22, 11, 90};
    int n = 7;

    cout << "Before sorting: ";
    for(int i = 0; i < n; i++)
        cout << arr[i] << " ";

    bubbleSort(arr, n);

    cout << "\nAfter sorting: ";
    for(int i = 0; i < n; i++)
        cout << arr[i] << " ";

    return 0;
}


---

Sample Code 3 — Factorial (Recursion)

// Factorial using Recursion
// Author: Anurag Lodhi

#include <iostream>
using namespace std;

int factorial(int n) {
    if(n < 0) return -1;   // Edge case
    if(n == 0 || n == 1) return 1;
    return n * factorial(n - 1);
}

int main() {
    for(int i = 1; i <= 10; i++)
        cout << i << "! = " << factorial(i) << endl;

    return 0;
}


---

Sample Code 4 — Linear Search

// Linear Search
// Author: Anurag Lodhi

#include <iostream>
using namespace std;

int linearSearch(int arr[], int n, int key) {
    for(int i = 0; i < n; i++) {
        if(arr[i] == key)
            return i;
    }
    return -1;
}

int main() {
    int arr[] = {10, 25, 30, 45, 60, 75};
    int n = 6;
    int key = 45;

    int result = linearSearch(arr, n, key);

    if(result != -1)
        cout << "Element found at index: " << result;
    else
        cout << "Element not found";

    return 0;
}


---

About

I am a Computer Science graduate with hands-on experience in C++, Data Structures, and problem-solving.

Degree: BSc Mathematics, Physics & Computer Science

University: Barkatullah University

College: Aryabhatta College

Year: 2020 – 2023

Result: First Division (69.8%)


---

Future Improvements

Add advanced algorithms (Merge Sort, Quick Sort)

Implement STL-based solutions

Add LeetCode / HackerRank problems

Convert programs into reusable modules


---
