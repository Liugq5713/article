## 基本算法

### 常见的排序算法

#### 交换位置

- 冒泡排序：过相邻的比较和交换
- 选择排序：通过对整体的选择

#### 自建位置

- 插入排序：通过比较找到合适的位置插入元素来达到排序的目的

### 实践题

如果是数组，[1,2,3,4,5,6,7,8,9]，采用什么排序方法运算速度最快，为什么

## DOM 操作

### 增删改查

- 查

CSS 选择器

### 如何优化 DOM 操作

> 题目：在页面上输出 1 到 100 ,这段代码有什么问题

```js
for(var i = 1;i≤100;i++){
  document.getElementById('res').innerHTML += ' ' + i;
}

```

- 减少 DOM 访问次数，尽量使用 JavaScript 处理
- 使用局部变量存储 DOM 引用
- 减少重绘和重排

## DOM 事件

### 委托事件至祖先元素

- 事件模型

### 多频事件

某些事件可能会在很短的时间内被触发多次，例如，mousemove、touchmove 等事件。

### 防抖(最后一定会触发)

```js
function debounce(func, wait) {
  let timeout;
  return function() {
    clearTimeout(timeout);
    timeout = setTimeout(func, wait);
  };
}
```

### 节流（一段事件内触发）

```js
function throttle(func, wait) {
  let timeout;
  return function() {
    context = this;
    args = arguments;
    if (!timeout) {
      timeout = setTimeout(function() {
        timeout = null;
        func.apply(context, args);
      }, wait);
    }
  };
}
```

## 常见的项目优化

## vue 相关

## 生命周期

## vue 的双向绑定

## v-model 具体是怎么实现的

## vue 的父子组件通信

## v-if 和 v-show 区别

## 组件重新渲染

- v-if 可以将组件重新渲染
- key 值
