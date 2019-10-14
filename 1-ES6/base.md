#### 声明
- **const** : 声明常量
- **let** : 声明变量
> 作用
- 作用域
    - 全局作用域
    - 函数作用域：`function(){}`
    - 块级作用域：`{}`
- 作用范围
    - `var` 在全局代码中执行
    - `const`和`let`只在代码块中执行
> 重点
- 不允许重复声明
- 未定义不可使用

#### 解构赋值
- **字符串解构**：`const [a,b,c,d,e] = "hello"`
- **数值解构**: `const {toString:s} = 123`
- **布尔值解构**: `const {toString:b} = true`

>应用场景
- 交换变量值：`[x,y]=[y,x]`
- 返回函数多个值：`const [x,y,z] = Func()`
- 提取JSON数据：`const {name,age} = packageJson`
- 遍历Map结构：`for (let [k,v] of Map){}`
- 输入模块指定属性和方法: `const {readFile,writeFile} = require('fs')`

>重点难点
- 匹配模式：只要等号两边的模式相同，左边的变量就会被赋予对应的值
- 解构赋值规则：只要等号右边的值不是对象或数组，就先将其转为对象
- 解构默认值生效条件：属性值严格等于`undefined`
- `undefined`和`null`无法转为对象，因此无法进行解构

#### 数组扩展
- 扩展运算符... 
- Array.from() : 将具有iterator接口的数据结构变成真正的数组
- Array.of()：转换一组值为真正数组，返回新数组
- find()：返回第一个符合条件的成员
- findIndex():返回第一个符合条件成员的索引
- fill()：根据指定值填充整个数组，返回原数组
- keys(): 返回以索引值为遍历器的对象
- values():返回以值为遍历器的对象
- entires(): 返回以索引和属性值为遍历器的对象

>扩展应用
- 克隆数组：`const arr= [...arr] `
- 合并数组： `const arr = [...arr1,..arr2]`   
- 拼接数组： `arr.push(...arr1)`
- 代替apply： `Math.max.apply(null,[x,y] => Max.max(...[x,y])`
- 转换字符串为数组：`[..."hello"]`

#### Class

- 类本身指向构造函数，所有方法定义在prototype上
    - constructor():构造函数
    - extends: 继承父类
    - super: 新建父类this
    - static: 定义静态方法属性
    - get: 取值函数

