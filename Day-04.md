# Day 04

## 136. Single Number

🧠 **Intuition**

- Every number appears twice except one.
- XOR cancels equal numbers: `a ^ a = 0`.
- `0 ^ x = x`, so only the single number remains.

💡 **Key Learning**

- XOR can be used to find the element that appears once when all others appear twice.

🔥 **Trick / Pattern**

- `a ^ a = 0`
- `a ^ 0 = a`
- **Pairs cancel → unique remains.**

⚠️ **What I Missed**

- None — solved independently.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 136](https://leetcode.com/problems/single-number/)

---

## 485. Max Consecutive Ones

🧠 **Intuition**

- Keep counting consecutive `1`s.
- When `0` appears, reset the count to `0`.
- Keep updating the maximum count.

💡 **Key Learning**

- For consecutive-element problems, maintain a **current count** and **maximum count**.

🔥 **Trick / Pattern**

- `1` → increment current count.
- `0` → reset current count.
- `max = Math.max(max, currentCount)`.

⚠️ **What I Missed**

- None — solved independently.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 485](https://leetcode.com/problems/max-consecutive-ones/)
