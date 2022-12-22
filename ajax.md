# 原生Ajax

## Ajax是什么?

* Ajax就`是`让浏览器跟服务器交互的一套`API`。 它的作用就是可以让浏览器和服务器进行交互。
  * 说人话： ajax 是一种 用于`向服务器请求数据`的 技术
* MDN官网传送门:https://developer.mozilla.org/zh-CN/docs/Web/Guide/AJAX
* Ajax 即`“**Asynchronous Javascript And XML**”`（异步 JavaScript 和 XML），是指一种创建交互式网页应用的网页开发技术。                
* **说人话**：ajax就是一套可以让网站跟服务器交互的一种技术，能在我们需要时，不用再刷新网页就能去服务器要一些数据回来
* 例：http://www.smzdm.com 里只要网站往下滚动，就能不用刷新页面跟服务器要数据

## Ajax原生语法

* 1.创建`XMLHttpRequest`对象（俗称小黄人）
  * `let xhr = new XMLHttpRequest();`
* 2.设置请求
  * `xhr.open('get', 'https://autumnfish.cn/api/joke');`
* 3.发送请求
  * `xhr.send();`
* 4.注册回调函数
  * * 这个函数不是立即执行的，而是等服务器把数据响应返回才会执行（PS：什么时候执行取决于你的网速快慢）
    * `xhr.onload = function () {console.log(xhr.responseText);}`

```javascript
  //1.创建小黄人对象XMLHTTPRequest
        let xhr = new XMLHttpRequest();
        //2.设置请求
        xhr.open('get', 'https://autumnfish.cn/api/joke');
        //3.发送请求
        xhr.send();
        //4.注册回调函数
        /* 这个函数不是立即执行的，而是等服务器把数据响应返回才会执行（PS：什么时候执行取决于你的网速快慢） */
        xhr.onload = function () {
            console.log(xhr.responseText);
            document.body.innerText = xhr.responseText;
        };
```

---

### 请求方式

> get和post请求方式有所不同
>
> 1. 传参方式不同
>    * get请求:直接在`url`后面拼接参数
>      *  参数在`url`安全性不高
>    * post请求:
>      * 需要设置一个请求头(固定语法)
>        * `xhr.setRequestHeader('Content-type','application/x-www-form-urlencoded')`
>      * 使用`xhr`的`send()`方法传参 `xhr.send('参数名=参数值')`

#### get请求

```javascript
// 1.实例化ajax对象
      let xhr = new XMLHttpRequest()
      // 2.设置请求方法和地址
      // get请求的数据直接添加在url的后面 格式是 url?key=value
      xhr.open("get", "https://autumnfish.cn/api/joke/list?num=10")
      // 3.发送请求
      xhr.send()
      // 4.注册回调函数
      xhr.onload = function() {
        console.log(xhr.responseText)
      }
```

---

#### post请求

```javascript
 //(1).实例化ajax对象
      let xhr = new XMLHttpRequest()
      //(2).设置请求方法和地址
      xhr.open("post", "https://autumnfish.cn/api/user/register")
      //(3).设置请求头（post请求才需要设置）
      xhr.setRequestHeader("Content-type", "application/x-www-form-urlencoded")
      //(4).发送请求 ： 参数格式  'key=value'
      xhr.send("username=admin")
      //(5).注册回调函数
      xhr.onload = function() {
        console.log(xhr.responseText)
      }
```

#### 其他请求方法

* `实际开发中，前端无权决定请求方法，只需要根据后台接口文档来就可以了`

| 请求方式 | 描述                 | 特点            |
| -------- | -------------------- | --------------- |
| post     | 一般用于新增数据     | 请求体传参      |
| get      | 一般用于查询数据     | 请求行(url)传参 |
| delete   | 一般用于删除数据     | 请求体传参      |
| put      | 一般用于更新全部数据 | 请求体传参      |
| patch    | 一般用于更新局部数据 | 请求体传参      |

---

## ajax其他知识点

### ajax的组成部分

* Ajax(阿贾克斯)：全称  `Asynchronous Javascript And XML(异步的js与xml)`
  * 说人话： 用js发送异步的网络请求
  * A :  Asynchronous  异步
    * 同步 ： 指的是代码按照从上往下顺序执行
    * 异步 ： 代码不会立即执行,而是要等一会儿执行
      * 目前我们学过的ECMAScript只有两个语法是异步的：  定时器 与  ajax
      * DOM事件也是属于异步的，但是这个是属于DOM的执行机制。所以一般在讨论js同步和异步的时候，主要以js为主，DOM一般不讨论。
  * J：Javascript
  * A ：And
  * X :  XML 与 XMLHttpRequest
    * XML ： 解决跨平台数据传输。
      *   在JSON没有出来以前, 网络传输主要以XML格式数据为主。  后来JSON问世，逐渐取代XML。 但是由于ajax技术出来的比json早，因此xml这个称呼一直保留至今

### 获取 json 格式的天气

* 请求地址：

  http://wthrcdn.etouch.cn/weather_mini

  * 示例：http://wthrcdn.etouch.cn/weather_mini?city=深圳

