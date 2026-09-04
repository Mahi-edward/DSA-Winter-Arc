# Day 03

## 283. Move Zeroes

🧠 **Intuition**

- Keep `pos` as the position where the next non-zero should go.
- Scan with `i`.
- When `nums[i] != 0`, swap it with `nums[pos]` and move `pos`.

💡 **Key Learning**

- No need to separately handle `0` and non-zero cases.
- `pos` represents the next position to place a non-zero element.

🔥 **Trick / Pattern**

- **Two pointers + swap:** one pointer scans, one pointer tracks the correct position.
- `pos++` only when a non-zero is found.
- This naturally moves all zeroes to the end while maintaining order.

⚠️ **What I Missed**

- I was thinking separately about `0`s and other numbers.
- The key is to think: **"Where should the next non-zero element go?"**
- The swap works because `pos` always points to the next available position.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 283](https://leetcode.com/problems/move-zeroes/)

---

## 540. Single Element in a Sorted Array

🧠 **Intuition**

- Every element appears twice except one.
- XOR can solve it in `O(n)`, but the sorted array allows `O(log n)` using binary search.
- Before the unique element, pairs start at **even indexes**.
- After the unique element, this pairing pattern shifts.

💡 **Key Learning**

- In binary search, first identify the **index pattern** created by pairs.
- Make `mid` even, then compare the pair:
  `nums[mid]` and `nums[mid + 1]`.
- If they match → unique element is on the right.
- If they don't match → unique element is at `mid` or on the left.

🔥 **Trick / Pattern**

- **Sorted + pairs + one unique → Binary Search.**
- Force `mid` to even:
  `if (mid % 2 == 1) mid--;`
- Pair check:
  `nums[mid] == nums[mid + 1]`
- Match → `left = mid + 2`
- No match → `right = mid`

⚠️ **What I Missed**

- I understood that the side with the odd number of elements contains the unique element, but couldn't translate it into code.
- The key simplification is to **always check an even-indexed `mid` with `mid + 1`**.
- I wasn't initially thinking about the **pair alignment pattern**: `(0,1), (2,3), (4,5)...`

⏱️ **TC / SC**

- TC: `O(log n)`
- SC: `O(1)`

🔗 [LeetCode 540](https://leetcode.com/problems/single-element-in-a-sorted-array/)
