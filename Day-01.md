# Day 01

## 1752. Check if Array Is Sorted and Rotated

🔗 [LeetCode](https://leetcode.com/problems/check-if-array-is-sorted-and-rotated/)

🧠 **Intuition**

- Count how many times the array decreases.
- A sorted + rotated array can have at most one such break.

💡 **Key Learning**

- Rotated sorted array → count order breaks.

🔥 **Trick / Pattern**

- Circular next index: `(i + 1) % n`
- At most 1 decreasing pair.

⚠️ **What I Missed**

- I didn't think about the property of a sorted array first.

⏱️ **TC / SC**

- TC: O(n)
- SC: O(1)

## 179. Largest Number

🔗 [LeetCode](https://leetcode.com/problems/largest-number/)

🧠 **Intuition**

- Normal sorting doesn't work because we need the best concatenation.
- Compare `a + b` with `b + a`.
- Put the string producing the larger combination first.

💡 **Key Learning**

- Custom sorting can be based on the final result of combining two elements.

🔥 **Trick / Pattern**

- Largest number → compare `a+b` vs `b+a`.

```java
        Arrays.sort(arr, (a,b) -> {
            return (b + a).compareTo(a + b);
        });
```

⚠️ **What I Missed**

- I initially thought about normal numeric sorting instead of how two numbers should be concatenated.

⏱️ **TC / SC**

- TC: O(n log n × k)
- SC: O(n)
