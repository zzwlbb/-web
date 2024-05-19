## 提交订单
向服务器发一次请求把支付信息传递给服务器
如果成功了那就路由跳转+传参
用query k+value的形式传参  this.orderId 应该是服务器返回来的订单号
this.$router.push(`/pay?orderId=￥{this.orderId} `)

## 如果不用vuex
可以直接在入口文件  
import * as API from '@/api';
Vue.prototype.$API = API;
在原型上使用api  这样以后用api 就直接this.$API

## 注意
不要在 声明周期函数上 async|await

## 二维码  qrcode
要获取到后台二维码的地址 然后再配合插件使用

显示二维码后判断 有没有支付成功  
后台会给你一个api接口
然后要一直向服务器问有没有支付成功 【定时器】
没支付成功为205 成功为200
如果成功了code为200 就停止定时器
然后保留成功的code
最后关闭弹窗
跳转到下个路由