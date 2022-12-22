# Web APl 基本认知

## DOM对象

* 浏览器根据html标签生成的js对象
  * 所有的标签属性都可以在这个对象上面找到
  * 修改这个对象的属性会自动映射到标签身上
* DOM核心思想
  * 把网页内容当做==对象==来处理
* document对象
  * 是DOM里提供的一个==对象==
  * 所以它提供的属性和方法都是==用来访问和操作网页内容的==
  * 网页所有内容都在document里面

---



# 获取DOM对象

## 根据CSS选择器来获取DOM元素

### 选择匹配的第一个元素

**语法：**

`    document.querySelector('CSS选择器')`

**参数**

包含一个或多个有效的CSS选择器 ==字符串==

**返回值**

CSS选择器匹配的==第一个元素==，一个`HTMLElement`对象

如果没有匹配到，则返回`null`

### 选择匹配的多个元素

**语法：**

`document.querySelectorAll('CSS选择器')`

**参数**

包含一个或多个有效的css选择器==字符串==

**返回值**

CSS选择器匹配的==NodeList 对象集合==

**例如：**

```javascript
document.querySelectorAll('ul li');
```

得到的是一个==伪数组==

* 有长度有索引号的数组
* 但是没有pop()等数组方法

利用for遍历伪数组得到每一个对象

```javascript
let lis = document.querySelectorAll('ul li');
      for (let i = 0; i < lis.length; i++) {
        console.log(lis[i]);
      }
```

> 注意事项：哪怕只有一个元素，通过`querySelectorAll()`获取过来的也是一个伪数组，里面只有一个元素而已

其他获取元素的方法 （了解）

根据id获取一个元素： `document.getElementById('ID名');`

根据标签获取一类元：`document.getElementsByClassName('标签');`

根据类名获取元素：` document.getElementsByName('类名');`

---

# 设置/修改DOM元素内容

1.`   document.write()`方法：只能追加到body中

2.`元素.innerText`属性 ：只识别内容，不能解析标签

3.`元素.innerHTML` 属性：能够解析标签

# 设置/修改DOM元素属性

## 设置/修改元素常用属性

语法： `对象.属性 = 值`

例子：

```javascript
let pic = document.querySelector('img');
      pic.src = './images/2.webp';
```

## 设置/修改元素样式属性

1. ### 通过style属性操作CSS

**语法：**`对象.style.样式属性 = 值`

**例子：**

```javascript
 let box = document.querySelector('div');
      //   对象.style.样式属性 = 值
      box.style.backgroundColor = 'hotpink';
      box.style.width = '300px';
```

> 注意：
>
> 1. 修改样式通过`style`属性引出
> 2. 如果属性有`-`连接符，需要转换为小驼峰命名法
> 3. 赋值的时候，需要的时候不要忘记加css单位

---

2. ### 操作类名(className)操作CSS

**语法：**`元素.className = '类名'`

> **注意**
>
> 1. 由于`class`是关键字，所以使用`className`去代替
> 2. `className`是使用新值**换**旧值，如果需要添加一个类，需要保留之前的类名

3. ### 通过classList操作类控制CSS

**语法：**

1. `box.classList.add('类名');`：追加一个类
2. ` box.classList.remove('类名');`：移除一个类
3. ` box.classList.toggle('类名');`：//切换类 如果有这个类则移除，没有则添加
4. `box.classList.contains('类名');`:看看有没有这个类，如果有返回`true` ，否则返回`false`

---

##　修改／设置表单元素属性

**语法：**

* 获取：`DOM对象.属性名` `表单.value = '用户名'`
* 设置：`DOM对象.属性名 = 新值`

表单属性中添加就有效果，移除就没有效果，一律使用布尔值表示 如果为`true`代表添加了该属性，如果是`false`代表移除了该属性

比如：`disabled`、`checked`、`selected`

例如：

```javascript
let checkbox = document.querySelector('input');
      checkbox.checked = true; // 默认勾选
```

---

# 定时器-间歇函数

**开启定时器**

`setInterval(函数, 间隔时间);`

* 作用：每隔一段时间调用这个函数
* 间隔时间单位是毫秒

```javascript
setInterval(function () {
        document.write(1);
      }, 1000);
//或者
      function show() {
        document.write(2);
      }
      setInterval(show, 1000);
```

**关闭定时器**

```javascript
let 变量名 = setInterval(函数, 间隔时间);
clearInterval(变量名);
```

---

# 事件

## 事件监听

**什么是事件监听？**：让程序检测是否有事件产生，一旦有事件触发，就立即调用一个函数做出相应，也称为注册事件

**语法：**

`元素.addEventListener('事件', 要执行的函数);`

