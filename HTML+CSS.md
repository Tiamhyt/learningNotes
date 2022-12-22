[TOC]



#  表单

## input系列标签

| 标签名 | type属性值 |                   说明                   |
| :----: | :--------: | :--------------------------------------: |
| input  |    text    |         文本框，用于输入单行文本         |
| input  |  password  |           密码框，用于输入密码           |
| input  |   radio    |            单选框，用于多选一            |
| input  |  checkbox  |            多选框，用于多选多            |
| input  |    file    |        文件选择，用于之后上传文件        |
| input  |   submit   |                 提交按钮                 |
| input  |   reset    |                 重置按钮                 |
| input  |   button   | 普通按钮，默认无功能，之后配合js添加功能 |
| input  |   images   |            图像形式的提交按钮            |
| input  |   hidden   |                  隐藏域                  |

### 1.2文本框

* type属性值：text

* 常用属性:

  |   属性名    |              说明              |
  | :---------: | :----------------------------: |
  | placeholder | 占位符，提示用户输入内容的文本 |


### 1.4单选框

* 场景：在网页中显示多选一的单选表单控件

* type属性值：radio

* 常用属性：

  | 属性名  |                             说明                             |
  | :-----: | :----------------------------------------------------------: |
  |  name   | 分组，有相同name属性值的单选框为一组，一组中同时只能有一个被选中 |
  | checked |                           默认选中                           |

* 注意点

  * name属性对于单选框有分组功能

### 1.6上传多个文件



* 场景：在网页中显示文件选择的表单控件

* type属性值：file

* 常用属性：

  |  属性名  |    说明    |
  | :------: | :--------: |
  | multiple | 多文件选择 |

  

### 1.7 按钮

* 场景：在网页中显示不同功能的按钮表单控件
* type属性值：

| 标签名 | type属性值 |                   说明                   |
| :----: | :--------: | :--------------------------------------: |
| input  |   submit   |  提交按钮。点击之后提交数据给后端服务器  |
| input  |   reset    |     重置按钮。点击之后恢复表单默认值     |
| input  |   button   | 普通按钮。默认无功能，之后配合js添加功能 |

* 注意点：
  * 如果需要实现以上按钮功能，需要配合form标签使用
  * form使用方法：用form标签把表单标签一起包裹起来即可

### 2.1button按钮标签

* 场景：在网页中显示用户点击的按钮

* 标签名：button

* type属性值（同input的按钮系列）：

  | 标签名 | type属性值 |                   说明                   |
  | :----: | :--------: | :--------------------------------------: |
  | button |   submit   |  提交按钮。点击之后提交数据给后端服务器  |
  | button |   reset    |     重置按钮。点击之后恢复表单默认值     |
  | button |   button   | 普通按钮。默认无功能，之后配合js添加功能 |

* 注意点

  * 谷歌浏览器中button默认是提交按钮
  * button标签是双标签，更便于包裹其他内容：文字、图片等



### 3.1select下拉菜单标签

* 场景：在网页中提供多个选择项的下拉菜单表单控件
* 空间组成：
  * select标签：下拉菜单的整体
  * optio标签：下拉菜单的每一项

* 常见属性：
  * selected：下拉按钮的默认选中



### 4.1 textarea文本域标签

* 场景：在网页中提供可输入多行文本的表格控件
* 标签名：textarea
* 常见属性
  * cols:规定了文本域内可见宽度
  * rows:规定了文本域内可见行数

* 注意点：
  * 右下角可以拖拽改变大小
  * 实际开发时针对于样式效果推荐用那个CSS设置



### 5.1 label标签

* 场景：常用于绑定内容和表单标签的关系
* 标签名：label
* 使用方法①：
  * 1.使用label标签把内容（如：文本）包裹起来
  * 2.在表单标签上添加id属性
  * 3.在label标签的for属性中设置对应的id属性值

* 使用方法②：

  * 1.直接使用label标签把内容（如：文本）和表单标签一起包裹起来
  * 需要把label标签的for属性删除即可

  

# 四、语义化标签

**目标：**能过认识开发中常用的  ==没有语义布局标签（div、span）和 有语义的布局标签==

**学习路径：**

1. ==没有语义的布局标签==
2. 有语义的布局标签（了解）

 

### 1.1没有语义的布局标签-div和span

* 场景：实际开发网页时会大量频繁的使用到div和span这两个没语义的布局标签
* div标签：一行只显示一个（独占一行）
* span标签：一行可以显示多个

  ### 2.1有语义的布局标签（了解）

* 场景：在HTML新版本中，推出了一些有语义的布局标签供开发者使用

* 标签：

  | 标签名  |    语义    |
  | :-----: | :--------: |
  | header  |  网页头部  |
  |   nav   |  网页导航  |
  | footer  |  网页底部  |
  |  aside  | 网页侧边栏 |
  | section |  网页区块  |
  | article |  网页文章  |

* 注意点：
  * 以上标签显示特点和div一直，但是比div多了不同的语义



# 五、字符实体

==目标：能通过 字符实体 在网页中显示特殊字符==

==学习路径：==



1. HTML中的空格合并现象
2. 常见字符实体

### 2.常见字符实体

* 场景：在网页中展现特殊符号效果时，需要使用字符实体替代
* 结构：&英文；
* 常见字符实体

| 描述 | 显示结果 | 实体名称        |
| ---- | -------- | --------------- |
|      | 空格     | &nbsp           |
| ＜   | 小于号   | &lt             |
| ＞   | 大于号   | &gt             |
| &    | 和号     | &amp            |
| “    | 引号     | &quot           |
| ′    | 撤号     | &apos(IE不支持) |
| ©    | 版权     | &copy           |



# CSS基础

## 一、基础认知

### 1.1CSS的介绍

* CSS：层叠样式表（Cascading style sheets）
* CSS作用是什么？？



css写在style标签中，style标签一般写在head标签里面，title标签下面

### 2.1CSS引入方式

* 内嵌式：CSS写在style标签中
  * 提示style标签虽然可以写在页面任意位置，但是通常约定写在head标签
* 外联式：CSS写在一个单独的.css文件中
  * 提示：需要通过link标签在网页中引入
* 行内式：CSS写在标签的style属性中
  * 提示：基础班不推荐使用，之后会配合js使用

### 2.2CSS引入方式-小节

* CSS常见三种引入方式的特点区别有哪些（书写位置、作用范围、使用场景）？

  | 书写位置 |                   引入方式                    | 作用范围 |  使用场景  |
  | :------: | :-------------------------------------------: | :------: | :--------: |
  |  内嵌式  |              CSS写在style标签中               | 当前页面 |   小案例   |
  |  外联式  | CSS写在一个单独的.css文件中，通过link标签引入 | 多个页面 |   项目中   |
  |  行内式  |           CSS写在标签的style属性中            | 当前标签 | 配合js使用 |

## 二、基础选择器

### 1.2标签选择器

* 结构：==标签名=={css属性名：属性值；}
* 作用：通过标签名，找到页面中所有这类标签，设置样式
* 注意点
* 1. 标签选择器选择的是一类标签，而不是单独某一个
  2. 标签选择器无论嵌套关系有多深，都能找到对应的标签

### 2.类选择器

* 结构：.类名{css属性名：属性值；}
* 作用：通过类名，找到页面中所有带有这个类名的标签，设置样式
* 注意点：
  1. 所有标签上都有class属性，class属性的属性值称为==类名==（类似于名字）
  2. 类名可以由数字、字母、下划线、中划线组成，但不能以数字或者中划线开头
  3. 一个标签可以同时有多个类名，类名之间以空格隔开
  4. 类名可以重复，一个类选择器可以同时选中多个标签

### 3.id选择器

* 结构：==#id属性值==（css属性名：属性值；）
* 作用：通过id属性值，找到页面中带有这个id属性值的标签，设置样式
* 注意点
  1. 所有标签上都有id属性
  2. id属性值类似于身份证号码，在一个页面中是唯一的，不可重复的！
  3. 一个标签上只能由一个id属性值
  4. 一个id选择器只能选中一个标签

### 4.通配符选择器

* 结构：*{css属性名：属性值；}
* 作用：找到页面中所有的标签，设置样式
* 注意点：
  1. 开发中使用极少，只会在极特殊情况下才会用到
  2. 在基础班小页面中可能会用于去除标签默认的margin和padding（后续讲解）

## 三、字体和文本样式

目标：能够使用  ==字体和文本相关样式== 修改元素外观样式

学习路径：

1. ==字体样式==
   1. 字体大小：font-size
   2. 字体粗细：font-weight
   3. 字体样式：font-style
   4. 字体类型：font-family
   5. 字体类型：font属性连写
2. 文本样式
3. line-height行高

### 1.1 字体大小

* 属性值：font-size
* 取值：数字+px
* 注意点：
  * 谷歌浏览器默认文字大小是16px
  * 单位需要设置：否则无效

### 1.2字体粗细

