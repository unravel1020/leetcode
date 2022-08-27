
# 1637. Widest Vertical Area Between Two Points Containing No Points - 两点之间不包含任何点的最宽垂直面积

## Tags - 题目标签

 <img src="https://img.shields.io/badge/Array-数组-blue.svg">   <img src="https://img.shields.io/badge/Sorting-排序-blue.svg">  


## Description - 题目描述

### EN:
<p>Given <code>n</code> <code>points</code> on a 2D plane where <code>points[i] = [x<sub>i</sub>, y<sub>i</sub>]</code>, Return<em>&nbsp;the <strong>widest vertical area</strong> between two points such that no points are inside the area.</em></p>

<p>A <strong>vertical area</strong> is an area of fixed-width extending infinitely along the y-axis (i.e., infinite height). The <strong>widest vertical area</strong> is the one with the maximum width.</p>

<p>Note that points <strong>on the edge</strong> of a vertical area <strong>are not</strong> considered included in the area.</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>
<img alt="" src="https://assets.leetcode.com/uploads/2020/09/19/points3.png" style="width: 276px; height: 371px;" />​
<pre>
<strong>Input:</strong> points = [[8,7],[9,9],[7,4],[9,7]]
<strong>Output:</strong> 1
<strong>Explanation:</strong> Both the red and the blue area are optimal.
</pre>

<p><strong>Example 2:</strong></p>

<pre>
<strong>Input:</strong> points = [[3,1],[9,0],[1,0],[1,4],[5,3],[8,8]]
<strong>Output:</strong> 3
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>n == points.length</code></li>
	<li><code>2 &lt;= n &lt;= 10<sup>5</sup></code></li>
	<li><code>points[i].length == 2</code></li>
	<li><code>0 &lt;= x<sub>i</sub>, y<sub>i</sub>&nbsp;&lt;= 10<sup>9</sup></code></li>
</ul>


### ZH-CN:
<p>给你 <code>n</code> 个二维平面上的点 <code>points</code> ，其中 <code>points[i] = [x<sub>i</sub>, y<sub>i</sub>]</code> ，请你返回两点之间内部不包含任何点的 <strong>最宽垂直面积</strong> 的宽度。</p>

<p><strong>垂直面积</strong> 的定义是固定宽度，而 y 轴上无限延伸的一块区域（也就是高度为无穷大）。 <strong>最宽垂直面积</strong> 为宽度最大的一个垂直面积。</p>

<p>请注意，垂直区域 <strong>边上</strong> 的点 <strong>不在</strong> 区域内。</p>

<p> </p>

<p><strong>示例 1：</strong></p>
<img alt="" src="https://assets.leetcode-cn.com/aliyun-lc-upload/uploads/2020/10/31/points3.png" style="width: 276px; height: 371px;" />​
<pre>
<b>输入：</b>points = [[8,7],[9,9],[7,4],[9,7]]
<b>输出：</b>1
<b>解释：</b>红色区域和蓝色区域都是最优区域。
</pre>

<p><strong>示例 2：</strong></p>

<pre>
<b>输入：</b>points = [[3,1],[9,0],[1,0],[1,4],[5,3],[8,8]]
<b>输出：</b>3
</pre>

<p> </p>

<p><strong>提示：</strong></p>

<ul>
	<li><code>n == points.length</code></li>
	<li><code>2 <= n <= 10<sup>5</sup></code></li>
	<li><code>points[i].length == 2</code></li>
	<li><code>0 <= x<sub>i</sub>, y<sub>i</sub> <= 10<sup>9</sup></code></li>
</ul>



## Link - 题目链接

[LeetCode](https://leetcode.com/problems/widest-vertical-area-between-two-points-containing-no-points/description/)  -  [LeetCode-CN](https://leetcode.cn/problems/widest-vertical-area-between-two-points-containing-no-points/description/)
## Latest Accepted Submissions - 最近一次 AC 的提交


| Language | Runtime | Memory | Submission Time |
|:---:|:---:|:---:|:---:|
| c  | 220 ms | 27.7 MB | 2021/12/17 22:15 |

```c

int Cmp(const void *a, const void *b)
{
    return *(int *)a - *(int *)b;
}
int maxWidthOfVerticalArea(int** points, int pointsSize, int* pointsColSize)
{
    int *tmp = (int *)malloc(pointsSize * sizeof(int));
    int count = 0;
    for (int i = 0; i < pointsSize; i++) {
        tmp[count++] = points[i][0];
    }
    qsort(tmp, count, sizeof(int), Cmp);
    int ret = 0;
    for (int j = 0; j < count - 1;  j++) {
        ret = fmax(tmp[j + 1] - tmp[j], ret);
    }
    return ret;
}


```
## My Notes - 我的笔记


No notes

