
# 3Sum

## LeetCode Problem
[3Sum – LeetCode](https://leetcode.com/problems/3sum/)

**Difficulty:** Medium

**Topics:** [Array](https://leetcode.com/tag/array/), [Two Pointers](https://leetcode.com/tag/two-pointers/), [Sorting](https://leetcode.com/tag/sorting/)

---

## Problem Description

Given an integer array `nums`, return all the triplets `[nums[i], nums[j], nums[k]]` such that:

- `i != j`
- `i != k`
- `j != k`
- `nums[i] + nums[j] + nums[k] == 0`

**Notice:** The solution set must not contain duplicate triplets.

### Examples

**Example 1:**

**Input:**
```text
nums = [-1,0,1,2,-1,-4]
```

**Output:**
```text
[[-1,-1,2],[-1,0,1]]
```

**Explanation:**

The valid triplets are:

- `nums[0] + nums[1] + nums[2] = (-1) + 0 + 1 = 0`
- `nums[1] + nums[2] + nums[4] = 0 + 1 + (-1) = 0`
- `nums[0] + nums[3] + nums[4] = (-1) + 2 + (-1) = 0`

The distinct triplets are `[-1,0,1]` and `[-1,-1,2]`. Duplicate triplets are not included.

**Example 2:**

**Input:**
```text
nums = [0,1,1]
```

**Output:**
```text
[]
```

**Explanation:**

The only possible triplet does not sum up to zero.

**Example 3:**

**Input:**
```text
nums = [0,0,0]
```

**Output:**
```text
[[0,0,0]]
```

**Explanation:**

The only possible triplet sums up to zero.

---

## Constraints

- `3 <= nums.length <= 3000`
- `-10^5 <= nums[i] <= 10^5`

---

## Approach: Sorting + Two Pointers

1. **Sort the Array:** Sort `nums` in ascending order to make it easier to identify triplets and handle duplicates.

2. **Fix the First Element:** Iterate through the array and consider each element as the first element of a potential triplet.

3. **Skip Duplicate Elements:** If the current element is the same as the previous element, skip it to avoid generating duplicate triplets.

4. **Initialize Two Pointers:** Set `left = i + 1` and `right = nums.length - 1` to find the remaining two elements.

5. **Calculate the Sum:** Calculate the sum of the three elements:
   - If the sum is `0`, add the triplet to the result.
   - If the sum is less than `0`, move the left pointer forward to increase the sum.
   - If the sum is greater than `0`, move the right pointer backward to decrease the sum.

6. **Skip Duplicate Pairs:** After finding a valid triplet, move both pointers and skip duplicate values to ensure unique triplets.

7. **Return the Result:** Continue until all possible first elements and pointer combinations have been evaluated.

---

## Complexity Analysis

| Complexity | Value | Explanation |
|---|---|---|
| Time Complexity | O(n²) | Sorting takes O(n log n), followed by an O(n²) two-pointer search. |
| Space Complexity | O(1)* | The sorting and two-pointer approach uses constant auxiliary space, excluding the output and implementation-dependent sorting stack. |

---

## Solution

**Language:** Java

**Data Structure:** Array, List (ArrayList)

**Algorithm:** Sorting + Two Pointers

**Java Filename:** `ThreeSum.java`

---

*Continuing the LeetCode journey — one problem at a time, strengthening problem-solving skills and building consistency in Data Structures and Algorithms.*