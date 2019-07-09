### css定位有哪些，区别是什么？

属性值 | 描述 | 脱离文档流？| 是否可以使用top,left|
--|--|--|--
static |默认值，默认位置没有定位|否|否|
relative |相对于自身第一个位置定位|否|是|
absolute |相对于离元素最近的设置了**绝对或相对定位**的父元素|是|是|
fixed |对于浏览器窗口是固定位置|是|是|
z-index|元素的堆叠顺序|否|否|
sticky|相对定位和固定定位的混合(适用于吸顶效果) |是|是
inherit|从父元素继承 position 属性的值。|


---

### 如何判断是否脱离文档流？
- relative布局时,设置了left.但下方盒子并没有上移，说明上方盒子占据着位置。他们是同一个文档流。对比absolute布局

![](./relative.jpg "relative布局")

- z-index布局时,下方盒子并没有上移，说明上方盒子占据着位置。他们是同一个文档流，对比fixed布局

![](./fixed.jpg "fixed布局")