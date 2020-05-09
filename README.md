# vue-travel

> A Vue.js project

## Build Setup

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

**移动端适配**

,minimum-scale=1.0,maximum-scale=1.0,user-scalable=no

**1 像素边框**

import './assets/styles/reset.css'//main.js

import './assets/styles/border.css'

cnpm i fastclick --save

**main.js中引入fastclick插件解决双击屏幕放大缩小问题**

import fastClick from 'fastclick'

fastClick.attach(document.body)

**问题：轮播图图片加载完成前页面抖动**

``` 
 overflow hidden
 height 0
 padding-bottom 55% 
```

 **问题：轮播图打开默认在最后一页** 

<swiper>标签中增加``` v-if="list.length" ```

**问题：轮播图部分样式无法选择修改**

```.wrapper>>>.swiper-pagination-bullet-active```<!--实现组件和插件的样式关联-->

**CSS全局变量**

cnpm i stylus --save

cnpm i stylus-loader --save

**问题：边框处理**

```.border-topbottom
&:before
	border-color: #ccc
```

**Q:城市选择后将所选城市记录本地导致BUG**

方案： ![localstorage](E:\my-project\readme-img\localstorage.png)

**性能优化：**前后页面多次跳转，通过**keep-alive** ， 页面被加载一次后把路由放置内存中，下次再进路由不需要重新渲染组件，只需要把以前的内容拿出来显示 

**图标更新后注意事项：**

![icon-update](E:\my-project\readme-img\icon-update.png)

**页面美化：** 图像下边缘颜色渐变效果 

 ![img](E:\my-project\readme-img\jianbian.png) 

``` background-image linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,.8))```

**Q: 画廊模式中轮播图点开后切换中断（两张图中间停住） **

原因：该模式中类发生变化

方案：在**swiperOptins**中添加**父子元素监视器**

```
        observeParents: true,
        observer: true,
```

#### 特殊生命周期钩子函数

**activated钩子在keep-alive缓存的组件激活时调用,deactivated在关闭时调用**

**问题：返回上一级页面后，window.addEventListener事件监听仍然生效**

![1589031556346](E:\my-project\readme-img\1589031556346.png)



方案：返回后关闭事件监听事件

``````
  deactivated() {
    window.removeEventListener('scroll', this.handleScroll)},
``````

**组件中name的用途：**

1. 递归组件
2. 取消页面缓存时（exclude=‘Detail’）
3. VUE开发工具显示

**Q:滚动行为**

router/index.js中

```
scrollBehavior(to, from, savedPosition) {
    return { x: 0, y: 0 }  },
```

