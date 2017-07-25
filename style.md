

## rn的所有布局[样式属性](http://reactnative.cn/docs/0.46/layout-props.html)一览

# 作用在父控件上样式Flexbox布局

在React Native中使用flexbox规则来指定某个组件的子元素的布局。Flexbox可以在不同屏幕尺寸上提供一致的布局结构。一般来说，使用`flexDirection`、`alignItems`和`justifyContent`三个样式属性就已经能满足大多数布局需求。

* Flex Direction

指定`flexDirection`可决定布局的主轴。子元素是应该沿着水平轴\(`row`\)方向排列，还是沿着竖直轴\(`column`\)方向排列呢？默认值是竖直轴\(`column`\)方向。还有`column-reverse`、`row-reverse`。

* Justify Content

在组件的style中指定justifyContent可以决定其子元素沿着主轴的排列方式。子元素是应该靠近主轴的起始端还是末尾段分布呢？亦或应该均匀分布？对应的这些可选项有：`flex-start`、`center`、`flex-end`、`space-around`以及`space-between`。

* Align Items

在组件的style中指定alignItems可以决定其子元素沿着次轴（与主轴垂直的轴，比如若主轴方向为row，则次轴方向为column）的排列方式。子元素是应该靠近次轴的起始端还是末尾段分布呢？亦或应该均匀分布？对应的这些可选项有：`flex-start`、`center`、`flex-end`以及`stretch`。

> 注意：要使stretch选项生效的话，子元素在次轴方向上不能有固定的尺寸。以下面的代码为例：只有将子元素样式中的`width: 50`去掉之后，`alignItems: 'stretch'`才能生效。

# 作用在子控件上样式