* 事件监听三要素
  * 事件源：哪个DOM元素被事件触发了，要获取DOM元素
  * 事件：用什么方式触发，单击 `click` 鼠标经过 `mouseover` 等
  * 事件调用的函数：要做什么事

**举例说明**

```javascript
  // 1.获取元素
      let btn = document.querySelector('button');
    //   2. 事件监听
      btn.addEventListener('click', function () {
        alert('被点击了');
      });
```

> 注意：
>
> 1. 事件监听要**加引号**
> 2. 函数是点击之后再去执行，每次点击都会执行一次

## 事件类型

##### 鼠标事件

`click`：鼠标点击 `mouseenter` ：鼠标经过 `mouseleave`：鼠标离开

##### 焦点事件

`focus`:获得焦点 `blur`：失去焦点

##### 键盘事件

`keydown`:键盘按下触发 `keyup`：键盘抬起触发

##### 文本事件

`input`：用户输入事件



##### 表单域提交

`submit`

##### 改变事件

`change`:当表单里面的值发生变化的时候触发

---

# 高阶函数

==高阶函数==可以简单理解为函数的高级运用，JavaScript中函数可以被当成【值】来对待，基于这个特性实现函数的高级应用

【值】就是JavaScript中的数据，如数值，字符串，布尔，对象等

##### 1.1 函数表达式 

函数表达式和普通函数并无本质上的区别：

```javascript
//函数表达式与普通函数本质上是一样的
let counter = function(x,y) {
    return x + y
}
// 调用函数
let result = counter(5,10)
console.log(result)
```

##### 回调函数

如果函数A做为参数传递给函数 B 时，我们称函数A为==回调函数==

简单理解：当一个函数当做参数来传递给另外一个函数是，这个函数就是==回调函数==

* 常见的使用场景:

  ```javascript
  function fn() {
      console.log('我是回调函数...')
  }
  setInteval(fn,1000)
  ```

  

# 环境对象

环境对象指的是函数内部特殊的==变量 this==，它代表着当前函数运行时所处的环境

**作用：**弄清楚this的指向，可以让我们代码更简洁

* 函数的调用方式不同，this 指代的对象也不同
* ==【谁调用， this 就是谁】== 是判断 this 指向的粗略规则

* 直接调用函数，其实相当于是 window.函数，所以 this 指代 window

---

# 编程思想

## 排他思想

当前元素为A状态,其他元素为B状态

**使用：**

1. 干掉所用人
   1. 使用for循环
2. 复活他自己
   1. 通过this或者下标找到自己或者对应的元素

> 个人理解：
>
> 当点击后，把所有同类型元素的样式干掉，给自己添加单独的元素

---

# 节点操作

## DOM节点

* DOM节点
  * DOM树里每个内容都称之为节点
* 节点类型
  * ==元素节点==
    * 所有的标签 比如body、div
    * html是根节点
  * 属性节点
    * 所有的属性 比如 href
  * 文本节点
    * 所有的文本
  * 其他 

---

## 查找节点

* 节点关系
  * 父节点
  * 子节点
  * 兄弟节点

##### 父节点查找：

* `parentNode`属性
* 返回最近一级的父节点 找不到返回为null
* `子元素.parentNode`

```html
<body>
    <div class="faher">
      <div class="son">儿子</div>
    </div>
    <script>
      let son = document.querySelector('.son');
      son.parentNode.style.display = 'none';
    </script>
  </body>
```

##### 子节点查找

* `childNodes`

  * 获得所有子节点、包括文本节点（空格、换号）、注释节点等

* ==children==

  * 仅获得所有元素节点
  * 返回的还是一个伪数组

  `父元素.children`

**例子**

```html
<body>
    <button>点击</button>
    <ul>
      <li>我是孩子</li>
      <li>我是孩子</li>
      <li>我是孩子</li>
      <li>我是孩子</li>
      <li>我是孩子</li>
      <li>我是孩子</li>
    </ul>
    <script>
      let btn = document.querySelector('button');
      let ul = document.querySelector('ul');
      btn.addEventListener('click', function () {
        // console.log(ul.children);
        for (let i = 0; i < ul.children.length; i++) {
          ul.children[i].style.color = 'red';
        }
      });
    </script>
```

---

##### 查找兄弟节点

1. 下一个兄弟节点

​	`nextElementSibling`属性

2. 上一个兄弟节点

   `previousElementSibling`属性

