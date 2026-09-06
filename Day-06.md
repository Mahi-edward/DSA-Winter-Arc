# Day 06

## 75. Sort Colors

🧠 **Intuition**

- Divide the array into three regions:
  - `0` → left
  - `1` → middle
  - `2` → right

- `mid` scans the unknown region.
- When `0` → swap with `low`.
- When `1` → already in the correct region.
- When `2` → swap with `high`.

💡 **Key Learning**

- Dutch National Flag Algorithm sorts `0, 1, 2` in **one pass** using three pointers.
- After each operation, maintain the invariant:
  - `[0 ... low-1]` → `0`
  - `[low ... mid-1]` → `1`
  - `[mid ... high]` → unknown
  - `[high+1 ... n-1]` → `2`

🔥 **Trick / Pattern**

- **3 values → 3 pointers → Dutch National Flag.**
- `0` → `low++`, `mid++`
- `1` → `mid++`
- `2` → `high--` **without increasing `mid`** because the swapped value is still unprocessed.

⚠️ **What I Missed**

- I initially solved it using counting + a second pass to overwrite the array.
- I knew the Dutch National Flag approach but had forgotten the core pointer logic.
- Main thing to remember: **`mid` represents the current unknown element.**

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 75](https://leetcode.com/problems/sort-colors/)

---

## 169. Majority Element

🧠 **Intuition**

- The majority element appears more than `n/2` times.
- Maintain a `candidate` and `count`.
- If `count == 0`, choose the current number as the new candidate.
- Same as candidate → `count++`; different → `count--`.
- Since the majority element has more occurrences than all other elements combined, it survives the cancellation.

💡 **Key Learning**

- **Majority element → Moore's Voting Algorithm.**
- We can find it without sorting or extra space.

🔥 **Trick / Pattern**

- **Pair cancellation:** majority element cannot be completely cancelled because it appears more than `n/2`.
- `count == 0` → new candidate.
- Same → `+1`
- Different → `-1`

⚠️ **What I Missed**

- None — I immediately recognized Moore's Voting Algorithm and solved it without a second guess.
- Good sign: I was able to identify the pattern from the **O(1) extra space** requirement.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 169](https://leetcode.com/problems/majority-element/)
