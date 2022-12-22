 

# JavaScript基础语法

## 1：计算机与编程语言

### 计算机组成 

- 硬件

	- 输入设备

		- 鼠标、键盘、手写板、摄像头等

	- 输出设备

		- 显示器、打印机、投影仪等

	- CPU

		- 负责处理数据与运算

	- 硬盘

		- 负责存储数据，硬盘永久存储数据

	- 内存

		- 内存暂时存储数据

- 软件

	- 系统软件

		- Windows、 Linux、 MacOS

	- 应用软件

		- 浏览器、QQ、 VSCode、Word

### 数据存储

- 计算机内部使用二进制 0 和 1来表示数据。
- 所有数据，包括文件、图片等最终都是以二进制数据（0 和 1）的形式存放在硬盘中的
- 所有程序，包括操作系统，本质都是各种数据，也以二进制数据的形式存放在硬盘中
- 硬盘、内存都是保存的二进制数据

### 数据存储单位

- 大小关系：bit < byte < kb < GB < TB< PB< EB< ZB< YB< ……
- 位(bit)：   1bit 可以保存一个 0 或者 1 （最小的存储单位）
- 字节(Byte)：1B = 8b
- 千字节(KB)：1KB = 1024B
- 兆字节(MB)：1MB = 1024KB
- 吉字节(GB):  1GB = 1024MB
- ......

### 计算机运行软件的过程

- 打开某个程序时，先从硬盘中把程序的代码加载到内存中
- CPU执行内存中的代码

### 编程语言

- 编程

	- 让计算机为解决某个问题而使用某种程序设计语言编写程序代码，并最终得到结果的过程。
	- 通过类似于人类语言的“语言”来控制计算机，让计算机为我们做事情，这样的语言就叫做编程语言
	- 编程语言是用来控制计算机的一系列指令，它有固定的格式和词汇

- 汇编语言

	- 直接对硬件操作，只不过指令采用了英文缩写的标识符，容易识别和记忆。

- 高级语言

	- 并不是特指某一种具体的语言，而是包括了很多编程语言，常用的有C语言、C++、Java、C#、Python、PHP、JavaScript、Go语言
	- 高级语言所编制的程序不能直接被计算机识别，必须经过转换才能被执行，为此，我们需要一个翻译器

## 2：JavaScript介绍 

### 是什么