```html
<body>
    <button>点击</button>
    <ul>
      <li>1</li>
      <li class="test">2</li>
      <li>3</li>
      <li>4</li>
    </ul>
    <script>
      let btn = document.querySelector('button');
      let test = document.querySelector(['.test']);
      btn.addEventListener('click', function () {
        //上一个
        test.nextElementSibling.style.color = 'red';
        // 下一个
        test.previousElementSibling.style.color = 'red';
      });
    </script>
  </body>
```

---

##　增加节点

#####　创建节点

**创建节点方法**

```javascript
document.createElement('标签名')
```

**2.追加节点**

* 要想界面看到，还得插入到某个父元素中

* 插入到父元素的最后一个子元素：

  `父元素.appendChild(子元素)`

* 插入到父元素中某个子元素的前面

  `父元素.insertBefore(子元素，放到那个元素前面)`

 ##### 复制节点

**克隆节点**

` 元素.clongNode(布尔值)`

> `cloneNode`会克隆出一个跟原标签一样的元素，括号内传入`布尔值`
>
> * 若为`true`，则代表克隆时会包含后代节点一起克隆
> * 若为`false`，则代表克隆时不包含后代节点
> * 默认为`false`

---

##### 删除节点

* 若一个节点在页面中不需要时，可以删除他

* 在JavaScript原生DOM操作中，要删除元素必须通过==父元素==删除

* **语法**

  ```javascript
  父元素.removeChild(子元素)
  ```

> 注意:
>
> ​	如果不存在父子关系则删除不成功
>
> ​	删除节点和隐藏节点(`dispaly:none`)有区别的：隐藏节点还是存在的，但是删除，则从html中删除节点

---

# 时间对象

* 时间对象：用来表示时间的对象
* 作用：可以得到当前系统时间



## 实例化

* 在代码中发现了 new 关键字时，一般将这个操作称为==实例化==

* 创建一个事件对象获取事件

  * 获得当前时间：

    ```javascript
    let date = new Date()//小括号为空可以得到当前时间
    ```

  * 获得指定时间

    ```javascript
    let date = new Date('1949-10-01')
    ```

    

---

## 时间对象方法

* 因为时间对象返回的数据我们不能够直接使用，所以需要转换为实际开发中常用的格式

|      方法       |        作用        |         说明         |
| :-------------: | :----------------: | :------------------: |
| `getFullYear()` |      获得年份      |    获取四位数年份    |
|  `getMonth()`   |      获得月份      |    取值为==0~1==     |
|   `getDate()`   | 获取月份中的每一天 | 不同月份取值也不相同 |
|   `getDay()`    |      获取星期      |    取值为==0~6==     |
|  `getHours()`   |      获取小时      |      取值为0~23      |
| `getMinutes()`  |      获取分钟      |      取值为0~59      |
| `getSeconds()`  |       获取秒       |      取值为0~59      |

```javascript
let date = new Date();
      //   年月日
      console.log(date.getFullYear()); //年份
      console.log(date.getMonth() + 1); //月份
      console.log(date.getDate()); //日
      //   时分秒
      console.log(date.getHours()); //时
      console.log(date.getMinutes()); //分
      console.log(date.getSeconds()); //秒
      console.log(date.getDay()); //星期
```

**案例代码** 

```javascript
 let arr = [
        '星期天',
        '星期一',
        '星期二',
        '星期三',
        '星期四',
        '星期五',
        '星期六',
      ];
      //   先调用，就省去了一秒空白
      getTime();
      setInterval(getTime, 1000);
      function getTime() {
        let date = new Date();
        let nian = date.getFullYear(); //年
        let yue = date.getMonth() + 1; //月
        let ri = date.getDate(); //日
        let hour = date.getHours(); //时
        let branch = date.getMinutes(); //分
        let second = date.getSeconds(); //秒
        let week = date.getDay(); //星期
        hour < 10 ? (hour = '0' + hour) : hour;
        branch < 10 ? (branch = '0' + branch) : branch;
        second < 10 ? (second = '0' + second) : second;
        h4.innerHTML = `当前时间为：${nian}年${yue}月${ri}日${hour}时${branch}分${second}秒 ${arr[week]}`;
      }
```

---

## 时间戳

* 什么是时间戳

  * 是指1970年01月01日00时00分00秒起至现在的==毫秒数==，他是一种特殊的计量时间的方式

* 三种方式获得时间戳

   1. 使用 getTime() 方法

      ```javascript
      //1. 实例化
      let date = new Date()
      // 2. 获取时间戳
      console.log(date.getTime)
      ```

      

   2. ==2. 简写 +new Date()==

      ```javascript
      console.log(+new Date())
      ```

      

   3. . 使用 Date().now()

      ```javascript
      console.log(Date.now())
      ```

      

      * 无需实例化
      * ==但是只能得到当前的时间戳， 而前面两种可以返回指定时间的时间戳==

