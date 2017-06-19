# Bootstrap
## 1.规范
 - 给每一个板块加上一个唯一的id，避免css样式上的冲突。例如<header id=""header></header>。
 
- 尽可能多使用直接自带选择器


---

## 2.外链字体

```
 @font-face {
    font-family: 'itcast';
    src:url('../font/MiFie-Web-Font.eot')  format('embedded-opentype'),
    url('../font/MiFie-Web-Font.svg')  format('svg'),
    url('../font/MiFie-Web-Font.ttf')  format('truetype'),
    url('../font/MiFie-Web-Font.woff') format('woff');
}

/*class以icon-开头且包含icon-*/
*[class^="icon-"],
*[class*=" icon-"] {
     font-family: wjs;
 }
```


---
## 3. + 下一个兄弟选择符来去掉第一个元素的边框

- 从第二个div开始选中，第一个div没有左边框
```
#header > .topbar > .container > .row > div + div {
    border-left: 1px solid #c0c0c0
}

```

---
## 4.自动生成自定义按钮
- [bbg网站](http://blog.koalite.com/bbg/)
- 打开网站，输入需要的选项，自动生成按钮css样式代码。

---

## 5.制作字体图标
- [icomoon网站](https://icomoon.io/)
- 上传svg文件可以自动生成字体文件。download下来，导入字体后直接可以使用字体图标。


---
## 6.bootstrap样式的扩展

- 例如我们要把nav自定义样式，原来的默认样式是navbar-default,我们可以改成navbar-defined。
```
/*修改前*/
<nav class="navbar navbar-static-top navbar-default"></nav>

/*修改后*/
<nav class="navbar navbar-static-top navbar-defined"></nav>
```

- 在原bootstrap中搜索navbar-default，相关样式全部复制下来。
- 粘贴自己的css文件里面，把css里的类名navbar-default都替换成navbar-defined。
- 调整样式。


---
## 如何让长条图在屏幕正中心展示
- 方式一：使用背景图片，再设置background-position :center center。
- 方式二：定位，left:50%;margin-left:-自身宽度一半。
- 响应式图片技巧：给图片盒子加上data属性,分别设置data-image-lt和data-image-lg为小图和大图的src路径。
- 大图的情况使用背景图片且居中，设置图片盒子的高度为图片的高度。小图用img标签插入且宽度设为100%，不设置高度，目的是使图片能随着屏幕的大小变化尺寸。
