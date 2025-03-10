# Merge Two Sorted Arrays - LeetCode Problem 88

## Problem Statement
Given two sorted integer arrays `nums1` and `nums2`, merge `nums2` into `nums1` as one sorted array.  
The number of elements initialized in `nums1` is `m` and in `nums2` is `n`.  
You must merge the two arrays by modifying `nums1` in-place without using extra space.

---

## Approach 1: Using Sorting (Your Code)
### **Explanation**
- In this approach, we first copy all elements from `nums2` to the remaining space of `nums1`.
- After that, we use the `sort()` function to sort the merged array.
- This approach is simple but inefficient due to the `O((m+n)log(m+n))` complexity.

### **Steps**
1. Copy elements from `nums2` to the empty spaces of `nums1`.
2. Use `sort()` to arrange elements in ascending order.
3. Return the merged array.

---

## Code (Approach 1)
```cpp
class Solution {
public:
    void merge(vector<int>& nums1, int m, vector<int>& nums2, int n) {
        for (int j = 0, i = m; j<n; j++){
            nums1[i] = nums2[j];
            i++;
        }
        sort(nums1.begin(), nums1.end());
    }
};
