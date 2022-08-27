
# 剑指 Offer 42. 连续子数组的最大和  LCOF - 连续子数组的最大和

## Tags - 题目标签

 <img src="https://img.shields.io/badge/Array-数组-blue.svg">   <img src="https://img.shields.io/badge/Divide and Conquer-分治-blue.svg">   <img src="https://img.shields.io/badge/Dynamic Programming-动态规划-blue.svg">  


## Description - 题目描述

### EN:
English description is not available for the problem. Please switch to Chinese.

### ZH-CN:
<p>输入一个整型数组，数组中的一个或连续多个整数组成一个子数组。求所有子数组的和的最大值。</p>

<p>要求时间复杂度为O(n)。</p>

<p>&nbsp;</p>

<p><strong>示例1:</strong></p>

<pre><strong>输入:</strong> nums = [-2,1,-3,4,-1,2,1,-5,4]
<strong>输出:</strong> 6
<strong>解释:</strong>&nbsp;连续子数组&nbsp;[4,-1,2,1] 的和最大，为&nbsp;6。</pre>

<p>&nbsp;</p>

<p><strong>提示：</strong></p>

<ul>
	<li><code>1 &lt;=&nbsp;arr.length &lt;= 10^5</code></li>
	<li><code>-100 &lt;= arr[i] &lt;= 100</code></li>
</ul>

<p>注意：本题与主站 53 题相同：<a href="https://leetcode-cn.com/problems/maximum-subarray/">https://leetcode-cn.com/problems/maximum-subarray/</a></p>

<p>&nbsp;</p>



## Link - 题目链接

[LeetCode](https://leetcode.com/problems/lian-xu-zi-shu-zu-de-zui-da-he-lcof/description/)  -  [LeetCode-CN](https://leetcode.cn/problems/lian-xu-zi-shu-zu-de-zui-da-he-lcof/description/)
## Latest Accepted Submissions - 最近一次 AC 的提交


| Language | Runtime | Memory | Submission Time |
|:---:|:---:|:---:|:---:|
| cpp  | 20 ms | 22.3 MB | 2022/04/01 10:36 |

```cpp

class Solution {
public:
    int maxSubArray(vector<int>& nums) {
        int pre=0;
        int ans = nums[0];
        for(const auto &x: nums)
        {
            pre = max(pre+x,x);
            ans = max(pre,ans);
        }
        return ans;
    }
};

```
## My Notes - 我的笔记


No notes

