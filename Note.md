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
## JSX语法
HTML 语言直接写在 JavaScript
```
var names = ['Alice', 'Emily', 'Kate'];

ReactDOM.render(
  <div>
  {
    names.map(function (name, index) {
      return <div key={index}>Hello, {name}!</div>
    })
  }
  </div>,
  document.getElementById('example')
);
```
[Demo2](demo02/index.html)
允许直接在模板插入 JavaScript 变量。如果这个变量是一个数组，则会展开这个数组的所有成员
[Demo3](demo03/index.html)
## 组件
```
// 新版本写法
class Hellodare extends React.Component{
  render(){
    return <h1>Hello {this.props.name}</h1>;
  }
}
```
- 属性值在this.props里
- class名首字母必须大写
- return值不能包含一个以上顶层标签
- 组件属性class 属性需要写成 className ，for 属性需要写成 htmlFor  避免跟js保留字冲突
[Demo4](demo04/index.html)
## this.props.children
