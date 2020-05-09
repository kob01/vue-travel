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

import './assets/styles/reset.css'
**// 1 像素边框**
import './assets/styles/border.css'

cnpm i fastclick --save

main.js中引入fastclick插件解决双击屏幕放大缩小问题

import fastClick from 'fastclick'

fastClick.attach(document.body)

cnpm i stylus --save

cnpm i stylus-loader --save

![1589031556346](E:\my-project\readme-img\1589031556346.png)



**问题：返回上一级页面后，window.addEventListener事件监听仍然生效**

方案：返回后关闭事件监听事件

``````
  deactivated() {
    window.removeEventListener('scroll', this.handleScroll)},
``````