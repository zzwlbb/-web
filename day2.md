## 三级联动组件完成
---由于三级联动，在Home，search，Detail出现 ,把他注册为全局组件

## axios的二次封装
请求拦截器，相应拦截器 
请求拦截器:发请求之前处理一些业务
相应拦截器：数据返回后可以处理一些业务

在项目中放AIP文件夹【axios】
接口当中：路径都带有/api 基础路径 
 baseURL:'/api'
 请求超时的时间
 timeout：5000


## 接口统一管理
项目小：完全可以在组件的生命周期函数中发送请求
项目大：创建一个js文件 将接口统一管理到js文件中

## 跨域问题 协议、域名、端口号不同就会出现跨域问题
JSONP SRPS 代理服务器


## :nprogress进度条的使用
注意：进度条一定要引入它的css样式
start进度条开始
done进度条结束


## vuex状态管理库
集中式管理组件中公用的数据

vuex实现模块式开发
要将每一个模块都准备一个js 再让入大模块中给入口(main)文件