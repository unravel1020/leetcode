
# 剑指 Offer 30. 包含min函数的栈 LCOF - 包含min函数的栈

## Tags - 题目标签

 <img src="https://img.shields.io/badge/Stack-栈-blue.svg">   <img src="https://img.shields.io/badge/Design-设计-blue.svg">  


## Description - 题目描述

### EN:
English description is not available for the problem. Please switch to Chinese.

### ZH-CN:
<p>定义栈的数据结构，请在该类型中实现一个能够得到栈的最小元素的 min 函数在该栈中，调用 min、push 及 pop 的时间复杂度都是 O(1)。</p>

<p>&nbsp;</p>

<p><strong>示例:</strong></p>

<pre>MinStack minStack = new MinStack();
minStack.push(-2);
minStack.push(0);
minStack.push(-3);
minStack.min();   --&gt; 返回 -3.
minStack.pop();
minStack.top();      --&gt; 返回 0.
minStack.min();   --&gt; 返回 -2.
</pre>

<p>&nbsp;</p>

<p><strong>提示：</strong></p>

<ol>
	<li>各函数的调用总次数不超过 20000 次</li>
</ol>

<p>&nbsp;</p>

<p>注意：本题与主站 155 题相同：<a href="https://leetcode-cn.com/problems/min-stack/">https://leetcode-cn.com/problems/min-stack/</a></p>



## Link - 题目链接

[LeetCode](https://leetcode.com/problems/bao-han-minhan-shu-de-zhan-lcof/description/)  -  [LeetCode-CN](https://leetcode.cn/problems/bao-han-minhan-shu-de-zhan-lcof/description/)
## Latest Accepted Submissions - 最近一次 AC 的提交


| Language | Runtime | Memory | Submission Time |
|:---:|:---:|:---:|:---:|
| cpp  | 28 ms | 14.7 MB | 2022/03/16 10:14 |

```cpp

class MinStack {
    stack<int> x_stack;
    stack<int> min_stack;
public:
    /** initialize your data structure here. */
    MinStack() {
    }
    
    void push(int x) {
        x_stack.push(x);
        if(min_stack.empty() || (x<=min_stack.top()))
            min_stack.push(x);
    }
    
    void pop() {
        if(x_stack.top()==min_stack.top())
            min_stack.pop();
        x_stack.pop();
    }
    
    int top() {
        return x_stack.top();
    }
    
    int min() {
        if(min_stack.empty())
            return NULL;
        return min_stack.top();
    }
};

/**
 * Your MinStack object will be instantiated and called as such:
 * MinStack* obj = new MinStack();
 * obj->push(x);
 * obj->pop();
 * int param_3 = obj->top();
 * int param_4 = obj->min();
 */

```
## My Notes - 我的笔记


No notes