* 属性名：font-weight

* 取值：

  * 关键字：

  | 正常 | normal |
  | ---- | ------ |
  | 加粗 | bold   |

  * 纯数字：100~9000的整百数

    | 正常 | 400  |
    | ---- | ---- |
    | 加粗 | 700  |

* 注意点：

  * 不是所有字体都提供了九种粗细，因此部分取值页面中无变化
  * 实际上开发中以：正常、加粗两种取值使用最多。

### 1.3字体样式（是否倾斜）

* 属性名：font-style
* 取值：
  * 正常（默认值）：normal
  * 倾斜：italic

### 1.4常见字体系列（了解）

* 无衬线字体（sans-serif）

1. 特点：文字笔画粗细均匀，并且首尾无装饰
2. 场景：网页中大多采用无衬线字体
3. 常见该系列字体：黑体、Arial

* 衬线字体（serif）

1. 特点：文字画笔粗细不均，并且首尾有笔锋装饰
2. 场景：报刊书籍中应用广泛
3. 常见该系列字体：宋体、Times New Roman

* 等宽字体（monospace）

1. 特点：每个字母或文字的宽度相等
2. 场景：一般用于程序代码编写，有利于代码的阅读和编写
3. 常见该系列字体：Consolas、fira code

### 1.5字体系列font-family

* 属性名：font-family

* 常见取值：具体字体1，具体文字2，具体文字3，具体文字4，......，字体系列
  * 具体文字：”Microsoft YaHei“\微软雅黑、黑体、宋体、楷体等......
  * 字体系列：sans-serif\serif\monospace等......
  
* 渲染规则:
  1. 从左往右按照顺序查找，如果电脑中未安装该字体，则显示下一个字体
  2. 如果都不支持，此时会根据操作系统，显示最后字体系列的默认字体
  
* 注意力：fh
  1. 如果字体名称中存在多个单词，推荐使用引号包裹
  2. 最后一项==字体系列不需要引号包裹==
  3. 网页开发时，尽量使用系统常见自带字体，保证不同用户浏览网页都可以正确显示
  
  | 系统    | 默认字体 |
  | ------- | -------- |
  | Windows | 微软雅黑 |
  | macOS   | 苹方     |
  
  

### 1.6样式的层叠问题

* 问题
  * 给同一个标签设置了相同的样式，此时浏览器会如何渲染呢？
* 结果：
  * 如果给同一个标签设置了相同的属性，此时像是会层叠（覆盖），写在最下面的会生效
* TIP：
  * CSS（Cascading style sheets）==层叠样式表==
  * 所谓的层叠即叠加的意思，表示样式可以一层一层的层叠覆盖

### 字体font相关属性的连写

* 属性名：font(符合属性)
* 取值：
  * font:style weight size family;
* 省略要求：
  * 只能省略前两个，如果省略了相当于设置了默认值
* 注意点：如果需要同时设置单独和连写形式
  * 要么把单独的样式写在连写的下面
  * 要么把单独的样式写在连写的里面



1. 字体样式
2. 文本样式
   1. 文本缩进：text-indent
   2. 文本水平对齐效果：text-align
   3. 文本修饰：text-decoration
3. line-height行高

### 2.1文本缩进

* 属性值：text-indent
* 取值：
  * 数字+px
  * 数字+em(推荐：1em=当前标签的font-size的大小)

### 2.2 文本水平对齐方式

* 属性名：text-align
* 取值：

| 属性值 |   效果   |
| :----: | :------: |
|  left  |  左对齐  |
| center | 居中对齐 |
| right  |  右对齐  |

* 注意点
  * 如果需要让文本水平居中，text-align属性给文本所在标签（文本的父元素）设置

### 2.3 文本修饰

* 属性名：text-decoration
* 取值：

| 属性值        | 效果               |
| ------------- | ------------------ |
| underlineunde | 下划线（常用）     |
| line-through  | 删除线（不常用）   |
| overline      | 上划线（几乎不用） |
| none          | 无装饰线（常见）   |

* 注意点：
  * 开发中会使用 ==text-decoration:none;清楚a标签默认的下划线==





### 2.4 水平居中方式总结 text-align:center

* text-align:center 能让哪些元素水平居中

1. 文本
2. span标签、a标签
3. input标签、img标签

* 注意点：

1. 如果需要让以上1元素水平居中，text-align:center需要给以上元素的父元素设置



### 3.1行高

* 作用：控制一行的上下行间距
* 属性名：line-height
* 取值：
  * 数字+px
  * 倍数（当前标签font-size的倍数）
* 应用：
  1. 让==单行文字==垂直居中可以设置==line-height：文字父元素高度==
  2. 网页精准布局时，会设置line-height:1可以取消上下间距
* 行高与font连写的注意点
  * 如果同时设置了行高和font连写，注意覆盖问题
  * font : style weight size/line-height family;

### 标签水平居中方法总结 margin:0 auto

* 如果需要让div、p、h（大盒子）水平居中？
  * 可以通过margin:0 auto；实现
* 注意点：
* 1. 如果需要让div、p、h（大盒子）水平居中，直接给==当前元素本身==设置即可
  2. margin：0 auto 一般针对固定宽度的盒子，如果大盒子没有设置宽度，此时会默认占满父元素的宽度





# CSS进阶

## 一、选择器进阶

### 1.1 后代选择器：空格

* 作用：根据 HTML标签的嵌套关系、选择父元素 后代中满足条件的元素
* 选择器语法：==选择器1 选择器2{css}==
* 结果：
  * 在选择器1所找到标签的后代（儿子、孙子、重孙子...）中、找到满足选择器2的标签，设置样式
* 注意点
  1. 后代包括：儿子、孙子、重孙子......
  2. 后代选择器中，选择器与选择器之前通过 ==空格== 隔开

### 1.2 子代选择器：>

* 作用：根据 HTML 标签的嵌套关系，选择父元素 子代中 满足条件的元素
* 选择器语法：选择器1>选择器2{css}
* 结果：
  * 在选择器1所找到的标签的子代（儿子）中，找到满足选择器2的标签，设置样式
* 注意点：
  1. 子代只包括：儿子
  2. 子代选择器中，选择器与选择器之前通过 > 隔开



### 2.1 并集选择器：,

* 作用：同时选择多组标签，设置相同的样式
* 选择器语法：选择器1，选择器2 {css}
* 结果：
  * 找到 选择器1 和  选择器2 选中的标签，设置样式
* 注意点：
  1. 并集选择器中的每组选择器之间通过,分隔
  2. 并集选择器中的每组选择器可以是基础选择器或者复合选择器
  3. 并集选择器中的每组选择器通常一行写一个，提高代码的可读性

### 2.2 交集选择器：紧挨着

* 作用：选中页面中 同时 ==同时满足== 多个选择器的标签
* 选择器语法：选择器1选择器2{css}
* 结果：
  * （既有原则）找到页面中 ==既== 能被选择器1选中， ==又== 能让选择器2选中的标签，设置样式
* 注意点：
  1. 交集选择器中的选择器之间是紧挨着的，没有东西分隔
  2. 交集选择器中如果右标签选择器，标签选择器必须写在最前面

### 4.1 hover伪类选择器

* 作用：选中鼠标悬停在元素上的状态，设置样式
* 选择器语法：选择器：hover{css}
* 注意点：
  1. 伪类选择器选中的元素的某种状态

### 5.1 emmet语法

* 作用：通过简写语法，快速生成代码

* 语法：

  * 类似于刚刚学习的选择器的写法

    |    记忆    |        示例         |                 效果                 |
    | :--------: | :-----------------: | :----------------------------------: |
    |   标签名   |         div         |             <div></div>              |
    |  类选择器  |        .red         |       <div class="red"></div>        |
    |  id选择器  |        #one         |         <div id="one"></div>         |
    | 交集选择器 |      p.red#one      |     <p class="red" id="one"></p>     |
    | 子代选择器 |        ul>li        |          <ul><li></li></ul>          |
    |  内部文本  | ul>li{我是li的内容} |    <ul><li>我是li的内容</li></ul>    |
    |  创建多个  |       ul>li*3       | <ul><li></li><li></li><li></li></ul> |

    

    

## 二、背景相关属性



### 1.1 背景颜色

* 属性名：==background-color(bgc)==
* 属性值：
  * 颜色取值：关键字、rgb表示法、rgba表示法、十六进制......
* 注意点：
  * 背景颜色默认值是透明：rgba(0,0,0,0)、transoarent
  * 背景颜色不会影响盒子大小、并且还能看清盒子的大小和位置，一般在布局中会习惯先给盒子设置背景颜色

### 2.1 背景图片

* 属性名：background-image (bgi)
* 属性值：background-image:url('图片的路径')
* 注意点：
  * 背景图片中url中可以省略引号
  * 背景图片默认是在水平和垂直方向平铺的
  * 背景图片仅仅是指给盒子起到装饰效果，类似于背景颜色，是不能撑开盒子的

