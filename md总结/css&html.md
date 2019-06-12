右键 HTML(offline) 输出html文档,包含样式.自动生成标签.
[链接](http://www.4399.com/) 中括号链接内容,括号内链接地址.
#符号:1-6级标题层级 
1.换行: 在一行文字后面空两格+回车
2.换段落:空一行
3.无序列表* + - 有序列表加.标识
4.代码块 ```
>5.引用:强调某段文字,高亮显示 

###06-昌隆随笔  
1.导航栏ul可不设宽度和高度,由内部元素li撑起,定位要用position.  
2.内部li嵌套a标签(displayblock)和底部横条span标签(posiion).
3.最右边li mr0 marginleft:-13px,可以实现左边整体游移.
4.导航底部横线不可见
```
.nav-item .line{
	display: none;
 .nav-item:hover a{
	color: 蓝色;
.nav-item:hover .line{
	display: block;
}
\*激活位置*\
.header-c .nav .nav-item.active a{
	color: 蓝色;
}
.header-c .nav .nav-item.active .line{
	display: block;
```
5.冒号符号(行内元素对齐方式)
外面最大div变行内块,内里包两个块
px;
6.转义字符:斜杠\*你好\*  
{
    display inline-block
    width:16px;
    height:6px;
    vertical align -3px;
}

\*内里上冒号块状自动占据顶部,下边块状+margin*\
.title .dots span{
	display: block;
	width: 6px;
	height: 6px;
	background-color: #0D3A69;
}
.title .dots .bottom{
	margin-top: 4px;
    
###05-京东随笔
1.text-indenct + 插入背景左对齐方式实现图标加文字总是text-aligin: center.
```.tips .title{

display: inline-block;
height: 100%;
margin: 0 auto;
text-indent: 20px;
background: url(img/icon-tips.png) no-repeat left center;
```
2.登录框:div内包裹两个浮动盒子,outline: none; 
input盒子不许点击,hover为光标.
```
.form .loginbar .icon{
float: left;
width: 36px;
height: 36px;
} 
.form .loginbar input{
float: left;
width: 270px;
height: 36px;
border: none;
/*聚焦的时候*/
outline: none;
text-indent: 12px;
```  
3.底部小图标,一个div大盒子嵌套a标签(左边留padding给图标).中间竖线span标签,内部元素全部浮动.
```
/*内部元素公共属性!!!*/
		.login-block .login-footer a{
			position: relative;
			float: left;
			height: 19px;
			line-height: 19px;
			margin-top: 16px;
			padding-left: 22px;
		}
        /*竖线*/
		.login-block .login-footer .line{
			float: left;
			width: 1px;
			height: 15px;
			background-color: #333;
			margin-top: 20px;
			margin-left: 16px;
			margin-right: 16px;
		}
```  
###05-ZX
1.垂直居中:top:50%,顶端对齐中线后mrgin-top负自身的一半.
```
.zx-details .title .close{
            /*垂直居中*/
			position: absolute;
			top: 50%;
			margin-top: -8px;
			
		}
```  
2.旋转
```
.zx-details .title .close:hover{
            /*css3 过渡效果*/
			transition: all ease .8s;
			transform: rotate(180deg);
            
```  
##浮动的影响
1.当一个块级元素浮动后,宽度会被内容默认撑开,因此需要为其指定一个宽度.  
浮动后元素脱离文档流,不再占用文档位置,不会再撑开父元素高度.
##z-index
2.元素开启定位后添加z-index属性显示优先级.








