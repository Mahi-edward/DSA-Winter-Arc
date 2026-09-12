# Day 07

## 121. Best Time to Buy and Sell Stock

🧠 **Intuition**

- Keep track of the lowest buying price seen so far.
- For each price, calculate the profit if sold today.
- Keep the maximum profit.

💡 **Key Learning**

- For **buy before sell** problems, maintain the best previous buying value while traversing once.

🔥 **Trick / Pattern**

- **Track minimum → calculate current profit → update maximum.**
- `profit = currentPrice - minPrice`

⚠️ **What I Missed**

- None — solved independently without hesitation.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 121](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)

---

## 53. Maximum Subarray

🧠 **Intuition**

- At every element, decide whether to:
  - extend the previous subarray, or
  - start a new subarray from the current element.

- Keep the largest sum found so far.

💡 **Key Learning**

- **Kadane's Algorithm:** the best subarray ending at the current index depends only on the previous best ending sum.

🔥 **Trick / Pattern**

- `currentSum = max(currentSum + num, num)`
- `maxSum = max(maxSum, currentSum)`
- **Negative running sum → start fresh.**

⚠️ **What I Missed**

- None — solved independently without hesitation.

⏱️ **TC / SC**

- TC: `O(n)`
- SC: `O(1)`

🔗 [LeetCode 53](https://leetcode.com/problems/maximum-subarray/)
