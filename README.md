# vue-cli 使用说明 
# <h2 style="color:red">使用问题整理</h2>
   1. npm run dev 自动打开浏览器   
    设置 config/index.js 中的 autoOpenBrowser: true,
   2. 关闭语法检测 单元测试  
   ```     Use ESLint to lint your code?(y/n)   这里选 n 敲回车
    Setup unit 项目名称 with karma + Mocha?(y/n) 这里选 n 敲回车
    Setup e2e 项目名称  with Nightwatch? (y/n) 这里选 n 敲回车
   ```
#   →  →  START
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

Mail: 211366323@qq.com
