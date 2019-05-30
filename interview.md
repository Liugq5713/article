- HTML
- CSS
- JS

## 基本算法

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


## webpack打包

webpack构建过程

从entry里配置的module开始递归解析entry依赖的所有module

每找到一个module，就会根据配置的loader去找对应的转换规则
对module进行转换后，再解析出当前module依赖的module
这些模块会以entry为单位分组，一个entry和其所有依赖的module被分到一个组Chunk
最后webpack会把所有Chunk转换成文件输出
在整个流程中webpack会在恰当的时机执行plugin里定义的逻辑

## 常见的DIV布局

- 两栏布局  => BFC

## DOM 事件

### 委托事件至祖先元素

- 事件模型

### 多频事件

某些事件可能会在很短的时间内被触发多次，例如，mousemove、touchmove 等事件。

### 防抖(最后一定会触发)

```js
function debounce(func, wait) {
  let timeout
  return function() {
    clearTimeout(timeout)
    timeout = setTimeout(func, wait)
  }
}
```

### 节流（一段事件内触发）

```js
function throttle(func, wait) {
  let timeout
  return function() {
    context = this
    args = arguments
    if (!timeout) {
      timeout = setTimeout(function() {
        timeout = null
        func.apply(context, args)
      }, wait)
    }
  }
}
```
## 常见的项目优化


## v-if 和 v-show 区别

## v-if可以将组件重新渲染嘛

## vue 父子组件通信

## 异步代码 

promise

获取setTimeout 的值

## 输出

## JQuery链式调用