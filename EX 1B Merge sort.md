# EX 1B Merge Sort
## DATE:
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm

1. If the array has more than one element, split it into two halves.
2. Recursively apply merge sort on both halves.
3. Compare elements of both halves and merge them into a sorted array.
4. Copy any remaining elements from the left or right half.
5. Return the fully sorted array.
   

## Program:

```
Developed by: SAKTHIVEL R
Register Number: 212222100044
```

```py
def merge_sort(inp_arr):
    if len(inp_arr) > 1:
        mid = len(inp_arr) // 2  
        left_half = inp_arr[:mid]  
        right_half = inp_arr[mid:]  

        merge_sort(left_half)  
        merge_sort(right_half)  
        i = j = k = 0  
        while i < len(left_half) and j < len(right_half):
            if left_half[i] < right_half[j]:
                inp_arr[k] = left_half[i]
                i += 1
            else:
                inp_arr[k] = right_half[j]
                j += 1
            k += 1

        while i < len(left_half):
            inp_arr[k] = left_half[i]
            i += 1
            k += 1

        while j < len(right_half):
            inp_arr[k] = right_half[j]
            j += 1
            k += 1

inp_arr = []     
n = int(input())  
for i in range(n):
    inp_arr.append(int(input()))  

print("Input Array:\n")
print(inp_arr)

merge_sort(inp_arr)  

print("Sorted Array:\n")
print(inp_arr)
```

## Output:

![op19b](https://github.com/user-attachments/assets/5a3d9356-2809-4981-87ce-6fe9b1292082)


## Result:

The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
