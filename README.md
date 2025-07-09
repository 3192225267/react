# 关于虚拟DOM

1. 本质是Object类型的对象
2. 虚拟DOM比较轻，真实DOM比较重（其实就是虚拟DOM包含的属性比真实DOM少），因为虚拟DOM都是React内部再在用，无需真实DOM上那么多的属性
3. 虚拟DOM最终会被React转为真实DOM，呈现在页面上。



# JSX

> React的文件类型

1. 全称：JavaScript XML
2. react定义的一种类型于XML的JS扩展语法：JS+XML
3. 本质是 React.createElemetn(component,props,children) 方法的语法糖
4. 作用：用来简化创建虚拟DOM
    1. 写法 var ele = <h1> hello </h1>
        1. 注意，它既不是字符串，也不是HTML/XML标签
        2. 它最终产生的就是一个JS对象
    2. 标签名是任意的，HTML标签或者其它三方库标签



## jsx语法规则

1. 定义虚拟DOM时，不要写引号
2. 标签中混入JS表达式时要用{}。
3. 样式的类名指定不要用class，要用className。
4. 内联样式，要用style={{key:value}} 的形式去写。
5. jsx内只可以有一个根标签
6. jsx内的标签必须闭合
7. 标签首字母匹配着不同的渲染规则
    1. 若小写字母开头，则该标签转换为html中同名元素( <span> -> <span>)，若html中无该标签对应的同名元素，则报错
    2. 若大写字母开头，react会将其渲染/转换为组件，若该组件未定义，则报错。
