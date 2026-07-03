# Remove Duplicates from Sorted Array

## Problem Statement

Given a sorted array `arr[]`, remove the duplicate elements **in-place** so that each unique element appears only once. Return the number of unique elements (`k`). The first `k` positions of the array should contain the unique elements, while the remaining positions can contain any value.

### Example

**Input:**

```
arr[] = [1, 1, 2, 2, 2, 3, 3]
```

**Output:**

```
arr[] = [1, 2, 3, _, _, _, _]
Return: 3
```

**Explanation:**
The unique elements in the array are `1`, `2`, and `3`. After removing duplicates, these elements are placed at the beginning of the array. Since there are **3 unique elements**, the function returns `3`.

---

## Brute Force Approach

### Idea

Create a temporary array to store only the unique elements. Traverse the sorted array and compare each element with its previous element. If the current element is different, store it in the temporary array. Finally, copy all unique elements back to the original array and return the count of unique elements.

### Algorithm

1. Create a temporary array.
2. Store the first element in the temporary array.
3. Traverse the array from the second element to the end.
4. If the current element is different from the previous element, add it to the temporary array.
5. Copy the unique elements back to the original array.
6. Return the number of unique elements.

### Time Complexity

**O(n)** – One traversal to collect unique elements and another to copy them back.

### Space Complexity

**O(n)** – Extra space is used for the temporary array.

---

## Optimal Approach (Two Pointers)

### Idea

Since the array is already sorted, duplicate elements appear consecutively. Use two pointers:

* One pointer keeps track of the position of the last unique element.
* The other pointer traverses the array.

Whenever a new unique element is found, place it in the next position of the unique portion of the array.

### Algorithm

1. Initialize the first pointer at the first element.
2. Traverse the array using the second pointer.
3. If the current element is different from the last unique element, move the first pointer forward and place the current element there.
4. Continue until the end of the array.
5. Return the count of unique elements.

### Time Complexity

**O(n)** – Single traversal of the array.

### Space Complexity

**O(1)** – No extra space is used; the array is modified in-place.

---

## Comparison

| Approach               | Time Complexity | Space Complexity |
| ---------------------- | --------------- | ---------------- |
| Brute Force            | O(n)            | O(n)             |
| Two Pointers (Optimal) | O(n)            | O(1)             |

### Conclusion

The **Two Pointers** approach is the optimal solution because it removes duplicates **in-place** while using **constant extra space**, making it the preferred solution for interviews and coding platforms like LeetCode and GeeksforGeeks.