---

# 事件对象

## 获取事件对象

* 事件对象是什么

  * 也是一个对象，这个对象里有事件触发的相关信息

* 如何获取

  * 在事件绑定的回调函数的第一个参数就是事件对象

  * 一般命名为event、ev、e

  * ```javascript
    元素.addEventListener('click',function(e){
        
    })
    ```

  * 

## 事件对象常用属性

* 部分常用属性
  * `type`
    * 获取当前的事件类型
  * `clientX`/`clientY`
    * 获取光标相对于浏览器可见窗口左上角的位置
  * `offsetX`/`offsetY`
    * 获取光标相对于当前DOM元素左上角的位置
  * `key`
    * 用户按下的键盘键的值
    * 现在不提倡使用`keyCode`

---

# 事件流

## 事件流和两个阶段说明

* ==事件流==指的是事件完整执行过程中的流动路径

![image-20221127154741160](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221127154741160.png)

* 说明：假设页面里有个div，当触发事件时，会经历两个阶段，分别是捕获阶段、冒泡阶段
* 简单来说：捕获阶段是 从父到子 冒泡阶段是从子到父

## 事件捕获和事件冒泡

##### 事件冒泡概念

当一个元素的事件被触发时，同样的事件将会在该元素的所有祖先元素中依次被触发。这一过程被称为事件冒泡

* 简单理解：当一个元素触发事件后，会依次向上调用所有父级元素的同名事件
* 事件冒泡是默认存在的

![image-20221127154949024](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221127154949024.png)

---

##### 事件捕获概念

从DOM的根元素开始去执行对应的事件 (从外到里)

* 事件捕获需要写对于代码才能看到效果

* 代码：

  ```javascript
  DOM.ddEventListener(事件类型,事件处理函数,是否使用捕获机制)
  ```

>* 说明
>  * `addEventListener`第三个参数传入`true`代表是捕获阶段触发（很少使用）
>  * 若传入`false`代表冒泡阶段触发，默认就是`false`
>  * 若是用 L0 事件监听，则只有冒泡阶段，没有捕获
>
>

---

## 阻止事件流动

* 因为默认就有冒泡模式的存在，所以容易导致事件影响到父级元素
* 若想把事件就限制在当前元素内，就需要阻止事件流动
* 阻止事件流动需要拿到事件对象
* 语法：

```javascript
事件对象.stopPropagation()
```

* 此方法可以阻断事件流动传播，不光在冒泡阶段有效，捕获阶段也有效

##### 鼠标经过事件：

`mouseover` 和 `mouseout` 会有冒泡效果

`mouseenter` 和 `mouseleave`没有冒泡效果(推荐)

`mousemove`:鼠标移动 `mouseleave`:鼠标移出

---

##### 阻止默认行为

比如链接点击不跳转，表单域不提交

* 语法：
* `e.preventDefault()`

![image-20221127155652166](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221127155652166.png)

---

##### 俩种注册事件的区别

* 传统on注册（L0）

  * 同一个对象,后面注册的事件会覆盖前面注册(同一个事件)

  * 直接使用`null`覆盖偶就可以实现事件的解绑

  * 都是冒泡阶段执行的

* 事件监听注册（L2）

  * 语法: `addEventListener(事件类型, 事件处理函数, 是否使用捕获)`

  * 后面注册的事件不会覆盖前面注册的事件(同一个事件)
  * 可以通过第三个参数去确定是在冒泡或者捕获阶段执行

  * 必须使用`removeEventListener(事件类型, 事件处理函数, 获取捕获或者冒泡阶段)`

  * 匿名函数无法被解绑

---

## 事件委托

* 事件委托是利用事件流的特征解决一些开发需求的知识技巧
* 总结：
  * **优点：**给父级元素加事件（可以提高性能）
  * **原理：**事件委托其实是利用事件冒泡的特点， 给父元素添加事件，子元素可以触发
  * **实现：**`事件对象.target` 可以获得真正触发事件的元素
  * ![image-20221127160001017](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221127160001017.png)

---

# 滚动事件

* 当页面进行滚动时触发的事件

* 事件名：`scroll`

* 监听整个页面滚动：

  ```javascript
   //页面滚动事件
  window.addEventListener('scroll', function () {
      //执行的操作
        });
  ```

  * 给`window`或者`document`添加`scroll`事件

* 监听某个元素的内部滚动直接给某个元素加即可

---

##### 加载事件

* 加载外部资源（如图片、外联CSS和JavaScript等）加载完毕时触发的事件
* 事件名：`load`
* 监听页面所有资源加载完毕：
  * 给`window`添加`load`事件

