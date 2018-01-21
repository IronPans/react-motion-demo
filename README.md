react-motion是一个强大的react动画库。

官网：<a href="https://github.com/chenglou/react-motion">react-motion</a>。

基于react-motion，写了三个简单的动画来讲解使用方法。

- 方块移动
- 跟随鼠标
- 折叠

在开始讲解实例之前，我们先来了解一个重要的函数：spring()

语法：
```
spring(val: number, config?: SpringHelperConfig)
```
- val：number, 终点值
- config: 用于生成动画缓动效果的配置
  - stiffness：默认值170
  - damping：默认值26
  - precision： 默认值0.01，用于配置val的精确度，一般不需改动

  仅从文字很慢描述，一起来感受一下效果：<a href="http://chenglou.github.io/react-motion/demos/demo5-spring-parameters-chooser/">http://chenglou.github.io/react-motion/demos/demo5-spring-parameters-chooser/</a>

  我们可以将设置动画物体想象成弹簧，而stiffness就相当于弹簧的强度，也可理解为弹簧被拉伸的长度（有效范围）；damping就相当于弹簧的硬度。
  - 相同硬度下，你拉的越长，它的回弹速度就越快；
  - 相同强度下，硬度越大，回弹（缓冲）的次数就越少。

  <img src="http://oumfrpm5j.bkt.clouddn.com/react-motion.jpg">

1. 方块移动

方块移动实例使用了Motion组件。

<Motion />适合编写单个组件的形变动画。

属性：
- style：Object，动画样式
- defaultStyle：Object，初始样式
- children：子元素
- onRest：动画结束时触发回调

<img src="http://oumfrpm5j.bkt.clouddn.com/react-motion-Motion.gif">

2. 跟随鼠标

跟随鼠标实例使用了StaggeredMotion组件。

<StaggeredMotion />用于编写一串有相互关联关系的实体的动画。

属性：
- styles：Array，动画样式
- defaultStyles：Array，初始样式
- children：子元素

<img src="http://oumfrpm5j.bkt.clouddn.com/react-motion-StaggeredMotion.gif">

3. 折叠

折叠实例使用了TransitionMOtion组件。

<TransitionMotion />则是用来编写组件mount和unmount的动画

属性：
- styles：Array，动画样式
- defaultStyles：Array，初始样式
- children：子元素

<img src="http://oumfrpm5j.bkt.clouddn.com/react-motion-TransitionMotion.gif">