* 请求方法：get

* 请求参数：city

| 参数名 | 参数说明     | 备注               |
| ------ | ------------ | ------------------ |
| City   | 查询的城市名 | 不能为空，不能写错 |

* 响应内容：json

```javascript
{
  "data": {
    "yesterday": {
      "date": "15日星期三",
      "high": "高温 31℃",
      "fx": "无持续风向",
      "low": "低温 26℃",
      "fl": "<![CDATA[<3级]]>",
      "type": "多云"
    },
    "city": "深圳",
    "forecast": [
      {
        "date": "16日星期四",
        "high": "高温 32℃",
        "fengli": "<![CDATA[<3级]]>",
        "low": "低温 27℃",
        "fengxiang": "无持续风向",
        "type": "阵雨"
      },
      {
        "date": "17日星期五",
        "high": "高温 32℃",
        "fengli": "<![CDATA[<3级]]>",
        "low": "低温 27℃",
        "fengxiang": "无持续风向",
        "type": "雷阵雨"
      },
      {
        "date": "18日星期六",
        "high": "高温 32℃",
        "fengli": "<![CDATA[<3级]]>",
        "low": "低温 27℃",
        "fengxiang": "无持续风向",
        "type": "雷阵雨"
      },
      {
        "date": "19日星期天",
        "high": "高温 32℃",
        "fengli": "<![CDATA[<3级]]>",
        "low": "低温 25℃",
        "fengxiang": "无持续风向",
        "type": "雷阵雨"
      },
      {
        "date": "20日星期一",
        "high": "高温 29℃",
        "fengli": "<![CDATA[<3级]]>",
        "low": "低温 24℃",
        "fengxiang": "无持续风向",
        "type": "阵雨"
      }
    ],
    "ganmao": "各项气象条件适宜，发生感冒机率较低。但请避免长期处于空调房间中，以防感冒。",
    "wendu": "30"
  },
  "status": 1000,
  "desc": "OK"
}
```

### 获取 xml 格式菜单

* 请求地址：https://autumnfish.cn/api/food.xml
* 请求方法：get
* 请求参数：无
* 响应内容：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<breakfast_menu>
	<food>
		<name>Belgian Waffles</name>
		<price>$5.95</price>
		<description>Two of our famous Belgian Waffles with plenty of real maple syrup</description>
		<calories>650</calories>
	</food>
	<food>
		<name>Strawberry Belgian Waffles</name>
		<price>$7.95</price>
		<description>Light Belgian waffles covered with strawberries and whipped cream</description>
		<calories>900</calories>
	</food>
	<food>
		<name>Berry-Berry Belgian Waffles</name>
		<price>$8.95</price>
		<description>Light Belgian waffles covered with an assortment of fresh berries and whipped cream</description>
		<calories>900</calories>
	</food>
	<food>
		<name>French Toast</name>
		<price>$4.50</price>
		<description>Thick slices made from our homemade sourdough bread</description>
		<calories>600</calories>
	</food>
	<food>
		<name>Homestyle Breakfast</name>
		<price>$6.95</price>
		<description>Two eggs, bacon or sausage, toast, and our ever-popular hash browns</description>
		<calories>950</calories>
	</food>
</breakfast_menu>
```

### 1.3-get请求与post请求区别(掌握)



* 1.传参方式不同
  * get在url后面拼接(请求行)
  * post在请求体传参
* 2.大小限制不同
  * get有大小限制，不同浏览器大小限制不同。 一般2-5 MB
  * post没有大小限制
* 3.安全性不同
  * get参数直接暴露在url，不安全(一般查询类数据都是get)
  * post参数在请求体中，更加安全（一般登录注册必须是post）
* 4.传输速度不同
  * get传输速度快
  * post传输速度慢




# axios框架

* axios(阿克休斯) 官网 : http://www.axios-js.com/
* 1. axios是什么 ：  一个js框架，用于发送ajax请求（底层使用XMLHttpRequest）

## axios的使用

* 官网文档：http://www.axios-js.com/zh-cn/docs/

```javascript
 get() :// 写url和请求参数
        then(res=>{}) : //成功回调， 相当于以前jq的success
        catch(err=>{})://失败回调，   一般可以省略不写
        then(()=>{})://完成回调，  表示请求完成，无论成功失败都会执行。一般可以省略不写
```

```javascript
axios.get("https://autumnfish.cn/api/joke/list?num=10").then(res => {
            //请求成功
            console.log(res)
          }).catch(err => {
            //请求失败 : (1)网址写错了  (2)网络出问题了
            console.log(err)
          }).then(() => {
            //请求完成
            console.log("本次请求完成")
          })
      }
```

---

### get请求

```javascript
axios.get("https://autumnfish.cn/api/joke/list", {
          params: {
              num: 10
            }
          })
          .then(res => {
            //请求成功
            console.log(res)
          })
      }
```

---

### post请求

```javascript
axios.post("http://www.liulongbin.top:3009/api/login", {
            username: "admin",
            password: "123456"
          })
          .then(res => {
            //请求成功
            console.log(res)
          })
          .catch(err => {
            //请求失败
            console.log(err)
          })
      }
