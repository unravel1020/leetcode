
# 1492. The kth Factor of n - n 的第 k 个因子

## Tags - 题目标签

 <img src="https://img.shields.io/badge/Math-数学-blue.svg">  


## Description - 题目描述

### EN:
<p>You are given two positive integers <code>n</code> and <code>k</code>. A factor of an integer <code>n</code> is defined as an integer <code>i</code> where <code>n % i == 0</code>.</p>

<p>Consider a list of all factors of <code>n</code> sorted in <strong>ascending order</strong>, return <em>the </em><code>k<sup>th</sup></code><em> factor</em> in this list or return <code>-1</code> if <code>n</code> has less than <code>k</code> factors.</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>

<pre>
<strong>Input:</strong> n = 12, k = 3
<strong>Output:</strong> 3
<strong>Explanation:</strong> Factors list is [1, 2, 3, 4, 6, 12], the 3<sup>rd</sup> factor is 3.
</pre>

<p><strong>Example 2:</strong></p>

<pre>
<strong>Input:</strong> n = 7, k = 2
<strong>Output:</strong> 7
<strong>Explanation:</strong> Factors list is [1, 7], the 2<sup>nd</sup> factor is 7.
</pre>

<p><strong>Example 3:</strong></p>

<pre>
<strong>Input:</strong> n = 4, k = 4
<strong>Output:</strong> -1
<strong>Explanation:</strong> Factors list is [1, 2, 4], there is only 3 factors. We should return -1.
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>1 &lt;= k &lt;= n &lt;= 1000</code></li>
</ul>

<p>&nbsp;</p>
<p><strong>Follow up:</strong></p>

<p>Could you solve this problem in less than O(n) complexity?</p>


### ZH-CN:
<p>给你两个正整数&nbsp;<code>n</code> 和&nbsp;<code>k</code>&nbsp;。</p>

<p>如果正整数 <code>i</code> 满足 <code>n % i == 0</code> ，那么我们就说正整数 <code>i</code> 是整数 <code>n</code>&nbsp;的因子。</p>

<p>考虑整数 <code>n</code>&nbsp;的所有因子，将它们 <strong>升序排列</strong>&nbsp;。请你返回第 <code>k</code>&nbsp;个因子。如果 <code>n</code>&nbsp;的因子数少于 <code>k</code>&nbsp;，请你返回 <code>-1</code>&nbsp;。</p>

<p>&nbsp;</p>

<p><strong>示例 1：</strong></p>

<pre>
<strong>输入：</strong>n = 12, k = 3
<strong>输出：</strong>3
<strong>解释：</strong>因子列表包括 [1, 2, 3, 4, 6, 12]，第 3 个因子是 3 。
</pre>

<p><strong>示例 2：</strong></p>

<pre>
<strong>输入：</strong>n = 7, k = 2
<strong>输出：</strong>7
<strong>解释：</strong>因子列表包括 [1, 7] ，第 2 个因子是 7 。
</pre>

<p><strong>示例 3：</strong></p>

<pre>
<strong>输入：</strong>n = 4, k = 4
<strong>输出：</strong>-1
<strong>解释：</strong>因子列表包括 [1, 2, 4] ，只有 3 个因子，所以我们应该返回 -1 。
</pre>

<p>&nbsp;</p>

<p><strong>提示：</strong></p>

<ul>
	<li><code>1 &lt;= k &lt;= n &lt;= 1000</code></li>
</ul>

<p>&nbsp;</p>

<p><strong>进阶：</strong></p>

<p>你可以设计时间复杂度小于 O(n) 的算法来解决此问题吗？</p>



## Link - 题目链接

[LeetCode](https://leetcode.com/problems/the-kth-factor-of-n/description/)  -  [LeetCode-CN](https://leetcode.cn/problems/the-kth-factor-of-n/description/)
## Latest Accepted Submissions - 最近一次 AC 的提交


| Language | Runtime | Memory | Submission Time |
|:---:|:---:|:---:|:---:|
| c  | 0 ms | 5.6 MB | 2021/11/24 19:36 |

```c

int kthFactor(int n, int k){
int i;
int count=0;
for(i=1;i<=n;i++)
    if(n%i==0)
        {
        count++;
        if(count==k)
            {
            return i;
            }
        }
return -1;
}

```
## My Notes - 我的笔记


No notes