```javascript
//页面加载事件
window.addEventListener('load',function(){
        //执行的操作
    })
```

> 注意： 不光可以监听整个页面资源加载完毕，还可以针对某个资源绑定`load`事件



* 当初始的 `HTML` 文档被完全加载和解析完成之后，`DOMContentLoaded` 事件被触发，而无需等待样式表 、图像等完全加载
* 事件名：`DOMContentLoaded`
* 监听页面`DOM`加载完毕：
  * 给 `document` 添加 `DOMContentLoaded`事件

```javascript
document.addEventListener('DOMContentLoaded',function() {
    //执行的操作    
    })
```



# 元素大小和位置

## scroll家族

* 使用场景： 
  * 我们想要页面滚动一段距离，比如100px，就让某些元素 显示隐藏那我们怎么知道，页面滚动了100像素呢？ 就可以使用`scroll` 来检测页面滚动的距离~~~

* 获取宽高：
  * 获取元素的==内容==总宽高（不包含滚动条）返回值不带单位
  *  `scrollWidth`和`scrollHeight`
* 获取位置：
  * 获取元素内容往左、往上滚出去看不到的距离
  * `scrollLeft`和`scrollTop`
  *  这两个属性是可以==修改==的

```javascript
window.addEventListener('scroll', function () {
        console.log(document.documentElement.scrollTop);
      });
```



* 开发中，我们经常检测页面滚动的距离，比如页面滚动100像素，就可以显示一个元素，或者固定一个元素

> 注意事项：
>
> document.documentElement HTML 文档返回对象为HTML元素

​                              

---

## offset家族

* 使用场景：

  前面案例滚动多少距离，都是我们自己算的，最好是页面 滚动到某个元素，就可以做某些事。 简单说，就是通过js的方式，得到元素在页面中的位置 这样我们可以做，页面滚动到这个位置，就可以返回 顶部的小盒子显示…

* 获取宽高：

  * 获取元素的自身宽高、包含元素自身设置的宽高、`padding`、`border`
  * `offsetWidth`和`offsetHeight`

* 获取位置：

  * 获取元素距离自己==定位父级==元素的左、上距离
  *  `offsetLeft`和`offsetTop` 注意是==只读==属性

---

## client家族

* 获取宽高：
  * 获取元素的可见部分宽高（不包含边框，滚动条等）
  * `clientWidth`和`clientHeight`
* 获取位置：
  *  获取左边框和上边框宽度
  * `clientLeft`和`clientTop` 注意是只读属性

---

# window对象

## BOM（浏览器对象模型）

**1.1 BOM**

* BOM(Browser Object Model ) 是浏览器对象模型
* `window` 是浏览器内置中的全局对象，我们所学习的所有 Web APIs 的知识内容都是基于 `window` 对象实现的
* `window` 对象下包含了 `navigator`、`location`、`document`、`history`、`screen` 5个属性，即所谓的 `BOM` （浏览器对象模型）
* `document` 是实现 `DOM` 的基础，它其实是依附于 `window` 的属性。

> 注：依附于 `window` 对象的所有属性和方法，使用时可以省略 `window`

## 1.2 定时器-延时函数

* JavaScript 内置的一个用来让代码延迟执行的函数，叫 `setTimeout`

* **语法：**

  ```javascript
  setTimeout(回调函数，等待的毫秒数)
  ```

* `setTimeout` 仅仅只执行一次，所以可以理解为就是把一段代码延迟执行, 平时省略window

* **清除延时函数**

```javascript
let timer = setTimeout (回调函数，等待的毫秒数)
clearTimeout(timer)
```

 

* 结合递归函数可以使用 setTimeout 实现 setInterval 一样的功能

```javascript
 // 利用递归函数，模拟了setinterval
      let div = document.querySelector('div');
      function fn() {
        div.innerHTML = new Date().toLocaleString();
        setInterval(fn, 1000);
      }
      fn();
```

**俩种定时器对比：**

* `setInterval` 的特征是重复执行，首次执行会延时 
* `setTimeout` 的特征是延时执行，只执行 1 次 
* `setTimeout` 结合递归函数，能模拟`setInterval` 重复执行
* `clearTimeout` 清除由 `setTimeout` 创建的定时任务

---

## JS执行机制

**JS是单线程**

JavaScript 语言的一大特点就是==单线程==，也就是说，==同一个时间只能做一件事==。这是因为 Javascript 这 门脚本语言诞生的使命所致——JavaScript 是为处理页面中用户的交互，以及操作 DOM 而诞生的。比 如我们对某个 DOM 元素进行添加和删除操作，不能同时进行。 应该先进行添加，之后再删除。

