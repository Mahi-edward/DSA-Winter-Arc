# Day 08

## 31. Next Permutation

🧠 **Intuition**

- Find the first decreasing point from the right (`pivot`).
- Find the smallest larger element from the right and swap it with the pivot.
- Reverse the suffix after the pivot to get the next smallest arrangement.

💡 **Key Learning**

- Next permutation = **find pivot → swap with rightmost larger → reverse suffix**.
- If no pivot exists, the array is in descending order, so reverse the entire array.

🔥 **Trick / Pattern**

- Scan from right to find:
  `nums[i] < nums[i + 1]`
- Find rightmost `nums[i] > nums[pivot]`.
- Reverse `pivot + 1 → n - 1`.

⚠️ **What I Missed**

- Newly learned problem.
- I was able to think of the brute-force permutation idea, but learned the optimal in-place approach and solved it.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 31](https://leetcode.com/problems/next-permutation/)

---

## 128. Longest Consecutive Sequence

🧠 **Intuition**

- Store all numbers in a `HashSet` for `O(1)` lookup.
- Only start counting when `num - 1` does not exist.
- Then keep checking `num + 1`, `num + 2`, etc.

💡 **Key Learning**

- Don't start a sequence from every number.
- **Start only from the beginning of a sequence** (`num - 1` doesn't exist).
- HashSet gives fast lookup and avoids duplicates.

🔥 **Trick / Pattern**

- `!set.contains(num - 1)` → sequence start.
- `while (set.contains(current + 1))` → extend sequence.
- **HashSet + sequence-start check → O(n).**

⚠️ **What I Missed**

- I initially knew only the `O(n²)` approach.
- Learned the HashSet approach and the important idea of checking whether `num - 1` exists before starting a sequence.

⏱️ **TC / SC**

- TC: `O(n)` average
- SC: `O(n)`

🔗 [LeetCode 128](https://leetcode.com/problems/longest-consecutive-sequence/)
