## 复习
商品分类的三级列表 由静态变动态 【获取服务器数据要解决代理跨域问题】
函数节流与防抖
路由导航：声明式导航 编程式导航


## 开发search模块中的typeNav商品分类菜单(过渡动画)
过度动画前提式必须要有 v-if|v-show指令才能进行过度
必须要用transition标签包裹

## 性能优化
把公共发起请求的数据可以写在app组件中 因为app组件只会执行一次

## 合并参数
注意：要将params与query参数合并
例子：我点击了手机 再去搜索华为 就不会被刷新掉(变成华为) 
而是变成手机华为

## 轮播图和Floor组件
mock数据(模拟) 需要插件mock.js 提供假数据 不会发ajax请求
1.使用步骤 创建mork文件夹 
2.准备假(JSON)数据 json文件
3.mock(虚拟数据)，通过mockjs模块实现
4.在入口文件引入mock.js

注意：默认对外暴露的有图片、JSON数据格式

轮播图  mounted  vuexactions  初始化swiper  vuexmutations
组件没有数据是因为异步

解决方法 watch+$nextick 数据监听 