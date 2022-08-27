
# 剑指 Offer 05. 替换空格 LCOF - 替换空格

## Tags - 题目标签

 <img src="https://img.shields.io/badge/String-字符串-blue.svg">  


## Description - 题目描述

### EN:
<p>English description is not available for the problem. Please switch to Chinese.</p>


### ZH-CN:
<p>请实现一个函数，把字符串 <code>s</code> 中的每个空格替换成&quot;%20&quot;。</p>

<p>&nbsp;</p>

<p><strong>示例 1：</strong></p>

<pre><strong>输入：</strong>s = &quot;We are happy.&quot;
<strong>输出：</strong>&quot;We%20are%20happy.&quot;</pre>

<p>&nbsp;</p>

<p><strong>限制：</strong></p>

<p><code>0 &lt;= s 的长度 &lt;= 10000</code></p>



## Link - 题目链接

[LeetCode](https://leetcode.com/problems/ti-huan-kong-ge-lcof/description/)  -  [LeetCode-CN](https://leetcode.cn/problems/ti-huan-kong-ge-lcof/description/)
## Latest Accepted Submissions - 最近一次 AC 的提交


| Language | Runtime | Memory | Submission Time |
|:---:|:---:|:---:|:---:|
| cpp  | 0 ms | 6 MB | 2022/03/18 8:08 |

```cpp

class Solution {
public:
    string replaceSpace(string s) {
               while(s.find(" ")!=-1)
               {
                             int pos =s.find(" ");
                            
                             s.replace(pos, 1, "%20"); 

               }
return s;
    }
};

```
## My Notes - 我的笔记


No notes

