
# Remove Duplicates from Sorted Array

## LeetCode Problem
[Remove Duplicates from Sorted Array – LeetCode](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)

**Difficulty:** Easy

**Topics:** [Array](https://leetcode.com/tag/array/), [Two Pointers](https://leetcode.com/tag/two-pointers/)

---

## Problem Description

Given an integer array `nums` sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once.

The relative order of the elements must remain unchanged.

Return the number of unique elements `k`. The first `k` elements of `nums` should contain all unique elements in sorted order. Elements beyond index `k - 1` can be ignored.

**Note:** The operation must be performed in-place without using extra space for another array.

### Examples

**Example 1:**

**Input:**
```text
nums = [1,1,2]
```

**Output:**
```text
2, nums = [1,2,_]
```

**Explanation:**

The unique elements are `1` and `2`. The function returns `k = 2`, and the first two positions contain `[1,2]`.

**Example 2:**

**Input:**
```text
nums = [0,0,1,1,1,2,2,3,3,4]
```

**Output:**
```text
5, nums = [0,1,2,3,4,_,_,_,_,_]
```

**Explanation:**

The unique elements are `0`, `1`, `2`, `3`, and `4`. The function returns `k = 5`, with the first five positions containing `[0,1,2,3,4]`.

---

## Constraints

- `1 <= nums.length <= 3 * 10^4`
- `-100 <= nums[i] <= 100`
- `nums` is sorted in non-decreasing order.

---

## Approach: Two Pointers

1. **Initialize the Pointer:** Set `k = 1` because the first element is always unique in a non-empty array.

2. **Traverse the Array:** Start iterating from index `1` using pointer `i`.

3. **Compare Elements:** Compare the current element `nums[i]` with the previous element `nums[i - 1]`.

4. **Identify Unique Elements:** If both elements are different, the current element is unique.

5. **Update the Array:** Place the unique element at index `k` using `nums[k] = nums[i]`, then increment `k`.

6. **Skip Duplicates:** If the current element matches the previous element, skip it without modifying the array.

7. **Return the Count:** Return `k`, representing the total number of unique elements.

---

## Complexity Analysis

| Complexity | Value | Explanation |
|---|---|---|
| Time Complexity | O(n) | Traverses the array exactly once. |
| Space Complexity | O(1) | Modifies the original array without using additional data structures. |

---

## Solution

**Language:** Java

**Data Structure:** Array

**Algorithm:** Two Pointers

**Java Filename:** `RemoveDuplicatesFromSortedArray.java`

---

*Continuing the LeetCode journey — one problem at a time, strengthening problem-solving skills and building consistency in Data Structures and Algorithms.*