# 🧠 LeetCode 435 - Non-overlapping Intervals

## 📘 Problem
Given an array of intervals intervals where intervals[i] = [starti, endi], return the minimum number of intervals you need to remove to make the rest of the intervals non-overlapping.

Note that intervals which only touch at a point are non-overlapping. For example, [1, 2] and [2, 3] are non-overlapping.

----
## 🧪 Example

Example 1:

Input: intervals = [[1,2],[2,3],[3,4],[1,3]]
Output: 1
Explanation: [1,3] can be removed and the rest of the intervals are non-overlapping.
Example 2:

Input: intervals = [[1,2],[1,2],[1,2]]
Output: 2
Explanation: You need to remove two [1,2] to make the rest of the intervals non-overlapping.
Example 3:

Input: intervals = [[1,2],[2,3]]
Output: 0
Explanation: You don't need to remove any of the intervals since they're already non-overlapping.

---

## ✅ Approach: Greedy Algorithm

- **Sort intervals by start time**
- Track `prevEnd`, the end of the last non-overlapping interval
- For each interval:
  - If it **doesn't overlap**, update `prevEnd`
  - If it **does overlap**, increment the removal count and keep the interval that ends earlier (to reduce future overlap)

---
