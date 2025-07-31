---
title: 每日一练
date: 2017-07-10 10:20:36
tags: 算法题
categories: 算法题
description : 每日一练--两数之和
---

## 两数之和

```js
示例 1：

输入：nums = [2,7,11,15], target = 9
输出：[0,1]
解释：因为 nums[0] + nums[1] == 9 ，返回 [0, 1] 。
示例 2：

输入：nums = [3,2,4], target = 6
输出：[1,2]
示例 3：

输入：nums = [3,3], target = 6
输出：[0,1]
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function (nums, target) {
const newobj={}
for(let i=0;i<nums.length;i++){
    const compolement=target-nums[i]
    if(compolement in newobj ){
        return [newobj[compolement],i]
    }
    newobj[nums[i]]=i
}
return []
};
```