### 3.1 背景平铺

* 属性名：background-repeat(bgr)

* 属性值：

  |   取值    |             效果             |
  | :-------: | :--------------------------: |
  |  repeat   | (默认值)水平和垂直方向都平铺 |
  | no-repeat |            不平铺            |
  | repeat-x  |   沿着水平方向（x轴）平铺    |
  | repeat-y  |   沿着垂直方向（y轴）平铺    |

  

### 4.1 背景位置

* 属性名：background-position(bgp)
* 属性值：background-position:水平方向 位置 垂直方向位置；
* ![image-20220516201404770](C:\Users\Shokuzaino\AppData\Roaming\Typora\typora-user-images\image-20220516201404770.png)
* 注意点：
  * 方位名词取值和坐标取值可以混用，第一个取值表示水平，第二个去指标是垂直

### 5.1 背景相关属性的连写形式

* 属性名：background（bg）
* 属性值：
  * 单个属性值的合写，取值之间以空格隔开
* 书写顺序：
  * 推荐：background： color image repeat position
* 省略问题
  * 可以按照需求省略
  * 特殊情况：在pc端，如果盒子大小和背景图片大小一样，此时可以直接写background：url()

* 注意点
  * 如果需要设置单独的样式和连写
  * ①要么把单独的样式写在连写的下面
  * ②要么把单独的样式写在连写的里面

### 6.1 （拓展）img标签和背景图片的区别

* 需求：需要在网页中展示一张图片的效果
* 方法一：直接写上img标签即可
  * img标签是一个标签，不设置宽高默认会以原尺寸显示
* 方法二：div标签+背景图片
  * 需要设置div的宽度，因为背景图片只是装饰的CSS样式，不能撑开div标签

## 三、元素显示模式

### 1.1 块级元素

* 显示特点：
  1. 独占一行(一行只能显示一个)
  2. 宽度默认是父元素的宽度，高度默认由内容撑开
  3. 可以设置宽高
* 代表标签：
  * div、p、h系列、ul、li、dl、dt、dd、form、header、nav、footer......

### 2.1 行内标签

* 显示特点：
  1. 一行可以显示多个
  2. 宽度和高度默认由内容撑开
  3. 不可以设置宽高
* 代表标签：
  * <b>a</b>、<b>span</b>、b、u、i、s、strong、ins、em、del......

### 3.1 行内块元素

* 显示特点：
  1. 一行可以显示多个
  2. 可以设置宽高
* 代表标签：
  * input、textarea、button、select......
  * 特殊情况：img标签有行内块元素特点，但是Chrome调试工具中显示结果是inline

### 4.1 元素显示模式转换

* 目的：改变元素默认的显示特点，让元素符合布局要求

* 语法：

  | 属性                 | 效果             | 使用频率 |
  | -------------------- | ---------------- | -------- |
  | display block        | 转换成块级元素   | 较多     |
  | display:inline-block | 转换成行内块元素 | 较多     |
  | displau:inline       | 转换成行内元素   | 极少     |




### 拓展1：HTML嵌套规范注意点

1. 块级元素一般作为大容器，可以嵌套：文本，块级元素，行内元素，行内块元素等等......

* 但是：==p标签中不要嵌套div、p、h等块级元素==

2. a标签内部可以嵌套任意元素

* 但是：==a标签不能嵌套a标签==

## 四、CSS特性

目标：能够学习CSS的 ==继承== 和 ==层叠== 特性

### 1.1继承性的介绍

* 特性：子元素有默认继承赋予元素样式的特点（子承父业）
* 可以集成的常见属性（文字控制属性都可以继承）
  1. color
  2. font-style、font-weight、ot-size、ont-family
  3. text-indent、text-align
  4. line-height
  5. ......
* 注意点：
* * 可以通过调试工具判断样式是否可以继承

### 2.1 层叠性的介绍

* 特性：
* 1. 给同一个标签设置不同的样式→此时样式会层叠叠加→会共同作用在标签上
  2. 给同一个标签设置相同的样式→此时样式会层叠覆盖→最终写在最后的样式会生效
* 注意点：
* 1. 当样式冲突时，只有当选择器优先级相同时，才能通过层叠性判断结果







# CSS盒子模型

## 一、CSS三大特性

目标：能认识不同选择器的 ==优先级== 公式，能够进行 ==CSS 权重叠加计算==，分析并解决CSS冲突问题

### 3.1 优先级的介绍

* 特性：不同选择器具有不同的优先级，优先级高的选择器样式会覆盖优先级低选择器样式

* 优先级公式：

* * 继承<通配符选择器<标签选择器<类选择器<id选择器<行内样式<！important

    （选中的范围越广优先级越低）

* 注意点：

* 1. ！important写在属性值的后面，分好的前面！
  2. ！important不能提升继承的优先级，==只要是继承 优先级最低！==
  3. 实际开发中不建议使用！important。

### 3.2权重叠加计算

* 场景：如果是复合选择器，此时需要通过权重叠加计算，判断最终哪个选择器优先级最高会生效

* 权重叠加计算公式：（每一级之间不存在进位）

  第一级	第二级	第三级	第四级

  （0      ，      0      ，    0       ，    0   ）

  ​						↓↓↓

  ==复合选择器中：行内样式的个数，id选择器的个数，类选择器的个数，标签选择器的个数==
  
* 比较规则：

* 1. 先比较第一级数字，如果比较出来了，之后的统统不看
  2. 如果第一级数字相同，此时再去比较第二级数字，如果比较出来了，之后的统统不看
  3. ......
  4. 如果最终所有数字都相同，表示优先级相同，则比较层叠性（谁写在下面，谁说了算！）

* 注意点：==!important如果不是继承，则权重最高，天下第一!==
# 文本样式属性

` text-align `:

` letter-spacing: 10px; `:字与字产生的距离

# 网页骨架

```html
<!DOCTYPE html>

<!-- 中文网站 -->
<html lang="zh-CN">
  <head>
      <!-- 规定网页字符的编码 -->
    <meta charset="UTF-8" />

    <!-- ie（兼容性差）/edge -->
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />

    <!-- 宽度 = 设备宽度：移动端网页的时候要用 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
```





# 表单属性

input 标签 可以通过type属性值的不同，  展现的效果也不一样<br />1.text：文本框，用于输入单行文本<br />2.password:密码框，用于输入密码<br />3.radio:单选框用于多选一<br />4.checkbox：复选框，用于多选<br />5.file：文件选择，用于上传文件<br />6.submit：提交按钮，用于提交数据<br />7.reset：重置按钮，用于重置数据

8.button：普通按钮，默认无功能，可配合js添加功能

autofocus自获取焦点

readonly 将文本框变更为不可编辑的状态

marquee标签：滚动标签

属性：directio  滚动方向

取值：left  right  bottom  top

属性：behavior  滚动的次数

属性 srcollamount   



```html
 <input
        type="button"
        value="关闭窗口"
        onclick="if(window.confirm('确定关闭吗？')) window.close()"
      />

```





# 结构伪类选择器

---

**目标：能够使用 结构伪类选择器 在html中定位元素**

1. 作用：根据元素在html中的结构关系查元素
2. 优势：减少对于html中的依赖，有利于保持代码整洁
3. 场景：常用与查找某父级元素中的子元素

```html
  <style>
        /* 取偶数 */
        /* li:nth-child(2n){
            color: red;
        } */
        /* 取奇数 */
        /* li:nth-child(2n+1){
            color: red;

        } */
        /* 取4的倍数 */
        li:nth-child(4n){
            color: red;
            
        }
    </style>
</head>
<body>
    <ul>
        <li>这是第1个结构</li>
        <li>这是第2个结构</li>
        <li>这是第3个结构</li>
        <li>这是第4个结构</li>
        <li>这是第5个结构</li>
        <li>这是第6个结构</li>
        <li>这是第7个结构</li>
        <li>这是第8个结构</li>
    </ul>
</body>
```

# 伪元素

**使用伪元素在网页中创建内容**

```html
 <style>
        .one{
            width: 200px;
            height: 200px;
            background-color: pink;
        }
        .one::before{
            /* 内容 */
            content: '老鼠';
        }
        .one::after{
            content: '大米';
        }
    </style>
</head>
<body>
    <!-- 伪元素 通过css创建标签，装饰性的不重要的小图 -->
    <!-- 找父级，在这个父级里面创建子级标签 -->
    <div class="one">爱</div>
</body>
```



# 标准流

**认识标准流的默认排布方式及其特点**

标准流：又称文档流，是浏览器在渲染网页内容时采用的排版规则

---

# 浮动

```html
<style>
    div{
            /* 浏览器解析行内块或者行内标签的时候如果标签换行书写会产生一个空格的距离 */
            width: 200px;
            height: 200px;
            display: inline-block;
        }
        .one{
            background-color: pink;
            float: left;
        }
        .tow{
            background-color: skyblue;
            float: left;
        }
</style>
<body>
  
    <!-- 网页布局 -->
    <div class="one"></div>
    <div class="tow"></div>
</body>
```