```

---

## ajax推荐的请求方式

### 基本语法

```javascript
 axios({
           url:'请求路径',
            method:'请求方式',
             data:{ post请求参数 },
            params:{ get请求参数 }
      }).then(res=>{
                    //成功回调
                    //console.log(res)
                });
```

##### get请求

```javascript
 axios({         
     url:`https://autumnfish.cn/api/joke/list`,
     method: "get",
     params:{
              num:10
            }
        }).then(res => {
          console.log(res)
        })
```

---

##### post请求

```javascript
 axios({
          url: "http://www.liulongbin.top:3009/api/login",
          method: "post",
          data: {
            username: "admin",
            password: "123456"
          }
        }).then(res => {
          console.log(res)
        })
```

---

##  axios拦截器

![image-20221219130114834](D:\网页制作\学习笔记\assets\image-20221219130114834.png)

axios拦截器工作流程
     1. axios 发起请求
          2. 执行 请求拦截器 : 添加ajax发送请求之前的操作
          3. 服务器 接收、处理、响应 请求
               4. 执行 响应拦截器 ： 添加服务器响应之后的操作
               4. axios 接收响应(执行then方法)

```javascript
// 添加请求拦截器
axios.interceptors.request.use(function (config) {
    // 在发送请求之前做些什么
    return config;
  }, function (error) {
    // 对请求错误做些什么
    return Promise.reject(error);
  });

// 添加响应拦截器
axios.interceptors.response.use(function (response) {
    // 2xx 范围内的状态码都会触发该函数。
    // 对响应数据做点什么
    return response;
  }, function (error) {
    // 超出 2xx 范围的状态码都会触发该函数。
    // 对响应错误做点什么
    return Promise.reject(error);
  });
```

## axios基地址

**语法:**

`axios.defaults.baseURL='URL'`

```javascript
axios.defaults.baseURL = 'http://www.liulongbin.top:3006'
```

## 文件上传

* FormData对象官方文档：https://developer.mozilla.org/zh-CN/docs/Web/API/FormData
* 文件上传必须要FormData对象 ： 因为文件数据 和 文本数据 在传输的时候，数据格式不同。需要formdata对象进行自动处理。
  * `file`表单默认自带一个点击事件,作用是选择文件
  * 上传文件==必须==要使用原生内置对象`FormData`==对象==
  * file表单有一个特殊的事件`onchange`事件:用户选择了文件就会执行

```html
<!DOCTYPE html>
<html lang="en"> 
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>案例-头像上传</title>
    <link rel="stylesheet" href="./lib/bootstrap-v4.6.0.css" />
    <style>
      .thumb-box {
        text-align: center;
        margin-top: 50px;
      }

      .thumb {
        width: 250px;
        height: 250px;
        object-fit: cover;
        border-radius: 50%;
      }
    </style>
  </head>

  <body>
    <div class="thumb-box">
      <!-- 头像 -->
      <img src="./images/cover.jpg" class="img-thumbnail thumb" alt="" />
      <div class="mt-2">
        <!-- 文件选择框 -->
        <!-- accept 属性表示可选择的文件类型 -->
        <!-- image/* 表示只允许选择图片类型的文件 -->
        <input type="file" id="iptFile" accept="image/*" />
        <br />
        <!-- 选择头像图片的按钮 -->
        <button class="btn btn-primary" id="btnChoose">选择 & 上传图片</button>
      </div>
    </div>

    <script src="./lib/axios.js"></script>
    <script>
      /*文件上传思路总结 
      1. 给file表单注册onchange事件 
        * 当用户选择图片之后执行
      2. 获取用户选择的图片 
        * this.files[0]
      3. 创建FormData对象 
        * 只有FormData才可以上传文件
      4. 将图片添加到FormData对象中 
        * fd.append('参数名', this.files[0])
      5. 发送ajax请求
        * 文件上传请求方法一定是post, 且请求参数为 FormData对象
      */
     
      //1. file类型表单自带一个选择文件点击按钮，当用户选择文件之后就会触发onchange事件
      document.querySelector("#iptFile").onchange = function() {
        //this : file表单
        //(1)获取用户选择的文件
        let file = this.files[0]
        // 非空判断，如果内容为undefined，给出提示
        if (file == undefined) {
          return alert("请选择上传文件！")
        }
        //(2)创建FormData对象， 只有FormData对象才可以上传文件
        let fd = new FormData()
        //(3)添加文件
        fd.append("avatar", file)
        //(4)发送ajax请求, 参数为 FormData对象
        axios({
          method: "POST",
          url: "http://www.liulongbin.top:3009/api/upload/avatar",
          data: fd
        }).then(({ data: res }) => {
          console.log(res)
          if (res.code != 200) {
            return alert(res.message)
          }
          // 成功后提示，修改图片路径
          alert("恭喜您，上传头像成功！")
          document.querySelector("img").src = `http://www.liulongbin.top:3009${res.url}`
        })
      }
    </script>
  </body>
</html>

```