单线程就意味着，所有任务需要排队，前一个任务结束，才会执行后一个任务。这样所导致的问 题是： 如果 JS 执行的时间过长，这样就会造成页面的渲染不连贯，导致页面渲染加载阻塞的感觉。

##### 同步和异步

为了解决这个问题，利用多核 CPU 的计算能力，HTML5 提出 Web Worker 标准，允许 JavaScript 脚本创建多个线程。于是，JS 中出现了==同步==和==异步。==

##### 同步

前一个任务结束后再执行后一个任务，程序的执行顺序与任务的排列顺序是一致的、同步的。比如做饭的同步 做法：我们要烧水煮饭，等水开了（10分钟之后），再去切菜，炒菜。

##### 异步

你在做一件事情时，因为这件事情会花费很长时间，在做这件事的同时，你还可以去处理其他事 情。比如做饭的异步做法，我们在烧水的同时，利用这10分钟，去切菜，炒菜。



> 他们的本质区别： 这条流水线上各个流程的执行顺序不同。

##### 同步任务

同步任务都在主线程上执行，形成一个==执行栈。==

##### 异步任务

JS 的异步是通过回调函数实现的。

 一般而言，异步任务有以下三种类型:

1. 普通事件，如 `click`、`resize` 等
2. 资源加载，如 `load`、`error` 等
3. 定时器，包括 `setInterval`、`setTimeout` 等

异步任务相关添加到==任务队列==中（任务队列也称为消息队列）。

##### JS执行机制

1.  先执行执行栈中的==同步任务==。
2. 异步任务放入任务队列中。
3. 一旦执行栈中的所有同步任务执行完毕，系统就会按次序读取任务队列中的异步任务，于是被读取的异步任务 结束等待状态，进入执行栈，开始执行。
4. ![image-20221129212638626](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221129212638626.png)

**图例**

![image-20221129212703572](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221129212703572.png)

由于主线程不断的重复获得任务、执行任务、再获取任务、再执行，所以这种机制被称为==事件循环（ event loop）==。

---

##  location对象

* `location` 的数据类型是对象，它拆分并保存了 URL 地址的各个组成部分

* **常用属性和方法：*

  * `href` 属性获取完整的 `URL` 地址，对其赋值时用于地址的跳转

  ![image-20221129213002460](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221129213002460.png)

  * `search` 属性获取地址中携带的参数，符号 ？后面部分

  ```javascript
  console.log(location.search)
  ```

  

  * `hash` 属性获取地址中的啥希值，符号 # 后面部分

  ```javascript
  console.log(location.hash)
  ```

  * >  后期vue路由的铺垫，经常用于不刷新页面，显示不同页面，比如 网易云音乐

  * `reload` 方法用来刷新当前页面，传入参数 true 时表示强制刷新

  ```html
  <button>点击刷新</button>
      <script>
          let btn = document.querySelector('button')
          btn.addEventListener('click',function(){
              location.reload()
          })
      </script>
  ```

  ---

  ##  navigator对象

* navigator的数据类型是对象，该对象下记录了浏览器自身的相关信息

* **常用属性和方法**

* 通过 userAgent 检测浏览器的版本及平台

```javascript
// 检测 userAgent（浏览器信息）
!(function () {
const userAgent = navigator.userAgent
// 验证是否为Android或iPhone
const android = userAgent.match(/(Android);?[\s\/]+([\d.]+)?/)
const iphone = userAgent.match(/(iPhone\sOS)\s([\d_]+)/)
// 如果是Android或iPhone，则跳转至移动站点
if (android || iphone) {
location.href = 'http://m.itcast.cn'
}
})()

```

---

##  histroy对象

* history 的数据类型是对象，该对象与浏览器地址栏的操作相对应，如前进、后退、历史记录等
* **常用属性和方法：**

| history对象方法 | 作用                                                       |
| --------------- | ---------------------------------------------------------- |
| back()          | 可以后退功能                                               |
| forward()       | 前进功能                                                   |
| go(参数)        | 前进后退功能 参数如果是1前进一个页面 如果是-1 后退一个页面 |

---

# 本地存储

##### 本地存储特性

随着互联网的快速发展，基于网页的应用越来越普遍，同时也变的越来越复杂，为了满足各种各样的需求，会经常性在 本地存储大量的数据，HTML5规范提出了相关解决方案。

1. 数据存储在用户浏览器中
2. 设置、读取方便、甚至页面刷新不丢失数据
3. 容量较大，`sessionStorage`和`localStorage`约 5M 左右

##### localStorage

1. 生命周期永久生效，除非手动删除 否则关闭页面也会存在
2. 可以多窗口（页面）共享（同一浏览器可以共享）
3. 以键值对的形式存储使用

