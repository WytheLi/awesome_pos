# awesome_pos

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


### Webpack+Vue-router的架构
1. 安装vue-cli脚手架
```
mpm install vue-cli -g
```
2. 采用的是webpack模板，初始化
```
vue init webpack
```
3. 添加线上icon图标库
> Iconfont网址：http://www.iconfont.cn
4. 安装element-ui组件库
在 main.js 中写入以下内容：
```
import Vue from 'vue';
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
import App from './App.vue';

Vue.use(ElementUI);

new Vue({
  el: '#app',
  render: h => h(App)
});
```
`npm install`安装依赖包


