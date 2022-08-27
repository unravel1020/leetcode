
# 950. Reveal Cards In Increasing Order - 按递增顺序显示卡牌

## Tags - 题目标签

 <img src="https://img.shields.io/badge/Queue-队列-blue.svg">   <img src="https://img.shields.io/badge/Array-数组-blue.svg">   <img src="https://img.shields.io/badge/Sorting-排序-blue.svg">   <img src="https://img.shields.io/badge/Simulation-模拟-blue.svg">  


## Description - 题目描述

### EN:
<p>You are given an integer array <code>deck</code>. There is a deck of cards where every card has a unique integer. The integer on the <code>i<sup>th</sup></code> card is <code>deck[i]</code>.</p>

<p>You can order the deck in any order you want. Initially, all the cards start face down (unrevealed) in one deck.</p>

<p>You will do the following steps repeatedly until all cards are revealed:</p>

<ol>
	<li>Take the top card of the deck, reveal it, and take it out of the deck.</li>
	<li>If there are still cards in the deck then put the next top card of the deck at the bottom of the deck.</li>
	<li>If there are still unrevealed cards, go back to step 1. Otherwise, stop.</li>
</ol>

<p>Return <em>an ordering of the deck that would reveal the cards in increasing order</em>.</p>

<p><strong>Note</strong> that the first entry in the answer is considered to be the top of the deck.</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>

<pre>
<strong>Input:</strong> deck = [17,13,11,2,3,5,7]
<strong>Output:</strong> [2,13,3,11,5,17,7]
<strong>Explanation:</strong> 
We get the deck in the order [17,13,11,2,3,5,7] (this order does not matter), and reorder it.
After reordering, the deck starts as [2,13,3,11,5,17,7], where 2 is the top of the deck.
We reveal 2, and move 13 to the bottom.  The deck is now [3,11,5,17,7,13].
We reveal 3, and move 11 to the bottom.  The deck is now [5,17,7,13,11].
We reveal 5, and move 17 to the bottom.  The deck is now [7,13,11,17].
We reveal 7, and move 13 to the bottom.  The deck is now [11,17,13].
We reveal 11, and move 17 to the bottom.  The deck is now [13,17].
We reveal 13, and move 17 to the bottom.  The deck is now [17].
We reveal 17.
Since all the cards revealed are in increasing order, the answer is correct.
</pre>

<p><strong>Example 2:</strong></p>

<pre>
<strong>Input:</strong> deck = [1,1000]
<strong>Output:</strong> [1,1000]
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>1 &lt;= deck.length &lt;= 1000</code></li>
	<li><code>1 &lt;= deck[i] &lt;= 10<sup>6</sup></code></li>
	<li>All the values of <code>deck</code> are <strong>unique</strong>.</li>
</ul>


### ZH-CN:
<p>牌组中的每张卡牌都对应有一个唯一的整数。你可以按你想要的顺序对这套卡片进行排序。</p>

<p>最初，这些卡牌在牌组里是正面朝下的（即，未显示状态）。</p>

<p>现在，重复执行以下步骤，直到显示所有卡牌为止：</p>

<ol>
	<li>从牌组顶部抽一张牌，显示它，然后将其从牌组中移出。</li>
	<li>如果牌组中仍有牌，则将下一张处于牌组顶部的牌放在牌组的底部。</li>
	<li>如果仍有未显示的牌，那么返回步骤 1。否则，停止行动。</li>
</ol>

<p>返回能以<strong>递增顺序</strong>显示卡牌的牌组顺序。</p>

<p>答案中的第一张牌被认为处于牌堆顶部。</p>

<p>&nbsp;</p>

<p><strong>示例：</strong></p>

<pre><strong>输入：</strong>[17,13,11,2,3,5,7]
<strong>输出：</strong>[2,13,3,11,5,17,7]
<strong>解释：
</strong>我们得到的牌组顺序为 [17,13,11,2,3,5,7]（这个顺序不重要），然后将其重新排序。
重新排序后，牌组以 [2,13,3,11,5,17,7] 开始，其中 2 位于牌组的顶部。
我们显示 2，然后将 13 移到底部。牌组现在是 [3,11,5,17,7,13]。
我们显示 3，并将 11 移到底部。牌组现在是 [5,17,7,13,11]。
我们显示 5，然后将 17 移到底部。牌组现在是 [7,13,11,17]。
我们显示 7，并将 13 移到底部。牌组现在是 [11,17,13]。
我们显示 11，然后将 17 移到底部。牌组现在是 [13,17]。
我们展示 13，然后将 17 移到底部。牌组现在是 [17]。
我们显示 17。
由于所有卡片都是按递增顺序排列显示的，所以答案是正确的。
</pre>

<p>&nbsp;</p>

<p><strong>提示：</strong></p>

<ol>
	<li><code>1 &lt;= A.length &lt;= 1000</code></li>
	<li><code>1 &lt;= A[i] &lt;= 10^6</code></li>
	<li>对于所有的&nbsp;<code>i != j</code>，<code>A[i] != A[j]</code></li>
</ol>



## Link - 题目链接

[LeetCode](https://leetcode.com/problems/reveal-cards-in-increasing-order/description/)  -  [LeetCode-CN](https://leetcode.cn/problems/reveal-cards-in-increasing-order/description/)
## Latest Accepted Submissions - 最近一次 AC 的提交


| Language | Runtime | Memory | Submission Time |
|:---:|:---:|:---:|:---:|
| c  | 8 ms | 7.1 MB | 2021/12/18 13:29 |

```c

/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
int cmp(const void *a, const void *b){
    return *(int *)a - *(int *)b;
}
int* deckRevealedIncreasing(int* deck, int deckSize, int* returnSize){
    qsort(deck, deckSize, sizeof(deck[0]), cmp);
    int queuesize = 2 * deckSize;
    int *pos = calloc(deckSize, sizeof(int));
    int *queue = calloc(deckSize, sizeof(int));
    for (int i = 0; i < deckSize; i++) 
    {
        queue[i] = i;
    }
    int l = 0;
    int r = deckSize - 1;
    int loop = 0;
    while (loop < deckSize) 
    {
        pos[loop++] = queue[l];
        l = (l + 1) % deckSize;
        r = (r + 1) % deckSize;
        queue[r] = queue[l];
        l = (l + 1) % deckSize;
    }
    for (int i = 0; i < deckSize; i++) 
    {
        queue[pos[i]] = deck[i];
    }
    free(pos);
    *returnSize = deckSize;
    return queue;
}


```
## My Notes - 我的笔记


No notes

