# Remove Duplicates from Sorted Array (Brute Force)

## Problem Statement

Given a sorted array `arr[]`, remove the duplicate elements and print only the unique elements using a temporary array.

---

## Example

### Input

```text
n = 7

arr[] = [1, 1, 2, 2, 2, 3, 3]
```

### Output

```text
Count = 3

Unique Elements:
1 2 3
```

---

## Approach

This solution uses the **Brute Force** approach with a temporary array.

* Traverse the original array one element at a time.
* For each element, check whether it has already been stored in the temporary array.
* If the element is not present, store it in the temporary array.
* Use the variable `k` to keep track of the number of unique elements.

---

## Algorithm

1. Read the size of the array (`n`).
2. Read all the array elements.
3. Create a temporary array `temp[]` of size `n`.
4. Initialize `k = 0`.
5. Traverse the original array.
6. For each element:

   * Initialize `found = 0`.
   * Compare the current element with the elements already stored in `temp`.
   * If a duplicate is found, set `found = 1`.
   * Otherwise, store the element in `temp[k]` and increment `k`.
7. Print the count of unique elements (`k`).
8. Print the first `k` elements from `temp`.

---

## Time Complexity

* **Time Complexity:** `O(n²)`

The outer loop runs `n` times, and for each element, the inner loop may compare against previously stored unique elements.

---

## Space Complexity

* **Space Complexity:** `O(n)`

An additional temporary array is used to store the unique elements.

---

## Key Concepts

* Arrays
* Nested Loops
* Brute Force
* Duplicate Detection
* Temporary Array
* Time Complexity Analysis

---

## Note

This solution is **not in-place** because it uses an extra array (`temp[]`).

The optimal solution uses the **Two Pointer** technique, which has:

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(1)`

---

## Language

**Java**
