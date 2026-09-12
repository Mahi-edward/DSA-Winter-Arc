# Day 09

## 48. Rotate Image

🧠 **Intuition**

- Rotate the matrix 90° clockwise in two steps:
  1. Transpose the matrix.
  2. Reverse every row.

💡 **Key Learning**

- The key pattern for **90° clockwise rotation** is:
  **Transpose + Reverse each row.**
- Important to transpose only the upper triangle to avoid swapping twice.

🔥 **Trick / Pattern**

- `Transpose → Reverse rows`
- Transpose: `matrix[i][j] ↔ matrix[j][i]`
- Reverse each row using two pointers.

⚠️ **What I Missed**

- I had solved this problem before but forgot the key pattern.
- Recalled **transpose + reverse each row** and solved it.

⏱️ **TC / SC**

- TC: `O(n²)`
- SC: `O(1)`

🔗 [LeetCode 48](https://leetcode.com/problems/rotate-image/)

---

## 73. Set Matrix Zeroes

🧠 **Intuition**

- First scan the matrix and remember which rows and columns contain `0`.
- Use two boolean arrays:
  - `rowsZeros` → zero rows
  - `colsZeros` → zero columns

- Second pass sets the required rows and columns to `0`.

💡 **Key Learning**

- We don't need to store every zero's position.
- Just track **which rows and columns need to become zero**.

🔥 **Trick / Pattern**

- **Matrix zeroing → mark rows + columns first, update later.**
- `boolean[] rowsZeros`
- `boolean[] colsZeros`
- Separate **identify** and **modify** phases to avoid newly created zeros affecting the scan.

⚠️ **What I Missed**

- Initially I thought of storing all zero positions in a `Set` and then processing them.
- The boolean-array approach is simpler and more efficient.
- Important idea: **first mark, then modify.**

⏱️ **TC / SC**

- TC: `O(n × m)`
- SC: `O(n + m)`

🔗 [LeetCode 73](https://leetcode.com/problems/set-matrix-zeroes/)
