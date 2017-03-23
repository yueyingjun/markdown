# 选择器
## 后代级别
* :nth-child(n)   选择的当前元素在父元素当中要作为子元素出现,他是第几个孩子（在乎其他元素）
* :first-child  作为第一个子元素出现
* :last-child    作为最后一个子元素出现
* :nth-last-child(n)   从后往前计数
* :only-child        作为独生子出现

## 同辈元素
 
* :nth-of-type(n)  作为同辈元素中的第n个(不在乎其他元素) 
* :nth-last-of-type(n) 从后往前计数
* :first-of-type  作为第一个兄弟元素出现(长兄)
* :last-of-type   作为最后的兄弟出现
##  伪类

* :hover          鼠标移入
* :after          一个元素的后面的部分
* :before         前面的部分
* :first-letter   元素的第一行文字
* :first-line     元素的第一个文字
* :focus          获得焦点
* ::selection     浏览器选中文字的样式
* :root           根元素


##  属性选择器

* [attr]  具有某个属性的元素
* [attr=val]  具有指定值得属性的元素
* [attr*=val] 包含有指定的值的一部分的属性得元素
* [attr^=val] 属性的值得开头和指定的值一样的元素
* [attr$=val] 属性的值得结尾和指定的值一样的元素



## 边框模型

### 圆角
*  border-raduis: 圆角的半径(%|px|em|rem|vm)
*  参数的顺序依次是:左上  右上  右下  左下  (顺时针的)

### 阴影

* box-shadow:x y blur color [inset],[x y blur color  inset]

*  x 阴影在x轴的偏移量
*  y 阴影在y轴的偏移量
*  blur 阴影的模糊程度 
*  color 阴影的颜色
* [inset]  内阴影

### 图片边框
* border-image-source:url()  图片的路径
* border-image-width     图片边框的宽度
* border-image-slice     在原图裁切的比例
* border-image-offset    图片边框的偏移量


## 字体图标实现步骤

1. 创建字体
    * 利用svg制作矢量图(借助矢量软件  ai)
    * 将svg格式的图片生成字体
        - 可以借助 阿里巴巴平台，在线转换
        - 可以自己下载字体生成器，本地转换
        - 字体格式  ttf  woff
2. 将创建的字体引入到css页面当中

    ```
    @font-face {font-family: "abc";
        src: url('../font/iconfont.eot?t=1489722221458'); /* IE9*/
        src: url('../font/iconfont.eot?t=1489722221458#iefix') format('embedded-opentype'), /* IE6-IE8 */
        url('../font/iconfont.woff?t=1489722221458') format('woff'), /* chrome, firefox */
        url('../font/iconfont.ttf?t=1489722221458') format('truetype'), /* chrome, firefox, opera, Safari, Android, iOS 4.2+*/
        url('../font/iconfont.svg?t=1489722221458#iconfont') format('svg'); /* iOS 4.1- */
    }
    
    ```                 
              
3. 给指定的元素指定相应的字体

```
1. 知道指定的字体对应的代码什么
 css代码
 
  div{
  font-family:指定的字体
  }
 
 html代码
 
 <div>指定的代码</div>
 
 
 2. 不知道指定的字体对应的代码
     css代码
     
     .one:before{
       content:"指定的代码"
     }
 
     html代码
     <div class="one"></div>
     
```

## 过渡

* transition: 属性  时间 [运动方式] [等待时间] , [属性  时间 运动方式 等待时间]
*  时间单位 [s|ms]


## 2d 转换
* transform:
    - matrix(a,b,c,d,e,f);
    - translate(x,y)
    - translateX()
    - translateY()
    - scale(x,y)
    - rotate(x,y)
    - skew(x,y)
* transform-origin:x y
    - x 基准点的x坐标
    - y 基准点的y坐标
    
## 3d 转换

*  transform:
    - matrix3d(1,2,3,....16)
    -  http://www.jianshu.com/p/52e0018e6ce2
    - translate3d(x,y,z)
    - scale3d(x,y,z)
    - rotate3d(x,y,z,angle)
* transform-origin:x y z;
    -变换的基准轴
* perspective 透视
* perspective-origin 灭点的位置
* transform-style   变换的风格
    -  preserve-3d  子元素保留3d的状态
* backface-visibility
    - hidden  背面不可见
    - visible  背面课间
    
## 颜色透明度
* rgba 
    - r 红色 (0-255)   
    - g 绿色 (0-255)   
    - b 蓝色 (0-255)
    - a 透明度 (0-1)
        
*  hsl  
*  hsla
        
*  线性渐变
        
    -  background:linear-gradient([角度],color color-stop, color color-stop, color color-stop);  
    - 角度  线性渐变的角度，默认角度为180deg
    - color  颜色
    - color-stop  颜色停靠的位置 
        
* 径向渐变
        
    - background:radial-gradient([[形状] [半径] [at x y] ],color color-stop )   
    - 形状 [circle | ellipse]  
    - 半径 渐变的作用区间
    -  x y 渐变中心点的位置
    - color  颜色
    - color-stop  颜色停靠的位置
    
##  背景模块
    
*  background-image:img1,img2
   -  可以设置多个背景
*  background-image-size: [cover|contain|px|%]
   -  设置背景的尺寸
*  background-image-origin:[border-box|padding-box|content-box]
   -  设置背景填充的原点 
*  background-image-clip:  [border-box|padding-box|content-box]
   -  设置背景裁切的区域
       


  
           
        







