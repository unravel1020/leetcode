
# 539. Minimum Time Difference - 最小时间差

## Tags - 题目标签

 <img src="https://img.shields.io/badge/Array-数组-blue.svg">   <img src="https://img.shields.io/badge/Math-数学-blue.svg">   <img src="https://img.shields.io/badge/String-字符串-blue.svg">   <img src="https://img.shields.io/badge/Sorting-排序-blue.svg">  


## Description - 题目描述

### EN:
Given a list of 24-hour clock time points in <strong>&quot;HH:MM&quot;</strong> format, return <em>the minimum <b>minutes</b> difference between any two time-points in the list</em>.
<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>
<pre><strong>Input:</strong> timePoints = ["23:59","00:00"]
<strong>Output:</strong> 1
</pre><p><strong>Example 2:</strong></p>
<pre><strong>Input:</strong> timePoints = ["00:00","23:59","00:00"]
<strong>Output:</strong> 0
</pre>
<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>2 &lt;= timePoints.length &lt;= 2 * 10<sup>4</sup></code></li>
	<li><code>timePoints[i]</code> is in the format <strong>&quot;HH:MM&quot;</strong>.</li>
</ul>


### ZH-CN:
<p>给定一个 24 小时制（小时:分钟 <strong>"HH:MM"</strong>）的时间列表，找出列表中任意两个时间的最小时间差并以分钟数表示。</p>

<p>&nbsp;</p>

<p><strong>示例 1：</strong></p>

<pre>
<strong>输入：</strong>timePoints = ["23:59","00:00"]
<strong>输出：</strong>1
</pre>

<p><strong>示例 2：</strong></p>

<pre>
<strong>输入：</strong>timePoints = ["00:00","23:59","00:00"]
<strong>输出：</strong>0
</pre>

<p>&nbsp;</p>

<p><strong>提示：</strong></p>

<ul>
	<li><code>2 &lt;= timePoints.length &lt;= 2 * 10<sup>4</sup></code></li>
	<li><code>timePoints[i]</code> 格式为 <strong>"HH:MM"</strong></li>
</ul>



## Link - 题目链接

[LeetCode](https://leetcode.com/problems/minimum-time-difference/description/)  -  [LeetCode-CN](https://leetcode.cn/problems/minimum-time-difference/description/)
## Latest Accepted Submissions - 最近一次 AC 的提交


| Language | Runtime | Memory | Submission Time |
|:---:|:---:|:---:|:---:|
| c  | 12 ms | 8 MB | 2021/11/27 19:23 |

```c

int cmp(const void *a, const void *b)
{
    return *(int *)a - *(int *)b;
}

int min(int a, int b)
{
    return a < b ? a : b;
}

int findMinDifference(char ** timePoints, int timePointsSize){
    int *ret = (int *) malloc( sizeof(int) * timePointsSize );
    int i, ans = 1440;
    int a, b;
    for(i = 0; i < timePointsSize; ++i)
    {
        sscanf(timePoints[i], "%d:%d", &a, &b);             
        ret[i] = a * 60 + b;                                
    }
    qsort(ret, timePointsSize, sizeof(int), cmp);           
    for(i = 1; i < timePointsSize; ++i)
    {
        ans = min(ans, ret[i] - ret[i-1]);                  
    }
    ans = min(ans, ret[0] - ret[timePointsSize-1] + 1440);  
    return ans;
}


```
## My Notes - 我的笔记


No notes

