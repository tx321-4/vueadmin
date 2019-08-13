# vueadmin
> vuejs 和 element 搭建的一个后台管理界面

## Build Setup

## [原文链接：（https://github.com/taylorchen709/vue-admin）](https://github.com/taylorchen709/vue-admin)

``` bash
# install dependencies
npm install


# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## 项目总结
```bash
#  eslint 结尾使用分号；
'semi': ["error", "always"] 
```
### 报错 `Cannot read property 'disabled' of null`
  
* 这个是因为在页面中使用了el-dropdown，但是在这个标签里面没有设置它的子元素，所以会报错，在el-dropdown中添加el-dropdown-menu标签就好