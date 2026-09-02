# Day 02

## 189. Rotate Array

🧠 **Intuition**

- To rotate right by `k`, reverse the entire array first.
- Then reverse the first `k` elements and the remaining elements.

💡 **Key Learning**

- The 3-reverse trick for right rotation is:
  `reverse(0, n-1) → reverse(0, k-1) → reverse(k, n-1)`

🔥 **Trick / Pattern**

- `k = k % n` handles `k > n`.
- **Right rotate → reverse all → reverse both parts.**

⚠️ **What I Missed**

- I knew the 3-reverse trick but mixed up the ranges.
- Remember: after reversing the whole array, split at `k`.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 189](https://leetcode.com/problems/rotate-array/)

---

## 26. Remove Duplicates from Sorted Array

🧠 **Intuition**

- Use `i` to point to the **last unique element**.
- Use `j` to scan the array.
- When `nums[j]` is new, move `i` forward and copy `nums[j]`.

💡 **Key Learning**

- Two pointers can **scan and update the array in-place**.
- `i` tracks the position where the next unique element should go.

🔥 **Trick / Pattern**

- **Sorted array + remove duplicates → slow/fast pointers.**
- `j` scans, `i` builds the unique portion.

⚠️ **What I Missed**

- I knew `j` helps find new unique elements, but wasn't sure where `i` should start.
- Start `i = 0` because the first element is always unique.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 26](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
