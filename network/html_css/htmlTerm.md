# HTML/CSS术语解释
 ## vw/vh
 ```
 .header_white {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: #242424;
}
```
 * 100vw = 是指屏幕的宽度百分之百（viewport width）。
 * 100vh = 是指屏幕的高度百分之百（viewport height）。
 * top是指元素离上方的距离
 * left是指元素离左方的距离

 ## 什么是容器
 * 容器就是指html中外层的元素。比如下面的例子，第一个div就是第二个div的容器 
 ```
 <div>  
 <div> A </div>
 </div>
 ```
 * 注：flex是应用在容器上的。
 * display: flex是横排。