- 布兰登·艾奇 10天完成 JavaScript设计
- 最初命名为Live Script，后来在与Sun合作之后将其改名为JavaScript.
- JavaScript 是世界上最流行的语言之一，是一种运行在客户端的脚本语言
- 脚本语言：不需要编译，运行过程中由 js 解释器( js 引擎）逐行来进行解释并执行
- 解释型语言和编译型语言

	- 编译型：在代码执行之前进行编译，生成中间代码文件
	- 解释型：是在运行时进行及时解释，并立即执行

###  JavaScript能做什么

- 表单动态校验（密码强度检测）  （ JS 产生最初的目的 ）
- 网页特效
- 服务端开发(Node.js)
- 桌面程序(Electron)
- App(Cordova) 
- 控制硬件-物联网(Ruff)
- 游戏开发(cocos2d-js)

### 浏览器执行 JS 

- 浏览器分成两部分：渲染引擎和 JS 引擎
- 1.渲染引擎：用来解析HTML与CSs，俗称内核，比如 chrome浏览器的 blink，老版本的 webkit
- 2.JS引擎：也称为JS解释器。用来读取网页中的 javaScript代码，对其处理后运行，比如 chrome浏览器的V8

### 组成

- ECMAScript

	- JavaScrip 网景公司
	- Jscript微软公司

- 浏览器

	- DOM——文档对象模型
	- BOM——浏览器对象模型

## 3：基础语法规则

### 写法

- 1. 内部JS：定义<script>，标签体内容就是js代码
- 2. 外部JS：定义<script>，通过src属性引入外部的js文件
- 注意：

	- 1. <script>可以定义在html页面的任何地方。但是定义的位置会影响执行顺序。
	- 2. <script>可以定义多个。

### JavaScript注释

- 单行注释

	- // 我是一行文字，不想被 JS引擎 执行，所以 注释起来	
	- // 用来注释单行文字（  快捷键   ctrl  +  /   ）

- 多行注释

	- /*
  获取用户年龄和姓名
  并通过提示框显示出来
	*/
	- /* */  用来注释多行文字（ 默认快捷键  alt +  shift  + a ） 

### 变量

- 变量的概念：一小块存储数据的内存空间
- 声明变量-- 语法：var 变量名
- 赋值-- age = 10; // 给 age  这个变量赋值为 10
- 变量声明并赋值：var 变量名 = 初始化值;
- 同时声明多个变量

	- var age = 10,  name = 'zs', sex = 2;       

- 变量命名规范

	- 数字、字母、下划线、$
	- 不能 以数字开头
	- 不能 是关键字、保留字
	- 严格区分大小写
	- 建议

		- 变量名必须有意义
		- 遵守驼峰命名法

### 数据类型

- 原始数据类型(基本数据类型)：

	- 1. number：数字类型 . 整数/小数/NaN(not a number 一个不是数字的数字类型)
	- 2. string：字符串.  字符串  "abc" "a" 'abc'
	- 3. boolean: true和false
	- 4. null：一个对象为空的占位符
	- 5. undefined：未定义。如果一个变量没有给初始化值，则会被默认赋值为undefined

- 引用数据类型：对象(对象类型默认值是null)
- typeof 可用来获取检测变量的数据类型
- 数据类型转换

	- 转换为字符串类型

		- toString() -- 转成字符串
		- String() -- 强制转换字符串
		- 加号拼接字符串  -- 和字符串拼接的结果都是字符串

	- 转换为数字型

		- parseInt（ string）函数  -- 将 string类型转成整数数值型
		- parseFloat（ string）函数 -- 将 string类型转成浮点数 数值型
		- Number() 强制转换函数 -- 将 string类型转换为数值型
		- js隐式转换（- * /） -- 利用算术运算隐式转换为数值型

	- 转换为布尔型

		- Boolean()函数  -- 其他类型转成布尔值

### 关键字和保留字

- 关键字

	- 是指 JS本身已经使用了的字，不能再用它们充当变量名、方法名。
	- 包括：break、case、catch、continue、default、delete、do、else、finally、for、function、if、in、instanceof、new、return、switch、this、throw、try、typeof、var、void、while、with 等。

- 保留字

	- 实际上就是预留的“关键字”，意思是现在虽然还不是关键字，但是未来可能会成为关键字，同样不能使用它们当变量名或方法名。
	- 包括：boolean、byte、char、class、const、debugger、double、enum、export、extends、fimal、float、goto、implements、import、int、interface、long、mative、package、private、protected、public、short、static、super、synchronized、throws、transient、volatile 等。

### 操作符

- 算数运算符

	- +  -  *  /  %  
	- 浮点数的精度问题

		- var result = 0.1 + 0.2;//结果是：0.30000000000000004
		- 不要直接判断两个浮点数是否相等

- 递增和递减运算符

	- 反复给数字变量添加或减去1
	- 使用递增（++）和递减（ -- ）运算符来完成
	- 放在变量前面称为前置递增（递减）运算符
	- 放在变量后面称为后置递增（递减）运算符

- 比较运算符

	- 两个数据进行比较时所使用的运算符，返回一个布尔值（true / false）作为比较运算的结果
	- < 小于号
	- > 大于号
	- >= 大于等于号（大于或者等于）
	- <= 小于等于号（小于或者等于）
	- == 判等号（会转型
	- !=  不等号
	- === 全等要求值和数据类型都一致

- 逻辑运算符

	- &&  逻辑与，简称"与" and
	- ||  逻辑或，简称"或" or
	- !  逻辑非，简称"非"not

- 赋值运算符

	- =  直接赋值
	- +=  -=  加、减一个数后再赋值
	- *=  /=  %=  乘、除、取模后再赋值

- 优先级

	- 

### 流程控制

- 顺序流程控制

	- 按照代码的先后顺序，依次执行
	- 

- 分支流程控制

	- 根据不同的条件，执行不同的路径代码
	- 
	- if 语句

		- // 条件成立执行代码，否则什么也不做
if (条件表达式) {
    // 条件成立执行的代码语句
}

	- if else语句（双分支语句）

		- // 条件成立  执行 if 里面代码，否则执行else 里面的代码
if (条件表达式) {
    // [如果] 条件成立执行的代码
} else {
    // [否则] 执行的代码
}

	- if else if 语句(多分支语句)

		- // 适合于检查多重条件。
if (条件表达式1) {
    语句1；
} else if (条件表达式2)  {
    语句2；
} else if (条件表达式3)  {
   语句3；
 ....
} else {
    // 上述条件都不成立执行此处代码
}

	- 三元表达式

		- 表达式1 ? 表达式2 : 表达式3;
		- 如果表达式1为 true ，则返回表达式2的值，如果表达式1为 false，则返回表达式3的值

	- switch分支流程控制

		- 

- 循环

	- for循环

		- for(初始化变量; 条件表达式; 操作表达式 ){
    //循环体
	}
		- 初始化变量：通常被用于初始化一个计数器，该表达式可以使用 var 关键字声明新的变量，这个变量帮我们来记录次数。
		- 条件表达式：用于确定每一次循环是否能被执行。如果结果是 true 就继续循环，否则退出循环。
		- 操作表达式：用于确定每一次循环是否能被执行。如果结果是 true 就继续循环，否则退出循环。
		- 双重for循环

			- 
			- 外层循环执行一次，内层循环要执行全部次数

	- while循环

		- while (条件表达式) {
    // 循环体代码 
	}
		- 1 先执行条件表达式，如果结果为 true，则执行循环体代码；如果为 false，则退出循环，执行后面代码
		- 2 执行循环体代码
		- 3 循环体代码执行完毕后，程序会继续判断执行条件表达式，如条件仍为true，则会继续执行循环体，直到循环条件为 false 时，整个循环过程才会结束
		- 使用 while 循环时一定要注意，它必须要有退出条件，否则会成为死循环

	- do-while循环

		- do {
    // 循环体代码 - 条件表达式为 true 时重复执行循环体代码
	} while(条件表达式);
		- 先执行一次循环体代码 
		- 再执行条件表达式，如果结果为 true，则继续执行循环体代码，如果为 false，则退出循环，继续执行后面代码	

	- 跳出

		- continue 关键字用于立即跳出本次循环，继续下一次循环
		- break 关键字用于立即跳出整个循环（循环结束）



# 变量

## 变量是什么？

**1.变量**

1. 白话：变量就是一个装东西的盒子。
2. 通俗：变量是计算机中用来存储数据的“==容器==”，它可以让计算机变得有记忆
3. 注意：变量不是数据本身，他们仅仅是一个用于存储数值的容器。可以理解为是一个个用来装东西的盒子。

---



## 变量的基本使用

**1.声明变量**

要想使用变量，首先需要创建变量

**语法：**

```javascript
let  变量名
```

* 声明变量有俩部分组成：声明关键字、变量名（标识）
* let即关键字，所谓关键字是系统提供专门用来声明变量的词语

**举例**

```javascript
let age;
```

**2.变量赋值**

定义了一个变量后，你就能够初始化他（赋值）。在变量名之后跟上一个‘’=‘’ 然后是数值

**3.更新变量**

变量赋值后，还可以通过简单地给它一个不同的值来更新它

注意：let 不能声明多次声明

**4.声明多个变量**

```javascript
let age = 18 ,uname = 'pink'
```

---

##  变量的本质

内存：计算机中存储数据的地方，相当于一个空间

变量：是程序在内存中申请的一块用来存放数据的小空间

---

##  变量命名规则于规范

**规则**：必须遵守，不遵守报错

**规范：**建议，不遵守不会报错，但不符合业内通识

==**1.规则**==：

* 不能用关键字
  * 关键字：有特殊含义的字符，例如：let  var  if  for 等
* 只能用下划线、字母、数字、$组成，且数字不能开通
* 字母严格区分大小写，如：Age和age是同的变量

==**规范**==：

* 起名要有意义
* 遵守小驼峰命名法
  * 第一个单词首字母小写，后面每个单词首字母大写。例如：useName
  
  * ---

## 变量扩展-数组

* 数组（Array）是一种可以按照顺序保存多个数据

```javascript
let arr = []  // []是数组字面量
```

**1.声明语法**

```javascript
let 数组名 = [数据1,数据2,......,数据n]
```

* 例

```javascript
let arr = ['展飞', '马超', '黄忠', '关羽']
```

* 数组是按照顺序保存，所以每个数字据都有自己的编号
* 计算机中的编号从0开始，所以展飞的编号为0，马超的编号为1，以此类推
* 在数组中，数据的编号也叫==索引或下标==

**2.取值语法**

`数组名[下标]`

**3.一些术语**

* 元素：数组中保存的每个数据都叫数组元素
* 下标：数组中数据的编号
* 长度：数组中数据的个数，通过数组的length属性获取

---

# 数据类型

## 数据类型

计算机程序可以处理大量的数据，为什么给数据分类？

* 更加充分和高效的利用内存
* 也更加方便程序员的使用数据

**JS数据类型整体分为两个大类：

* 基本数据类型
  * number 数字型
  * string 字符串型
  * boolean 布尔型
  * undefined 未定义型
  * null 空类型
  
* 引用数据类型
  * object 对象
  * function 函数
  * arrat 数组
  
  ---

## 基本数据类型

#### 数据类型-数字类型（number）

JavaScript中的正数，负数，小数，等统一称为 数字类型

==注意事项==：js是弱数据类型，变量到底属于那种类型，只有赋值之后，我们才能确认。Java是强数据类型，例如 int a = 3 必须是整数

---

#### 字符串类型（string）

==通过单引号、双引号、或反引号、包裹的数据都叫字符串==，单引号和双引号本质没有区别  推荐使用单引号

**注意事项***

1. 无论单引号或是双引号必须成对使用
2. 单引号/双引号可以互相嵌套，但是不以自己嵌套自己（口诀：外双内单，外单内双）
3. 必要时可以使用转义符\，输出单引号或者双引号

**字符串拼接**

```javascript
   console.log('我是' + 'pink老师  ');

      console.log('我今年年龄是' + 18);

      let age = 18;
      console.log('我今年年龄是' + age);
```

---

#### 模板字符串

**1.作用**

* 拼接字符串和变量
* 在没有它之前，要拼接变量比较麻烦

**2.符号**

* ``
* 在英文模式下按键盘的tab上方哪个键
* 内容拼接变量时，用${}包住变量

```javascript
let age = 18;
      document.write(`我今年${age}`);
```

---

#### 布尔类型（boolean）

表示肯定或否定时在计算机中对应的是布尔类型数据

他有俩个固定的值 true 和false ，表示肯定的数据用 true（真） 表示否定的就是false （假）

---

#### 未定义类型（undefined）、

未定义是比较特殊的类型，只有一个值 undefined

**什么情况出现未定义类型？**
只声明变量，不赋值的情况下，变量的默认值为 undefined ，一般很少直接为某个变量赋值为undefined

```javascript
let age //声明变量但是未赋值
document.write(age)  // 输出undefined
```

**工作中的使用场景**

我们开发中，经常声明一个变量，等待传送过来的数据。

如果我们不知道这个数据是否传递过来，此时我们可以通过检测这个变量是不是undefined，就判断用户是否有数据传递过来

---

 #### null（空类型）

null表示 值为空

`let obj = null`

null和undefined区别：

1. undefined 表示没有赋值
2. null表示赋值了，但是内容为

**null开发中的使用场景**

官方解释：把null作为尚未创建的对象

大白话：将来有个变量里面存放的是一个对象，但是对象还没创建好，可以先给个null

---

### 控制台输出语句和检测数据类型

**通过typeof 关键字检测数据类型**

```javascript
let age = 18;
      let name = '小明';
      console.log(typeof age);
      console.log(typeof name);
```

# 类型转换

## 为什么需要类型转换

JavaScript是弱数据类型：JavaScript也不知道变量到底是属于那种数据类型，只有赋值了才知道。

坑：使用表单，prompt获取过来的数据默认是字符串类型吗，此时就不能简单的进行加法运算

通俗来说就是，把一种==数据类型的变量转换成我们需要的数据类型==

---

## 隐式转换

某些运算符被执行时，系统内部自动将数据类型进行转换，这种转换称为隐式转换。

**规则**

* +号俩边只要有一个是字符串，都会把另外一个转成字符串
* ==除了+以外==的算数运算符，比如 - * / 等都会把数据类型转换成数字类型

**缺点**

* 转换类型不明确，靠经验才能总结

**小技巧**

* +号作为正号解析可以转换成Number

```javascript
 //   内部悄悄的把18转换为了字符串;
      console.log('pink' + 18);

      console.log(10 + '10'); //1010
      //   - * / 把字符串的‘10’，转换成数字型 10
      console.log(10 - '10'); //0
      //小技巧
      let num = '10';
      console.log(+num); //正数10 显示数字型10
      console.log(10 + +'10'); //20
```

---

## 显示转换

编写程序时过度依靠系统内部的隐式转换时不严谨的，因为隐式转换规律并不清晰，大多是靠经验总结的规律。

为了避免因隐式转换带来的问题，通常更逻辑需要对数据进行显示转换。

**概念**

自己写代码告诉系统该转成什么类型

**转换从数字型**

* ==Number（数据）==
  * 转换成数据类型
  * 如果字符串内容里面有非数字，转换失败结果为NaN 即不是一个数字
  * NaN也是number类型的数据，代表非数字

* ==parselint(数据)==
  * 只保留整数
* ==parseFloat(数据)==
  * 可以保留小数
  * 

```javascript
let nume = '10';
      console.log(Number(nume));
      //   转换成数字型，只保留整数，没有四舍五入
      console.log(parseInt('10'));
      //   转换为数字型，会保留小数
      console.log(parseFloat(1.99));

      //   区别
      // 1.Number() 只能放数字类型的字符，不能放abc这样的
      // 否则返回的是NaN
      console.log(Number('10abc'));
    //   parseFloat 经常用于过滤px单位
      console.log(parseFloat('123px'));
```

**转换成字符型**

==String(数据)==

==变量.toSring(进制)==

```javascript
      console.log(String(10));
      let age = 19;
      console.log(age.toString());
```

---

# 运算符

## 算数运算符

数学运算符也叫算数运算符，主要包括加、减、乘、除、取余（求模）

* +：求和
* -：求差
* *：求积
* /：求商
* %：取模（取余数  ）
  * 在开发中经常作为某个数字是否被整除

同时使用多个运算符编写程序时，会按照某种顺序先后执行，我们称之为优先级。

JavaScript中，优先级越高越先被执行，==优先级相同时依次从左向右执行。==

* 乘、除、取余优先级相同
* 加、减优先级相同
* 乘、除、取余优先级大于减
* 使用（）可以提升优先级
* 总结：先乘除后加减，有括号先算括号里面的

---

## 赋值运算符

* **赋值运算符：对变量进行赋值的运算符**
  * 已经学过的赋值运算符： = ==将等号右边的值赋予给左边，要求左边必须时一个容器==
* 其他赋值运算符：
  *  +=
  * -=
  * *=
  * /=
  * %=

例：

```javascript
let num = 10;
      num += 1;
      console.log(num); // 结果是2
```

---

## 一元运算符

众多的JavaScript的运算符可以根据所需表达式的个数，分为一元运算符、二元运算符、三元运算符

* 二元运算符

  * 例子

* ```javascript
  let num = 10 + 20
  ```

* 一元运算符：
  * 例：正负号

* 自增：
  * 符号：++
  * 作用：让变量的值==+1==
* 自减
  * 符号：--
  * 作用：让变量的值==-1==
* 使用场景：
  * 经常用于==计数==来使用。

**自增运算符的用法**

```javascript
let num = 1
++num
```

```javascript
let num = 1
num++
```

* 每执行一次，当前变量数值加一，其作用相当于`num+=1`

**前后置自增的区别**

* 前置：先自增后运算
* 后置：先运算后自增
* 自减同理
* 开发中，我们一般都是单独使用的，后置++更多使用

---

## 比较运算符

* 比较运算符
  * \>：左边是否大于右边
  * <： 左边是否小于右边
  * \>=：左边是否大于或等于右边
  * <=：左边是否小于或等于右边
  * ==：左右俩边是否相等
  * ===：左右俩边是否类型和值都相等
  * !==：左右俩边是否不全等 (! ==)
  * 比较结果为Boolean类型，即只会得到true或者flase 

**比较运算符的细节**

* 字符串比较，是比较字符串对应的ASCII码
  * 从左往右一次比较
  * 如果第一位一样再比较第二位，以此类推
  * 比较的少，了解即可

* NaN的不等于任何值，包括它本身

* 尽量不要比较小数，因为小数有精度问题
* 不同类型之间比较会发生隐式转换

## 逻辑运算符

* 逻辑运算符

  | 符号 |  名称  | 日常读法 |             特点             |      口诀      |
  | :--: | :----: | :------: | :--------------------------: | :------------: |
  |  &&  | 逻辑与 |   并且   | 符号俩边都为true结果才为true |    一假则假    |
  | \|\| | 逻辑或 |   或者   |  符号俩边有一个true就为true  |    一真则真    |
  |  !   | 逻辑非 |   取反   |   true变flase false变true    | 真变假，假变真 |

  

**逻辑运算符里的短路**

* 短路：只存在于&&和 || 中，当满足一定条件会让右边代码不执行

  | 符号 |     短路条件      |
  | :--: | :---------------: |
  |  &&  | 左边为flase就短路 |
  | \|\| | 左边为true就短路  |

* 原因：通过左边能得到整个式子的结果，因此没必要再判断右边

* 运算结果：无论 && 还是 || ，运算结果都是最后被执行的表达式值，一般用在变量赋值

```javascript
// 有五个值是当flase 来看的 其余是真的
        // flase 数字0 '' undefined null
```

---

## 运算符的优先级

| 优先级 | 运算符     | 顺序              |
| ------ | ---------- | ----------------- |
| 1      | 小括号     | ( )               |
| 2      | 一元运算符 | ++ -- !           |
| 3      | 算数运算符 | 先* / 后 + -      |
| 4      | 比较运算符 | >  >=  <  <=      |
| 5      | 相等运算符 | ==  !=  = ==  !== |
| 6      | 逻辑运算符 | 先&& 后 \|\|      |
| 7      | 赋值运算符 | =                 |
| 8      | 逗号运算符 | ,                 |

* 一元运算符里面的==逻辑非优先级很高==
* 逻辑与比逻辑或优先级高

---

# 语句

## 表达式和语句

* 表达式：
  表达式时一组代码的集合，JavaScript解释器会将其计算出一个结果

  ```javascript
  x = 7 
  3 = 4
  num++
  ```

* 语句：

  js整句或命令， js语句是以分号结束（可以省略）

  比如：if语句 for循环语句

* 区别：

  表达式计算出一个值，但语句用来自行以使某件事发生（做什么事）

* ==表达式==  :`3 + 4`

* ==语句==：`alert( )` 弹出对话框

  ==其实某些情况，也可以把表达式理解为语句，因为它是在计算结果，也是做事==

---

## 分支语句

* 分支语句可以让我们有==选择性==的执行想要的代码
* 分支语句包含：
  * ==if分支语句==
  * 三元运算符
  * switch 语句

### if 分支语句

1. **if语句**

* if语句有三种使用方法：单分支、双分支、多分支

* 单分支使用语法：

  ```javascript
  if (条件) {
      满足条件要执行的代码
  }
  ```

  * 括号内的条件为==true==时，进入大括号里执行代码
  * 小括号内的结果若不是布尔类型时，会发生隐式转换为布尔类型

* 双分支if语法

  ```javascript
  if (条件) {
      
      满足条件要执行的代码
      
  } else {
      
      不满足条件执行的代码
  }
  ```

* 多分支if语法：

  ```javascript
  if (条件) {
      
      代码1
  } else if (条件2) {
      
      代码2
  } else if (条件3) {
      
      代码3
  } else{
      
      代码n
  }
  ```

---

### 三元运算符

* 其实是比`if`双分支 更简单的写法，有时候也叫做三元表达式

* 符号：？与：配合使用

* 语法：

  ```javascript
  条件 ? 满足条件执行的代码 : 不满足条件执行的代码
  ```

* 一般用来取值

写法：

```javascript
3 > 5 ? alert('大于') : alert('小于')
```

**案例 数字补0**

```javascript
let num = +prompt('请输入一个数值');
      num < 10 ? alert(`0${num}`) : alert(num);
```

---

### switch语句

```javascript
switch (数据) {
            case 值1:
                代码1
                break
            case 值2:
                代码2
                break
            default:
                代码n
                break
        }
```

**释义**

* 找到小括号里数据**全等**的case值，并执行里面对应的代码
* 若没有全等的则执行default里面的代码

```javascript
// 实例
  let num1 = +prompt('请输入第一个数值');
      let num2 = +prompt('请输入第二个数值');
      let suan = prompt('输入算法');
      let he;
      switch (suan) {
        case '+':
          he = num1 + num2;
          alert(he);
          break;
        case '-':
          he = num1 - num2;
          alert(he);
          break;
        case '*':
          he = num1 * num2;
          alert(he);
          break;
        case '/':
          he = num1 / num2;
          alert(he);
          break;
      }
```

> 1. switch语句一般用于等值判断，不适合区间判断
> 2. switch case一般需要配合break关键字使用 没有break会造成case穿透。

---

## 循环语句

### 断点调试

* 作用：学习时可以帮助更好的理解代码运行，工作时可以更快找到bug
* 浏览器打开调试界面
  1. 按F12打开开发者工具
  2. 点到sources一栏
  3. 选择代码文件

---

### while循环

循环：重复执行某段代码，而while：在...区间

**1.while循环语法：**

```javascript
while (循环条件) {
    
    要重复执行的代码(循环体)
}
```

**释义：**

* 和if语句很像，都要满足小括号里的条件为==true==才会进入执行代码
* while大括号里代码执行完毕后不会跳出，而是继续回到小括号里判断条件是否满足，若满足又执行大括号里面的代码，然后再回到小括号判断条件，直到括号内条件不满足，即跳出

```javascript
//实例
let i = 1;
      while (i <= 10) {
        document.write(`月薪过万 <br/>`);
        i++;
      }
```



> **while循环注意事项**
>
> 循环的本质就是以某个变量为起始值，然后不断产生变化量，慢慢靠近终止条件的过程。
>
> 所以，==循环需要具备三要素：==
>
> 1. 变量起始值
> 2. 终止条件（没有终止条件，循环会一直执行，造成死循环）
> 3. 变量变化量（用自增或者自减）

####　循环退出

* 循环结束:

  * continue:结束本次循环，继续下次循环

    ```javascript
    let i = 1;
          while (i <= 6) {
            if (i === 3) {
              i++;
              continue; // 结束本次循环 继续下一次循环
            }
            document.write(`这是数字${i}`);
            i++;
          }
    ```

  * break:跳出所在循环

    ```javascript
     let i = 1;
          while (i <= 6) {
            if (i === 3) {
              // 退出循环
              break; 
            }
            document.write(`这是数字${i}`);
            i++;
          }
    ```


---

### for循环

**1.for循环语法**

* 也是重复执行代码

* 好处：把声明起始值、循环条件、变化值写到一起，让人一目了然

  ```javascript
  for (声明记录循环次数的变量; 循环条件; 变化值) {
      
      循环体
  }
  ```

* **例**

  ```javascript
  // for (起始条件; 退出条件;变化量){
        //     循环语句
        // }
        for (let i = 0; i <= 10; i++) {
          console.log('打印十次');
        }
  ```

  

* ==for循环的最大价值：遍历数组==

  ```javascript
  let arr = ['马超', '赵云', '张飞', '关羽', '黄忠'];
        for (let i = 0; i < arr.length; i++) {
          document.write(arr[i]);
        }
  ```

####　退出循环

* 循环结束：
* * continue：结束本次循环，继续下次循环
  * break：跳出所在循环

```javascript
for (let i = 1; i < 6; i++) {
        if (i === 2) {
          continue; //继续 退出本次循环，继续下一次循环
          break; // 结束循环  退出整个循环
        }
      }
```

#### 循环嵌套

**for循环嵌套语法**

```javascript
for (外部声明记录循环次数的变量; 循环条件; 变化值) {
    
    for (内部声明记录循环次数的变量; 循环条件; 变化值) {
        
        循环体
    }
}
```

* 一个循环里再套一个循环，一般用在for循环里

**例：**

```javascript
for (let i = 1; i < 6; i++) {
        for (let j = 1; j < 6; j++) {
          document.write('*');
        }
      }

      //外面循环执行一次，里面循环执行全部（5次）
```

---

# 数组

## 数组是什么

* 数组（Array）是一种可以按顺序保存数据的数据类型
* 为什么要用数组？
  * 如果有多个数据，可以用数组保存起来

## 数组的基本使用

```javascript
let arr = []  // []是数组字面量
```

**1.声明语法**

```javascript
let 数组名 = [数据1,数据2,......,数据n]
```

* 例

```javascript
let arr = ['展飞', '马超', '黄忠', '关羽']
```

* 数组是按照顺序保存，所以每个数字据都有自己的编号
* 计算机中的编号从0开始，所以展飞的编号为0，马超的编号为1，以此类推
* 在数组中，数据的编号也叫==索引或下标==
* 数组可以存储任意类型的数据

**2.取值语法**

`数组名[下标]`

**3.一些术语**

* 元素：数组中保存的每个数据都叫数组元素
* 下标：数组中数据的编号
* 长度：数组中数据的个数，通过数组的length属性获取

**4.遍历数组：**

用循环把数组数组中每个元素都访问到，一般会用for循环便利

* 语法：

  ```javascript
  for (let i = 0; i < 数组名.length; i++) {
      数组名[i]
  }
  ```

    ```javascript
    let arr = ['马超', '赵云', '张飞', '关羽', '黄忠'];
          for (let i = 0; i < arr.length; i++) {
            document.write(arr[i]);
          }
    ```

## 操作数组

数组本质是数据集合，操作数据无非就是==增 删 改 查==

**查询数组数据**

`数组[下标]`或者我们称为访问组数据

**改 查询赋值**

`数组[下标]=新值 `

```javascript
let arr = [1, 2, 3, 4, 5];
      arr[0] = 2;
      console.log(arr[0]);
```



**增 数组添加新的数据**

`arr.push(新增的内容)`

`arr.unshift(新增的内容)`

**删 删除数组中的数据**

`arr.pop` `arr.shift` `arr.splice(操作的下标,删除的个数)`

### 增加数据

**数组==增加==新的数据**

`数组.push()`方法将一个或多个元素添加到数组的==末尾==，并返回该数组的新长度

**语法：**

```javascript
arr.push(元素1,..., 元素n)
```

**例子**

```javascript
let arr = ['red', 'green'];
	// 把blue放到 arr 后面
	// 返回值是新的数组长度
	//不但把数据放入数组，而且返回了新数组的长度
      arr.push('bule');
      console.log(arr); //'red', 'green' , 'bule'
```



`arr.unshift(新增的内容)`方法将一个或多个元素添加到数组的**开头**，并返回该数组的新长度

**语法：**

```javascript
arr.unshift(元素1,...,元素n)
```

**例如：**

```javascript
let arr = ['red', 'green'];
      arr.unshift('pink');
      console.log(arr); //'pink','red', 'green'
```

### 删除数据

**2.数组==删除==元素**

`数组.pop()`方法从数组中删除最后一个元素，并返回该元素的值

**语法：**

```javascript
arr.pop()
```

**例子：**

```javascript
let arr = ['red', 'green', 'bule'];
      // 删除最后一个元素
      arr.pop();
      // 返回删除的值
      console.log(arr.pop());
      console.log(arr);
```

`数组.shift()`方法从数组中删除第一个元素，并返回该元素的值

**语法：**

```javascript
arr.shift()
```

**例子：**

```javascript
let arr = ['red', 'green', 'bule'];
      arr.shift()
      console.log(arr);
```

`数组.splice()`方法 删除指定元素

**语法：**

```javascript
arr.splice(start,deleteCount)

arr.splice(起始位置,删除几个元素)
```

**释义**

==start 起始位置==

* 指定修改的开始位置（从0计数）

==deleteCount:==

* 表示要移除的数组元素的个数
* 可选的。如果省略则默认从指定的起始位置删除到最后

**例子：**

```javascript
let arr = ['red', 'green', 'bule'];
    //   第一个1是从索引号位置开始删;
    //   第二个1是删除几个;
      arr.splice(1, 1);
      console.log(arr); //'red', 'bule'
```

**删除元素的使用场景：**

1. 随机抽奖，中将的用户就需要从数组例删除，不允许重复抽奖
2. 点击删除按钮，相关的数据会从商品数据中删除

---

## 数组中map方法 迭代数组

* 作用: map 迭代数组
* **语法:**

```javascript
 const arr = ['red', 'bule', 'green'];
      // map 方法也是遍历 处理数据 可以返回一个数组
      const newArr = arr.map(function (item, i) {
        console.log(item); //  数组元素 等价于arr[i]
        console.log(i); // 下标
        return item + '老师';
      });
      console.log(newArr);
```

## 数组中join方法

* 作用:
  * `join()`方法用于把数组中的所有元素转换成一个字符串
* **语法:**

```javascript
const arr = ['red', 'bule', 'green'];
      // 把数组元素转换成字符串
      console.log(arr.join(','));
```

* **参数:**
* 数组元素是通过参数里面指定的分隔符进行分隔的

# 案例-冒泡排序

==冒泡排序==

冒泡排序是一种简单的排序算法

它重复地走访过要排序的数列，一次比较俩个元素，如果他们的顺序错误就把他们交换过来。走访数列的工作是重复地进行直到没有再需要交换，也就是说该数列已经排序完成

**代码如下：**

```javascript
let arr = [5, 4, 3, 2, 1, 8, 9, 7];
      // 1. 外层循环控制趟数  循环4次  arr。length - 1
      for (let i = 0; i < arr.length - 1; i++) {
        //2.里层循环 控制一趟交换的次数 arr.length - i - 1
        let arr1 = arr[0];
        for (let j = 0; j < arr.length - i - 1; j++) {
          let arr1 = [];
          if (arr[j] > arr[j + 1]) {
            arr1 = arr[j];
            arr[j] = arr[j + 1];
            arr[j + 1] = arr1;
          }
        }
      }
      document.write(arr);
```

---

# 函数

## 为什么需要函数？

**函数：**
function，是被设计为==执行特定任务的==代码块

**说明：**
函数可以把具有相同或相似逻辑的代码“包裹”起来，通过函数调用执行这些
“包裹”的代码逻辑，这么做的优势是有利于==精简代码方便复用==

## 函数使用

* 函数的声明语法：

  ```javascript
  function 函数名() {
      函数体
  }
  ```

**例子**

* ```javascript
  function sauHi() {
          document.write('你好~~');
        }
  ```

* 函数命名规范
  * 和变量命名基本一致
  * 尽量使用小驼峰命名法
  * 前缀应该为动词
  * 命名建议：常用动词约定

| 动词 | 含义                   |
| ---- | ---------------------- |
| can  | 判断是否可执行某个动作 |
| has  | 判断是否含义某个值     |
| is   | 判断是否为某个值       |
| get  | 获取某一个值           |
| set  | 设置某个值             |
| load | 加载某些数据           |

* 函数的调用语法：

  ```javascript
  // 函数调用，这些函数体内的代码逻辑会被执行
  函数名()
  ```

> 注意：声明（定义）的函数必须调用才会真正被执行，使用()调用函数

* **例**

  ```javascript
  // 函数一次声明可以多次使用，每一次函数调用函数体里面的代码会重新执行一次
  sayHi()
  sayHi()
  ```

* 我们曾经使用的alert() promt() 本质都是函数的调用

* **函数体**

  函数体是函数的构成部分，它负责将相同或相似代码”包裹“起来，直到函数调用时函数体内代码才会被执行。函数的功能代码都要写在函数体当中

  ```javascript
  //打招呼
  function sayHi() {
      console.log('hi~')
  }
  sayHi() //调用函数
  ```



## 函数传参

* 声明语法

  ```javascript
  function 函数名(参数列表) {
      函数体
  }
  ```

* 参数列表

  * 传入数据列表
  * 声明这个函数需要传入几个值
  * 多个数据用逗号隔开

  ```javascript
  function getSquare(num1) {
  	document.write(num1+num1)
  }
  ```

* **调用语法**

  ```javascript
  函数名(传递的参数列表)
  ```

* 例

  ```javascript
  getSquare(8)
  ```

  ```javascript
  function getSum(num1, num2) {
          document.write(num1 + num2);
        }
        getSum(1, 2);
  ```

* **形参和实参**

  * 形参：声明函数时写在函数名右边小括号里的叫形参（形式上的参数）
  * 实参：调用函数时写在函数名右边小括号里的叫实参（实际上的参数）
  * ==形参可以理解为是==在这个函数内声明的==变量==实参可以理解为是给这个变量赋值
  * ==开发中尽量保持形参和实参个数一致==

  

## 函数的返回值

**1.为什么要让函数有返回值**

执行完特定任务后，需要把结果返回给我们。

**2.用return返回数据**

* 当函数需要返回数据出去时，用`return`关键字

* 语法

  `return 数据` `return 20`

* 怎么使用呢？

  ```javascript
  function getSum(x,y) {
  	return x + y
  }
  let num = getSum(10,30)
  document.write(num)
  ```

* **细节**

  * 在函数体中使用`return`关键字能够将内部的执行结果交给函数外部使用
  * 在函数内部只能出现一次`return`,并且`return`后面代码不会再被执行，所以==`return` 后面的数据不要换行写==
  * `return`会立即结束当前函数
  * 函数可以没有`return`这种情况函数默认返回值为undefined

**return返回多个值**

```javascript
function fn(x, y) {
        let jia = x + y;
        let jian = x - y;
        return [jia, jian];
      }
      let maxAmin = fn(2, 4);
      console.log(`加起来是${maxAmin[0]},减起来是${maxAmin[1]}`);
```

* 利用数组来存储多个数据

## 作用域

 **1.作用域概述**
通常来说，一段程序代码中所用到的名字并不总是有效和可用的，而限定这个名字的==可用性的代码范围==就是这个名字的==作用域==。作用域的使用提高了程序逻辑的局部性，增强了程序的可靠性，减少了名字冲突。

**1.1全局作用域**

全局有效，作用于所有代码执行的环境（整个script标签内部）或者一个独立的js文件

**1.2局部作用域**

局部有效，作用于函数内代码环境，就是局部作用域。因为跟函数有关系，所以也称为函数作用域。

**1.3块级作用域**

{}内有效 块作用域由{}包括，if语句和for语句里面的{}等

**2.变量的作用域**

在JavaScript中，根据作用域的不同，变量可以分为

* 全局变量： ==函数外部let的变量==，全局变量在任何区域都可以访问和修改
* 局部变量：==函数内部let的变量==，局部变量只能在当前函数内部访问和修改
* 块级变量：=={}内部的let变量==，let定义的变量，只能在块级作用域里访问，不能跨块访问，也不能跨函数访问

**变量的坑**

* 如果含糊内部或者块级作用域内部，变量没有声明，直接赋值，也当==全局变量==看，但是强烈不推荐
* 但是有一种情况，函数内部的形参可以看做是局部变量

**3.变量的访问原则-作用域链**

* 只要是代码，就至少有一个作用域
* 写在函数内部的局部作用域
* 如果函数中还有函数，那么在这个作用域中就又可以诞生一个作用域
* 根据在内部函数可以访问外部函数变量的这种机制，用链式查找决定那些数据能被内部函数访问，就被称作作用域链
* 作用域链：采取==就近原则==的方式来查找变量最终的值

## 匿名函数

`function() {}`

**1.匿名函数**

将匿名函数赋值给一个变量，并且通过变量名称进行调用，我们将这个成为函数表达式

**语法：**

```javascript
let fn = function () {
    //函数体
}
```

**调用**

```javascript
fn()
```

 **2.立即执行函数**

场景介绍：避免全局变量之间的污染

**语法：**

```javascript
//方式1
(function() { console.log(111) })()
//方法2
(function() { console.log(111) }())
// 不需要调用，立即执行
```

> 注意：多个立即执行函数要用;隔开，要不然会报错

---

# 对象

## 什么是对象？

**1.1对象是什么 **

* 对象（object）：JavaScript里的一种数据类型
* 可以理解为是一种无序的数据集合
* 用来描述某个事物，例如描述一个人
  * 人有姓名、年龄、性别等信息
  * 如果用多个变量保存则比较散，用对象比较统一
* 比如描述班主任的信息
  * 静态特征（姓名、年龄、身高、性别）=> 可以使用数字，字符串，数组，布尔类型等表示
  * 动态行为（点名、唱、跳）=> 使用函数表示

---

## 对象使用

**1.对象声明语法**

`let 对象名 = {}`

**例如**

`let person = {} `://声明了一个person的对象

**2.对象有属性和方法组成**

* 属性：信息或叫特征（名词）

* 方法：功能或叫行为（动词）

  ```javascript
  let 对象名 = {
      属性名: 属性值,
      方法名: 函数
  }
  ```

**3.属性**
数据描述性的信息称为属性，如人的姓名、身高、年龄等，一般是名词性的

```javascript
let person = {
    uname : 'andy',
    age : 18 ,
    sex : '男'
}
```

* 属性都是成对出现的，包括属性名和值，它们之间使用英文 : 分割
* 多个属性之间使用英文 , 分隔
* 属性就是依附在对象上的变量（外面是变量，对象内是属性）
* 属性名可以使用“”或‘’，==一般情况下省略==，除非名称遇到特殊符号如空格，中横线等

**4.属性访问**
声明对象，并添加了若干属性后，可以使用.或[]获得对象中属性对应的值，我们称之为属性访问

```javascript
let person = {
    uname : 'andy',
    age : 18 ,
    sex : '男'
}
console.log(person.name)
console.log(person.age)//第一种访问方法
//第二种
console.log(person['name'])
console.log(person['age'])
```

**5.对象中的方法**
数据行为性的信息称为方法、如跑步、唱歌等，一般是动词性的，其本质是函数

```javascript
let person = {
    name: 'andy'
    sayHi: function() {
        document.write('hi~~~')
    }
}
```

1. 方法是由方法名和函数俩部分构成，他们之间使用 : 分隔
2. 多个属性之间使用英文 , 分隔
3. 方法是依附在对象里面的函数
4. 方法名可以使用“” 或 ‘’ ，一情况下省略。除非名称遇到特殊符号如空格、中横线等。

**6.对象中的方法访问**
声明对象，并添加了若干方法后，可以使用 . 调用对象中函数，称之为方法调用

```javascript
let person = {
        uname: 'andy',
        sayHi: function () {
          console.log('hi~~');
        },
      };
      // 调用方法 对象.方法名()
      person.sayHi();
```

---

## 操作对象

对象本质是无序的数据集合，操作数据无非就是 ==增 删 改 查==语法：

**查询对象**

`对象.属性`或者`对象['属性']` `对象.方法( )`

**重新赋值**

`对象.属性 = 值`  	`对象.方法 = function() {}`

**对象添加新的数据**

`对象名.新属性名 = 新值`

==增加属性==：也可以动态为对象添加属性，动态添加与直接定义是一样的，只是语法上更加灵活

```javascript
let person = {
    name: 'andy',
    age: '18’
}
person.hobby = '足球'
person['sex'] = '男'
console.log(person)
```

打印结果如下：![image-20221118144212892](C:\Users\20747\Desktop\JavaScript学习\assets\image-20221118144212892.png)

==新增对象中的方法==:也可以动态为对象添加方法，动态添加与直接定义是一样的，只是语法上更加灵活

```javascript
person.move = function() {
    console.log('移动一点点')
}
```

> 无论是属性或是方法，同一个对象中出现名称一样的，后面会覆盖前面的

**删除对象中属性**

`delete 对象名 .属性名`

---

## 遍历对象

**遍历对象**

对象没有像数组一样的length属性，所以无法确定长度

对象里面是无需的键值对，没有规律，不像数组里面有规律的下标

**语法：**

`for(let k in 对象名){}`

**例**

```javascript
 let person = {
        name: 'andy',
        age: '18',
        sex: '男',
      };
      //   for in 循环语句
      // 语法
      // for(let k in 对象名){}
      // k 是变量  k  或者 key
      for (let k in person) {
        console.log(k); // 属性名
        console.log(person[k]);
      }
```

*一般不用这种方式遍历数组、主要是用来遍历对象

一定记住：==k==是获得对象的==属性名==，==对象名[k]==是获得==属性值==

**遍历数组对象**

```javascript
let students = [
        { name: '小明', age: 18, gender: '男', hometown: '河北省' },
        { name: '小红', age: 19, gender: '女', hometown: '河南省' },
        { name: '小刚', age: 17, gender: '男', hometown: '山西省' },
        { name: '小丽', age: 18, gender: '女', hometown: '山东省' },
      ];
      for (let i = 0; i < students.length; i++) {
        console.log(students[i].name);
      }
```

---

## 内置对象

 ## 内置对象是什么？

* JavaScript内部提供的对象，包含各种属性和方法给开发者调用

## 内置对象Math

* math对象是JavaScript提供的一个”数学高手“对象
* 提供了一系列做数学运算的方法
* 方法有
  * random ：生成0-1之间的随机数（包含0不包括1）
  * ceit：向上取整
  * floor：向下取整
  * max：找最大数
  * min：找最小数
  * pow：幂运算
  * abs：绝对值

[MDN Web 在线文档][https://developer.mozilla.org/zh-CN/] :可查询语法

**随机数公式**

`Math.floor(Math.random() * (M - N + N)) + N;`

**封装随机数函数**

```javascript
 function getRandom(min, max) {
        return Math.floor(Math.random() * (max - min + min)) + min;
      }
```

---

 # 拓展-基本数据类型和引用数据类型

简单类型又叫做基本数据类型或者==值类型==，复杂类型又叫做==引用类型==

* 值类型：简单数据类型/基本数据类型，在存储时变量中存储的是值本身，因此叫做值类型

`string` ，`number`，`boolean`，`undefined`，`null`

* 引用类型：复杂数据类型，在存储时变量中存储的仅仅是地址（引用），因此叫做引用数据类型 通过 `new` 关键字创建的对象（系统对象、自定义对象），如 `Object`、`Array`、`Date`等

**堆栈空间分配区别：**

1.栈（操作系统）：由操作系统自动分配释放存放函数的参数值、局部变量的值等。其操作方式类似于数据结构中 的栈；

==简单数据类型存放到栈里面==

2. 堆（操作系统）：存储复杂类型(对象)，一般由程序员分配释放，若程序员不释放，由垃圾回收机制回收

==引用数据类型存放到堆里面==

## 简单类型的内存分配

* 值类型（简单数据类型）： `string` ，`number`，`boolean`，`undefined`，`null`

* 值类型变量的数据直接存放在变量（栈空间）中

![image-20221119205353464](C:\Users\20747\Desktop\JavaScript学习\assets\image-20221119205353464.png)

## 复杂类型的内存分配

* 引用类型（复杂数据类型）：通过 `new` 关键字创建的对象（系统对象、自定义对象），如 `Object`、`Array`、`Date`等

* 引用类型变量（栈空间）里存放的是地址，真正的对象实例存放在堆空间中

![image-20221119205450950](C:\Users\20747\Desktop\JavaScript学习\assets\image-20221119205450950.png)

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

`change`:当表单里面的值发生变化的时候触发;

##### 视频事件

`   ontimeupdate` 事件在视频/音频当前的播放位置发送改变时触发；

`   onloadeddata` 时间在当前帧的数据加载完成且还没有足够的数据播放视频/音频的下一帧触发

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
  * `e.target.tagName`:可以获得点击元素的==大写==标签名 
  * `e.target.dataset.自定义属性`可以获得自定义属性的值
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

---

# JavaScript 进阶

> 学习作用域、变量提升、闭包等语言特征，加深对 JavaScript 的理解，掌握变量赋值、函数声明的简洁语法，降低代码的冗余度。

- 理解作用域对程序执行的影响
- 能够分析程序执行的作用域范围
- 理解闭包本质，利用闭包创建隔离作用域
- 了解什么变量提升及函数提升
- 掌握箭头函数、解析剩余参数等简洁语法

### 一、作用域

> 了解作用域对程序执行的影响及作用域链的查找机制，使用闭包函数创建隔离作用域避免全局变量污染。

作用域（scope）规定了变量能够被访问的“范围”，离开了这个“范围”变量便不能被访问，作用域分为全局作用域和局部作用域。

#### 1.1 局部作用域

局部作用域分为函数作用域和块作用域。

##### 函数作用域

在函数内部声明的变量只能在函数内部被访问，外部无法直接访问。

```html
<script>
  // 声明 counter 函数
  function counter(x, y) {
    // 函数内部声明的变量
    const s = x + y
    console.log(s) // 18
  }
  // 设用 counter 函数
  counter(10, 8)
  // 访问变量 s
  console.log(s)// 报错
</script>
```

总结：

1. 函数内部声明的变量，在函数外部无法被访问
2. 函数的参数也是函数内部的局部变量
3. 不同函数内部声明的变量无法互相访问
4. 函数执行完毕后，函数内部的变量实际被清空了

##### 块作用域

在 JavaScript 中使用 `{}` 包裹的代码称为代码块，代码块内部声明的变量外部将【有可能】无法被访问。

```html
<script>
  {
    // age 只能在该代码块中被访问
    let age = 18;
    console.log(age); // 正常
  }
  
  // 超出了 age 的作用域
  console.log(age) // 报错
  
  let flag = true;
  if(flag) {
    // str 只能在该代码块中被访问
    let str = 'hello world!'
    console.log(str); // 正常
  }
  
  // 超出了 age 的作用域
  console.log(str); // 报错
  
  for(let t = 1; t <= 6; t++) {
    // t 只能在该代码块中被访问
    console.log(t); // 正常
  }
  
  // 超出了 t 的作用域
  console.log(t); // 报错
</script>
```

JavaScript 中除了变量外还有常量，常量与变量本质的区别是【常量必须要有值且不允许被重新赋值】，常量值为对象时其属性和方法允许重新赋值。

```html
<script>
  // 必须要有值
  const version = '1.0.0';

  // 不能重新赋值
  // version = '1.0.1';

  // 常量值为对象类型
  const user = {
    name: '小明',
    age: 18
  }

  // 不能重新赋值
  user = {};

  // 属性和方法允许被修改
  user.name = '小小明';
  user.gender = '男';
</script>
```

总结：

1. `let` 声明的变量会产生块作用域，`var` 不会产生块作用域
2. `const` 声明的常量也会产生块作用域
3. 不同代码块之间的变量无法互相访问
4. 推荐使用 `let` 或 `const`

注：开发中 `let` 和 `const` 经常不加区分的使用，如果担心某个值会不小被修改时，则只能使用 `const` 声明成常量。

#### 1.2 全局作用域

`<script>` 标签和 `.js` 文件的【最外层】就是所谓的全局作用域，在此声明的变量在函数内部也可以被访问。

```html
<script>
  // 此处是全局
  
  function sayHi() {
    // 此处为局部
  }

  // 此处为全局
</script>
```

全局作用域中声明的变量，任何其它作用域都可以被访问，如下代码所示：

```html
<script>
    // 全局变量 name
    const name = '小明'
  
  	// 函数作用域中访问全局
    function sayHi() {
      // 此处为局部
      console.log('你好' + name)
    }

    // 全局变量 flag 和 x
    const flag = true
    let x = 10
  
  	// 块作用域中访问全局
    if(flag) {
      let y = 5
      console.log(x + y) // x 是全局的
    }
</script>
```

总结：

1. 为 `window` 对象动态添加的属性默认也是全局的，不推荐！
2. 函数中未使用任何关键字声明的变量为全局变量，不推荐！！！
3. 尽可能少的声明全局变量，防止全局变量被污染

JavaScript 中的作用域是程序被执行时的底层机制，了解这一机制有助于规范代码书写习惯，避免因作用域导致的语法错误。

#### 1.3 作用域链

在解释什么是作用域链前先来看一段代码：

```html
<script>
  // 全局作用域
  let a = 1
  let b = 2
  // 局部作用域
  function f() {
    let c
    // 局部作用域
    function g() {
      let d = 'yo'
    }
  }
</script>
```

函数内部允许创建新的函数，`f` 函数内部创建的新函数 `g`，会产生新的函数作用域，由此可知作用域产生了嵌套的关系。

如下图所示，父子关系的作用域关联在一起形成了链状的结构，作用域链的名字也由此而来。

---



作用域链本质上是底层的==变量查找机制==

* 在函数被执行时，会==优先查找当前==函数作用域中查找变量
* 如果当前作用域查找不到则会依次==逐级查找父级作用域==直到全局作用域，如下代码所示：

```html
<script>
  // 全局作用域
  let a = 1
  let b = 2

  // 局部作用域
  function f() {
    let c
    // let a = 10;
    console.log(a) // 1 或 10
    console.log(d) // 报错
    
    // 局部作用域
    function g() {
      let d = 'yo'
      // let b = 20;
      console.log(b) // 2 或 20
    }
    
    // 调用 g 函数
    g()
  }

  console.log(c) // 报错
  console.log(d) // 报错
  
  f();
</script>
```

总结：

1. 嵌套关系的作用域串联起来形成了作用域链
2. 相同作用域链中按着从小到大的规则查找变量
3. 子作用域能够访问父作用域，父级作用域无法访问子级作用域

#### 1.4 闭包

闭包是一种比较特殊和函数，使用闭包能够访问函数作用域中的变量。从代码形式上看闭包是一个做为返回值的函数，如下代码所示：

```html
<script>
  function foo() {
    let i = 0;

    // 函数内部分函数
    function bar() {
			console.log(++i);
    }

    // 将函数做为返回值
    return bar;
  }
  
  // fn 即为闭包函数
  let fn = foo();
  
  fn(); // 1
</script>
```

总结：

1. 闭包本质仍是函数，只不是从函数内部返回的
2. 闭包能够创建外部可访问的隔离作用域，避免全局变量污染
3. 过度使用闭包可能造成内存泄漏

注：回调函数也能访问函数内部的局部变量。

#### 1.5 变量提升

变量提升是 JavaScript 中比较“奇怪”的现象，它允许在变量声明之前即被访问，

```html
<script>
  // 访问变量 str
  console.log(str + 'world!');

  // 声明变量 str
  var str = 'hello ';
</script>
```

总结：

1. 变量在未声明即被访问时会报语法错误
2. 变量在声明之前即被访问，变量的值为 `undefined`
3. `let` 声明的变量不存在变量提升，推荐使用 `let`
4. 变量提升出现在相同作用域当中
5. 实际开发中推荐先声明再访问变量

注：关于变量提升的原理分析会涉及较为复杂的词法分析等知识，而开发中使用 `let` 可以轻松规避变量的提升，因此在此不做过多的探讨，有兴趣可[查阅资料](https://segmentfault.com/a/1190000013915935)。

### 二、函数

> 知道函数参数默认值、动态参数、剩余参数的使用细节，提升函数应用的灵活度，知道箭头函数的语法及与普通函数的差异。

#### 2.1 函数提升

函数提升与变量提升比较类似，是指函数在声明之前即可被调用。

```html
<script>
  // 调用函数
  foo()
  // 声明函数
  function foo() {
    console.log('声明之前即被调用...')
  }

  // 不存在提升现象
  bar()  // 错误
  var bar = function () {
    console.log('函数表达式不存在提升现象...')
  }
</script>
```

总结：

1. 函数提升能够使函数的声明调用更灵活
2. 函数表达式不存在提升的现象
3. 函数提升出现在相同作用域当中

#### 2.2 参数

函数参数的使用细节，能够提升函数应用的灵活度。

##### 默认值

```html
<script>
  // 设置参数默认值
  function sayHi(name="小明", age=18) {
    document.write(`<p>大家好，我叫${name}，我今年${age}岁了。</p>`);
  }
  // 调用函数
  sayHi();
  sayHi('小红');
  sayHi('小刚', 21);
</script>
```

总结：

1. 声明函数时为形参赋值即为参数的默认值
2. 如果参数未自定义默认值时，参数的默认值为 `undefined`
3. 调用函数时没有传入对应实参时，参数的默认值被当做实参传入

##### 动态参数

`arguments` 是函数内部内置的伪数组变量，它包含了调用函数时传入的所有实参。

```html
<script>
  // 求生函数，计算所有参数的和
  function sum() {
    // console.log(arguments)
    let s = 0
    for(let i = 0; i < arguments.length; i++) {
      s += arguments[i]
    }
    console.log(s)
  }
  // 调用求和函数
  sum(5, 10)// 两个参数
  sum(1, 2, 4) // 两个参数
</script>
```

总结：

1. `arguments` 是一个伪数组
2. `arguments` 的作用是动态获取函数的实参

##### 剩余参数

```html
<script>
  function config(baseURL, ...other) {
    console.log(baseURL) // 得到 'http://baidu.com'
    console.log(other)  // other  得到 ['get', 'json']
  }
  // 调用函数
  config('http://baidu.com', 'get', 'json');
</script>
```

总结：

1. `...` 是语法符号，置于最末函数形参之前，用于获取多余的实参
2. 借助 `...` 获取的剩余实参，是个真数组

#### 2.3 箭头函数

箭头函数是一种声明函数的简洁语法，它与普通函数并无本质的区别，差异性更多体现在语法格式上。

```html
<script>
  // 箭头函数
  const foo = () => {
    console.log('^_^ 长相奇怪的函数...');
  }
  // 调用函数
  foo()
  
  // 更简洁的语法
  const form = document.querySelector('form')
  form.addEventListener('click', ev => ev.preventDefault())
</script>
```

```javascript
 //  普通的函数表达式
      let fun = function () {
        console.log(1);
      };
      //   箭头函数表达式
      let fun1 = () => {
        console.log(1);
      };
      //  当形参只有一个的时候可以省略小括号
      let fun2 = x => {
        console.log(x + x);
      };
      //   当只有一句话的时候，可以省略大括号并且之间返回
      let fun3 = x => console.log(x + x);
      //   可以返回一个对象
      let fun4 = uname => ({ uname: uname });
      console.log(fun4('刘德华'));
```

##### 箭头函数参数

1. 普通函数里有`arguments`动态参数
2. ==箭头函数==没有`arguments`动态参数,但是==有剩余参数===`...arr`

**例子:**

```javascript
const getSum = (...arr) => {
        let sum = 0;
        for (let i = 0; i < arr.length; i++) {
          sum += arr[i];
        }
        return sum;
      };
      console.log(getSum(2, 3));
```

---

##### 箭头函数this

在箭头函数出现之前,每一个新函数根据它是被==如何调用的==来定义这个函数的this值,非常令人讨厌.

==箭头函数不会创建自己的this==

总结：

1. 箭头函数属于表达式函数，因此不存在函数提升
2. 箭头函数只有一个参数时可以省略圆括号 `()`
3. 箭头函数函数体只有一行代码时可以省略花括号 `{}`，并自动做为返回值被返回
4. 箭头函数中没有 `arguments`，只能使用 `...` 动态获取实参

### 三、解构赋值

> 知道解构的语法及分类，使用解构简洁语法快速为变量赋值。

解构赋值是一种快速为变量赋值的简洁语法，本质上仍然是为变量赋值，分为数组解构、对象解构两大类型。

#### 3.1 数组解构

数组解构是将数组的单元值快速批量赋值给一系列变量的简洁语法，如下代码所示：

```html
<script>
  // 普通的数组
  let arr = [1, 2, 3];
  // 批量声明变量 a b c 
  // 同时将数组单元值 1 2 3 依次赋值给变量 a b c
  let [a, b, c] = arr;
  console.log(a); // 1
  console.log(b); // 2
  console.log(c); // 3
</script>
```

总结：

1. 赋值运算符 `=` 左侧的 `[]` 用于批量声明变量，右侧数组的单元值将被赋值给左侧的变量
2. 变量的顺序对应数组单元值的位置依次进行赋值操作
3. 变量的数量大于单元值数量时，多余的变量将被赋值为  `undefined`
4. 变量的数量小于单元值数量时，可以通过 `...` 获取剩余单元值，但只能置于最末位
5. 允许初始化变量的默认值，且只有单 元值为 `undefined` 时默认值才会生效

注：支持多维解构赋值，比较复杂后续有应用需求时再进一步分析

#### 3.2 对象解构

对象解构是将对象属性和方法快速批量赋值给一系列变量的简洁语法，如下代码所示：

```html
<script>
  // 普通对象
  const user = {
    name: '小明',
    age: 18
  };
  // 批量声明变量 name age
  // 同时将数组单元值 小明  18 依次赋值给变量 name  age
  const {name, age} = user

  console.log(name) // 小明
  console.log(age) // 18
</script>
```

##### 对象改名

```javascript
//   对象解构的变量名可以重新改名 旧变量名：新变量名
      const { uname: username, age } = {
        uname: '刘德华',
        age: 18,
      };
      console.log(username);
```

##### 解构数组对象

```javascript
const pig = [
        {
          unmae: '小明 ',
          age: 18,
        },
      ];
      const [{ unmae }] = pig;
      console.log(unmae);
```

##### 多级对象解构

```javascript
const pig = {
        name: '佩奇',
        family: {
          mother: '猪妈妈',
          father: '猪爸爸',
          sister: '乔治',
        },
      };
      const {name,family: { mother, father, sister },} = pig;
      console.log(mother);
```



总结：

1. 赋值运算符 `=` 左侧的 `{}` 用于批量声明变量，右侧对象的属性值将被赋值给左侧的变量
2. 对象属性的值将被赋值给与属性名相同的变量
3. 对象中找不到与变量名一致的属性时变量值为 `undefined`
4. 允许初始化变量的默认值，属性不存在或单元值为 `undefined` 时默认值才会生效

注：支持多维解构赋值，比较复杂后续有应用需求时再进一步分析

---

##### 遍历数组forEach方法

* `forEach()`方法用于调用数组的每个元素,并将元素传递给回调函数
* 主要使用场景:**遍历数组的每个元素**
* **语法**

```javascript
被遍历的数组.forEach(function (当前数组元素,当前元素索引号) {
    //函数体
})
```

**例如:**

```javascript
 const arr = ['red', 'pink', 'green'];
      arr.forEach(function (item, i) {
        console.log(item); //数组元素
        console.log(i); //下标
      });
```

> 注意:
>
> 1. `forEach`主要是遍历数组
> 2. 参数当前数组元素必须要写,索引号可选.

##### 筛选数组 filter方法

* `filter()`方法创建一个新的数组,新数组中的元素是通过检查指定数组中符合条件的所有元素
* 主要使用场景:==筛选数组符合条件的元素==,并返回筛选之后元素的新数组
* **语法:**

```javascript
被遍历的数组.filter(function (当前数组元素,当前元素索引号) {
	return 筛选条件
})
```

* **例子:**

```javascript
const arr = [12, 12, 43, 543];
      const arr1 = arr.filter(function (item) {
        return item >= 20;
      });
      console.log(arr1);
```

> 返回值:返回数组,包含了符合条件的所有元素.如果没有符合条件的元素则返回空数组
>
> **参数**:数组元素必须写 索引号可选
>
> 因为返回新数组,所以不会影响原数组


> 了解面向对象编程的基础概念及构造函数的作用，体会 JavaScript 一切皆对象的语言特征，掌握常见的对象属性和方法的使用。

- 了解面向对象编程中的一般概念
- 能够基于构造函数创建对象
- 理解 JavaScript 中一切皆对象的语言特征
- 理解引用对象类型值存储的的特征
- 掌握包装类型对象常见方法的使用

### 一、深入对象

> 了解面向对象的基础概念，能够利用构造函数创建对象。

#### 1.1创建对象的三种方法

1. **使用对象字面量创建对象**

```javascript
let obj = { }
```

2. **利用`new Object`创建对象**

```javascript
const obj  = new Object({ nemr: '佩奇' })
console.log(obj)
```

3. **利用构造函数创建对象**

#### 1.2 构造函数

构造函数是专门用于创建对象的函数，如果一个函数使用 `new` 关键字调用，那么这个函数就是构造函数。

```html
<script>
  // 定义函数
  function foo() {
    console.log('通过 new 也能调用函数...');
  }
  // 调用函数
  new foo;
</script>
```

```javascript
// 创建一个猪 构造函数
      function Pig(uname, age) {
        this.uname = uname;
        this.age = age;
      }
      //   2. new 关键字调用函数
      //   接受创建的对象
      const pig = new Pig('佩奇', 6);
      console.log(pig);
```



总结：

2. 使用 `new` 关键字调用函数的行为被称为实例化
3. 实例化构造函数时没有参数时可以省略 `()`
4. 构造函数的返回值即为新创建的对象
5. 构造函数内部的 `return` 返回的值无效！

注：实践中为了从视觉上区分构造函数和普通函数，习惯将构造函数的==首字母大写==。

##### 实例化执行过程

1. 立马创建一个空的对象
2. 构造函数里面的this指向的是这个空的对象
3. 执行构造函数里面的代码,修改this 添加新的对象
4. 返回新的对象

#### 1.3 实例成员

通过构造函数创建的对象称为实例对象，实例对象中的属性和方法称为实例成员。

```html
<script>
  // 构造函数
  function Person() {
    // 构造函数内部的 this 就是实例对象
    // 实例对象中动态添加属性
    this.name = '小明'
    // 实例对象动态添加方法
    this.sayHi = function () {
      console.log('大家好~')
    }
  }
  // 实例化，p1 是实例对象
  // p1 实际就是 构造函数内部的 this
  const p1 = new Person()
  console.log(p1)
  console.log(p1.name) // 访问实例属性
  p1.sayHi() // 调用实例方法
</script>
```

总结：

1. 构造函数内部 `this` 实际上就是实例对象，为其动态添加的属性和方法即为实例成员
2. 为构造函数传入参数，动态创建结构相同但值不同的对象

注：构造函数创建的实例对象彼此独立互不影响。

#### 1.4 静态成员

在 JavaScript 中底层函数本质上也是对象类型，因此允许直接为函数动态添加属性或方法，构造函数的属性和方法被称为静态成员。

```html
<script>
  // 构造函数
  function Person(name, age) {
    // 省略实例成员
  }
  // 静态属性
  Person.eyes = 2
  Person.arms = 2
  // 静态方法
  Person.walk = function () {
    console.log('^_^人都会走路...')
    // this 指向 Person
    console.log(this.eyes)
  }
</script>
```

总结：

1. 静态成员指的是添加到构造函数本身的属性和方法
2. 一般公共特征的属性或方法静态成员设置为静态成员
3. 静态成员方法中的 `this` 指向构造函数本身

### 二、内置构造函数

> 掌握各引用类型和包装类型对象属性和方法的使用。

在 JavaScript 中**最主要**的数据类型有 6 种，分别是字符串、数值、布尔、undefined、null 和 对象，常见的对象类型数据包括数组和普通对象。其中字符串、数值、布尔、undefined、null 也被称为简单类型或基础类型，对象也被称为引用类型。

在 JavaScript 内置了 一些构造函数，绝大部的数据处理都是基于这些构造函数实现的，JavaScript 基础阶段学习的 `Date` 就是内置的构造函数。

```html
<script>
  // 实例化
	let date = new Date();
  
  // date 即为实例对象
  console.log(date);
</script>
```

甚至字符串、数值、布尔、数组、普通对象也都有专门的构造函数，用于创建对应类型的数据。

#### 2.1 引用类型

##### Object

`Object` 是内置的构造函数，用于创建普通对象。

```html
<script>
  // 通过构造函数创建普通对象
  const user = new Object({name: '小明', age: 15})

  // 这种方式声明的变量称为【字面量】
  let student = {name: '杜子腾', age: 21}
  
  // 对象语法简写
  let name = '小红';
  let people = {
    // 相当于 name: name
    name,
    // 相当于 walk: function () {}
    walk () {
      console.log('人都要走路...');
    }
  }

  console.log(student.constructor);
  console.log(user.constructor);
  console.log(student instanceof Object);
</script>
```

###### 三个常用的静态方法

* `Object.keys`作用: 静态方法获取对象中所有属性(键)

* **语法:**

* ```javascript
  const o = {name:'佩奇',age:6}
  //获得对象的所有键,并且返回是一个数组
  const arr = Object.keys(o)
  console.log(arr)//['name','age']
  ```

* > 注意:返回的是一个数组

* `Object.values`作用:静态方法获取对象中所有的属性值 

* **语法;**

* ```javascript
  const o = {name:'佩奇',age:6}
  //获得对象的所有键,并且返回是一个数组
  const arr = Object.values(o)
  console.log(arr)//['佩奇',6]
  ```

**例子:**

```javascript
const o = { uname: 'pink', age: 16 };
      //   获得所有属性名
      console.log(Object.keys(o)); //返回的是一个数组
      //   获得所有的属性值
      console.log(Object.values(o)); // 返回的还是一个数组
```

* `Object.assign`:静态方法常用于对对象拷贝

* 使用:经常使用的场景==给对象添加属性==

* ```javascript
  const o = { uname: 'pink', age: 16 };
        const oo = {};
        Object.assign(oo, o);
        console.log(oo);
  ```

  ---

总结：

1. 推荐使用字面量方式声明对象，而不是 `Object` 构造函数
2. `Object.assign` 静态方法创建新的对象
3. `Object.keys` 静态方法获取对象中所有属性
4. `Object.values` 表态方法获取对象中所有属性值

##### Array

`Array` 是内置的构造函数，用于创建数组。

```html
<script>
  // 构造函数创建数组
  let arr = new Array(5, 7, 8);

  // 字面量方式创建数组
  let list = ['html', 'css', 'javascript']

</script>
```

数组赋值后，无论修改哪个变量另一个对象的数据值也会相当发生改变。

###### 数组常见实例方法-核心方法

| 方法      | 作用     | 说明                                                       |
| --------- | -------- | ---------------------------------------------------------- |
| `forEcah` | 遍历数组 | 不返回,用于不改变值,经常用于查找打印输出值                 |
| `filter`  | 过滤数组 | 筛选数组元素.并生成新的数组                                |
| `map`     | 迭代数组 | 返回新数组,新数组里面的元素是处理之后的值,经常用于处理数据 |
| `reduce`  | 累计器   | 返回函数累计处理的结果,经常用于求和等                      |

###### reduce

* **作用**:`reduce` 返回函数累计处理的结果,经常用于求和等

* **基本语法:**

* ```javascript
  arr.reduce(function(){},起始值)
  ```

* 参数:

  * 起始值可以忽略,如果写就作为第一次累计的起始值

* **语法:**

  ```javascript
  arr.reduce(function(累计值,当前元素[,索引号][,源数组]){ },起始值)
  ```

* **累计值参数:**

  1. 如果有起始值,则以起始值为准开始累计,累计值 = 起始值
  2. 如果没有起始值,则累计值以数组的第一个数组元素作为起始值开始累计
  3. 后面每次遍历就会用后面的数组元素,累计到==累计值==里面(类似求和里面的sum)

* ```javascript
  const arr = [1, 2, 3, 4, 5];
        arr.reduce(function (prev, item) {
          return prev + item;
        }, 0);
        //   箭头函数的写法
        const re = arr.reduce((prev, item) => prev + item);
        console.log(re);
  ```

---

###### 将伪数组转换成真数组

`Array.from()`传入一个伪数组后可以返回一个真数组

**语法:**

```javascript
 const lis = document.querySelectorAll(' ul li ');
      //   console.log(lis);
      const liss = Array.from(lis);
      console.log(liss);
```



总结：

1. 推荐使用字面量方式声明数组，而不是 `Array` 构造函数

2. 实例方法 `forEach` 用于遍历数组，替代 `for` 循环 (重点)

3. 实例方法 `filter` 过滤数组单元值，生成新数组(重点)

4. 实例方法 `map` 迭代原数组，生成新数组(重点) 

5. 实例方法 `join` 数组元素拼接为字符串，返回字符串(重点)

6. 实例方法  `find`  查找元素， 返回符合测试条件的第一个数组元素值，如果没有符合条件的则返回 undefined(重点)

7. 实例方法`every` 检测数组所有元素是否都符合指定条件，如果**所有元素**都通过检测返回 true，否则返回 false(重点)

8. 实例方法`some` 检测数组中的元素是否满足指定条件   **如果数组中有**元素满足条件返回 true，否则返回 false

9. 实例方法 `concat`  合并两个数组，返回生成新数组

10. 实例方法 `sort` 对原数组单元值排序

11. 实例方法 `splice` 删除或替换原数组单元

12. 实例方法 `reverse` 反转数组

13. 实例方法 `findIndex`  查找元素的索引值

    

#### 2.2 包装类型

在 JavaScript 中的字符串、数值、布尔具有对象的使用特征，如具有属性和方法，如下代码举例：

```html
<script>
  // 字符串类型
  const str = 'hello world!'
 	// 统计字符的长度（字符数量）
  console.log(str.length)
  
  // 数值类型
  const price = 12.345
  // 保留两位小数
  price.toFixed(2) // 12.34
</script>
```

之所以具有对象特征的原因是字符串、数值、布尔类型数据是 JavaScript 底层使用 Object 构造函数“包装”来的，被称为包装类型。

##### String

`String` 是内置的构造函数，用于创建字符串。

```html
<script>
  // 使用构造函数创建字符串
  let str = new String('hello world!');

  // 字面量创建字符串
  let str2 = '你好，世界！';

  // 检测是否属于同一个构造函数
  console.log(str.constructor === str2.constructor); // true
  console.log(str instanceof String); // false
</script>
```

总结：

1. 实例属性 `length` 用来获取字符串的度长(重点)
2. 
3. 实例方法 `split('分隔符')` 用来将字符串拆分成数组(重点)
4. 实例方法 `substring（需要截取的第一个字符的索引[,结束的索引号]）` 用于字符串截取(重点)
5. 实例方法 `startsWith(检测字符串[, 检测位置索引号])` 检测是否以某字符开头(重点)
6. 实例方法 `includes(搜索的字符串[, 检测位置索引号])` 判断一个字符串是否包含在另一个字符串中，根据情况返回 true 或 false(重点)
7. 实例方法 `toUpperCase` 用于将字母转换成大写
8. 实例方法 `toLowerCase` 用于将字母转换成小写
9. 实例方法 `indexOf`  检测是否包含某字符
10. 实例方法 `endsWith` 检测是否以某字符结尾
11. 实例方法 `replace` 用于替换字符串，支持正则匹配
12. 实例方法 `match` 用于查找字符串，支持正则匹配

注：String 也可以当做普通函数使用，这时它的作用是强制转换成字符串数据类型。

##### Number

`Number` 是内置的构造函数，用于创建数值。

```html
<script>
  // 使用构造函数创建数值
  let x = new Number('10')
  let y = new Number(5)

  // 字面量创建数值
  let z = 20

</script>
```

总结：

1. 推荐使用字面量方式声明数值，而不是 `Number` 构造函数
2. 实例方法 `toFixed` 用于设置保留小数位的长度



---

## 原型

* 构造函数通过原型分配的函数是所有对象所==共享的==。

* JavaScript 规定，==每一个构造函数都有一个 prototype 属性==，指向另一个对象，所以我们也称为原型对象
* 这个对象可以挂载函数，对象实例化不会多次创建原型上函数，节约内存
* ==我们可以把那些不变的方法，直接定义在 prototype 对象上，这样所有对象的实例就可以共享这些方法。==

### constructor 属性



* 每个原型对象里面都有个`constructor` 属性（`constructor` 构造函数）
* 作用:该属性指向该原型对象的==构造函数==， ==简单理解，就是指向我的爸爸，我是有爸爸的孩子==

![image-20221209150724390](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221209150724390.png)

**使用场景:**

如果有多个对象的方法，我们可以给原型对象采取对象形式赋值. 

但是这样就会覆盖构造函数原型对象原来的内容，这样修改后的原型对象 `constructor` 就不再指向当前构造函数了 

此时，我们可以在修改后的原型对象中，添加一个 `constructor` 指向原来的构造函数

**代码演示**

```javascript
function Gonezao() {}
      console.log(Gonezao.prototype.constructor === Gonezao); //true
```



---

### 对象原型

==对象都会有一个属性\__proto__== ==指向构造函数的 `prototype` 原型对象==，之所以我们对象可以使用构造函数 `prototype`  原型对象的属性和方法，就是因为对象有 `__proto__` 原型的存在。

![image-20221209150904260](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221209150904260.png)

> 注意：
>
> *  `__proto__` 是JS非标准属性
> * `[[prototype]]`和`__proto__`意义相同
> * 用来表明当前实例对象指向哪个原型对象`prototype`
> * `__proto__`对象原型里面也有一个 `constructor`属性，指向创建该实例对象的构造函数

![image-20221209151043089](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221209151043089.png)

**关系图**

![image-20221209151113176](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221209151113176.png)

**代码解释**

```javascript
 //构造函数
function Gonezao() {}
//实例化对象
      const baby = new Gonezao();
//验证实例化对象里面的__proto__对象原型是不是指向构造函数的原型对象上
      console.log(baby.__proto__ === Gonezao.prototype); // true
```



###　原型继承

**代码解释**

```javascript
      // 创建公共的属性和方法 用构造函数
      function Public() {
        this.skin = '黄皮肤';
        this.head = 1;
        this.leg = 2;
      }
      //   创建中国人 构造函数
      function Cn() {}
      //   将公共的属性挂载到中国人的原型上
      Cn.prototype = new Public();
      // 这相当于重新赋值,会导致原型对象的constructor属性被覆盖,无法指向该构造函数,我们得重新添加回去
      Cn.prototype.constructor = Cn;

      // 创建日本人
      // 中国人和日本人都有一个公共的特征 那就是 黄皮肤 俩条腿 一个鼻子
      function Rb() {}
      // 将公共的特征挂载到日本人的构造函数的原型里面
      Rb.prototype = new Public();
      Rb.prototype.constructor = Rb;
      //   比如日本人独有的一项特征就是矮 给日本人添加独有的方法
      Rb.prototype.shengao = function () {
        console.log('矮');
      };
      //   new 一个日本人出来
      const bx = new Rb();
      //   new 一个中国人
      const xm = new Cn();
      bx.shengao();
      console.log(xm);
```

---

### 原型链

基于原型对象的继承使得不同构造函数的原型对象关联在一起，并且这种关联的关系是一种链状的结构，我们将原型对 象的链状结构关系称为原型链

**图示例**

![image-20221209151339125](C:\Users\20747\Desktop\JavaScript学习\笔记\assets\image-20221209151339125.png)

#### 原型链-查找规则

1.  当访问一个对象的属性（包括方法）时，首先查找这个==对象自身==有没有该属性。
2. 如果没有就查找它的原型（也就是 __proto__指向的 ==`prototype` 原型对象==）
3. 如果还没有就查找原型对象的原型（`Object`的==原型对象==）
4. 依此类推一直找到 Object 为止（`==null`==）
5. \__proto__对象原型的意义就在于为对象成员查找机制提供一个方向，或者说一条路线

---

### 总结

> 1. 每一个构造函数都有一个`prototype`属性,这个属性的作用是用来挂载一些公共的方法,达到减少内存占用的问题,这个属性被称为原型对象,本质是一个对象
> 2. 每一个对象里面都有一个`constructor`属性,作用是指回创造自己的构造函数上去
> 3. 实例化(new)出来的对象里面也有一个\__proto__属性,用来指向原型对象,实例对象里面的原型被称之为对象原型
> 4. 构造函数和原型对象里面的`this`都指向实例化的对象
> 5. 原型链本质就是为查找开辟的一个空间,先从自身查找有没有该方法,如果没有则往上找,一直找到最大的构造函数也就是`object`原型对象,如果这个对象没有再往上找,此时返回`null`
