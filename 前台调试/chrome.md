#### 基本输出

- `console.log`
- `console.error`: 错误
- `console.info`: 信息
- `console.warn`: 警告
- `console.debug`: 调试
- `console.clear`: 清空控制台

#### 格式化输出

> 使用占位符输出, 类似 c 语言的 printf
>
> _eg_:`console.log("%c字体大小%c颜色","font-size: 20px","color: red")`

- `%s`: 表示字符串
- `%d`: 表示整数
- `%f`: 表示小数
- `%o`: 表示对象

#### DOM 输出

- `console.dirxml($0)`

#### 对象输出

- `console.dir(obj)`: **输出对象**
- `console.table([{a:'a1',b:'b1'},{a:'a2',b:'b2'}])`: **输出对象集合**

#### 成组输出

```js
console.group("start");
console.log("1");
console.log("2");
console.log("3");
console.groupEnd();
```

#### 函数计数与追踪

- `console.trace()`: 输出 函数调用栈

#### 计时

```js
console.time();
fib(100);
console.timeEnd();
```

#### 断言

> 当第一个表达式或参数为 true 时候什么也不发生，为 false 时终止程序并报错

```js
console.assert(true, "无事发生");
console.assert(false, "断言输出");
```

#### 性能分析 ??

- `console.profile()`
- `console.profileEnd()`

```js
function F() {
  let i = 0;
  function f() {
    while (i++ == 1000);
  }
  f();
}
console.profile();
F();
console.profileEnd();
```

#### Sources 代码调试

- Watch：Watch 表达式
- Call Stack: 栈中变量的调用，这里是递归调用，肯定是在内存栈部分调用。
- Scope：当前作用域变量观察。
- BreakPoints：当前断点变量观察。
- XHR BreakPoints：面向 Ajax，专为异步而生的断点调试功能。
- DOM BreakPoints：主要包括下列 DOM 断点，注册方式见下图：
  - 当节点属性发生变化时断点（Break on attributes modifications）
  - 当节点内部子节点变化时断点（Break on subtree modifications）
  - 当节点被移除时断点（Break on node removal）
- Global Listeners：全局事件监听
- Event Listener Breakpoints：事件监听器断点，列出了所有页面及脚本事件，包括：鼠标、键盘、动画、定时器、XHR 等等

####
