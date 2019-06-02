## 基础

仅仅需要安装 typescript，然后就可以使用 tsc 命令去将 ts 文件转为 js 文件了

`npm install -g typescript`

不过基于项目驱动学习的方法，我是新建了一个使用 ts 的 react 项目

`npx create-react-app my-app --typescript`

一般问题，查一下文档基本就可以解决。我把花时间较多解决的问题记录一下。

## Cannot compile namespaces when the '--isolatedModules' flag is provided

```ts
const obj = {
  name: "lily",
  age: 12
};

Object.keys(obj).map(item => {
  console.log(obj[item]);
  return item;
});
```

这个报错

Turns out A global file cannot be compiled using '--isolatedModules'. Ensure your file contains imports, exports, or an 'export {}' statement.
