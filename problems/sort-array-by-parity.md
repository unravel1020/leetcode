
# 905. Sort Array By Parity - 按奇偶排序数组

## Tags - 题目标签

 <img src="https://img.shields.io/badge/Array-数组-blue.svg">   <img src="https://img.shields.io/badge/Two Pointers-双指针-blue.svg">   <img src="https://img.shields.io/badge/Sorting-排序-blue.svg">  


## Description - 题目描述

### EN:
<p>Given an integer array <code>nums</code>, move all the even integers at the beginning of the array followed by all the odd integers.</p>

<p>Return <em><strong>any array</strong> that satisfies this condition</em>.</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>

<pre>
<strong>Input:</strong> nums = [3,1,2,4]
<strong>Output:</strong> [2,4,3,1]
<strong>Explanation:</strong> The outputs [4,2,3,1], [2,4,1,3], and [4,2,1,3] would also be accepted.
</pre>

<p><strong>Example 2:</strong></p>

<pre>
<strong>Input:</strong> nums = [0]
<strong>Output:</strong> [0]
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>1 &lt;= nums.length &lt;= 5000</code></li>
	<li><code>0 &lt;= nums[i] &lt;= 5000</code></li>
</ul>


### ZH-CN:
<p>给你一个整数数组 <code>nums</code>，将 <code>nums</code> 中的的所有偶数元素移动到数组的前面，后跟所有奇数元素。</p>

<p>返回满足此条件的 <strong>任一数组</strong> 作为答案。</p>

<p>&nbsp;</p>

<p><strong>示例 1：</strong></p>

<pre>
<strong>输入：</strong>nums = [3,1,2,4]
<strong>输出：</strong>[2,4,3,1]
<strong>解释：</strong>[4,2,3,1]、[2,4,1,3] 和 [4,2,1,3] 也会被视作正确答案。
</pre>

<p><strong>示例 2：</strong></p>

<pre>
<strong>输入：</strong>nums = [0]
<strong>输出：</strong>[0]
</pre>

<p>&nbsp;</p>

<p><strong>提示：</strong></p>

<ul>
	<li><code>1 &lt;= nums.length &lt;= 5000</code></li>
	<li><code>0 &lt;= nums[i] &lt;= 5000</code></li>
</ul>



## Link - 题目链接

[LeetCode](https://leetcode.com/problems/sort-array-by-parity/description/)  -  [LeetCode-CN](https://leetcode.cn/problems/sort-array-by-parity/description/)
## Latest Accepted Submissions - 最近一次 AC 的提交


| Language | Runtime | Memory | Submission Time |
|:---:|:---:|:---:|:---:|
| c  | 24 ms | 8.9 MB | 2021/11/27 18:00 |

```c

int Qua(int x)
{
    return x & 1;
}

int cmp(const void *a, const void *b)
{
    return Qua(*(int *)a) - Qua(*(int *)b);
}

int* sortArrayByParity(int* nums, int numsSize, int* returnSize){
    int i;
    int *ret = (int *)malloc( sizeof(int) * numsSize );  
    for(i = 0; i < numsSize; ++i)
    {
        ret[i] = nums[i];                                
    }
    qsort(ret, numsSize, sizeof(int), cmp);              
    *returnSize = numsSize;                              
    return ret;
}


```
## My Notes - 我的笔记


No notes