## 浮动的特点

1. 浮动元素会脱离标准流，在标准流不占位置
2. 浮动不标准流高半个级别，可以覆盖标准流的元素
3. 浮动找浮动，下一个浮动元素会在上一个浮动元素后面左右浮动
4.  浮动元素有特殊的显示效果 

* 一行可以显示多个
* 可以设置宽高

```html
<style>
    /* 浮动的标签 顶对齐 */
    /* 浮动：在一行排列，宽高生效--浮动后的标签具有行内块特点*/
    .one{
        width: 100px;
        height: 100px;
        background-color: pink;
        float:left;
        margin-top: 50px;
    }
    .tow{
        width: 200px;
        height: 200px;
        background-color:skyblue;
        float: left;
        /* 因为有浮动，不能生效 */
        margin: 0 auto;
    }
    .three{
        width: 300px;
        height: 300px;
        background-color: orange;
    }
</style>
<body>
    <div class="one">one</div>
    <div class="tow">tow</div>
    <div class="three">three</div>
</body>
```

## 清除浮动

清除浮动带来的影响

* 影响：如果子元素浮动了，此时子元素不能撑开标准流的块
* 父子级标签 子级浮动，父级没有高度，后面标准流高度会收到影响

### 清除浮动的方法-额外标签法

操作：

1. 在父元素内容最后添加一个块级元素
2. 给添加的块级元素设置**clear:both**

特点：

* 缺点：会在页面中添加额外的标签，会让html结构增加

### 单伪元素清除法

```html
<style>
.clearfix::after{
content:'';
disolay:block;
clear:both;
     /* 为了兼容性 */
    height:0;
    visibility:hidden;
}
   
</style>
```



### 双伪元素清除法

```html
<style>
 /* .ckearfix::before作用：解决外边距塌陷问题 */
        /* 清除浮动 */
        .ckearfix::before,
        .cekarfix::after {
            content: '';
            display: table;
        }
        /* 真正清除浮动标签 */
        .clearfix::after {
            clear: both;
        }</style>
```

### 给父元素设置overflow: hidden

```html
<style>
    .one{
        overflow: hidden
    }
        }</style>
```



#	CSS书写顺序

1. 浮动/display
2. 盒子模型：margin boder padding 宽度 高度 背景色
3. 文字样式

