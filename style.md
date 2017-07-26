

## RN的所有[style样式属性](http://reactnative.cn/docs/0.46/layout-props.html)一览

## 作用在父控件上Flexbox布局

在React Native中使用flexbox规则来指定某个组件的子元素的布局。Flexbox可以在不同屏幕尺寸上提供一致的布局结构。一般来说，使用`flexDirection`、`alignItems`和`justifyContent`三个样式属性就已经能满足大多数布局需求。
* __flex__

类似于Android中的权重。

* __flexDirection__

`flexDirection`可决定布局的主轴。子元素是应该沿着水平轴\(`row`\)方向排列，还是沿着竖直轴\(`column`\)方向排列呢？默认值是竖直轴\(`column`\)方向。还有`column-reverse`、`row-reverse`。

* __justifyContent__

`justifyContent`可以决定其子元素沿着主轴的排列方式。子元素是应该靠近主轴的起始端还是末尾段分布呢？亦或应该均匀分布？对应的这些可选项有：`flex-start`、`center`、`flex-end`、`space-around`以及`space-between`。

* __alignItems__

`alignItems`可以决定其子元素沿着次轴（与主轴垂直的轴，比如若主轴方向为row，则次轴方向为column）的排列方式。子元素是应该靠近次轴的起始端还是末尾段分布呢？亦或应该均匀分布？对应的这些可选项有：`flex-start`、`center`、`flex-end`以及`stretch`。

> 注意：要使stretch选项生效的话，子元素在次轴方向上不能有固定的尺寸。以下面的代码为例：只有将子元素样式中的`width: 50`去掉之后，`alignItems: 'stretch'`才能生效。

## 作用在子控件上
* __alignSelf__

`enum('auto', 'flex-start', 'flex-end', 'center', 'stretch') `决定了元素在父元素的次轴方向的排列方式（此样式设置在子元素上），其值会覆盖父元素的`alignItems`的值。
* __borderWidth__

控件边框的宽度，具体的还有`borderLeftWidth`，  `borderTopWidth`， `borderRightWidth`， `borderBottomWidth`。
* __position__

`enum('absolute', 'relative') `RN中`position`的默认值都是`relative`，并且`absolute`值也是控件相对于父控件的绝对值。当你想让子控件的位置是相对于父控件时，可以设置为`absolute`。如果你想让控件的位置不是相对于父控件时，要设置为`relative`。
* __控件相对于四周的距离__

`left`， `top`， `right`， `bottom`定位控件距四周的逻辑像素，四周的定义取决于`position`的值。

* __margin__

和`marginLeft`， `marginTop`， `marginRight`， `marginBottom`一起，决定控件对四周的边距，是相对于父控件的。另的还有`marginHorizontal`，`marginVertical`。
* __控件宽高__

`width`， `height`，`maxWidt`， `maxHeight`， `minWidth`， `minHeight`。
* __padding__

内边距，还有`paddingLeft`, `paddingTop`, `paddingRight`, `paddingBottom`, `paddingHorizontal`, `paddingVertical`
* __overflow__

`enum('visible', 'hidden', 'scroll')`当内容溢出时，控件发生的事情。
* __zIndex__

控件哪个控件显示在最上面。