**存储数据**

`localStorage.setItem(key, value)`

**获取数据**

`localStorage.getItem(key)`

**删除数据**
`localStorage.removeItem(key)`

**存储复杂数据类型存储**

本地只能存储字符串,无法存储复杂数据类型.需要将复杂数据类型转换成JSON字符串,在存储到本地

**`JSON.stringify`(复杂数据类型)**

 将复杂数据转换成JSON字符串==存储==本地存储中

**`JSON.parse`(JSON字符串)**

将JSON字符串转换成对象==取出==时候使用

```javascript
let obj = {
        uname: '刘德华',
        age: 17,
        address: '巴啦啦能量',
      };
      // 本地存储只能存储字符串 所以我要转换 转换为JSON格式的字符串
      localStorage.setItem('obj', JSON.stringify(obj));
      //   获取过来的值是字符串，不是对象了，没有办法直接使用，因此我们首先吧字符串转化为对象、
      console.log(JSON.parse(localStorage.getItem('obj')))
```

---

##### sessionStorage（了解）

1. 生命周期为关闭浏览器窗口
2. 在同一个窗口(页面)下数据可以共享
3. 以键值对的形式存储使用
4. 用法跟localStorage 基本相同

# 拓展-自定义属性

## 自定义属性

**固有属性: **

标签天生自带的属性 比如`class` `id` `title`等, 可以直接使用点语法操

**自定义属性：**

由程序员自己添加的属性,在DOM对象中找不到, 无法使用点语法操作,必须使用专门的API

`getAttribute('属性名')` // 获取自定义属性

`setAttribute('属性名', '属性值')` // 设置自定义属性

`removeAttribute('属性名')` // 删除自定义属性

![image-20221201150302836](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221201150302836.png)

**data-自定义属性:**

传统的自定义属性没有专门的定义规则,开发者随意定值,不够规范,所以在html5中推出来了专门的data-自定义属性 在 标签上一律以data-开头

在DOM对象上一律以dataset对象方式获取

![image-20221201150247147](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221201150247147.png)

---

# 正则表达式

##### 什么是正则表达式

* 正则表达式在 JavaScript中的使用场景：
* 例如验证表单：用户名表单只能输入英文字母、数字或者下划线， 昵称输入框中可以输入中文(==匹配==)
* 比如用户名: `/^[a-z0-9_-]{3,16}$/`
* 过滤掉页面内容中的一些敏感词(替换)，或从字符串中获取我们想要的特定部分(==提取==)等 。

##### 语法:

* JavaScript 中定义正则表达式的语法有两种
* **定义正则表达式语法：**

```javascript
let 变量名 = /表达式/
```

* 其中` / / `是正则表达式字面量
* 比如：

```javascript
let reg = /前端/
```

* JavaScript 中定义正则表达式的语法有两种，我们先学习其中比较简单的方法：

1. **判断是否有符合规则的字符串：**

* 语法：

 ```javascript
 regObj.test(被检测的字符串)
 ```

* 比如：

```javascript
let str = '大家都在学前端'
let reg = /前端/
let re = re.test(str)
console.log(re)// true
```

*  如果正则表达式与指定的字符串匹配 ，返回`true`，否则`false`

##### 检索（查找）符合规则的字符串：

`exec() `方法 在一个指定字符串中执行一个搜索匹配

* 语法：

```javascript
regObj.exec(被检测的字符串)
```

* 比如：

```javascript
let str = '大家都在学前端'
let reg = /前端/
let re = re.exec(str)
console.log(re)// true
```

如果匹配成功，`exec()` 方法返回一个数组，否则返回`null`

## 元字符

* **普通字符：**

大多数的字符仅能够描述它们本身，这些字符称作普通字符，例如所有的字母和数字。 也就是说普通字符只能够匹配字符串中与它们相同的字符。

* **元字符（特殊字符）**

是一些具有特殊含义的字符，可以极大提高了灵活性和强大的匹配功能。

* ​	比如，规定用户只能输入英文26个英文字母，普通字符的话 abcdefghijklm….
* 但是换成元字符写法： [a-z]

**参考文档**

MDN：https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions

正则测试工具: http://tool.oschina.net/regex

---

##### 边界符

1. ==边界符（表示位置，开头和结尾，必须用什么开头，用什么结尾）==

* 正则表达式中的边界符（位置符）用来提示字符所处的位置，主要有两个字符

| 边界符 | 说明                           |
| ------ | ------------------------------ |
| ^      | 表示匹配行首的文本（以谁开始） |
| $      | 表示匹配行尾的文本（以谁结束） |

> 如果 ^ 和 $ 在一起，表示必须是精确匹配。

