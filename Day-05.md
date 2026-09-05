# Day 05

## 1. Two Sum

🧠 **Intuition**

- Traverse the array and store previous values in a HashMap.
- For current value `nums[i]`, find its required pair:
  `target - nums[i]`.
- If the pair already exists, return its index and current index.

💡 **Key Learning**

- **HashMap turns repeated searching into O(1) lookup.**
- Instead of finding the pair after reaching an element, check whether its complement was already seen.

🔥 **Trick / Pattern**

- `complement = target - current`
- **Store previous → check complement.**

⚠️ **What I Missed**

- None — solved independently on the first try.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(n)`

🔗 [LeetCode 1](https://leetcode.com/problems/two-sum/)

---

## 2. Subarray Sum Equals K

🧠 **Intuition**

- Brute force checks every subarray → `O(n²)`.
- Use prefix sum to represent the sum from the beginning up to the current index.
- If:
  `currentPrefix - previousPrefix = k`
- Then:
  `previousPrefix = currentPrefix - k`
- So check whether `currentPrefix - k` has appeared before.

💡 **Key Learning**

- **Exact subarray sum + negative numbers → Prefix Sum + HashMap.**
- Store the **frequency** of previous prefix sums because the same prefix sum can occur multiple times.

🔥 **Trick / Pattern**

- Key question:
  **"Have I seen `currentSum - k` before?"**
- If yes:
  `count += frequency[currentSum - k]`
- Initialize:
  `map.put(0, 1)`
  → represents a prefix sum of `0` before the array starts.
- **Prefix Sum + HashMap → count subarrays with exact sum K.**

⚠️ **What I Missed**

- I could solve it using brute force `O(n²)`, but couldn't derive the optimal approach.
- The key observation is:
  `subarray sum = currentPrefix - previousPrefix`
- Rearrange it to:
  `previousPrefix = currentPrefix - k`
- This converts the problem into a **HashMap lookup**.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(n)`

🔗 [LeetCode 560](https://leetcode.com/problems/subarray-sum-equals-k/)
