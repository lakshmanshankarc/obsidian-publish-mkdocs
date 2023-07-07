# Sorting

Arrange the elements in the Ascending order or descending order

# Quick Sort:

<aside>
💡 Approach :     Divide and conqueror

</aside>

Time Complexity

$$
Worst Case = O(n^2) \newline
Average Case  = O(n log n) 
                                     
$$

1. Take a Pivot (Which In this case is Last char
2. Try to find the right position for pivot meaning all the smallest elements needs to be on the left of the pivot
3. Now the pivot is in the right place now we can recursively call the left and right sub arrays

[QuickSort - Data Structure and Algorithm Tutorials - GeeksforGeeks](https://www.geeksforgeeks.org/quick-sort/)

```tsx
def quicksort(arr, l, r):
    if l < r:
        mid = partition(arr, l, r)
        quicksort(arr, l, mid - 1)
        quicksort(arr, mid + 1, r)
    return arr

def partition(arr, l, r):
    i, j = l - 1, l

    while j <= r:
        if arr[j] < arr[r]:
            i += 1
            arr[i], arr[j] = arr[j], arr[i]
        j += 1
    
    i += 1 
    arr[i], arr[r] = arr[r], arr[i]
    return i
```

<aside>
💡 Smallest Element should always before the pivot

</aside>

$$
f(x) = f(6*n)
$$

