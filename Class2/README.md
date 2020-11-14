# Class 2

## 目录

- [Class 2](#class-2)
  - [目录](#目录)
  - [下载VSCode](#下载vscode)
  - [配置VSCode环境](#配置vscode环境)
  - [下载Node](#下载Node)
  - [实战 echarts —— 实现一个简单的图表](#实现)

## 下载VSCode

大家根据各自电脑的操作系统在[官网](https://code.visualstudio.com/)下载适配各自的VSCode

## 配置VSCode环境

![image-20201113182019528](C:\Users\seduos-03\AppData\Roaming\Typora\typora-user-images\image-20201113182019528.png)



### 下载Node

1. 在[官网](https://nodejs.org/en/download/)中根据各自电脑的操作系统下载适配自己的 Node 

   **Tips**：由于是外网，可能下载速度比较慢，可以选择[国内镜像](http://nodejs.cn/download/)进行下载

2. 测试自己是否安装成功：Windows 用户键入 win+R；mac 用户键入 command+space，搜索 terminal；输入 `node -v`，查看 node 版本；输入`npm -v` ，查看 npm 的安装版本



### node 和 npm 

- 简单来说，node 就是运行在服务端的 Javascript，你就可以想象成是运行在你自己本地的一个服务，可以通过命令行去调用它所实现的各种功能，每当我们遇到一个新的应用程序时，我们可以通过 `--help / -h` 的形式来查看他的功能实现。例如 `node -h`



- 而 npm ，全称是 node package management，即 node 的包管理软件，在开源的世界里，我们需要共享各自的代码，我们把各种各样的库上传到线上，供大家来下载，而 npm 就是作为一个去线上拉代码的工具，以及对本地代码库的管理。



所以这两个是不同的软件，但在新版本的 node 中自带了 npm，所以就不需要二次下载了。



###  实战

1. 在 echarts [官网](https://github.com/apache/incubator-echarts/tree/4.9.0)下载其源码

2. ```html
   <!DOCTYPE html>
   <html>
   <head>
       <meta charset="utf-8">
       <title>ECharts</title>
       <!-- 引入 echarts.js -->
       <script src="./echarts.min.js"></script>
   </head>
   <body>
       <!-- 为ECharts准备一个具备大小（宽高）的Dom -->
       <div id="main" style="width: 600px;height:400px;"></div>
       <script type="text/javascript">
           // 基于准备好的dom，初始化echarts实例
           var myChart = echarts.init(document.getElementById('main'));
   
           // 指定图表的配置项和数据
           var option = {
               title: {
                   text: 'ECharts 入门示例'
               },
               tooltip: {},
               legend: {
                   data:['销量']
               },
               xAxis: {
                   data: ["衬衫","羊毛衫","雪纺衫","裤子","高跟鞋","袜子"]
               },
               yAxis: {},
               series: [{
                   name: '销量',
                   type: 'bar',
                   data: [5, 20, 36, 10, 10, 20]
               }]
           };
   
           // 使用刚指定的配置项和数据显示图表。
           myChart.setOption(option);
       </script>
   </body>
   </html>
   ```

   

### 绝对路径和相对路径

- **绝对路径**：`C:/Users/seduos-03/Desktop/incubator-echarts-4.9.0/dist/echarts.simple.min.js`

- **相对路径**：`./echarts.simple.min.js`