# 案例 小米布局

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .box{

            margin: 0 auto;

            width: 1226px;
            height: 614px;
        }
        .left{
            float: left;

            width: 234px;
            height: 614px;
            background-color: #800088;
        }
        .tow{
            float: right;
            width: 978px;
            height: 614px;
        }
        ul{
            list-style: none;
        }
        .tow li{
            float: left;
            margin-right: 14px;
            margin-bottom: 14px;

            width: 234px;
            height: 300px;
            background-color: #87ceeb;
        }
        /* 如果父级宽度不够，子级会自动换行 */
        .tow li:nth-child(4n){
            margin: 0;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="left"></div>
        <div class="tow">
            <ul>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ul>
        </div>
    </div>
</body>
</html>
```

# 定位

## 1.1网页常见布局方式

1. **标准流**

1. 块级元素独占一行-垂直布局
2. 行内元素/行内块一行显示多个--水平布局

**2. 浮动**

1. 可以让原本垂直布局的==块级元素变成水平布局==

**3. 定位**

1. 可以让元素自由拜放在网页的任意位置

2. 一般用于==盒子之间层叠的情况==

   

   ## 2.2使用定位的步骤

   **1. 设置定位方式**

   1. 属性名：position
   2. 属性值 静态定位  static
   3. 相对定位 relative
   4. 绝对定位 absolute
   5. 固定定位 fixed

   **2.设置偏移值**

   1. 偏移值设置分俩个方向，水平或者垂直方向各选一个使用
   2. 选取的原则一般是就近原则

   水平：left  数字+px

   right 数字+px

   top 数字+px

   bottom 数字+px



## 相对定位

介绍：自恋型定位，相对于自己之前的位置进行移动

代码：position：relative;

特点

1. 需要配合方位属性实现移动
2. 相对于自己原来的位置进行移动
3. 在页面中占位置-----没有托标

**应用场景**

1. 配合绝对定位组CP
2. 用于小范围移动

```HTML
<style>
    .box{
        position: relative;
        left: 200px;
        top: 100px;
        /*
        1.占有原来的位置
        2.仍然具备标签原有的显示模式特点
        3.改变位置是参照自己原来的位置 
         */
        width: 200px;
        height: 200px;
        background-color: pink;
    }
</style>
```



## 绝对定位

介绍：拼爹型定位，相对于非静态定位的父元素进行定位

```HTML
<style>
    .box{
    /* 绝对定位：
    先找已经定位的父级，如果有这样的父级就以这个父级为参照物进行定位
    有父级，但父级没有定位，以浏览器窗口为参照物进行定位
    */
    position: absolute;
    /* 脱标，不占位置 
    2.改变标签显示模式特点：具备了行内块的特点（在一行共存且宽高生效）
    */
    left: 0px;
    top: 0;
        width: 200px;
        height: 200px;
        background-color: pink;
    }

    .father{
        width: 400px;
        height: 400px;
        background-color: pink;
    }

    .son{
        /* 父级采用相对定位 子级采用绝对定位----子绝父相   */
        position: relative;
        width: 300px;
        height: 300px;
        background-color: skyblue;
    }

    .sun{
        position: absolute;
        bottom: 50px;
        right: 20px;
        width: 200px;
        height: 200px;
        background-color: green;
    }
    /* 绝对定位查找父级方式：就近找定位的父级，如果逐层找不到这样的父级，就以浏览器窗口定位 */
</style>
```

## 定位的盒子居中的俩种方法

### 第一种

```HTML
<style>
    .box{
    /* 绝对定位：
    先找已经定位的父级，如果有这样的父级就以这个父级为参照物进行定位
    有父级，但父级没有定位，以浏览器窗口为参照物进行定位
    */
    position: absolute;
    /* 脱标，不占位置 
    2.改变标签显示模式特点：具备了行内块的特点（在一行共存且宽高生效）
    */
    left: 0px;
    top: 0;
        width: 200px;
        height: 200px;
        background-color: pink;
    }

    .father{
        width: 400px;
        height: 400px;
        background-color: pink;
    }

    .son{
        /* 父级采用相对定位 子级采用绝对定位----子绝父相   */
        position: relative;
        width: 300px;
        height: 300px;
        background-color: skyblue;
    }

    .sun{
        position: absolute;
        bottom: 50px;
        right: 20px;
        width: 200px;
        height: 200px;
        background-color: green;
    }
    /* 绝对定位查找父级方式：就近找定位的父级，如果逐层找不到这样的父级，就以浏览器窗口定位 */
</style>
```

### 第二种方法

```html
 <style>
        .center{
            /* 绝对定位的盒子，不能使用margin auto居中 */
            position: absolute;
            /* 使整个盒子移动到浏览器中间偏右的位置 */
            left: 50%;
            top: 50%;
           transform:translate(-50%,-50%);
            width: 300px;
            height: 300px;
            background-color: pink;
        }
    </style>
```

## 固定定位

介绍：死心眼型定位，相对于浏览器进行定位移动

代码：position:fixed

特点：

1. 需要配合方位属性实现移动
2. 相对于浏览器可视区域进行移动
3. 在页面中不占位置---已经脱标

应用场景：

1. 让盒子固定在屏幕中的某个位置

```html
<style>
        .box{
            position: fixed;
            left: 0;
            top: 0;

            /* 
            1.脱标：不占位置
            2.改变位置参照浏览器窗口
            3.具备行内块特点
            
            */
            width: 200px;
            height: 200px;
            background-color: pink;
        }
    </style>
```



## 元素的层级关系

不同布局方式元素的层级关系

* 标准流<浮动<定位

不同定位之间的层级关系

* 相对 绝对 固定默认层级相同
* 此时html中写在下面的元素层级更高，会覆盖上面的元素

```html
    <style>
        div{
            width: 200px;
            height: 200px;
        }

        .one{
            position: absolute;
            left: 20px;
            z-index: 2;
            top: 50px;
            background-color:pink;
        } 

        .two{
             position: absolute;
             z-index: 1;
             left: 20px;
             top: 80px;
            background-color: aqua;
        }

        /* 默认情况下,定位的盒子 后来居上 
        z-inedx:整数：取值越大，显示顺序越靠上 ,z-index默认值是0  必须要配合定位属性才生效*/
    </style>
```

# 装饰

 ## 1.1 认识基线

**基线**：浏览器文字类型元素排版中存在用于对齐的基线

## 1..2垂直对齐方式

属性名：vertcal-align  

属性值：

默认 基线对齐：baseline

顶部对齐： top

中部对齐： middle 

底部对齐： bottom

```html
<style>
input{
height:50px;
vertcal-align:middle
}
    </style>
```

## 光标的类型

场景：设置鼠标光标在元素上时显示的样式

属性名：cursor

常见属性值：

default  默认

pointer  小手效果，提示用户可以点击

text 工字型，提示用户可以选择文字

move 十字光标，提示用户可以移动 

not-allowed  禁止，提示用户禁止点击

```html
<style>
      div {
        width: 200px;
        height: 200px;
        background-color: pink;
        /* 手型 */
        /* cursor: pointer;
        */

        /* 工字型，表示可以复制 */
        /* cursor:text; */

        /* 十字型光标，表示可以移动 */
        cursor: move;
      }
    </style>
```

##　表单轮廓线

 <style>
        input {
            取消表单轮廓
            outline: none;
        }
    </style>

　

## 防止拖拽文本域 resizi

` resize: none;`

## 边框圆角

场景：让盒子四个角变得圆润，增加页面细节，提升用户体验

属性名：border-radius

常见取值：数字+px、百分比

赋值规则：从左上角开始赋值，然后顺时针赋值，没有赋值的看对角

```html
 <style>
      .box {
        width: 200px;
        height: 200px;
        background-color: pink;

        /* 一个值表示四个角是相同的 */
        border-radius: 10px;

        /* 4值：左上 右上 右下 左下----从左上顺时针转一圈 */
        /* border-radius: 10px 20px 40px 80px; */

        /* border-radius: 10px 40px 80px;
        
        */

        /* border-radius: 10px 80px; */
      }
    </style>
```

### 边框圆角的常见应用

#### **画一个正圆**

1. 盒子必须是正方形
2. 设置边框圆角为盒子宽高的一半---border-radius:50%

```html
 <style>
      .one {
        width: 200px;
        height: 200px;
        background-color: pink;

        /* border-radius: 100px;
         */

        /* 取盒子尺寸一半 */
        border-radius: 50%;
      }
    </style>
```



#### 胶囊按钮

1. 要求盒子是长方形
2. 设置--border-radius:盒子高度的一半

```HTML
 <style>
      .one {
        width: 200px;
        height: 100px;
        background-color: pink;

        /* border-radius: 100px;
         */

        /* 取盒子高度一半 */
        border-radius: 50px;
      }
    </style>
```

## overflow 溢出部分显示效果

溢出部分：指盒子==内容部分==所超出盒子范围的区域

场景：控制内容溢出部分的显示效果，如：显示、隐藏、滚动条

属性名：overflow

常见属性值：

* visible:默认值 溢出部分可见
* hidden：溢出部分隐藏
* scroll：无论是否溢出，都显示滚动条
* auto：根据是否溢出，自动显示滚动条


```html
 <style>
    .box {
      width: 300px;
      height: 300px;
      background-color: pink;

      /* 溢出隐藏 */
      overflow: hidden;

      /* 滚动 */
      /* overflow: scroll;
       */

      /* 根据内容的多少，判断是否超出，超出就显示滚动条 */
      /* overflow: auto; */
    
    }
  </style>
```

#### 溢出文字显示省略号

1. 单行文本溢出显示省略号--必须满足三个条件

   * 1. 先强制一行内显示文本

   white-space:nowrap;

   * 2. 超出部分隐藏

   overflow:hidden;

   * 隐藏部分用省略号显示
   
    text-overflow: ellipsis;
   
   ```html
    <style>
           div {
               width: 150px;
               height: 80px;
               font-size: 12px;
               background-color: pink;
               margin: 100px auto;
               /*这个单词的意思是如果这个文字显示不开自动换行 */
               /* white-space: normal;
                */
               /* 如果显示不开必须一行内显示 */
               white-space: nowrap;
               /* 溢出部分隐藏 */
               overflow: hidden;
               /* 溢出部分用省略号代替 */
               text-overflow: ellipsis;
           }
       </style>
   
   ```

#### 多行文本溢出显示省略号

多行文本谥出显示省略号，有较大兼容性问题，适合于webKit浏览器或移动端（移动端大部分是webkitp内
核)

overflow:hidden;
text-overflow:ellipsis;
/*弹性伸缩盒子模型显示*/
display:-webkit-box;
/*限制在一个块元素显示的文本的行数*/
-webkit-line-clamp:2;
/*设置或检索伸缩盒对像的子元素的排列方式*/
-webkit-box-orient:vertical;



```html
 <style>
        div {
            width: 150px;
            height: 80px;
            font-size: 12px;
            background-color: pink;
            margin: 100px auto;
            overflow: hidden;
            text-overflow: ellipsis;
            /* 弹性伸缩盒子模型显示 */
            display: -webkit-box;
            /* 限制在一个块元素显示的文本行数 */
            -webkit-line-clamp: 5;
            /* 设置或检索伸缩盒对象的子元素的排列方式 */
            -webkit-box-orient: vertical;
        }
    </style>
```



## 元素本身的隐藏

场景：让元素本身在屏幕中不可见。如：鼠标:hover之后元素隐藏

常见属性：

1. visibility:hidden·
2. display:none

```html
<style>
      .one {
        width: 200px;
        height: 200px;
        background-color: pink;

        /* 占位隐藏 */
        /* visibility: hidden; */

        /* 不占位置的隐藏 */
        display: none;
      }

      .tow {
        width: 200px;
        height: 200px;
        background-color: rgb(62, 56, 56);
      }
    </style>
```



## 拓展 元素整体透明度

场景：让某元素整体（包括内容） 一起半透明

属性名：opacity

属性值：0~1之间的数字

**注意**

* opacity会让元素整体透明，包括里面的内容



# CSS 高级技巧

## 精灵图

### 1.1 为什么需要精灵图

 一个网页中往往会应用很多小的背景图像作为修饰，当网页中的图像过多时，服务器就会频繁地接收和发送

请求图片，造成服务器请求压力过大，这将大大降低页面的加载速度。
因此，为了有效地减少服务器接收和发送请求的次数，提高页面的加载速度，出现了CSS精灵技术（也称
CSS Sprites、CSS雪碧)。

 ### 1.2 精灵图的使用

**使用精灵图核心**

1. 精灵图技术主要针对于背景图片

使用。就是把多个小背景图片整合到一张大图中。

2. 这个大图片也被称为 sprites 精灵图 或者雪碧图
3. 移动背景图片位置，此时可以使用==bcakground-position==
4. 移动的距离就是这个目标图片的x和y轴。注意网页中的坐标有所不同
5. 因为一般情况下都是往上往左移动，所以数值是负值
6. 使用精灵图的时候需要精确测量，每个小背景图片的大小和位置 
7. ​    background-position: right 0; (显示最右边)

```html
<style>
      span {
        display: inline-block;
      }

      .p {
        width: 100px;
        height: 100px;
        /* background-color: pink; */
        background: url(../01-案例/images/floor1.jpg) no-repeat 0 0px;
      }
      .o {
        width: 100px;
        height: 100px;
        background: url(./images/floor1.jpg) no-repeat 0 -103px;
      }
    </style>
  </head>
  <body>
    <span class="p"></span>
    <span class="o"></span>
    <span class="w"></span>
    <span class="b"></span>
  </body>
```

## 字体图标

字体图标使用场景：主要用于显示网页中通用，常用的一些小图标

精灵图有许多优点，但是缺点也很明显

1. 图标文件还是比较大的
2. 图标本身放大和缩小会失真
3. 一旦图片制作完毕想要更换非常复杂



此时，有一种技术的出现很好的解决了以上的问题，就是字体图标==iconfont==

字体图标可以为前端工程师提供一种方便高效的图标使用方式，展示的是图标，本质属于字体

### 字体图标的优点

* 轻量级：一个图标字体要比一系列的图像都要小。一旦字体加载了，图标就会马上渲染出来，减少了服务器请求
* 灵活性：本质其实是文字，可以随意的改变颜色、产生的阴影、透明效果等
* 兼容性：几乎支持所有浏览器，请放心使用

注意：字体图标不能替代精灵技术，只是对工作中图标部分技术的提升和优化



### incomfont 类



## 背景图片大小

作用：设置背景图片的大小

语法：background-size:宽度 高度

取值:
数字+px

百分比

contain ：包含，将背景图片等比例缩放，直到不会超出盒子的最大

cover：覆盖，将背景图片等比例缩放，直到刚好填满整个盒子的空白



## 盒子阴影

 作用：给盒子添加阴影

属性名：box-shadow

取值：

1. h-shadow :必须 水平偏移量，允许负值
2. v-shadow:必须 垂直偏移量，允许负值
3. blur：可选，模糊度
4. spread：可选，阴影扩大
5. color：可选：阴影颜色
6. inset：可选，将阴影改为内部阴影

```html
  <style>
      .box {
        width: 200px;
        height: 200px;
        background-color: pink;

        /* 注意，如果是外阴影不能添加 */
        box-shadow: 5px 10px 20px 10px green inset;
      }
    </style>
```

## 过渡

作用：让元素的样式慢慢变化，常配合hover使用，增强网页交互体验

属性名：transition

常见取值：

|    参数    |                             取值                             |
| :--------: | :----------------------------------------------------------: |
| 过渡的属性 | ` a11`:所有能过渡的属性都过渡、` 其具体属性名如：width`：只有width有过渡 |
| 过渡的时长 |                         数字+s（秒）                         |

注意点：

1. 过渡需要：默认状态和hover状态样式不同，才能有过渡效果
2.transition属性给需要过渡的元素本身加
3.
transition,属性设置在不同状态中，效果不同的
①
给默认状态设置，鼠标移入移出都有过渡效果
②
给hover状态设置，鼠标移入有过渡效果，移出没有过渡效果

```html
 <style>
      /* 过渡配合hover使用 */
      .box {
        width: 200px;
        height: 200px;
        background-color: pink;

        /* 宽度200，鼠标悬停的时候宽度600,花费1秒钟 */
        /* transition: width 1s, background-color 1s; */

        /* 如果变换的属性多，直接写all表示所有 */
        transition: all 1s;
      }

      .box:hover {
        width: 600px;
        background-color: red;
      }
    </style>
```



## 平面转换



目标：使用transform属性实现元素的位移、旋转、缩放等效果



* **平面转换**

1. 改变盒子在平面内的形态（位移、旋转、缩放）
2. 2D转换

* **平面转换属性**
* transform

### 位移

语法
transform:translate(水平移动距离，垂直移动距离)；

* 取值（正负均可）  

  * 像素单位数值 

  * 百分比（参照物为盒子自身尺寸）

    ==注意：轴正向为右，Y轴正向为下==

    * 技巧
       translate()如果只给出一个值，表示x轴方向移动距离
        单独设置某个方向的移动距离：translateX（）& translateY（）

```html
  <style>
      .father {
        width: 500px;
        height: 300px;
        margin: 100px auto;
        border: 1px solid #000;
      }

      .son {
        width: 200px;
        height: 100px;
        background-color: pink;
        transition: all 0.75s;
      }

      /* 鼠标移入到父盒子，son改变位置 */
      .father:hover .son {
        /* transform: translate(100px, 50px) */

        /* 百分比：盒子自身尺寸的百分比 */
        /* transform: translate(100%, 50%);
         */
        /*  transform: translate(-100%, 50%);*/
          
             transform: translateX(100px);
      }
    </style>
```



### 旋转

语法：

transform:rotate(角度)

注意：角度单位是deg

取值可正负

```html
 <style>
      img {
        width: 250px;
        /* 必须要有过渡属性 */
        transition: all 2s;
      }

      img:hover {
        /* 顺 */
        transform: rotate(360deg);

        /* 逆 */
        /* transform: rotate(-360deg); */
      }
    </style>
```

### 转换原点

**目标**：使用transform：origin 可以改变转换原点

* 语法

  * 默认原点是盒子中心

  * transform：origin ：原点水平位置     原点垂直位置

* 取值

* * 方位名词 （常用）
  * 像素单位数值
  * 百分比

```html
<style>
      img {
        width: 250px;
        border: 1px solid #000;
        transition: all 60s;
        transform-origin: left bottom;
      }

      img:hover {
        transform: rotate(360deg);
      }
    </style>
```

###　多重转换

```html
 <style>
      .box {
        width: 800px;
        height: 200px;
        border: 1px solid #000;
      }

      img {
        width: 200px;
        transition: all 8s;
      }

      .box:hover img {
        /* 边走边转  */
        transform: translate(600px) rotate(720deg);
        /* 因为旋转可以改变坐标轴向 */
        /* transform: rotate(720deg) translate(600px); */

        /* 层叠性 */
        /* transform: rotate(720deg);
        这一段生效
        transform: translate(600px);
      } */
    </style>
```

### 缩放

**目标**：使用scale改变元素的尺寸

一般情况下，只为scale设置一个值，表示x轴和y轴缩

* ==transform:scale(缩放倍数);==

```html
 <style>
      .box {
        width: 300px;
        height: 210px;
        margin: 100px auto;
        background-color: pink;
        overflow: hidden;
      }

      .box img {
        width: 100%;
        transition: all 0.5s;
      }

      .box:hover img {
        /* width: 150%; */

        transform: scale(1.1);
      }
    </style>
```



##　渐变

**目标：使用packground-image属性实现渐变背景效果**

* 渐变是多个颜色逐渐变化的视觉效果
* 一般用于设置盒子的背景

```html
<style>
        div {
            width: 200px;
            height: 200px;
            /* background-image: linear-gradient(red,
                    green,
                    pink);
        } */

            background-image: linear-gradient(transparent,
                    rgba(0, 0, 0, .3)
                    );
    </style>
```



## 3.2 SEO三大标签

SEO(Search Engine Optimization):搜索引擎优化
作用让网站在搜索引擎上的排名靠前
提升SEO的常见方法：
1.竞价排名
2.
将网页制作成html后缀
3.
标签语义化（在合适的地方使用合适的标签）

1. title：网页标题标签
2. description:网页描述标签
3. keywords:网页关键词标签



##ｉｃｏ图标设置

场景：显示在标签页标题左侧的小图标，习惯使用．ｉｃｏ图标

` <link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />`

# 项目结构搭建

## 文件和目录准备

1. 新建项目文件夹xtx-pc-client,在VScode中打开
   在实际开发中，项目文件夹不建议使用中文
   所有项目相关文件都保存在tx-pc-client目录中
2. 复制favicon.ico到tx-pc-client目录
   ·一般习惯将co图标放在项目根目录
3. 复制images和uploads目录到xtx-pc-client目录中
   images：存放网站**固定使用**的图片素材，如：logo、样式修饰图片.等
   uploads:存放网站**非固定使用**的图片素材，如：商品图片、宣传图片.等
4. 新建index..html在根目录
5. 新建css文件夹保存网站的样式，并新建以下CSS文件：
   base.css:基础公共样式
   common.css:该网站中多个网页相同模块的重复样式，如：头部、底部
   index.css:首页样式



# HTML5新特性

## 新增 语义化标签

 `  <header> `:头部标签

` <nav>`：导航标签

` <article>`:内容标签

` <section> `:定义文档某个区域

` <aside>` :侧边栏标签

` <footer> ` :尾部标签



# 空间转换

   目标：使用tranform属性实现元素在空间内的位移，旋转，缩放等效果

* 空间：是从坐标轴角度定于的。==x，y和z==三条坐标轴构成了一个立体空间，==z轴位置与视线方向相同。==
* 空间转换也叫==3D转换==
* ==属性：transform==



* 语法
  *  transform: translate3d(x,y,z);
  *  transform: translateX(值);
  * transform: translateY值);
  * transform: translateZ(值);
* 取值（正负即可）
* 像素单位数值
* 百分比

## 透视

* 思考：生活中，同一个物体，观察距离不同，视觉上有什么区别？
  * 近大远小，近距离清楚远距离模糊
* 思考：默认情况下，为什么无法观察到z轴位移效果？
  * 答：Z轴是视线方向，移动效果也该是距离的远或近，电脑屏幕是平面，默认无法观察到远近效果

* 属性（==添加给父级==）
  * perspective：值
  * 取值：像素单位数值，数值建议一般在800-1200
  * 透视距离也称为视距，所谓的视距就是==人的眼睛到电脑屏幕的距离

## 空间旋转

目标：使用rotate实现元素==空间旋转==效果



* 语法
  * transform:rotateZ(值)
  * transform: rotateX(值);
  * transform: rotateY(值);
* 取值单位为deg



* 拓展
  * rotate3d(x,y,z,角度度数):用来设置自定义旋转轴的位置以及旋转的角度
  * x,y,z取值为0-1之间的数字

## 立体呈现

* 实现方法
  * 添加==transform-style:perseve-3d;==
  * 使元素处于真正的==3d空间==

* 呈现立体图形步骤
  1. 盒子==父元素添加transform-style:perseve-3d==
  2. 按需求设置子盒子的==位置（位移或者旋转）==

## 空间缩放

目标：使用==scale==实现==空间缩放效果==



* 语法
  * transform:scaleX(倍数);
  * transform:scaleY(倍数);
  * transform:scaleZ(倍数);
  * transform:scale3d(x,y,z);

# 动画

目标：使用==animation==添加==动画==效果

* 思考：过渡可以实现什么效果？
  * 答：实现2个状态间的变化过程

* 动画效果：实现==多个状态==间的变化过程，动画==过程可控==（重复播放，最终画面，是否暂停）

  

  **什么是动画**

* 动画的本质是快速切换大量图片是在人脑中形成具有==连续性的画面
* 构成动画的最小单元：==帧或动画帧==

------

**实现步骤**

1. 定义动画

```css
@keyfrmes 动画名称{
    from{}
    to{}
}
```

or

```css
@keyfrmes 动画名称{
    0%{}
    10%{}
    15%{}
    100%{}
}
```

2. 使用动画

`animation: 动画名称 动画花费时长`

**代码参考**

```css
 .box {
        width: 200px;
        height: 100px;
        background-color: pink;

        /* 使用动画 */
        animation: change 1s;
      }

      /* 一. 定义动画：从200变大到600 */
      /* @keyframes change {
        from {
          width: 200px;
        }
        to {
          width: 600px;
        }
      } */

      /* 二. 定义动画：200 到 500*300 到 800*500 */
      /* 百分比指的是动画总时长的占比 */0
      @keyframes change {
        0% {
          width: 200px;
        }
        50% {
          width: 500px;
          height: 300px;
        }
        100% {
          width: 800px;
          height: 500px;
        }
      }
```

------

## 动画属性

目标：使用animation相关属性控制动画执行过程

`animation: 动画名称 动画时长 速度曲线 延迟时间 重复次数 动画方向 执行完毕时状态；`

**注意**

* 动画名称和动画时长必须赋值
* 取值不份分先后顺序
* 如果有俩个时间值，第一个时间表示动画时长，第二个时间表示延迟时间

1. 速度曲线取值有：linear（匀速）、steps(60)（分60段执行）
2. 重复次数取值有：数字、infinite（无线循环）
3. 动画方向取值有：alternate
4. 执行完毕取值有：forwards（动画停留在结束转台）、backwards（动画停留开始状态 默认值）

------

|             属性             |        作用        |                       取值                       |
| :--------------------------: | :----------------: | :----------------------------------------------: |
|      animation-name: ;       |      动画名称      |                                                  |
|    animation-duration: ;     |      动画时长      |                                                  |
|      animation-delay: ;      |      延迟时间      |                                                  |
|    animation-fill-mode: ;    | 动画执行完毕时状态 | forwards：最后一帧状态     backwards：第一帧状态 |
| animation-timing-function: ; |      速度曲线      |             steps（数字）：逐帧动画              |
| animation-iteration-count: ; |      重复次数      |                infinite为无限循环                |
|    animation-direction: ;    |    动画执行方向    |                 alternate为反向                  |
|   animation-play-state: ;    |      暂停动画      |           peused为暂停，通常配合hover            |

## 逐帧动画

目标：使用==steps实现逐帧动画==

| 属性                      | 作用     |         取值         |
| ------------------------- | -------- | :------------------: |
| animation-timing-function | 速度曲线 | steps(数字):逐帧动画 |

* 逐帧动画：帧动画。开发中，一般配合==精灵图==实现动画效果。
* animation-timing-function：steps(N);
  * 将动画过程等分成N份
* 精灵动画制作步骤
  * ==准备显示区域==
    * 设置盒子尺寸是一张小图的尺寸，背景图为当前精灵图
  * ==定义动画==
    * 改变背景图的位置（移动的距离就是==精灵图的宽度==）
  * ==使用动画==
    * 添加速度曲线==steps(N)==，N与精灵图上小图==个数相同==
    * 添加无限重复效果

## 多组动画

目标：能够使用animation属性给一个元素 添加多个动画效果

```css
animation:
动画1,
动画2,
动画N

```

# 移动端特点

## 屏幕尺寸

目标：了解屏幕尺寸的概念

* 屏幕尺寸
  * 指的是屏幕==对角线==的长度，一般用==英寸==表示

## 分辨率

目标：了解移动端主流设备分辨率

* pc分辨率
  * 1920*1080
  * 1366*768
* 缩放（150%）
  * （1920/150%）*（1080/150%）
* ==总结==
  * ==硬件分辨率（出厂设置）==
  * ==缩放调节的分辨率（软件设置）==
* 分辨率分类
  * ==物理分辨率==是生产屏幕时就固定的，他是不可被改变的
  * ==逻辑分辨率==是由软件（驱动）决定的

## 视口

目标：使用meta标签设置视口宽度，制作适配==不同设备宽度的网页==

* 思考：默认情况下，网页的宽度和逻辑分辨率相同？
  * 不同，默认网页宽度980px



* 目标：==网页宽度和设备宽度（分辨率）相同==
* 解决办法：添加视口标签。

## 二倍图

目标：能够使用==像素大厨==软件测量二倍中==元素的尺寸==

 # 百分比布局

目标：能够使用百分比布局开发网页

* 百分比布局，也叫流式布局
* 效果：宽度自适应，高度固定

# Flex布局

* Flex布局/弹性布局：
  * 是一种==浏览器提倡==的==布局模型==、
  * 布局网页更简单、灵活
  * 避免==浮动脱标==的问题
* 作用

  * 基于Flex精确灵活控制块级盒子的布局方式，==避免浮动布局中脱离文档流现
  * 
  * 象发生。
  * Flex布局非常适合结构化布局
* 设置方式

  * 父元素添加==display:flex==，子元素可以自动挤压或拉伸

* 组成部分
  * 弹性容器
  * 弹性盒子
  * ==主轴==
  * ==侧轴/交叉轴==

## 主轴对齐方式

目标：使用justify-content调节元素在主轴的对齐方式

* 思考：网页中，盒子之间有距离嘛？
* 答：有
  * 在Flex布局模型中，调节==主轴或侧轴的对齐方式来设置盒子之间的间距。
* 修改主轴对齐方式属性：==justify-content: ;==

|    属性值     |                         作用                         |
| :-----------: | :--------------------------------------------------: |
|  flex-start   |               默认值，起点开始依次排列               |
|   flex-end    |                   终点开始依次排列                   |
|    center     |                    沿主轴居中排列                    |
| space-around  |  弹性盒子沿主轴均匀排列，空白间距均分在弹性盒子两侧  |
| space-between |   弹性盒子沿主轴均匀排列，空白间距分在相邻盒子之间   |
| space-evenly  | 弹性盒子沿主轴均匀排列，弹性盒子与容器之间的间距相等 |

```css
<style>
      * {
        margin: 0;
        padding: 0;
      }

      .box {
        display: flex;
        /* 居中 */
        justify-content: center;
        /* 间距在弹性盒子（子级）之间 */
        justify-content: space-between;
        /* 所有地方的间距都相等 */
        justify-content: space-evenly;
        /* 间距加在子级的俩侧 */
        /* 视觉效果：子级之间的距离是父级俩头距离的二倍 */
        justify-content: space-around;
        height: 200px;
        margin: auto;
        border: 1px solid #000;
      }

      .box div {
        width: 100px;
        height: 100px;
        background-color: pink;
      }
    </style>
```

## 侧轴对齐方式

目标：使用==align-items==调节元素在==侧轴的对齐方式==

* 修改侧轴的对齐方式属性：
  * ==align-items（添加到弹性容器）==
  * align-seif：控制某个弹性盒子在侧轴的对齐方式（==添加到弹性盒子==）

|   属性值   |                    作用                    |
| :--------: | :----------------------------------------: |
| felx-start |         默认值，起点开始，依次排列         |
|  flex-end  |              终点开始依次排列              |
|   center   |               沿侧轴居中排列               |
|  stretch   | 默认值，弹性盒子沿着侧轴线被拉伸至铺满容器 |

```css
    <style>
      * {
        margin: 0;
        padding: 0;
      }

      .box {
        display: flex;
        /* 居中 */
        align-items: center;
        /* 拉伸，默认值（现有状态，测试的时候去掉子级高度） */
        align-items: stretch;
        height: 300px;
        margin: auto;
        border: 1px solid #000;
      }

      .box div {
        width: 100px;
        height: 100px;
        background-color: pink;
      }

      /* 单独设置某个弹性盒子的侧轴对齐方式 */
      .box div:nth-child(2){
        align-self: center;
      }
    </style>
```

## 伸缩比

目标：使用==flex==属性修改弹性盒子==伸缩比==

* 属性
  * flex：值;
* 取值分类
  * 数值（整数）

==注意：只占用父盒子剩余尺寸==

##　改变元素排列方向

目标：使用flex-direction 改变元素排列方向

* 思考：flex布局模型中，弹性盒子默认沿着那个方向排列?
* 答：==水平方向。==



* 主轴==默认是水平方向==，侧轴默认是垂直方向
* 修改主轴方向属性：==flex-direction==

| 属性值         | 作用               |
| -------------- | ------------------ |
| row            | 行，水平（默认值） |
| column         | 列，垂直           |
| row-reverse    | 行，从右向左       |
| column-reverse | 列，从下向上       |

##　弹性盒子换行

目标：使用==flex-wrap==实现弹性盒子==多行==排列效果

* 思考：默认情况下，多个弹性盒子如何显示？

* 弹性盒子换行显示：==flex-wrap:wrap;==

* 调整行的对齐方式：==align-content==

  * 取值与    justify-content: ;基本相同

  ```css
   display: flex;
          /* 默认值，不换行 */
          /* flex-wrap: nowrap; */
          /* 弹性盒子换行 */
          flex-wrap: wrap;
  ```

  

# 移动适配

* rem :目前多数企业在用的解决方案
* vw/ vh：未来的解决方案

## rem

目标：能够使用==rem单位==设置网页元素==尺寸==

* 网页效果
  * 屏幕==宽度不同==，网页元素==尺寸不同==（等比缩放）
* px单位或百分比布局可以实现吗？
  * px单位是绝对单位
  * 百分比布局特点是宽度自适应，高度固定
* 适配方案
  * rem
  * vw / vh



* rem单位
  * ==相对==单位
  * ren单位是相对于==HTML标签字号==计算结果
  * ==1rem = 1HTML字号大小==

* 思考：
  * 1. 手机屏幕大小不同，分辨率不同，如何设置不同的HTML标签字号？
    1. 设备宽度不同，HTML标签字号设置多少合适？
* 目前rem布局方案中，将网页等分成10份，HTML标签的字号为==视口宽度==的1/10

### 媒体查询

 目标：能够使用==媒体查询==设置==差异化==CSS样式

* ==媒体查询==能够==检测视口的宽度==，然后编写差异化CSS样式
* 当某个条件成立时，执行对应的CSS样式



* 写法

  * ```css
    @media(媒体特性){
        选择器{
            CSS属性
        }
    }
    ```

```css
@media(width:320px){
    html{
        font-size:32px;
    }
}
```

### rem适配原理

* 思考：
  * 工作中，书写代码的尺寸要参照设计稿尺寸，设计稿中是px还是rem？
  * 如何确定rem的数值？
* 目标：计算68px是多少个rem？（假定设计稿适配375）
* N * 375 = 68 ——N = 68 / 37.5



* rem单位尺寸
  1. 确定设计稿==对应==的设备的HTML标签字号
     * 查看==设计稿宽度==--确定参考==设备宽度==--确定==基准根字号==（1/10视口宽度）
  2. rem单位尺寸
     * rem单位尺寸 = ==px单位数值 / 基准根字号==



## vw / vh

目标：能够使用==vw==单位设置网页元素尺寸

* 相对单位
* 相对==视口的尺寸==计算结果
* vw：viewport width;
  * 1vw = ==1/100==视口宽度
* vh：viewport height;
  * 1vh = ==1/100==视口宽度



### vw适配原理

* vw单位尺寸
  1. 确定设计稿对应的vw尺寸（1/100视口宽度）
     * 查看==设计稿宽度==--确定参考==设备的宽度==--确定==vw尺寸==
  2. vw单位的尺寸 = px单位数值 / （1/100视口宽度）

## flexble

目标：使用flexble.js配合rem实现在==不同宽度==的设备中，网页元素尺寸==等比缩放==效果

* flexble.js是手淘开发出的一个用来适配移动端的==js框架==
* 核心原理就是根据==不同视口宽度==给网页中html节点设置不同的font-size

# less

* 思考：在px单位转换到rem单位过程中，哪项工作是最麻烦的？
* 答：除法运算 。 ==CSS不支持计算写法==
* ==解决方案：可以通过less实现==

目标：使用==less==语句快速编译==生成CSS样式==

* less是一个==CSS预处理器==，Less文件后缀是.less
* 扩充了CSS语言，使CSS具备一定的逻辑性、计算能力
* 注意：浏览器不识别less代码，目前阶段，网页要引入对应的CSS文件



**注释：**

* 单行注释
  * 语法：//注释内容
  * 快捷键：ctrl+/
* 块注释
  * 语法：/ * 注释内容 * /
  * 快捷键：shift+alt+a

**运算：**

* 加减乘直接书写计算表达式
* 除法需要添加小括号或.



**嵌套：**

* 作用：快速生成后代选择器

* 语法：

* ```css
  .父级选择器{
      //父级样式
      .子级选择器{
          //子级样式
      }
  }
  ```

* ```less
  .father {
      color:red;
      .son{
          width:100px;
  	}
  }
  ```

* 注意：&==不==生成后代选择器，表示当前选择器，通常配合==伪类或者伪元素==使用



**变量：**

* 网页中：文字文字颜色基本都是统一的，如果网站改版，变换文字颜色，如何修改代码？

  * 方法一：逐一修改属性值（太麻烦）
  * 方法二：
  * 把颜色提前存储到一个容器，设置属性值为这个容器名

* 变量：存储数据，方便使用和修改。

* **语法：**

  * 定义变量：==@变量名:值;==
  * 使用变量：==CSS属性:@变量名;==

* ```less
  // 1. 定义. 2.使用
  @colora:green;
  
  .box {
      color: @colora;
  }
  
  .father {
      background-color: @colora;
  }
  
  .aa {
      color: @colora;
  }
  ```

* ```css
  .box {
    color: green;
  }
  .father {
    background-color: green;
  }
  .aa {
    color: green;
  }
  
  ```



**导入：**

* 使用less语法导入其他less文件

* 导入：@impot”文件路径”;

* ```less
  @import './01-体验less.less';
  //如果引入的时less文件，可以不用.less后缀
  @import './02-注释';
  ```



**导出**

* 方法一：
  * 配置EasyLess插件，实现所有Less有相同的导出路径 

* 禁止导出：
  * 在less文件第一行添加：//out:false



# 响应式布局

## 媒体查询

目标：能够根据设备宽度的变化，设置差异化样式

* 开发常用写法
  * 媒体特性常用写法
    * max-width(从小到大写)
    * min-width（从大到小写）

```css
@media(媒体特性){
    选择器{
        样式
    }
}
```

* 完整写法 （了解）

  `@media 关键词 媒体类型 and (媒体特性) {css代码}`

* 媒体是用来区分设备类型的，如屏幕设备，打印设备等，其中手机、电脑、平板都属于屏幕设备。

|  类型名称  |   值   |          描述           |
| :--------: | :----: | :---------------------: |
|    屏幕    | screen |      带屏幕的设备       |
|  打印预览  | print  |      打印预览模式       |
|   阅读器   | speech |      屏幕阅读模式       |
| 不区分类型 |  all   | 默认值，包括以上3种情形 |

* 媒体特性主要用来描述媒体类型的具体特征，如当前屏幕的宽高、分辨率、横屏或竖屏等。

|    特性名称    |         属性          |              值               |
| :------------: | :-------------------: | :---------------------------: |
|  视口的宽和高  |     width、height     |             数值              |
| 视口最大宽或高 | max-width、max-height |             数值              |
| 视口最小宽或高 | min-width、min-height |             数值              |
|    屏幕方向    |      orientation      | portrait:竖屏、landscape:横屏 |

* 外链式CSS引入

`<link rel="stylesheet" media="逻辑符 媒体类型 and (媒体特性)" href="xx.css">`

* 实际开发写法

`<link rel="stylesheet" href="./one.css" media="(min-width: 992px)">`



## BootStrap

* BootStrap 是由Twitter公司开发维护==前端UI框架==，它提供了大量编写好的CSS样式，允许开发者结合一定HTML结构及JavaScript，快速编写功能完善的网页及常见交互效果

* 使用步骤
* 1. ==引入==：Bootstrap提供的CSS代码

`<link rel="stylesheet" href="./bootstrap-3.4.1-dist/css/bootstrap.min.css">`

2. 调用类：使用bootstrap提供的样式
   * container：响应式布局版心类

### BootStrap栅格系统

* 栅格系统是指将整个网页的宽度分成若干等份
* BootStrap默认将网页分成12份

|          | 超小屏幕 |  小屏幕  | 中等屏幕 |  大屏幕  |
| :------: | :------: | :------: | :------: | :------: |
| 响应断点 |  <768px  | >=768px  | >=992px  | >=1200px |
|   别名   |    xs    |    sm    |    md    |    lg    |
| 容器宽度 |   100%   |  750px   |  970px   |  1170px  |
|  类前缀  | col-xs-* | col-sm-* | col-md-* | col-lg-* |
|   列数   |    12    |    12    |    12    |    12    |
|  列间隙  |   30px   |   30px   |   30px   |   30px   |

* ==.container==是BootStrap中专门提供的类名，所有应用该类名的盒子，默认已被指定宽度居中。
* ==.container-fluid==也是BootStrap中专门提供的类名，所有应用该类名的盒子，宽度均为100%
* 分别使用.row类名和.col类名定义栅格布局的行和列。

**注意**

==1. container类自带间距15px==

==2.row类自带间距-15px==

### Glyphicons字体图标

* html页面引入Bootstrap样式文件
* 空标签调用对应类名
  * glyphicon
  * 图标类

###　插件

目标：使用BootStrap==插件==实现常见的==交互效果==



* 插件的使用步骤
  * 引入BootStrap样式
  * 引入js文件：jQuer.js+BootStrap.min.js
  * 复制HTML结构，并适当调整结构内容



