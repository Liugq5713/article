# [11. Container With Most Water](https://leetcode.com/problems/container-with-most-water/)

## 我的解决方案

这种思路最简单，遍历所有的`i`，`j`，算出所有的情况

```js
var maxArea = function(height) {
  let maxArea = 0;
  for (let i = 0; i < height.length; i++) {
    for (let j = height.length - 1; j > i; j--) {
      maxArea = Math.max(maxArea, (j - i) * Math.min(height[i], height[j]));
    }
  }
  return maxArea;
};
```

## 优秀的解决方案

该方案也是遍历，但是它去除了一些不必要的遍历

当 height[i] < height[j] 时，我们就不要去计算所有的 (i,j-1)，(i,j-2)...因为由题目规则，面积其实由最小的那个值，即 height[i]决定，且此时面积最大

我根据作者的思路写了一下，但是实际上，作者写的其实更好

### 我的改良代码

```js
var maxArea = function(height) {
  let maxArea = 0;
  for (let i = 0; i < height.length; i++) {
    for (let j = height.length - 1; j > i; j--) {
      maxArea = Math.max(maxArea, (j - i) * Math.min(height[i], height[j]));
      if (height[i] < height[j]) {
        break;
      }
    }
  }
  return maxArea;
};
```

### 优秀解法

个人感觉 while 循环更好理解一点，双层 for 循环让人不太好理解

```js
var maxArea = function(height) {
  let S = 0;
  let i = 0;
  let j = height.lenght - 1;
  let maxArea = 0;
  while (i < j) {
    S = Math.max(S, (j - i) * Math.min(A[i], A[j]));
    if (A[i] < A[j]) {
      i++;
    } else {
      j--;
    }
  }
  return maxArea;
};
```
