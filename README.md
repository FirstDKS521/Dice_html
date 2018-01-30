#前端开发：使用flex布局实现骰子1-6饼

![效果图.png](http://upload-images.jianshu.io/upload_images/1840399-6da4425e5a4272fd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

我目前开发HTML时，使用的布局最多的就是`flex`，好学，容易上手；话不多说，直接上代码！

####HTML代码如下：
```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width,minimum-scale=1.0,maximum-scale=1.0,user-scalable=no">
        <link rel="stylesheet" href="circle.css">
        <title></title>
    </head>
    <body>
        <div class="box box1">
            <span class="item1"></span>
        </div>
        <div class="box box2">
            <span class="item1"></span>
            <span class="item2"></span>
        </div>
        <div class="box box3">
            <span class="item1"></span>
            <span class="item2"></span>
            <span class="item3"></span>
        </div>
        <div class="box box4">
            <div class="column">
                <span class="item1"></span>
                <span class="item2"></span>
            </div>
            <div class="column">
                <span class="item1"></span>
                <span class="item2"></span>
            </div>
        </div>
        <div class="box box5">
            <div class="column">
                <span class="item1"></span>
                <span class="item2"></span>
            </div>
            <div class="column">
                <span class="item1"></span>
            </div>
            <div class="column">
                <span class="item1"></span>
                <span class="item2"></span>
            </div>
        </div>
        <div class="box box6">
            <div class="column">
                <span class="item1"></span>
                <span class="item2"></span>
                <span class="item3"></span>
            </div>
            <div class="column">
                <span class="item1"></span>
                <span class="item2"></span>
                <span class="item3"></span>
            </div>
        </div>
    </body>
</html>
```
####CSS代码如下：
```
body {
    margin: 0;
    padding: 0;
    background-color: black;
    display: flex;
    display: -webkit-flex;
    flex-flow: row wrap;
    -webkit-flex-flow: row wrap;
    justify-content: space-around;
    -webkit-justify-content: space-around;
}

.box1 {
    display: flex;
    display: -webkit-flex;
    justify-content: center;
    -webkit-justify-content: center;
    align-items: center;
    -webkit-align-items: center;
}

.box2 {
    display: flex;
    display: -webkit-flex;
    justify-content: space-between;
    -webkit-justify-content: space-between;
    flex-flow: column nowrap;
    -webkit-flex-flow: column nowrap;
}

.box2 .item2 {
    align-self: flex-end;
    -webkit-align-self: flex-end;
}

.box3 {
    display: flex;
    display: -webkit-flex;
    flex-flow: column nowrap;
    -webkit-flex-flow: column nowrap;
    justify-content: space-between;
    -webkit-justify-content: space-between;
}

.box3 .item2 {
    align-self: center;
    -webkit-align-self: center;
}

.box3 .item3 {
    align-self: flex-end;
    -webkit-align-self: flex-end;
}

.box4 {
    display: flex;
    display: -webkit-flex;
    flex-flow: column nowrap;
    -webkit-flex-flow: column nowrap;
    justify-content: space-between;
    -webkit-justify-content: space-between;
}

.box4 .column {
    display: flex;
    display: -webkit-flex;
    justify-content: space-between;
    -webkit-justify-content: space-between;
}

.box5 {
    display: flex;
    display: -webkit-flex;
    flex-flow: column nowrap;
    -webkit-flex-flow: column nowrap;
    justify-content: space-between;
    -webkit-justify-content: space-between;
}

.box5 .column {
    display: flex;
    display: -webkit-flex;
    justify-content: space-between;
    -webkit-justify-content: space-between;
}

.box5 .column:nth-of-type(2) {
    justify-content: center;
    -webkit-justify-content: center;
}

.box6 {
    display: flex;
    display: -webkit-flex;
    justify-content: space-between;
    -webkit-justify-content: space-between;
}

.box6 .column {
    display: flex;
    display: -webkit-flex;
    flex-flow: column nowrap;
    -webkit-flex-flow: column nowrap;
    justify-content: space-between;
    -webkit-justify-content: space-between;
}


.box {
    margin-top: 20px;
    width: 100px;
    height: 100px;
    background-color: white;
    border-radius: 4px;
}

span {
    display: block;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color: black;
}
```
参考文章：[文章一](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)，[文章二](http://www.ruanyifeng.com/blog/2015/07/flex-examples.html)
