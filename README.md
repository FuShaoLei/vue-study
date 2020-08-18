# 黑马程序员Vue教程笔记

## Vue简介
- JavaScript框架
- 简化Dom操作
- 响应式数据驱动

> Dom是什么，👴不懂

## 第一个vue程序
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id="app">
        {{ message }}
    </div>   
</body>
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<script>
    var app=new Vue({
        el: '#app',
        data: {
            message: 'Hello Vue !'
        }
    })
</script>
</html>
```

### el：挂载点
- 作用：el是用来设置Vue实例挂载管理的元素
- 作用范围：el选项命中元素及其内部的后代元素
- 建议使用id选择器
- 可使用在除了在html和body的双标签上

### data：数据对象
- Vue中用到的数据定义在data中
- 可写复杂类型的数据

## 基础Vue指令

### 指令总结

指令 | 说明
--|--
`v-text` | 设置文本值，将覆盖原来的值 
`v-html` | 设置innerHTML，内有html结构的话会被解析成标签 
`v-on` | 为元素绑定事件，指令可简写为@，绑定的方法定义在**methods**属性中，方法内部通过this关键字可访问定义在data中的数据 