# hello-world

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).



### Vue class1
1. Vue-cli安装(cnp配置)
    1. 检查node和npm是否安
        node -v
    2. 将npm转换为cnpm
        npm install -g cnpm --registry=https://registry.npm.taobao.org
    3. npm install -g @vue/cli

2. Vue指令创建项目
    1. 在硬盘上找一个文件夹放工程用的
    2. vue create hello-world

3. Vue npm 运行Vue项目指令 
    Vue run serve

4. 工程目录文件/文件夹名字
    assets 用来放置图片
    components 用来放置组件文件
    App.vue  项目的入口文件，主要编写文件

5. 编辑App.Vue查看样式
    
6. Vue模板语法
    v-bind  用于绑定数据和元素属性
    v-if  判断语句
    v-for  循环语句
    v-on  添加一个事件监听器
    v-model  表单输入和应用状态之间的双向绑定
7. data方法以及数据
    return 一个数组，里面数值可以后续拿到，或者赋值
8. methods属性及方法
    写一些方法，便于后面的调用
9. v-bind:class特殊处理
10. 元素样式依然写在style里
11. templete标签有一个限制
    只能有一个直接子标签
12. this
    在方法里调用data中的数据

作业
1. 完成百度新闻 
2. 使用Vue写朋友圈(展示,发布)
3. 随机点名
需要新创建,上传git hub
git 主页  new 