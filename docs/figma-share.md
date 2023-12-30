## PPT

## 内容

前端开发者怎样使用 figma。

### 1. 优点

### 2. how to use

1. layout - auto layout
2. style - ICG DS
3. assets
4. components
5. comments

### 3. dev mode

- figma dev mode
- vs code plugin

最后和大家介绍一下 figma 新出的开发者模式。

1. layout - auto layout
2. style - ICG DS
3. assets
4. components
5. comments

今天我就是给大家分享一下关于 figma 的一些我自己使用的一些心得，作为一个程序员的理解，主要是怎么把 figma 与前端开发结合

给我们 dev 的一般是 view 权限

怎么样去看 figma 来做前端开发

figma 有几个基本的东西，就像我们写 html 的时候会有 div，对应到 figma 可以理解成是这个 Frame。

figma 本身会有 X Y W H，XY 位置，WH 宽高

auto layout <-> flex box, gap

figma 和我们的组件也是一一对应的，组件：紫色，菱形

- 在实际开发中，我们经常遇到一个问题就是我们的实现效果和 figma 上的边距不一样，比如这个元素距离顶部的高度太大，这时候我们可能有好几种方式减少这里的高度，比如减少这个 box 的 margin 或者 padding， 但是建议大家来通过 figma 查看各个元素之间的边距，找到是哪个元素导致的，这样当 figma 有更新时，我们的调整可能更少一些。
