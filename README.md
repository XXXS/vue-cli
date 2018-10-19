# vue-cli 使用说明 
# 使用问题整理 
   1. npm run dev 自动打开浏览器   
    设置 config/index.js 中的 autoOpenBrowser: true,
   2. 关闭语法检测 单元测试  
   ```    
    Use ESLint to lint your code?(y/n)   这里选 n 敲回车
    Setup unit 项目名称 with karma + Mocha?(y/n) 这里选 n 敲回车
    Setup e2e 项目名称  with Nightwatch? (y/n) 这里选 n 敲回车
   ```
   3.npm run build 打包以后图片失效
   解决方法:  在build目录下 utils.js 文件下
   ```
     if (options.extract) {
        return ExtractTextPlugin.extract({
        use: loaders,
        fallback: 'vue-style-loader',
        publicPath:'../../'   // 新增这一行解决打包之后图片失效问题

      })
    } else {
      return ['vue-style-loader'].concat(loaders)
    }
   ```

## 1. [安装node.js](https://nodejs.org/zh-cn/)
## 2. [安装Git](https://git-scm.com/)
## 3. 切换淘宝镜像
```
  $ npm install -g cnpm --registry=https://registry.npm.taobao.org
```
## 4.安装 webpack
```
 cnpm install webpack -g
```
## 5. 安装脚手架 vue-cli
```
  cnpm install -global vue-cli
```
## 6. 初始化项目
```
  vue-init webpack vue-demo    (vue-demo为项目名称)
```

## 7. 构建完成 
```   cd vue-demo  / 进入项目根目录
  npm run dev     / 运行项目
  npm run build   / 打包上线 运行build会生成 dist文件夹 
 ```
 
## 8. vue使用 sass
```
npm install --save-dev sass-loader
npm install --save-dev node-sass

<style  lang="scss" type="text/scss" scoped>
@import  "./common/scss/reset.scss";
</style>

```
## 9.vue路由懒加载

```
import Vue from 'vue'
import Router from 'vue-router'
Vue.use(Router)

export default new Router({
     // mode:'history',  //消除url中的 #
    routes: [
        { path:'*', redirect: 'test' }, //路由重定向 路由错误跳转到home页
        {
            path:'/', //首页
            component:resolve => require(['../components/home.vue'],resolve)
        },
        {
            path: '/list',
            component: resolve => require(['../components/list.vue'], resolve)
        }
    ]
})

```

## 10. vue打包部署在非根目录下配置
```
 10.1  build 文件夹下 utils.js 文件中  
        publicPath: '/'  设置为:  publicPath: '../../'  
 10.2  config 文件夹下 idnex.js 文件中
     assetsPublicPath: './',  改为  assetsPublicPath: '/test/001/',   ( '/test/001/' == 你的服务器路径)
```


Mail: 211366323@qq.com
