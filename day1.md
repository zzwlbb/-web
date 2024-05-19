## 总结 1
 路由组件放在 pages或者views文件中
 非路由放在components文件中


 我们可以根据组件身上的$route获取路由信息
 控制路由的显示隐藏 路由元信息 用 meta 


## 路由跳转有两种
声明式导航
编程式导航路由 会报错 不能持续点击 因为用了promise
function push(){
    return new promise(req,res)=>{}
}
通过给push方法传递相应的成功或者失败的回调函数，可以捕获当前错误，可以解决
但是指标不治本
解决方法：
this.$router是VueRouter的实例
push在原型对象上
VueRouter.prototype.push = function(){
    函数的上下文为VueRouter类的一个实例
}
 在他的原型上封装
