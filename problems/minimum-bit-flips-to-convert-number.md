
# 2220. Minimum Bit Flips to Convert Number - 转换数字的最少位翻转次数

## Tags - 题目标签

 <img src="https://img.shields.io/badge/Bit Manipulation-位运算-blue.svg">  


## Description - 题目描述

### EN:
<p>A <strong>bit flip</strong> of a number <code>x</code> is choosing a bit in the binary representation of <code>x</code> and <strong>flipping</strong> it from either <code>0</code> to <code>1</code> or <code>1</code> to <code>0</code>.</p>

<ul>
	<li>For example, for <code>x = 7</code>, the binary representation is <code>111</code> and we may choose any bit (including any leading zeros not shown) and flip it. We can flip the first bit from the right to get <code>110</code>, flip the second bit from the right to get <code>101</code>, flip the fifth bit from the right (a leading zero) to get <code>10111</code>, etc.</li>
</ul>

<p>Given two integers <code>start</code> and <code>goal</code>, return<em> the <strong>minimum</strong> number of <strong>bit flips</strong> to convert </em><code>start</code><em> to </em><code>goal</code>.</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>

<pre>
<strong>Input:</strong> start = 10, goal = 7
<strong>Output:</strong> 3
<strong>Explanation:</strong> The binary representation of 10 and 7 are 1010 and 0111 respectively. We can convert 10 to 7 in 3 steps:
- Flip the first bit from the right: 101<u>0</u> -&gt; 101<u>1</u>.
- Flip the third bit from the right: 1<u>0</u>11 -&gt; 1<u>1</u>11.
- Flip the fourth bit from the right: <u>1</u>111 -&gt; <u>0</u>111.
It can be shown we cannot convert 10 to 7 in less than 3 steps. Hence, we return 3.</pre>

<p><strong>Example 2:</strong></p>

<pre>
<strong>Input:</strong> start = 3, goal = 4
<strong>Output:</strong> 3
<strong>Explanation:</strong> The binary representation of 3 and 4 are 011 and 100 respectively. We can convert 3 to 4 in 3 steps:
- Flip the first bit from the right: 01<u>1</u> -&gt; 01<u>0</u>.
- Flip the second bit from the right: 0<u>1</u>0 -&gt; 0<u>0</u>0.
- Flip the third bit from the right: <u>0</u>00 -&gt; <u>1</u>00.
It can be shown we cannot convert 3 to 4 in less than 3 steps. Hence, we return 3.
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>0 &lt;= start, goal &lt;= 10<sup>9</sup></code></li>
</ul>


### ZH-CN:
<p>一次 <strong>位翻转</strong>&nbsp;定义为将数字&nbsp;<code>x</code>&nbsp;二进制中的一个位进行 <strong>翻转</strong>&nbsp;操作，即将&nbsp;<code>0</code>&nbsp;变成&nbsp;<code>1</code>&nbsp;，或者将&nbsp;<code>1</code>&nbsp;变成&nbsp;<code>0</code>&nbsp;。</p>

<ul>
	<li>比方说，<code>x = 7</code>&nbsp;，二进制表示为&nbsp;<code>111</code>&nbsp;，我们可以选择任意一个位（包含没有显示的前导 0 ）并进行翻转。比方说我们可以翻转最右边一位得到&nbsp;<code>110</code>&nbsp;，或者翻转右边起第二位得到&nbsp;<code>101</code>&nbsp;，或者翻转右边起第五位（这一位是前导 0 ）得到&nbsp;<code>10111</code>&nbsp;等等。</li>
</ul>

<p>给你两个整数&nbsp;<code>start</code> 和&nbsp;<code>goal</code>&nbsp;，请你返回将&nbsp;<code>start</code>&nbsp;转变成&nbsp;<code>goal</code>&nbsp;的&nbsp;<strong>最少位翻转</strong>&nbsp;次数。</p>

<p>&nbsp;</p>

<p><strong>示例 1：</strong></p>

<pre>
<b>输入：</b>start = 10, goal = 7
<b>输出：</b>3
<b>解释：</b>10 和 7 的二进制表示分别为 1010 和 0111 。我们可以通过 3 步将 10 转变成 7 ：
- 翻转右边起第一位得到：101<strong><em>0</em></strong> -&gt; 101<strong><em>1 。</em></strong>
- 翻转右边起第三位：1<strong><em>0</em></strong>11 -&gt; 1<strong><em>1</em></strong>11 。
- 翻转右边起第四位：<strong><em>1</em></strong>111 -&gt; <strong><em>0</em></strong>111 。
我们无法在 3 步内将 10 转变成 7 。所以我们返回 3 。</pre>

<p><strong>示例 2：</strong></p>

<pre>
<b>输入：</b>start = 3, goal = 4
<b>输出：</b>3
<b>解释：</b>3 和 4 的二进制表示分别为 011 和 100 。我们可以通过 3 步将 3 转变成 4 ：
- 翻转右边起第一位：01<strong><em>1</em></strong> -&gt; 01<em><strong>0 </strong></em>。
- 翻转右边起第二位：0<strong><em>1</em></strong>0 -&gt; 0<strong><em>0</em></strong>0 。
- 翻转右边起第三位：<strong><em>0</em></strong>00 -&gt; <strong><em>1</em></strong>00 。
我们无法在 3 步内将 3 变成 4 。所以我们返回 3 。
</pre>

<p>&nbsp;</p>

<p><strong>提示：</strong></p>

<ul>
	<li><code>0 &lt;= start, goal &lt;= 10<sup>9</sup></code></li>
</ul>



## Link - 题目链接

[LeetCode](https://leetcode.com/problems/minimum-bit-flips-to-convert-number/description/)  -  [LeetCode-CN](https://leetcode.cn/problems/minimum-bit-flips-to-convert-number/description/)
## Latest Accepted Submissions - 最近一次 AC 的提交


| Language | Runtime | Memory | Submission Time |
|:---:|:---:|:---:|:---:|
| cpp  | 0 ms | 5.8 MB | 2022/04/03 8:30 |

```cpp

class Solution {
public:
    int minBitFlips(int start, int goal) {
        bitset<32> m,n;
        int num=0;
        m=start;
        n=goal;
        for(int i=0;i<32;i++){
            if(m[i]!=n[i])num++;
            }
        return num;
    }
};
\

```
## My Notes - 我的笔记


No notes

