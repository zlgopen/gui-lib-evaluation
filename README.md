# GUI 引擎评价指标

github 上的开源 GUI 引擎至少有数十个，如何去评估它们的优劣，如何选择你需要的 GUI 引擎？这个是艰巨的任务，每个人的需求不一样，GUI 开发者的意图也不同，很难找到统一的标准去选出最好的 GUI。QT 是最强大的，没有之一，但也不一定适合你。

不管怎么样，总有些指标可以提供有价值的参考，尽管这些指标在遇到不同使用的场景，不同的公司背景，不同的个人喜好，它们所占的权重也大不相同。但是并不能抹杀这些指标的价值，关键在于如何根据自己的需要调整它们的比重。

在 [《这个开源的 6 千行 UI 框架，能打败 QT，MFC 吗？》](https://www.zhihu.com/question/66934513/answer/248036488) 这篇文章里，[诸葛不亮](https://www.zhihu.com/people/ZgblKylin) 的 37 问给了我极大的启发，在开发 AWTK 的过程中，多次重读这篇文章，这篇文章堪称是 GUI 引擎开发者的指路明灯。

> 如果诸葛大侠不介意，为了活跃气氛，我就把本文提到的指标称为《诸葛不亮-李先静 GUI 引擎评价指标》，把诸葛大侠放在前面，是表示对他的感谢，把我的名字放在里面，是由我承担一些人的指责。

先开个头，算是抛砖引玉吧。后续会不断完善，希望大家也把自己选择 GUI 引擎时的指标补充进来，文本。

## 1. 基本指标

#### 1.1 开发者的心态

> 当你用他们的 GUI 时，他们是感谢你的支持，还在觉得你欠他们的呢？如果他们没有心存感谢，你最好别用。否则，遇到问题时，你怎么能指望他们帮你解决呢？

#### 1.2 帮助文档

> 是否有《API 手册》、《使用手册》、《常见问题》、《移植文档》和《HowTo》，文档是否在定期更新？

#### 1.3 示例代码

> 是否有简单的入门示例、各种控件的的用法、完整功能的示例？

#### 1.4 代码风格

> 目录名、文件名、类名、函数名、函数参数、局部变量名、全局变量名、注释和缩进是否一致。

#### 1.5 编程的语言

> 对于 GUI 引擎来说，支持多种编程语言是重要的，可以满足不同的开发者的需要。对于使用者来说，GUI 是否提供了你需要的编程语言才是最重要的。

#### 1.6 支持的平台

> 对于 GUI 引擎来说，支持多种平台是重要的，可以满足不同的开发者的需要。对于使用者来说，支持多种平台也是重要的，你现在开发嵌入式系统，过段时间你可能要开发一个 APP 控制你设备，没有必要浪费时间去学习不同的 GUI。
>
> GUI 是否支持目标平台的界面风格，是否提供跨平台的运行库，是否对平台基本的原生功能进行了包装，能否扩展新的功能。 

#### 1.7 是否提供了可视化的界面设计工具

> 所见即所得方式开发界面可以降低学习门槛，提高开发效率。

#### 1.8 可视化的界面设计工具是否是用该 GUI 本身开发的

> 用该 GUI 本身开发的界面设计工具，可以验证该 GUI 本身的功能是否强大和稳定。
> 
> 另外用该 GUI 本身开发的界面设计工具，才能把界面设计工具做得易用。比如 TabControl 控件，在设计时可以切换页面，只有用该 GUI 本身开发的界面设计工具才容易实现。

#### 1.9 能否在开发环境模拟运行

> 运行环境和开发环境往往不同， 如果每次都要部署一下才能看到效果，那开发速度一定上不来。

#### 1.10 是否支持用 XML/JSON 等数据来描述界面

> XML/JSON 是声明式的语法，不但手工编写比写程序容易，也方便借助工具的支持。
>
> 对于嵌入低端嵌入式系统来说，XML/JSON 效率不高，最好的办法是运行时转换成高效的二进制格式。就像代码一样，编译之前的代码给人看，编译之后的代码给机器看。

#### 1.11 是否支持用 XML/CSS 等数据来描述界面的风格

> XML/JSON 是声明式的语法，不但手工编写比写程序容易，也方便借助工具的支持。
> 
> 把界面风格从 UI 描述文件和代码中剥离出来，也有利于后期的维护，毕竟界面效果是最容易变化的。
>
> 对于嵌入低端嵌入式系统来说，XML/JSON 效率不高，最好的办法是运行时转换成高效的二进制格式。就像代码一样，编译之前的代码给人看，编译之后的代码给机器看。

#### 1.12 字体格式

> 支持点阵字体吗？支持矢量字体吗？支持自定义字体格式吗？支持只加载部分字体到内存吗？配套工具完善吗？

#### 1.13 图片格式

> 支持常见的 png/jpg/gif/bmp 格式吗？支持 SVG 等矢量图形吗？能扩展支持新的格式吗？

#### 1.14 输入法

> 支持拼音输入法吗？支持软键盘的 T9 输入法吗？支持硬键盘的 T9 输入法吗？支持语音输入法吗？支持手写输入法吗？可以扩展支持新的输入吗？

#### 1.15 基本架构模式

> 是否内置提供支持 MVC、MVP 和 MVVM 等架构模式。

## 2. 功能指标

#### 2.1 是否支持高清屏

> 是否支持高清屏？在 PC 上运行时界面变糊了，在手机上运行时字体变小了，都是不支持高清屏的特征。不支持高清屏就不用谈什么跨平台了。

#### 2.2 矢量图 API

> 矢量图 API 是非常重要的，强大矢量图 API 能实现很多神奇的效果。个人觉得 HTML5 Canvas 2D API 是最好的矢量图 API。用 cairo、skia、agge 和 nanovg 这些开源的库很容易实现类似的 API。
> 
> GUI 一定要提供一个抽象的接口，在不同的情况下，可以无缝的切换到最优的实现方案上。比如在嵌入式平台用 agge，在嵌入式 linux 平台用 cairo，在 PC 上用 skia 或 nanovg。

#### 2.3 窗口动画

> 是否支持窗口动画？窗口动画的种类是否够用？是否可以扩展自己的窗口动画。窗口动画的效率如何？窗口动画使用是否方便？

#### 2.4 控件动画

> 是否支持控件动画？支持那些控件动画？是否支持自定义的控件动画？控件动画使用是否方便？控件动画的参数有哪些？是否可以停止、暂停和播放控件动画。

#### 2.5 内置控件是否丰富

> 是否有你目前需要的控件和将来可能用到的控件。

#### 2.6 控件组合是否方便

> 有的 GUI 把控件分成叶子节点控件和容器控件，label、image、edit 和 button 都是叶子节点控件。这样做灵活性很差，往 button 放个图片或者动画，往 label 里放个图片，往 edit 里放一个"清除"/"查找"的 button，不是方便的事吗，为什么要限制呢？

#### 2.7 是否支持自定义控件

> 没有一个 GUI 能够满足所有的需求，如果不支持自定义控件就悲催了。这样一个简单的需要，在有的 GUI 里却需要修改 GUI 引擎的代码，那就不好玩了。

#### 2.8 布局 (layout) 参数是否强大

> 通过布局参数控制控件布局，可以让应用程序适用于不同大小的屏幕。是否支持布局参数，布局功能是否强大，是否可以扩展自定义布局。

#### 2.9 控件是否自定义属性

#### 2.10 控件：label

#### 2.11 控件：label

#### 2.12 控件：edit

#### 2.13 控件：button

#### 2.14 控件：软键盘

#### 2.15 控件：table view

## 3. 性能

#### 3.1 是否支持高效的算法

> 是否支持脏矩形算法、3 framebuffer 和 二进制格式。开发时使用 XML 方便程序员修改，运行时使用高效二进制格式提高运行效率。

#### 3.2 是否支持 2D 硬件加速
> 是否支持常见的加速接口，如 STM32 的 DMA2D 和 NXP 的 PXP。厂家是可以扩展自己的加速接口。

#### 3.3 是否支持 3D 硬件加速

> 是否支持 OpenGL、DirectX、Vulkan 和 Metal 等。

#### 3.4 是否支持低端平台

## 4. 国际化

#### 4.1 是否支持 Unicode。
#### 4.2 是否支持输入法。
#### 4.3 是否支持字符串翻译。
#### 4.4 是否支持图片翻译。
#### 4.5 是否文字双向排版。
#### 4.6 是否提供了编码转换函数。

## 5 软件质量

#### 5.1 是否有完整的单元测

#### 5.2 是否有内存耗尽处理流程

#### 5.3 是否内存检查泄露检查机制

#### 5.4 是否进行了全面的静态检查。

#### 5.5 是否提供事件录制和重放功能进行压力测试。

#### 5.6 是否提供 Appuim 进行自动测试
