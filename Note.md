## 代码环境
- <script> 标签的 type 属性为 text/babel
- 三个库： react.js 、react-dom.js 和 Browser.js ，它们必须首先加载
- 将 src 子目录的 js 文件进行语法转换，转码后的文件全部放在 build 子目录
```
babel src --out-dir build
```
## ReactDOM.render()
```
ReactDOM.render(
  <html>,
  document.getElementById('dom')
);
```
不能用jquery  [Demo1](demo01/index.html)
## 代码