```javascript
  console.log(/哈/.test('哈哈')); //true
      console.log(/哈/.test('二哈')); //true
      //   ^开头
      console.log(/^哈/.test('fd哈')); //false

      console.log(/^哈$/.test('我开心的哈哈大笑')); //false
      console.log(/^哈$/.test('哈哈')); //false
      console.log(/^哈$/.test('哈')); //true 精确匹配
```

---

##### 量词

量词用来==设定某个模式出现的次数==

| 量词  | 说明             |
| ----- | ---------------- |
| *     | 重复零次或更多次 |
| +     | 重复一次或更多次 |
| ？    | 重复零次或一次   |
| {n}   | 重复n次          |
| {n,}  | 重复n次或更多次  |
| {n,m} | 重复n次到m次     |

```javascript
 console.log(/a/.test('a'));
      // * n >= 0
      console.log(/a*/.test('a')); // true
      console.log(/a*/.test('aa')); // true
      console.log(/a*/.test('')); // true
      console.log(/a*/.test('b')); // true
      // + n >= 1
      console.log(/^a+$/.test('a')); // true
      console.log(/^a+$/.test('')); // false
      console.log(/^a+$/.test('b')); // false
      console.log(/^a+$/.test('aaaa')); // true
      //? 出现0 || 1
      console.log(/^a?$/.test('')); // true
      console.log(/^a?$/.test('a')); // true
      console.log(/^a?$/.test('aa')); // false

      // {n} 只能出现n次
      console.log(/^a{3}$/.test('aaa')); // true
      console.log(/^a{3}$/.test('aa')); // false
      console.log(/^a{3}$/.test('aaaa')); // false

      // {n,} >=n
      console.log(/^a{3,}$/.test('aaa')); // true
      console.log(/^a{3,}$/.test('aa')); // false
      console.log(/^a{3,}$/.test('aaaa')); // false

      // {n,m} >=n <=m
      console.log(/^a{3,4}$/.test('aaa')); // true
      console.log(/^a{3,4}$/.test('aa')); // false
      console.log(/^a{3,4}$/.test('aaaa')); // true
```

> 注意： 逗号左右两侧千万不要出现空格

---

##### 字符类

(1) `[ ] `匹配字符集合

* 后面的字符串只要包含 abc 中任意一个字符，都返回 `true` 

```javascript
console.log(/[abc]/.test('andy')); //true
      console.log(/[abc]/.test('baby')); //true
      console.log(/[abc]/.test('cry')); //true
      console.log(/[abc]/.test('die')); //false
```

---

(1.1)`[ ]` 里面加上 `-` 连字符

* 使用连字符 `-` 表示一个范围

```javascript
console.log(/^[a-z]$/.test('c'))//true
```

* 比如：
  * [a-z] 表示 a 到 z 26个英文字母都可以
  * [a-zA-Z] 表示大小写都可以
  * [0-9] 表示 0~9 的数字都可以

---

(1.2) `[ ]` 里面加上` ^ `取反符号

* 比如：
  * [^a-z] 匹配除了小写字母以外的字符

> 注意要写到中括号里面

---

（2） `. `匹配除换行符之外的任何单个字符

---

(3) 预定义：指的是某些常见模式的简写方式。

| 预定类 | 说明                                                       |
| ------ | ---------------------------------------------------------- |
| \d     | 匹配0-9之间的任一数字，相当于[0-9]                         |
| \D     | 匹配所有0-9以外的字符，想当于[^0-9\]                       |
| \w     | 匹配任意的字母、数字和下划线，相当于[A-Za-z0-9_]           |
| \W     | 除所有字母、数字和下划线以外的字符，相当于[^A-Za-z0-9_\]   |
| \s     | 匹配空格（包括换行符、制表符、空格符等）相当于[\t\r\n\v\f] |
| \S     | 匹配非空格的字符，相当于[^\t\t\n\v\f\]                     |

```javascript
日期格式：^\d{4}-\d{1,2}-\d{1,2}
```

## 修饰符

修饰符约束正则执行的某些细节行为，如是否区分大小写、是否支持多行匹配等

**语法：**

`/表达式/修饰符`

*  i 是单词 ignore 的缩写，正则匹配时字母不区分大小写
* g 是单词 global 的缩写，匹配所有满足正则表达式的结果

```javascript
      console.log(/a/i.test('a')); //true
      console.log(/a/i.test('A')); //true
```

---

##### 替换 replace 替换

**语法：**

```javascript
字符串.replace(/正则表达式/,'替换的文本')
```

**例子：**

```javascript
console.log('巴啦啦能量'.repeat(/啦啦/g, '**'));
```

