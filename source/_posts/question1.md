---
title: 每日一练11111
date: 2017-07-10 10:20:36
tags: 算法题
categories: 算法题
description: 每日一练--首尾交换法
---

## 整数反转--首尾交换法

```js
示例 1：

输入：x = 123
输出：321
示例 2：

输入：x = -123
输出：-321
示例 3：

输入：x = 120
输出：21
示例 4：

输入：x = 0
输出：0
/**
 * @param {number} x
 * @return {number}
 */
var reverse = function (x) {
  const str = Math.abs(x).toString();
  const arr = str.split("");
  let left = 0;
  let right = arr.length - 1;
  while (left < right) {
    [arr[left], arr[right]] = [arr[right], arr[left]];
    left++;
    right--;
  }
  const rever = arr.join("");
  const result = x < 0 ? -rever : +rever;
  const INT_MAX = 2147483647;
  const INT_MIN = -2147483648;
  return result > INT_MAX || result < INT_MIN ? 0 : result;
};
```
