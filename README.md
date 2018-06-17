Hexi
====

** Hexi **是制作HTML5游戏或任何其他游戏的有趣和简单的方法
使用纯JavaScript代码的亲切互动媒体。看一眼
该功能列表和 [examples](https://github.com/kittykatattack/hexi/tree/master/examples) 文件夹即可开始使用。继续向下滑，
你会发现一个完整的快速入门指南和新手教程。如果你以前从未做过游戏，那么教程是最好的开始。

Hexi有什么好处？您将获得WebGL渲染的所有功能
一个简化的API，可以让你编写你的代码
[minimalist](https://en.wikipedia.org/wiki/Haiku),
[declarative](http://latentflip.com/imperative-vs-declarative/) 的方式。
它使得编写游戏与编写诗歌或绘画一样简单而有趣。尝试一下！如果你
需要任何帮助或有任何问题，请在此发布一些内容
存储库的[Issues](https://github.com/kittykatattack/hexi/issues)。
问题页面是Hexi友好的聊天室 - 不要害怕
请求帮忙 ：） 

您只需从此存储库中获取一个文件即可开始使用Hexi：
[`hexi.min.js`](https://github.com/kittykatattack/hexi/blob/master/bin/hexi.min.js)。就这样！[Link it to your HTML document with a `<script>` tag](http://www.quackit.com/javascript/tutorial/external_javascript_file.cfm)，然后去做！
Hexi从头开始写了最新版本
JavaScript（ES6 / 7,20015/6），但编译到ES5（使用[Babel](https://babeljs.io)），以便它可以在任何地方运行。在开始使用Hexi之前，你需要知道什么？您应该对HTML和JavaScript有合理的理解。你不必成为专家，只是一个渴望学习的雄心勃勃的初学者。如果您不了解HTML和JavaScript，那么开始学习它的最佳地点就是这本书：

[Foundation Game Design with HTML5 and JavaScript](http://www.apress.com/9781430247166)

我知道这是最好的书，因为我写了它！

好的，我知道了？你知道JavaScript变量，函数，数组和对象是什么以及如何使用它们吗？你知道 [JSON data files](http://www.copterlabs.com/blog/json-what-it-is-how-it-works-how-to-use-it/)是什么吗？你使用过[Canvas Drawing API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Drawing_graphics_with_canvas)吗？然后你就可以开始使用Hexi了！  

当然，Hexi完全可以自由使用：为了任何事情，永远！它是在加拿大（多伦多，汉密尔顿），印度（克卢谷，拉达克），尼泊尔（加德满都，博克拉，安纳普尔纳大本营），泰国（帕岸岛，高涛）和南非（开普敦）写成的，结果是对游戏设计的API可用性进行了15年的研究。“Hexi”这个名字来自 ["Hex"](https://en.wiktionary.org/wiki/hex) + ["Pixi"](https://github.com/pixijs/pixi.js/) = "Hexi". [It has absolutely no other meaning](https://www.youtube.com/watch?v=XYGmNs6274A)。

### 目录:
1. [特点](#特点)
2. [模块](#模块)
3. [快速启动](#快速启动)
    1. [页面容器](#页面容器)
    2. [代码结构](#代码结构)
    3. [设置启动](#设置启动)
    4. [加载函数](#加载函数)
    5. [设置函数](#设置函数)
    6. [运行函数](#运行函数)
    7. [更进一步](#更进一步)
4. [教程](#教程)
    1. [宝藏猎人](#宝藏猎人)
        1. [容器页面](#容器页面)
        2. [初始化](#初始化)
        3. [定义全局变量](#定义全局变量)
        4. [设置游戏](#设置游戏)
            1. [自定义画布](#自定义画布)
            2. [创建声音对象](#创建声音对象)
            3. [制作游戏场景](#制作游戏场景)
            4. [制作精灵](#制作精灵)
            5. [定位精灵](#定位精灵)
            6. [分配动态属性](#分配动态属性)
            7. [创造敌人精灵](#创造敌人精灵)
            8. [生命栏](#生命栏)
            9. [游戏结束](#游戏结束)
            10. [按键交互](#按键交互)
            11. [游戏状态](#游戏状态)
        5. [游戏循环的逻辑](#游戏循环的逻辑)
            1. [移动玩家精灵](#移动玩家精灵)
            2. [控制精灵](#控制精灵)
            3. [检测碰撞](#检测碰撞)
                1. [与宝藏碰撞](#与宝藏碰撞)
            4. [结束游戏](#结束游戏)
        6. [使用图像](#使用图像)
            1. [单个图像](#单个图像)
                1. [加载图像文件](#加载图像文件)
                2. [用图像制作精灵](#用图像制作精灵)
                3. [微调收容区域](#微调收容区域)
        7. [使用纹理图集](#使用纹理图集)
            1. [准备图像](#准备图像)
            2. [加载纹理图集](#加载纹理图集)
    2. [外星舰队](#外星舰队)
        1. [加载并使用自定义字体](#加载并使用自定义字体)
        2. [在浏览器中缩放游戏中心](#在浏览器中缩放游戏中心)
        3. [加载进度条](#加载进度条)
        4. [射击子弹](#射击子弹)
        5. [精灵状态](#精灵状态)
        6. [随机产生外星人](#随机产生外星人)
            1. [外星人定时器](#外星人定时器)
            2. [随机开始位置](#随机开始位置)
        7. [移动外星人](#移动外星人)
        8. [让外星人爆炸](#让外星人爆炸)
        9. [显示分数](#显示分数)
        10. [结束并重置游戏](#结束并重置游戏)
    3. [飞扬的仙女!](#飞扬的仙女)
        1. [制作按钮](#作)
        2. [让仙女飞翔](#让仙女飞翔)
        3. [制作滚动背景](#制作滚动背景)
        4. [仙女爆炸](#仙女爆炸)
        5. [使用粒子发射器](#使用粒子发射器)
        6. [创建和移动支柱](#创建和移动支柱)
5. [集成HTML、CSS](#集成HTML、CSS)
6. [实例指南](#实例指南)

特点
--------

这里是Hexi的核心功能列表：

- 你需要的所有最重要的精灵：矩形，圆圈，线条，文字，图像精灵和动画“MovieClip”风格的精灵。
  你可以用一行代码来制作任何这些精灵。您也可以创建自己的自定义精灵类型。
- 一个完整的场景图，包含嵌套的子父级层次结构（包括一个`stage`和`addChild`/`removeChild`方法），
  本地和全局坐标，深度图层和旋转枢轴。
- `group` 精灵一起制作游戏场景。 
- 具有用户可定义的`fps` 并可完全自定义的游戏循环简单的游戏状态管理器。 
  `pause`和`resume` 游戏随时循环。
- Tileset (spritesheet)支持使用`frame`和`filmstrip`方法制作精灵使用瓷砖框架。
- 为流行的纹理打包机内置纹理地图集支持格式。 
- 精灵的关键帧动画和状态管理器。使用`show`来显示精灵的图像状态。
  使用`playAnimation`来玩一系列的帧（如果你想要的话，在一个“循环”中）。
  使用`show`显示一个特定的帧号。用'fps`来设置精灵动画的帧速率与游戏无关帧率。
- 互动的`button` 精灵具有`up`，`over` 和`down`的状态。
- 任何精灵都可以设置为 `interact`来接收鼠标和触摸动作。
  直观的`press`, `release`, `over`, `out`和`tap`按钮和交互式的方法精灵。
- 易于使用的键盘键绑定。用键盘轻松定义你自己的方法。
- 内置的通用`pointer`，可与鼠标和键盘一起使用触摸。
  分配您自己的自定义`press`, `release` 和 `tap`方法或者使用指针的任何内置属性：`isUp`, `isDown`，`tapped`, `x` 和 `y`。
  根据需要为多点触控定义多个指针。（它也适用于等轴测图！）
- 方便地定位精灵相对于其他精灵使用`putTop`, `putRight`, `putBottom`, `putLeft` 和 `putCenter`。
  对齐使用`flowRight`, `flowLeft`,`flowUp` 或 `flowDown`。
- 一个通用资产加载器，用于预加载图像，字体，声音和JSON数据文件。
  支持所有流行的文件格式。您可以随时将新资产加载到游戏中。
- 可选的“加载”状态，可让您在资产处于运行状态时执行操作
  加载。你可以使用`load`状态来添加一个加载进度条。
- 一个快速和专注 [Pixi-based](https://github.com/pixijs/pixi.js/)渲染引擎。
  如果Pix溪能做到的，Hexi也是如此！HEXI只是位于Pixi之上的一小部分代码。
  你可以访问全局`PIXI`对象随时可以直接编写纯Pixi代码至。
  HEXI包括最新稳定版Pixi v3.0自动捆绑为您服务。
- 一个复杂的游戏循环，使用带变量渲染的固定时间步长和sprite插值。
  这意味着你会得到黄油平滑的动画以任何帧率。
- 一个紧凑而强大的"Haiku"风格的API，可组合组件。获得更多完成更少的代码。
- 使用内置的WebAudio API声音管理器导入和播放声音。
  用`play`，`pause`，`stop`，`restart`，`playFrom`，`fadeIn`和`fadeOut`方法。
  改变声音的 `volume` 和 `pan`。
- 使用纯代码生成您自己的自定义音效多功能的`soundEffect`方法。
- 用`shake`摇动精灵或屏幕。
- 用于精灵和场景转换的补间函数：`slide`,`fadeIn`, `fadeOut`, `pulse`, `breathe`, `wobble`, `strobe`
  和一些有用的低级补间方法可帮助您创建自己的补间自定义补间。
- 制作一个精灵，连接一系列的`walkPath` 和 `walkCurve`的路点。 
- 一些有用的便利功能：
  `followEase`,`followConstant`,`angle`, `distance`, `rotateAroundSprite`, `rotateAroundPoint`, `wait`,
  `randomInt`, `randomFloat`, `contain` , `outsideBounds`。
- 一种处理碰撞测试和处理的快速通用 `hit` 方法所有类型的精灵的反应（阻塞和反弹）。
  使用一种碰撞方法一切：矩形，圆形，点和精灵数组。简单！
- 一套轻量级，低级2D几何碰撞方法的配套套件。
- 游戏资源的加载进度条。
- 让精灵用`shoot`射击东西。 
- 通过`grid`轻松地绘制网格图形中的精灵。
- 使用`tilingSprite`轻松创建无缝滚动背景。
- 创建各种粒子的`createParticles`函数游戏效果。使用`particleEmitter`函数来创建一个常量粒子流。
- 使用`scaleToWindow`使游戏自动缩放到最大尺寸，并使其自身在浏览器窗口内保持最佳状态。 
- 使用`makeTiledWorld`支持拼贴编辑器。
  设计你的游戏平铺编辑器并直接访问所有精灵，图层和对象在你的游戏代码中。
  这是一个非常有趣，快速和简单的方法游戏。
- 处理所有碰撞的多功能`hitTestTile`方法检查你需要基于瓦片的游戏。
  你可以结合使用它与任何2D几何碰撞方法进行优化宽相/窄相碰撞检查，如果你想。
- 使用`updateMap`来保持基于瓦片的世界地图数据数组处于最新状态与移动的精灵。
- 创建一个`worldCamera`，跟随精灵围绕滚动游戏世界。
- 一个`lineOfSight`函数，告诉你一个精灵对另一个精灵是否可见。
- 与HTML和CSS元素无缝集成以创建丰富的内容用户界面。使用Hexi还可以使用 Angular, React , Elm!
- 一整套用于轻松创建等距游戏世界的工具，包括：等距鼠标/触摸指针，使用`hitTestIsoTile`的等角拼贴碰撞以及使用`makeIsoTiledWorld`完整的Tiled Editor等轴测图支持。
- 一个`shortestPath`函数，用于通过基于瓦片的环境（如迷宫和`tileBasedLineOfSight`）执行A-Star寻路，以告诉您迷宫游戏环境中的精灵是否可以互相看到。
- 是的，由于Pixi渲染器提供的[`accessible`](http://www.goodboydigital.com/pixi-becomes-accessible/) 属性（yay Pixi！），Hexi应用程序符合W3C可访问性准则。


模块
--------

Hexi包含了一些有用的模块，你可以使用其中的任何一个
这些模块的属性或方法在您的Hexi高级代码中。

-  [Pixi](https://github.com/pixijs/pixi.js/): 世界上最快的2D WebGL和画布渲染器。
-  [Bump](https://github.com/kittykatattack/bump): 一套完整的2D游戏碰撞函数。
-  [Tink](https://github.com/kittykatattack/tink): 拖放，按钮，通用指针和其他有用的交互工具。
-  [Charm](https://github.com/kittykatattack/charm): 简单易用的Pixi sprite动画效果。
-  [Dust](https://github.com/kittykatattack/dust): 用于创建爆炸，火灾等粒子效果和魔法。
-  [Sprite Utilities](https://github.com/kittykatattack/spriteUtilities): 更简单，更直观的方法创建和使用Pixi sprites，
   以及添加一个状态机和动画播放器
-  [Game Utilities](https://github.com/kittykatattack/gameUtilities): 游戏有用方法的集合。
-  [Tile Utilities](https://github.com/kittykatattack/tileUtilities): 用[Tiled Editor](http://www.mapeditor.org)
   制作基于瓦片的游戏世界的有用方法集合。包括一整套等轴测图工具。
-  [Sound.js](https://github.com/kittykatattack/sound.js): 一个用于加载，控制和生成的微库声音和音乐效果。
   您需要为游戏添加声音的所有内容。
-  [Smoothie](https://github.com/kittykatattack/smoothie): 使用超平滑精灵动画真正的增量时间插值。
   它还可以让你指定在哪个帧的每秒帧数你的游戏或应用程序运行，并完全分离你的精灵渲染循环应用程序逻辑循环

阅读代码库中的文档以找出每个模块
你可以用他们做什么以及他们的工作方式。因为他们
所有内置到Hexi，你不必自己安装 - 他们
刚开箱即可使用。

Hexi让你访问大部分这些模块方法和属性
**顶级对象**。例如，如果你想访问`hit`方法
从撞击碰撞模块，你可以这样做：
```js
g.hit(spriteOne, spriteTwo);
```
但是，如果需要，也可以直接访问Bump模块，如下所示：
```js
g.bump.hit(spriteOne, spriteTwo);
```
（这个假设你的Hexi实例叫`g`）;

只需使用** lowerCamelCase **引用模块名称即可。
这意味着你可以以`smoothie` 和 Sprite Utilities 的形式访问Smoothie模块作为`spriteUtilities`。

这个约定有两个例外。你可以访问Pixi
全局对象直接作为`PIXI`。此外，Sound.js模块中的功能
也只能作为顶级全局对象访问。这已完成
简化这些模块与Hexi的整合方式
保持尽可能广泛的跨平台兼容性。

如果你是一名开发人员，并希望为Hexi做出贡献，那么最好
方式是为这些模块贡献新的和改进的功能。要么，
如果你真的有雄心，为Hexi提出一个新模块
开发团队（在这个回购的[Issues](https://github.com/kittykatattack/hexi/issues)中，也许我们会把它加到Hexi的核心！）


快速启动
--------

要快速开始与Hexi合作，请查看快速入门
项目在Hexi的例子
 [examples
folder](https://github.com/kittykatattack/hexi/tree/master/examples)。
你会在这里找到[HTML container page here](https://github.com/kittykatattack/hexi/blob/master/examples/01_quickStart.html)和 [JavaScript
source file here](https://github.com/kittykatattack/hexi/blob/master/examples/src/quickStart.js)。源代码已经完全评论并解释了所有的一切如何运作，如果你愿意，你可以直接跳到那个文件并通读它。（您会在 [in the `bin` folder](https://github.com/kittykatattack/hexi/tree/master/examples/bin)。）

快速启动项目是Hexi所有主要功能的参考，您可以将它用作制作自己的新Hexi应用程序的模板。点击下面的图片来尝试一个工作示例：

[![Quick start](/tutorials/screenshots/30.png)](https://cdn.gitcdn.xyz/cdn/kittykatattack/hexi/a1713aa19bdcc9a0c661e67d079a205d7c221917/examples/01_quickStart.html)

您将首先看到一个加载栏，显示文件的百分比
（声音和图像）被加载。然后你会看到一个旋转的信息，要求你点击屏幕创建猫。无论您在音乐播放时用鼠标点击指针，猫都会出现在屏幕上
的背景。（糟糕，对不起！我忘了提醒你音乐！）文本字段旋转并计算猫的数量
你已经创建。猫自己移动和反弹周围
屏幕，同时缩小尺寸并摆动它们的透明度。
以下是您将看到的内容的图示：

![Quick start illustration](/tutorials/screenshots/31.png)

为什么是猫？[Because](http://motherboard.vice.com/blog/toxo-terror-are-our-brains-controlled-by-cat-loving-parasites).

如果你知道这个快速入门应用程序是如何制作的，那么你就会很好以Hexi快速生产的方式 - 让我们找到！

（注意：如果你对游戏编程不熟悉，并觉得你需要一个温和的，更有条理的介绍Hexi，请查看[Tutorials](#tutorials) 部分。
你将学习如何从头开始制作3个完整的游戏，并且每个游戏都逐渐建立在前一个游戏中学到的技能上。）


### 页面容器

你需要开始使用Hexi的唯一文件是
[`hexi.min.js`](https://github.com/kittykatattack/hexi/blob/master/bin/hexi.min.js)
它有一个令人难以置信的简单"installation"：只需用一个`<script>`标签将其链接到一个HTML页面。
然后链接您的主要JavaScript文件，其中将包含您的游戏或应用程序代码。以下是典型的HexiHTML容器页面的样子：
```html
<!doctype html>
<meta charset="utf-8">
<title>Hexi</title>
<body>
<script src="hexi.min.js"></script>
<script src="main.js"></script>
</body>
```
当然，您可以加载所需的外部脚本文件
为你的游戏。

如果你需要更精细的控制，你可以选择加载
Hexi使用三个单独的文件：Pixi渲染器，Hexi的模块和Hexi的`core.js`文件。 
```html
<!doctype html>
<meta charset="utf-8">
<title>Hexi</title>
<body>

<!-- Pixi renderer, Hexi's modules, and Hexi's core  -->
<script src="pixi.js"></script>
<script src="modules.js"></script>
<script src="core.js"></script>

<!-- Main application file -->
<script src="bin/quickStart.js"></script>
</body>
```
这样做的好处是它可以让你换掉Hexi的
内部版本的Pixi，以及您自己定制的Pixi，或者
您想要使用的特定版本的Pixi。或者，也许你做了一些
对你想要试用的Hexi模块进行其他疯狂的修改。但通常情况下，您可能永远不需要这样做。

### 代码结构

所有的乐趣都发生在您的主JavaScript文件中。Hexi
应用程序有一个非常简单但灵活的架构，您可以
缩放到任何你需要的尺寸。有几百行代码的小游戏或有几百个文件的大型游戏 - Hexi可以做到！
以下是典型Hexi应用的结构：

1.启动Hexi。
2.`load` 函数，将在文件加载时运行。
3.`setup` 函数初始化你的游戏对象，变量和精灵。
4.`play` 函数，这是您的游戏或应用程序逻辑，循环运行。

以下是实际代码中的实际情况：



```js
//1.建立和启动Hexi

//你想加载的文件数组
let thingsToLoad = ["anyFiles", "youWant", "toLoad"];

//初始化并启动Hexi
let g = hexi(canvasWidth, canvasHeight, setup, thingsToLoad, load);
g.start();

//2.加载文件时将运行的`load`函数

function load(){
  
  //显示一个可选的加载条
  g.loadingBar();
}

//3.`setup`函数初始化你的游戏对象，变量和精灵

function setup() {

  //在这里创建你的游戏对象

  //将游戏状态设置为“play”来启动游戏循环
  g.state = play;
}

//4. `play`功能，这是您的游戏或应用程序逻辑运行在一个循环中

function play(){
  //这是你的游戏循环，你可以移动精灵并添加你的游戏
  //游戏逻辑
}
```

这个简单的模型是您创建任何类型的游戏或应用程序所需的全部。
您可以将其用作您自己的项目的起始模板，这也是一样
基本模型可以缩放到任何尺寸。

我们来看看这个架构模型是如何用来构建Quick的
开始申请。


### 设置启动

首先，创建一个列出您想要加载的所有文件的数组。快速
启动项目加载图像文件，字体文件和音乐文件。
```js
let thingsToLoad = [
  "images/cat.png",
  "fonts/puzzler.otf",
  "sounds/music.wav"
];
```
如果您没有任何要加载的文件，请跳过此步骤。

接下来，用Hexi函数初始化Hexi。以下是如何初始化a
全新的Hexi应用程序，屏幕尺寸为512x512像素。它说
Hexi将文件加载到`thingsToLoad`数组中，同时运行一个名为`load`的函数
它的加载，然后在一切准备就绪时运行一个名为`setup`的函数。
```js
let g = hexi(512, 512, setup, thingsToLoad, load);
```
你现在可以通过一个来访问你的应用程序中的Hexi实例
叫'g`的对象（虽然，你可以给这个任何你喜欢的名字
比如使用“g”，因为它代表“游戏”，并且键入的很短。）

`hexi`函数有5个参数，但只有前3个是必需的。

1. 画布宽度。
2. 画布高度。 
3. `setup`函数。
4. 上面定义的`thingsToLoad`数组。这是可选的。
5. `load` 函数。这也是可选的。

如果你跳过最后两个参数，Hexi将跳过加载过程并直接跳到`setup`函数。

（可选）设置游戏逻辑循环应运行的帧数。
（精灵将独立渲染，插值，全速60 fps）
如果你不设置fps，Hexi的默认值是60。
```js
g.fps = 30;
```
设置一个低于60的fps会给你带来更多的性能开销
与，和你的游戏仍然看起来不错。

您还可以选择添加边框并设置背景颜色。
```js
g.border = "2px red dashed";
g.backgroundColor = 0x000000;
```
而且，如果您想缩放游戏屏幕并将其与最大浏览器对齐
窗口大小，你可以使用`scaleToWindow`方法。
```js
g.scaleToWindow();
```
最后，调用`start`方法让Hexi运行
```js
g.start();
```
这个很重要！没有调用Hexi不会启动的方法
开始！

### 加载函数

如果您在初始化时为Hexi提供了一个名为`load`的函数，则可以显示加载栏并加载进度信息。只需创建一个名为`load`的函数，如下所示：
```js
function load(){

  //显示当前正在加载的文件
  console.log(`loading: ${g.loadingFile}`); 

  //显示当前加载的文件的百分比
  console.log(`progress: ${g.loadingProgress}`);

  //添加一个可选的加载栏 
  g.loadingBar();
}
```

### 设置启动

现在你已经启动了Hexi并加载了所有的文件，你就可以开始了
制作东西！这发生在`setup`函数中。如果你有任何
对象或变量，你想跨越多个使用
函数，在`setup`函数之外定义它们，如下所示：
```js
//这些将被用在多个函数中
let cats, message;

//使用`setup`函数来创建事物
function setup(){

  //...在这里创造东西！...
}
```
我们来看看`setup`函数中的代码是如何工作的。本来打算
要做猫 - 很多猫！ - 所以创建一个名为“group”的组件非常有用
`cats`把它们放在一起。
```js
cats = g.group();
```
在快速启动项目中，您可以点击按钮来制作新的猫
用鼠标（或触摸）屏幕。因此，我们需要一个功能
为我们生产新的猫**精灵**。（Sprites是交互式图形，您可以在屏幕上进行动画和移动。）Hexi可以使用`sprite`方法创建一个新的精灵。只需提供您想用于精灵的文件名称的“精灵”。使用addChild方法，每个新创建的猫小精灵都应该定位并添加到cats组中。我们还希望猫可以使用“呼吸”方法使其缩放比例动画化，并使用“脉冲”方法使其透明度动画化。一个名为`makeCats`的函数完成了这一切。`makeCats`有两个参数：x和y
您希望猫出现的位置，相对于屏幕的左上角。
```js
let makeCat = (x, y) => {

  //创建猫精灵。提供`sprite`方法
  //应该显示的加载图像的名称
  let cat = g.sprite("images/cat.png");

  //设置'cat'的位置
  cat.setPosition(x, y);

  //你也可以设置位置来修改精灵的`x`和
  //````属性直接，就像这样
  //cat.x = x;
  //cat.y = y;

  //从Hexi的中添加一些可选的补间动画效果 
  //内置的补间库（称为Charm）。“呼吸”使
  //精灵缩放进出。`脉冲`振荡它的透明度
  g.breathe(cat, 2, 2, 20);
  g.pulse(cat, 10, 0.5);

  //将猫的速度设置为-10到10之间的随机数
  cat.vx = g.randomInt(-10, 10);
  cat.vy = g.randomInt(-10, 10);

  //将猫添加到`cats`组
  cats.addChild(cat);
};

```

（您可以了解更多关于“呼吸”和“脉搏”方法的工作方式
在 [tweening example](https://github.com/kittykatattack/hexi/blob/master/examples/src/tweening.js)中的
[examples folder](https://github.com/kittykatattack/hexi/tree/master/examples).)

我们还需要创建一个“文字”精灵，以显示“点击搜索”
猫！“我们可以用Hexi的”文字“方法来做到这一点。
```js
message = g.text("Tap for cats!", "38px puzzler", "red");
```
`text`方法的参数是你想要显示的文本，
字体大小和家族以及颜色（您可以使用任何HTML / CSS颜色
字符串值，RGBA或HSLA值）。

使用Hexi的`putCenter`方法将文本置于`stage`中。
```js
g.stage.putCenter(message);
```
'舞台'是什么？这是所有Hexi精灵的根源容器
属于他们第一次创建时。 

您还可以使用`putLeft`，`putRight`，`putTop`或`putBottom`方法来帮助您将对象相对于其他对象对齐。这些方法的可选第二个和第三个参数定义了x和y偏移量，这可以帮助您微调定位。

因为我们希望短信围绕其中心点旋转
必须将其`pivotX`和`pivotY`值设置为0.5。
```js
message.pivotX = 0.5;
message.pivotY = 0.5;
```
0.5意味着“精灵的中心”。

您也可以使用此替代语法来设置枢轴点：
```js
message.setPivot(0.5, 0.5);
```
我们需要某种方式告诉Hexi每当屏幕时都要创造一只新的猫
被点击或点击。我们还希望短信告诉我们屏幕上有多少只猫。Hexi有一个内置`tap`方法的`pointer`对象，我们可以编程来帮助我们做到这一点。

```js
g.pointer.tap = () => {
  
  //用指针的`x`和`y`坐标提供`makeCat`。
  makeCat(g.pointer.x, g.pointer.y);

  //使`message.content`显示cats 的数量 
  message.content = `${cats.children.length}`;
};
```

我们还希望我们加载的音乐文件开始播放。我们可以
用Hexi的`sound`方法访问音乐声音对象。使用声音对象的“循环”
方法使其不断循环，并使用`play`来立即开始播放。
```js
let music = g.sound("sounds/music.wav");
music.loop = true;
music.play();
```
我们现在完成了一切设置！这意味着我们完成了
我们的应用程序的`setup`状态，现在可以将状态转换为`play`。以下是如何做到这一点：
```js
g.state = play;
```
`play`状态是一个将在循环中运行的函数，并且是在哪里
我们所有的应用逻辑是。让我们来看看接下来的工作。


### 运行函数

你在Hexi应用程序中需要的最后一件事是`play`函数。
```js
function play() {

  //所有这些代码都会在循环中运行
}
```

在任何fps下，连续循环都会调用`play`函数（每秒帧数）值。
这是你的**游戏逻辑循环**。（该渲染循环将由Hexi在最高fps的背景下运行你的系统可以处理。）
你可以随时暂停Hexi的游戏循环用`pause`方法，并用`resume`方法重新启动它。
（请查看 [Flappy Fairy](https://github.com/kittykatattack/hexi/blob/master/tutorials/src/flappyFairy.js) 项目，了解 `pause` 和
`resume`可用于管理具有复杂状态的应用程序。）

快速启动项目的 `play` 函数只是做两件事：
它使文本旋转，并移动和反弹周围的猫屏幕。
这是完成这一切的 `play` 函数。
```js
function play() {
  
  //旋转文字 
  message.rotation += 0.1;

  //循环所有的猫，让它们移动并反弹掉
  //舞台的边缘
  cats.children.forEach(cat => {

    //让cat从屏幕边缘反弹
    let collision = g.contain(cat, g.stage, true);

    //移动cat
    g.move(cat);
  });
}
```

就这样！与我们放入`setup`函数的所有工作相比，
“play”功能几乎没有任何作用！但它是如何工作的？

它首先通过更新文本来围绕其中心旋转文本
`message` 文本sprite的`rotation`属性为0.1弧度。
```js
message.rotation += 0.1;
```
由于此新旋转值正在应用于连续循环内的旧旋转值，因此它会逐渐增加该值并使文本旋转。

代码的下一件事是循环遍历所有的精灵`cat` 组的 `children`数组。
```js
cats.children.forEach(cat => {
  //遍历`chidren`数组中的每个`cat`精灵
});

```
所有的Hexi组织都有一个名为“儿童”的阵列
告诉你它们包含哪些精灵。每当你将一个精灵添加到一个
组使用`addChild`方法，将精灵添加到组中
`孩子`阵列。Hexi的根容器，称为“舞台”，也有
一个包含你所有精灵和组的子元素数组
Hexi申请。即使`sprite`对象有一个`children`数组，并且
这意味着你可以使用`addChild`来将精灵与其他精灵分组
创建复杂的游戏对象。

当代码循环通过每只猫时，它首先检查是否猫
正在触摸屏幕的边缘，如果是，它会将其弹开
在相反的方向。Hexi的“含有”方法可以帮助我们做到这一点。
```js
let collision = g.contain(cat, g.stage, true);
```
将第三个参数设置为“true”是导致猫反弹的原因。

猫在“移动”方法的帮助下在屏幕上移动。
```js
g.move(cat);
```
`move`方法通过`vx`和`vy`速度值更新精灵的位置。（所有Hexi精灵都有`vx`和`vy`值，初始化为零）。您可以一次移动多个精灵，方法是向精灵列表中的“精灵”移动，并用逗号分隔。你甚至可以提供一个包含你想要移动的所有精灵的数组。下面是`move`实际上在做的事情：
```js
cat.x += cat.vx;
cat.y += cat.vy;
```
这就是它的全部！这是您了解快速启动应用程序的所有信息，以及几乎所有您需要了解的有关Hexi的信息！

### 更进一步

有了这个基本的Hexi建筑，你可以创建任何东西。只需将Hexi的`state`属性设置为任何其他函数即可切换应用程序的行为。就是这样：
```js
g.state = anyStateFunction;
```
各国只是简单的旧JavaScript功能！
好而简单！

根据需要写入尽可能多的状态函数。如果它是一个小项目，您可以将所有这些功能保存在一个文件中。但是，对于一个大项目来说，根据需要从外部JS文件加载你的函数。使用你喜欢的任何模块系统，比如ES6模块，CommonJS，AMD或者好的旧的HTML标签。这个简单的架构模型可以扩展到任意大小，并且是您需要知道的唯一架构模型。保持简单并保持快乐！

现在您已对Hexi的工作方式有了一个全面的了解，请仔细阅读
教程深入细节。

教程
---------

我们将要做的第一个游戏是一个简单的对象集合
敌方躲避游戏称为宝藏猎人。打开文件
在网页浏览器中使用`01_treasureHunter.html`。（你会发现它在Hexi的
`tutorials`文件夹，你需要在a中运行它
[webserver](https://github.com/nodeapps/http-server)）。如果你不这样做
想打扰建立一个网络服务器，使用文本编辑器
[Brackets](http://brackets.io) ，将为您启动一个
自动生成（请参阅此功能的支架文档）。

[![Treasure Hunter](/tutorials/screenshots/01.png)](https://gitcdn.xyz/repo/kittykatattack/hexi/master/tutorials/01_treasureHunter.html)

（按照上图中的链接玩游戏。）使用键盘移动资源管理器（蓝色方块），收集
宝藏（黄色方块），避开怪物（红色方块）和
到达出口（绿色广场）。是的，你必须使用你的
想象力 - 现在。 

### 宝藏猎人
以下是完整的JavaScript源代码：

[!Treasure Hunter Source](https://github.com/kittykatattack/hexi/blob/master/tutorials/src/treasureHunter.js)

不要被它显而易见的简单性所愚弄。宝藏猎人包含
视频游戏需要的一切：

- 交互性
- 碰撞
- 精灵
- 一个游戏循环
- 场景
- 游戏逻辑
- "Juice"（以声音的形式）

[Watch this video](https://www.youtube.com/watch?v=Fy0aCDmgnxg) 
[read this article](http://www.gamasutra.com/view/feature/130848/how_to_prototype_a_game_in_under_7_.php?print=1) 
学习关于这个基本的游戏设计成分。

如果你可以制作一个像宝藏猎人这样的简单游戏，你可以制作
几乎任何其他类型的游戏。对真的！从宝藏中获得
猎人到天际或者塞尔达
只是一小步的问题; 增加更多
细节随你去。你想添加多少细节取决于你。

在本教程的第一阶段中，您将学习基本知识
宝藏猎人游戏制作完成后，我们将添加一些有趣的功能，如图像和
角色动画，会给你一个完整的概述如何
Hexi的作品。 

如果你是一位经验丰富的游戏程序员和
快速自启动器，你可以在 [Hexi's `examples` folder](https://github.com/kittykatattack/hexi/tree/master/examples)
中找到代码成为一个更有效率的地方开始学习 - 检查出来。
充分评论`examples`文件夹中的代码还详细介绍了特定的和高级的用法的功能，不是在这些教程中涵盖。
当你完成这些工作教程，`例子`将带你进入你的下一个阶段旅程。

#### 容器页面

在您开始使用JavaScript进行编程之前，您需要设置一个
最小的HTML容器页面。HTML页面加载`hexi.min.js`哪个
是您需要使用Hexi全部文件的唯一文件
特征。它还加载了`treasureHunter.js`文件，这是
包含所有游戏代码的JavaScript文件。 
```js
<!doctype html>
<meta charset="utf-8">
<title>Treasure hunter</title>
<body>
<!-- Hexi -->
<script src="../bin/hexi.min.js"></script>

<!-- Main application file -->
<script src="bin/treasureHunter.js"></script>
</body>
```
[minimum amount of HTML code you need for a valid HTML5document](http://stackoverflow.com/questions/9797046/whats-a-valid-html5-document).

取决于您的系统，文件路径可能与您的系统不同
你已经建立了你的项目文件结构。

#### 初始化

下一步是编写一些初始化和启动Hexi的JavaScript代码 
根据你指定的一些参数。这一点
下面的代码初始化一个屏幕尺寸为512 x 512像素的游戏。
它还预加载了`sounds`中的`chimes.wav`声音文件
夹。
```js
//初始化Hexi并加载chimes声音文件
let g = hexi(512, 512, setup, ["sounds/chimes.wav"]);

//将游戏画布缩放到浏览器中的最大尺寸
g.scaleToWindow();

//启动Hexi
g.start();

```
你可以看到`hexi`函数的结果被分配给了
一个名为`g`的变量。 
```js
let g = hexi(//...
```
现在，只要你想使用Hexi的习俗
方法或对象在你的游戏中，只需要用`g`作为前缀。（你没有
必须用`g`来表示游戏引擎，你可以使用任何变量
你想要的名字。`g`只是很好，简短而且易于记忆; `g` =
“游戏”。）

在这个例子中，Hexi创建了一个大小为512×512的画布元素
像素。这由前两个参数指定：
```js 
512, 512, setup,
```
第三个参数`setup`意味着只要Hexi初始化，
它应该在你的游戏代码`setup`中寻找并运行一个函数。
无论代码在`setup`函数中完全取决于你，并且
你很快就会看到你如何使用它来初始化一个游戏。（你没有
必须调用这个函数`setup`，你可以使用任何你喜欢的名字。） 

Hexi让你预先加载游戏资产，可选的第四个参数
是一个文件名的数组。在第一个例子中，你只需要预载一个文件：`chimes.wav`
你可以看到`chimes.wav`的完整文件路径被列为a
字符串中
初始化数组：
```js
["sounds/chimes.wav"]

```
你可以在这里列出尽可能多的游戏资源，包括图像，
字体和JSON文件。Hexi以前会为你装载所有这些资产
运行任何游戏代码。

Hexi只是实现了[Pixi的超级资源加载器]（https://github.com/englercj/resource-loader）
下引擎罩。您可以通过Hexi的`loader`直接访问装载机
属性，您可以通过`resources`属性访问资源。或者，如果你想直接使用`PIXI.loader`。您可以
了解更多关于[Pixi的加载器如何在这里工作]（https://github.com/kittykatattack/learningPixi#loading）。

我们希望游戏画布可以缩放到
浏览器窗口的最大尺寸，使其显示为很大
尽可能。我们可以使用一个名为`scaleToWindow`的有用方法来完成
这对我们来说。
```js
g.scaleToWindow();
```
`scaleToWindow`会将你的游戏集中到最合适的位置。长，宽
游戏画面垂直居中。高或方形屏幕
水平居中。如果你想指定你自己的浏览器
背景颜色与游戏边界相接，以“scaleToWindow”的形式提供
参数，如下所示：
```
g.scaleToWindow("seaGreen");
```
你需要做的最后一件事就是打电话给Hexi的“开始”方法。 
```js
g.start();
```
这是启动Hexi发动机的开关。

#### 定义全局变量

Hexi开始后，申报你的比赛的所有变数
函数将需要使用。
```js
let dungeon, player, treasure, enemies, chimes, exit,
    healthBar, message, gameScene, gameOverScene;
```
因为它们没有包含在函数中，所以这些变量是“全局的” 
因为您可以在所有游戏功能中使用它们。
（他们不一定是“全球”，因为他们居住在这个意义上
全局JavaScript名称空间。如果你想确保他们不是，[全部包装
你的JavaScript代码放在**即时函数**中以隔离它
来自全球
空间（http://stackoverflow.com/questions/17058606/why-using-self-executing-function-in-javascript）。或者，如果你想
做它的花哨的方式，使用JavaScript ES6 / 2015 [模块]（http://exploringjs.com/es6/ch_modules.html）或[类]（https://developer.mozilla.org/en/docs/Web/ JavaScript / Reference / Classes）来执行本地范围。


#### 设置游戏

Hexi一开始，它就会在你的游戏中寻找并运行一个功能
称为`setup`的代码（或者其他想要给它的名字
函数。）`setup`函数只运行一次，并允许您执行
一次性为您的游戏设置任务。这是创建和初始化的好地方
对象，创建精灵，游戏场景，填充数据数组或解析
加载JSON游戏数据。 

以下是宝藏猎人中“安装”功能的缩略鸟瞰图，
和它执行的任务。
```js
function setup() {
  //创建`chimes`声音对象
  //创建`gameScene`组
  //创建`出口`门精灵
  //创建`player`精灵
  //创建宝藏精灵
  //制造敌人
  //创建健康栏
  //通过消息为游戏添加一些文本
  //创建一个`gameOverScene`组 
  //分配播放器的键盘控制器

  //将游戏状态设置为“play”
  g.state = play;
}
```

最后一行代码`g.state = play`可能是最重要的
因为它启动了“播放”功能。“play”功能运行所有的游戏逻辑
在一个循环中。但是在我们研究这些工作方式之前，让我们先看看它是什么
`setup`函数中的特定代码会执行。

##### 创建声音对象

你会记得从上面的代码中我们预先加载了一个声音文件
进入名为`chimes.wav`的游戏。在您可以在游戏中使用它之前，
你必须使用Hexi的`sound`方法来参考它，
喜欢这个：
```js
chimes = g.sound("sounds/chimes.wav");
```
##### 创建游戏场景

Hexi有一个叫做`group`的有用方法，可以让你分组游戏对象
在一起，这样你就可以和他们一起工作。组用于
将特殊的对象叫做** sprites **（你会的
在下一节中学习所有的知识）。但它们也用于制作游戏场景。 

宝藏猎人使用两个游戏场景：`gameScene`这是主要游戏， 
和游戏结束时显示的`gameOverScene`。 
这是`gameScene`是如何使用`group`方法创建的：
```js
gameScene = g.group();
```
在创建组之后，您可以使用添加精灵（游戏对象）到`gameScene`
`addChild`方法。
```js    
gameScene.addChild(anySprite);
```
或者，您可以使用`add`方法一次添加多个精灵，如下所示：
```js
gameScene.add(spriteOne, spriteTwo, spriteThree);
```
或者，如果你愿意，你可以在完成所有游戏后创建游戏场景
精灵，并将所有精灵与一行代码一起分组，如下所示：
```js
gameScene = g.group(spriteOne, spriteTwp, spriteThree);
```
你会看到几个不同的例子，说明如何将精灵添加到组中
前面的例子。

但是，什么是精灵，你如何制造它们？

##### 制作精灵

精灵是任何游戏中最重要的元素。精灵是
只是您可以控制的图形（形状或图像）
特殊属性。你可以在游戏中看到的所有东西，比如
游戏人物，物体和背景，都是精灵。Hexi让你做
5种基本精灵：矩形，圆形，线条，文字和
`sprite`（一个基于图像的精灵）。你几乎可以制作任何2D动作游戏
与这些基本的精灵类型。（如果他们还不够，你也可以定义你自己的习惯
精灵类型）。这是宝藏猎人的第一个版本
只使用`矩形`精灵。你可以制作一个矩形精灵
这个：
```js
let box = g.rectangle(
  widthInPixels, 
  heightInPixels, 
  "fillColor", 
  "strokeColor", 
  lineWidth, 
  xPosition, 
  yPosition
);
```
你可以用Hexi的`circle`方法制作一个圆形的精灵：
```js
let ball = g.circle(
  diameterInPixels, 
  "fillColor", 
  "strokeColor", 
  lineWidth,
  xPosition, 
  yPosition 
);
```
仅使用“矩形”和“原型”来创建新游戏通常很有用
`圆圈`精灵，因为这可以帮助你专注于你的机制
游戏以纯粹的，元素的方式进行。这是第一个版本
寻宝猎人呢。这是来自`setup`函数的代码
创造出口，玩家和宝藏精灵。
```js
///出口门
exit = g.rectangle(48, 48, "green");
exit.x = 8;
exit.y = 8;
gameScene.addChild(exit);

//玩家精灵
player = g.rectangle(32, 32, "blue");
player.x = 68;
player.y = g.canvas.height / 2 - player.halfHeight;
gameScene.addChild(player);

//创建宝藏
treasure = g.rectangle(16, 16, "gold");

//将它放在画布左边的旁边
treasure.x = g.canvas.width - treasure.width - 10;
treasure.y = g.canvas.height / 2 - treasure.halfHeight;

//或者，您可以使用Ga内置的易用方法
//叫做`putCenter`来放置这个精灵：
//g.stage.putCenter(treasure, 208, 0);

//在宝藏上创建一个`拾取'属性来帮助我们
//了解玩家是否已经领取了宝藏
treasure.pickedUp = false;

//将宝藏添加到 `gameScene`
gameScene.addChild(treasure);
``` 

请注意，在创建每个精灵之后，它将被添加到
`gameScene`使用`addChild`。这是上面的代码生成的内容：

![Treasure Hunter](/tutorials/screenshots/03.png)

让我们多了解一下这些精灵如何定位画布。

##### 定位精灵

所有的精灵都有`x`和`y`属性，你可以用它来精确
在画布上定位精灵。`x`和`y`值是指精灵的像素
坐标相对于画布的左上角。顶端
左边角落的'x'和'y'值为0.这意味着任何
您分配给精灵的正面`x`和`y`值将定位在左侧（`x`）并向下
（`y`）相对于该角点。例如，这是
定位`exit`门的代码（绿色方块）。 
```js
exit.x = 8;
exit.y = 8;
```
你可以看到这个代码将门8个像素放置在右边8个像素之下
画布的左上角。积极的`x`值定位于精灵
画布左边的右边。积极的'y`值定位他们
低于画布的上边缘。

精灵也有'宽度'和'高度'
属性，以像素为单位告诉你它们的宽度和高度。如果你需要
找出一个精灵的宽度或一半高度是多少，使用
`halfWidth`和`halfHeight`。

Hexi还有一些便利的方法可以帮助你快速定位
精灵相对于其他精灵：putTop，putRight，putBottom，putLeft和putCenter。
例如，以下是上述代码中的行
定位宝藏精灵（金盒）。代码放置了
宝藏在左边的26像素
帆布的右边缘，并垂直居中。
```js
treasure.x = g.canvas.width - treasure.width - 10;
treasure.y = g.canvas.height / 2 - treasure.halfHeight;
```
这是很多复杂的定位代码来编写的。相反，你
可以使用Hexi内置的`putCenter`方法来达到同样的效果
喜欢这个：
```js
g.stage.putCenter(treasure, 220, 0);
```
什么是'舞台'？它是所有精灵的根容器，并且
具有与画布完全相同的尺寸。你可以想到的
`舞台'是一个巨大的，不可见的精灵，与画布的大小相同，它包含着
你游戏中的所有精灵，以及那些精灵的任何容器
可能被分组（像`gameScene`）。`putCenter`的作品
将 `treasure`集中在`stage`内，然后抵消它
`x`位置220像素。这里是使用`putCenter`的格式：
```js
anySprite.putCenter(anyOtherSprite, xOffset, yOffset);
```
你可以用同样的方法使用其他的`put`方法。例如，如果
你想将一个精灵直接放在另一个的左边
精灵，没有任何抵消，你可以使用`putLeft`，就像这样：
```js
spriteOne.putLeft(spriteTwo);
```
这会将`spriteTwo`直接放在`spriteOne`的左边，并且
垂直对齐。您会看到很多关于如何在整个过程中使用这些“放置”方法的示例
这些教程。

##### 分配动态属性

在我们继续之前，您需要注意一个小细节。该
创建精灵的代码还会为其添加“拾取”属性
宝藏精灵：
```js
treasure.pickedUp = false;
```
你会看到我们将如何在游戏逻辑中使用`treasure.pickedUp`来帮助我们确定
比赛的进展。如果需要，可以动态地将任何自定义属性或方法分配给像这样的精灵。

##### 创造敌人精灵

宝藏猎人中有6个敌人精灵（红色方块）。他们是
水平间隔均匀但具有随机初始垂直
位置。所有的敌人精灵都是在`for`循环中创建的
这个代码在`setup`函数中：

```js
//制造敌人
let numberOfEnemies = 6,
    spacing = 48,
    xOffset = 150,
    speed = 2,
    direction = 1;

//定义一个数组来存储所有的敌人 
enemies = [];

//制造 `numberOfEnemies` 数量众多的敌人 
for (let i = 0; i < numberOfEnemies; i++) {

  //每个敌人都是一个红色的矩形
  let enemy = g.rectangle(32, 32, "red");

  //根据“间距”值水平放置每个敌人。
  //`xOffset`确定屏幕左侧的点
  //第一个敌人应该加入的地方
  let x = spacing * i + xOffset;

  //给敌人一个随机的y位置
  let y = g.randomInt(0, g.canvas.height - enemy.height);

  //设定敌人的方向
  enemy.x = x;
  enemy.y = y;

  //设定敌人的垂直速度。`方向'将是`1`或
  //`-1`。`1`意味着敌人会向下移动，`-1`意味着敌人会移动
  //提升。用'速度'乘以'方向'决定敌人的方向
  //垂直方向
  enemy.vy = speed * direction;

  //反转下一个敌人的方向
  direction *= -1;

  //将敌人压入敌人数组 `enemies`
  enemies.push(enemy);

  //将敌人添加到  `gameScene`
  gameScene.addChild(enemy);
}

```

以下是这段代码产生的内容：

![Treasure Hunter](/tutorials/screenshots/04.png)

该代码在帮助下给每个敌人一个随机的“y”位置
Hexi的`randomInt`方法：
```js
let y = g.randomInt(0, g.canvas.height - enemy.height);
```
`randomInt`会给你一个任意两个整数之间的随机数
提供参数。（如果你需要一个随机的十进制数，使用
`randomFloat`代替）。

所有精灵都有属性，称为`vx`和`vy`。他们确定了
速度和方向，精灵会在水平方向移动
方向（`vx`）和垂直方向（`vy`）。中的敌人
寻宝者只能上下移动，所以他们只需要一个'vy'值。
他们的`vy`是`speed`（2）乘以`direction`（这将是
'1'或'-1'）。
```js
enemy.vy = speed * direction;
```
如果`方向'是`1`，敌人的`vy`将是`2`。这意味着
敌人将以每帧2像素的速度向下移动屏幕。如果
`direction`为`-1`，敌人的速度为`-2`。这意味着
敌人将以每帧2个像素向上移动屏幕。 

在敌人'vy`设置后，'direction'被颠倒，以便下一个
敌人会朝相反的方向移动。
```js
direction *= -1;
```
你可以看到每个被创建的敌人被推入一个数组中
称为'敌人'。
```js
enemies.push(enemy);
```
在后面的代码中，你会看到我们将如何访问这里的所有敌人
以确定他们是否触摸了该玩家。

##### 生命栏

玩家时你会注意到
触及其中一个敌人，右上角的生命栏的宽度
屏幕减少。 

![Treasure Hunter](/tutorials/screenshots/05.png)

这个健康吧怎么样？它只是两个长方形的精灵
位置：后面是一个黑色矩形，前面是绿色矩形。他们被分组
一起制作一个名为`healthBar`的单个复合精灵。该
`healthBar`然后被添加到`gameScene`。
```js
//创建健康栏
let outerBar = g.rectangle(128, 16, "black"),
    innerBar = g.rectangle(128, 16, "yellowGreen");

//分组内外栏
healthBar = g.group(outerBar, innerBar);

//将`innerBar`设置为`healthBar`的一个属性
healthBar.inner = innerBar;

//将 `healthBar` 添加到`gameScene`
healthBar.x = g.canvas.width - 148;
healthBar.y = 16;

//将 `healthBar` 添加到 `gameScene`
gameScene.addChild(healthBar);
```

你可以看到名为`inner`的属性已经被添加到了`healthBar`。
它只是引用`innerBar`（绿色的矩形）稍后访问会很方便。
```js
healthBar.inner = innerBar;
```
你不*有*这样做; 但是，嘿，为什么不呢！这意味着如果你
想要控制`innerBar`的宽度，你可以写一些流畅的代码
看起来像这样：
```js
healthBar.inner.width = 30;
```
这非常整洁可读，所以我们会保留它！

##### 游戏结束

如果玩家的生命值降至零，或玩家设法降低
将宝藏带到出口处，游戏结束，游戏结束
被展示。场景中的游戏只是一些显示“你赢了！”的文字 或者你
失去了！“取决于结果。 

![Treasure Hunter](/tutorials/screenshots/06.png)

这是怎么产生的？文本是由一个`text`精灵制作的。
```js
let anyText = g.text(
  "Hello!", "CSS font properties", "fillColor", xPosition, yPosition
);
```
第一个参数，“你好！” 在上面的例子中，是文本内容
你想显示。使用`content`属性来改变文本
精灵的内容。
```js
anyText.content = "Some new content";
```
以下是游戏结束消息文本是如何在`setup`中创建的功能。 
```js
//通过消息为游戏添加一些文本
message = g.text("Game Over!", "64px Futura", "black", 20, 20);
message.x = 120;
message.y = g.canvas.height / 2 - 64;
```
接下来，创建一个名为`gameOverScene`的新组。 `message` 文本
被添加到它。`gameOverScene`的`visible`属性设置为
`false'，以便在游戏首次启动时不可见。
```js
//创建一个`gameOverScene`组并添加 'message' 精灵到它
gameOverScene = g.group(message);

//现在让'gameOverScene`不可见
gameOverScene.visible = false;
```
在游戏结束时，我们将设置 `gameOverScene` 的`visible`属性设置为 `true`以显示文本消息。
我们也会设置`gameScene`的`visible`属性为`false`，这样所有的游戏精灵是隐藏的。

##### 按键交互

用键盘上的箭头键控制播放器（蓝色方块）。
Hexi有一个内置的`arrowControl`方法，可以让你快速添加
方向键交互游戏。提供您想要移动的精灵
第一个参数，以及它每帧的像素数量 
应该作为第二个参数。这是`arrowControl`
方法用于帮助玩家角色每移动5个像素
当按下箭头键时框架。
```js
g.arrowControl(player, 5);
```
使用`arrowControl`是实现键盘的一种简单快捷的方法交互性，
但通常需要更好地控制什么时候发生键被按下。
Hexi有一个内置的 `keyboard`方法，可以让你定义自定义键。

```js
let customKey = g.keyboard(asciiCode);
```
为密钥提供[ascii key code number](http://www.asciitable.com)
你想用作第一个参数。

所有这些键都有`press`和
你可以定义的`release`方法。以下是您可以选择创建和使用这些键盘对象来帮助移动玩家角色的方法
淘金者。（你可以在`setup`函数中定义这个代码。）：

```js
  //使用Hexi的`keyboard`方法创建一些键盘对象。
  //你通常会在`setup`函数中使用这段代码。
  //将ASCII码值作为单个参数提供
  let leftArrow = g.keyboard(37),
      upArrow = g.keyboard(38),
      rightArrow = g.keyboard(39),
      downArrow = g.keyboard(40);

  //左键按下 `press` 方法
  leftArrow.press = () => {
    //按下按键时更改播放器的速度
    player.vx = -5;
    player.vy = 0;
  };

  //左键释放 `release` 方法
  leftArrow.release = () => {
    //如果左箭头已被释放，并且右箭头未关闭，
    //并且播放器没有垂直移动：
    //停止播放器
    if (!rightArrow.isDown && player.vy === 0) {
      player.vx = 0;
    }
  };

  //上键
  upArrow.press = () => {
    player.vy = -5;
    player.vx = 0;
  };
  upArrow.release = () => {
    if (!downArrow.isDown && player.vx === 0) {
      player.vy = 0;
    }
  };

  //右键
  rightArrow.press = () => {
    player.vx = 5;
    player.vy = 0;
  };
  rightArrow.release = () => {
    if (!leftArrow.isDown && player.vy === 0) {
      player.vx = 0;
    }
  };

  //下键
  downArrow.press = () => {
    player.vy = 5;
    player.vx = 0;
  };
  downArrow.release = () => {
    if (!upArrow.isDown && player.vx === 0) {
      player.vy = 0;
    }
  };

```

你可以看到玩家的`vx` 和 `vy`属性的值是
根据哪些按键被按下或释放而改变。
积极的`vx`值会使玩家向右移动，否则
价值会让它向左移动。一个积极的 `vy` 值将会使得这个
玩家向下移动，负值会使其向上移动。 

第一个参数是你想要控制的sprite：`player`。该
第二个参数是精灵应该移动每个帧的像素数：`5`。
最后四个参数是顶部的[ascii关键代码数字]（http://www.asciitable.com）
右键，底键和左键。（你可以记住这一点，因为他们的
顺序从顶部开始顺时针列出。）


##### 游戏状态

**游戏状态**是Hexi目前正在运行的功能。什么时候
Hexi首先启动，运行`setup`函数（或其他任何其他功能）
函数在Hexi的构造函数参数中指定。）如果你
想要改变游戏状态，给Hexi的“国家”分配一个新的功能
属性。就是这样：
```js
g.state = anyFunction;
```
在寻宝游戏中，当 `setup` 函数完成时，游戏
`state`设置为`play`：
```js
g.state = play;
```
这使得Hexi寻找并运行一个名为`play`的函数。默认，
分配给游戏状态的任何函数都将在连续循环中运行，
每秒60帧。（您可以随时通过设置Hexi的来改变帧率
`fps`属性）。游戏逻辑通常运行在一个连续的循环中
被称为**游戏循环**。Hexi为您处理循环管理，
所以你不必担心它是如何工作的。 

（如果你很好奇，Hexi使用
一个带有[固定逻辑时间步长和可变渲染时间]的requestAnimationFrame循环（http://gameprogrammingpatterns.com/game-loop.html）。它
精灵位置插值也可以平滑任何不一致
峰值帧率。它运行[思慕雪]（https://github.com/kittykatattack/smoothie）
引擎盖下做这一切，所以你可以使用任何思慕雪的属性
微调你的Hexi应用游戏循环以获得最佳效果。）

如果您需要暂停循环，只需使用Hexi的“暂停”方法即可
这个：
```js
g.pause();
```
您可以使用`resume`方法重新开始游戏循环，如下所示：
```js
g.resume();
```
现在让我们来看看Treasure Hunter的“play”功能是如何工作的。 

#### 游戏循环的逻辑

正如你刚刚学到的，`play`函数中的所有内容都运行在a中
连续循环。
```js
function play() {
  //这段代码每秒从上到下循环60次  
}
```
这是所有游戏逻辑发生的地方。这是有趣的部分，
所以让我们来看看`play`函数里面的代码是干什么的。

##### 移动玩家精灵

宝藏猎人在`play`函数中使用Hexi的`move`方法来移动魔鬼中的精灵
游戏。

```js
g.move(player);
```

这相当于编写这样的代码：

```js
player.x += player.vx;
player.y += player.vy;
```

它只是通过添加`vx`来更新玩家的'x`和`y`位置
和'vy'速度值。（请记住，这些值是
按`press` 和`release` 方法设置。）使用`move`只需保存
你不必键入和查看这个非常标准的样板
码。

你也可以用一行代码来移动一组精灵
提供数组作为参数。

```js
g.move(arrayOfSprites);
```

所以现在你可以轻松地移动播放器，但是当播放器发生什么时，
玩家到达屏幕的边缘？

##### 控制精灵

使用Hexi的“包含”方法来保持精灵在界限内屏幕。

```js
g.contain(player, g.stage);
```

第一个参数是你想要包含的精灵，第二个
参数是任何具有 `x`, `y`, `width`的JavaScript对象
和`height`属性。 

正如你以前所学到的，`stage`是所有Hexi精灵的根容器对象，它已经成为了
与“画布”相同的宽度和高度。 

但是你也可以提供一个自定义的`contains`方法 
反对做同样的事情。就是这样：

```js
g.contain(
  player, 
  {
    x: 0,
    y: 0,
    width: 512,
    height: 512
  }
);
```

这会将`player`精灵包含到由.de定义的区域
物体的尺寸。如果你想，这真的很方便
精确地调整对象应该包含的区域。

`contains`有一个额外的有用功能。如果精灵达到其中一个
包含边，`contains`将返回一个[JavaScript Set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set) ，告诉你
它到达哪个边界： "top", "right", "bottom", 或 "left"。就是这样
你可以使用这个特性来找出画布的哪个边缘
精灵感人：

```js
let playerHitsEdges = g.contain(player, g.stage);

if(playerHitsEdges) {

  //找出碰撞发生在哪一边
  let collisionSide;
  if (playerHitsEdges.has("left")) collisionSide = "left";
  if (playerHitsEdges.has("right")) collisionSide = "right";
  if (playerHitsEdges.has("top")) collisionSide = "top";
  if (playerHitsEdges.has("bottom")) collisionSide = "bottom";

  //在文本精灵中显示结果
  message.content = `The player hit the ${collisionSide} of the canvas`; 
} 
```

##### 检测碰撞

当玩家击中任何敌人时，健康栏的宽度
减少，玩家变得半透明。

![Treasure Hunter](/tutorials/screenshots/07.png)

这个怎么用？

Hexi有一整套有用的2D几何和瓷砖碰撞
检测方法。Hexi实施[Bump collision module](https://github.com/kittykatattack/bump)，所有
碰撞的方法与Hexi合作。 

寻宝者只使用这些碰撞方法之一：
`hitTestRectangle`。它需要两个矩形的精灵并告诉你
它们是否重叠。如果它们是，那么它将返回`true` ，并且
如果不是，则为`false` 。

```js
g.hitTestRectangle(spriteOne, spriteTwo);
```
以下是`play`函数中的代码如何使用`hitTestRectangle`
检查任何敌人与玩家之间的碰撞。
```js
//在检查碰撞之前将`playerHit`设置为`false`
let playerHit = false;

//遍历`enemies`数组中的所有精灵
enemies.forEach(enemy => {

  //移动敌人
  g.move(enemy);

  //检查敌人的屏幕边界
  let enemyHitsEdges = g.contain(enemy, g.stage);

  //如果敌人击中舞台的顶部或底部，则相反
  //它的方向
  if (enemyHitsEdges) {
    if (enemyHitsEdges.has("top") || enemyHitsEdges.has("bottom")) {
      enemy.vy *= -1;
    }
  }

  //测试碰撞。如果有任何敌人在触碰
  //玩家，将`playerHit`设置为`true`
  if (g.hitTestRectangle(player, enemy)) {
   playerHit = true;
  }
});

//如果玩家被击中......
if (playerHit) {

  //使玩家半透明
  player.alpha = 0.5;

  //将'healthBar'内部矩形的宽度减少1个像素
  healthBar.inner.width -= 1;
} else {

  //如果玩家没有被击中，则使玩家完全不透明（不透明）
  player.alpha = 1;
}
```
这段代码创建了一个名为`playerHit`的变量，它是
在`forEach`循环检查全部之前，初始化为`false` 
碰撞的敌人。
```js
let playerHit = false;
```
（因为`play`函数每秒运行60次，`playerHit`
将在每个新帧上重新初始化为 `false` 。）

如果`hitTestRectangle`返回`true`，则`forEach`循环设置
`playerHit`为`true`。
```js
if(g.hitTestRectangle(player, enemy)) {
  playerHit = true;
}
```
如果玩家已经被击中，则代码使玩家半透明
将其 `alpha`值设置为0.5。它也减少了宽度
`healthBar`的`inner` 精灵1个像素。
```js
if(playerHit) {

  //使玩家半透明
  player.alpha = 0.5;

  //将`healthBar`内部矩形的宽度减少1个像素
  healthBar.inner.width -= 1;

} else {

  //如果玩家没有被击中，则使玩家完全不透明（不透明）
  player.alpha = 1;
}
```

你可以将sprite的`alpha`属性设置为`0`之间的任何值
（完全透明）到'1'（完全不透明）。值为0.5
半透明.b（** Alpha **是一个
精心设计的图形设计术语，意味着**透明**。）

这部分代码还使用“移动”方法来移动敌人，并且
“包含”使它们保持在画布内。该代码也使用
“包含”的返回值来判断敌人是否击中敌人
画布的顶部或底部。如果它击中顶部或底部，敌人的方向是
在此代码的帮助下逆转：
```js
//检查敌人的屏幕边界
let enemyHitsEdges = g.contain(enemy, g.stage);

//如果敌人击中舞台的顶部或底部，则相反
//它的方向
if (enemyHitsEdges) {
  if (enemyHitsEdges.has("top") || enemyHitsEdges.has("bottom")) {
    enemy.vy *= -1;
  }
}
```
将敌人的`vy` （垂直速度）值乘以负1
使其走向相反的方向。这是一个非常简单的**反弹**
影响。

###### 与宝藏碰撞

如果玩家触摸宝藏（黄色方块），即“钟声”
声音播放。玩家可以
把宝藏带到出口处。宝藏集中在玩家身上
随着它一起移动。 

![Treasure Hunter](/tutorials/screenshots/08.png)

这是来自`play`函数的代码，可以实现这些效果。

```js
//检查玩家与宝藏之间的碰撞
if (g.hitTestRectangle(player, treasure)) {

  //如果宝藏正在触碰玩家，请将其置于玩家之上
  treasure.x = player.x + 8;
  treasure.y = player.y + 8;

  if(!treasure.pickedUp) {

    //如果宝藏尚未被拾取，
    //播放`chimes`声音
    chimes.play();
    treasure.pickedUp = true;
  };
}
```
你可以看到代码在`if`中使用`hitTestRectangle`
声明来测试玩家和宝藏之间的碰撞。
```js
if (g.hitTestRectangle(player, treasure)) {
```
如果它是“真的”，宝藏就集中在玩家身上。
```js
treasure.x = player.x + 8;
treasure.y = player.y + 8;
```
如果`treasure.pickedUp`是`false`，那么你知道宝藏还没有 
拿起来，你可以播放`chimes`声音：
```js
chimes.play();
```
除了`play`，Hexi的声音对象还有其他一些方法可以用来控制它们：
`pause`, `restart` 和 `playFrom`。（使用`playFrom`开始播放
声音文件中特定秒的声音，如下所示：
`soundObject.playFrom(5)`。这将使声音开始播放
5秒标记）。

您还可以通过分配设置声音对象的 `volume`
介于0和1之间的值。以下是如何将 `volume`设置为中等水平
（50％）。
```js
soundObject.volume = 0.5;
```
您可以通过在-1（左扬声器）之间分配一个值来设置声音对象的 `pan` 
到1（右扬声器）。平移值为0会使声音等于音量
两位发言者。以下是您如何设置 `pan` 的方法
在左边的发言者突出。
```js
soundObject.pan = -0.2;
```
如果你想连续不断地重复声音，可以将`loop`属性设置为`true`。
```js
soundObject.loop = true;
```
Hexi实现 [Sound.js module](https://github.com/kittykatattack/sound.js)来控制声音，
所以你可以在您的Hexi使用任何Sound.js的属性和方法应用。

因为你不想一次又一次地播放`chimes` 
宝藏已经被拿起，代码将 `treasure.pickedUp` 设置为在声音播放之后`true`。
```js
treasure.pickedUp = true;
```
现在玩家拿起了宝藏，你怎么能检查
比赛结束？

##### 结束游戏

游戏结束有两种方式。玩家的健康可能会用完，
在这种情况下，游戏丢失了。或者，玩家可以成功携带
宝藏出口，在这种情况下，游戏赢了。如果其中之一
这两个条件都满足了，游戏的`state`被设置为 `end` 
`message`文本的`content`显示结果。这是最后一个
在`play`函数中的一小部分代码可以做到这一点：
```js
//玩家是否有足够的生命值？如果'innerBar`的宽度
//小于零，结束游戏并显示 "You lost!"
if (healthBar.inner.width < 0) {
  g.state = end;
  message.content = "You lost!";
}
//如果玩家将宝藏带到出口处，
//结束游戏并显示 "You won!"
if (g.hitTestRectangle(treasure, exit)) {
  g.state = end;
  message.content = "You won!";
}
```
`end`功能非常简单。它只是隐藏`gameScene`和
显示`gameOverScene`。
```js
function end() {
  gameScene.visible = false;
  gameOverScene.visible = true;
}
```
这就是寻宝者！在继续之前，尝试制作
从头开始使用这些相同的技术。什么时候
你准备好了，继续阅读！

#### 使用图像

有三种主要方式可以在Hexi游戏中使用图像。 

- 为每个精灵使用单独的图像文件。
- 使用**纹理地图集**。这是一个包含的单个图像文件
  您游戏中每个精灵的子图像。图像文件是
  伴随着一个匹配的JSON
  数据文件，描述每个文件的名称，大小和位置
  子图像。
- 使用** tileset **（也称为** spritesheet **）。这也是一个单一的
  包含每个精灵的子图像的图像文件。但是，不像一个
  纹理图集，它没有附带描述的JSON文件
  精灵数据。相反，您需要指定大小和位置
  您的游戏代码中的每个精灵都使用JavaScript。这可以有一些
  在某些情况下优于纹理图集。

所有三种制作图像精灵的方法都是使用Hexi的 `sprite`方法。
以下是使用它制作图像精灵的最简单方法。
```js
let imageSprite = g.sprite("images/theSpriteImage.png");
```
在下一节中，我们将使用图像精灵来更新宝藏猎人
您将学习将图像添加到游戏的所有三种方式。

（本节中的所有图像均由Lanea Zimmerman创作
可以找到更多她的作品 [here](http://opengameart.org/users/sharm)。谢谢，Lanea！）

##### 个人图像

打开并玩下一个版本的寻宝者：
`02_treasureHunterImages.html`（你可以在`tutorials`中找到它
文件夹）。它的播放与第一个版本完全相同，但都是
彩色正方形已被图像取代。

[![Treasure Hunter](/tutorials/screenshots/09.png)](https://cdn.gitcdn.xyz/cdn/kittykatattack/hexi/7349658f295c120ca7f3bab94d31379a0c02952e/tutorials/02_treasureHunterImages.html)

（点击图片并按照链接玩游戏。）看看源代码，你会注意到游戏逻辑
结构与游戏的第一个版本完全相同。
唯一改变的是精灵的外观。
这是如何完成的？

###### 加载图像文件 

游戏中的每个精灵都使用一个单独的PNG图像文件。你会找到
教程 `images` 子文件夹中的所有图像。

![Treasure Hunter](/tutorials/screenshots/10.png)

在你使用它们制作精灵之前，你需要预先加载它们
Hexi的 `assets`。最简单的方法是列出图像名称，
以及他们完整的文件路径，当你第一次在Hexi的资产阵列
初始化引擎。创建一个名为`thingsToLoad`的数组，列出
文件名，作为字符串，你想加载。然后提供该数组
作为`hexi` 方法的第四个参数。就是这样：
```js
//包含所有要加载的文件的数组
let thingsToLoad = [
  "images/explorer.png",
  "images/dungeon.png",
  "images/blob.png",
  "images/treasure.png",
  "images/door.png",
  "sounds/chimes.wav"
];

//创建一个新的Hexi实例，并启动它
let g = hexi(512, 512, setup, thingsToLoad);

//启动Hexi
g.start();
```
（如果您在Web浏览器中打开JavaScript控制台，则可以
监控这些资产的加载进度。）

现在你可以像这样访问游戏代码中的任何图像：
```JS
g.image（ “图像/ blob.png”）
```
尽管预加载图像和其他资产是最简单的方法
让他们进入你的游戏，你也可以在任何其他时间加载资产
使用`loader`对象及其方法。正如我前面提到的，
`loader`只是Pixi加载器运行的别名
引擎盖下，你可以[learn more about how to use it here](https://github.com/kittykatattack/learningPixi#loading).

现在您已经将图像加载到游戏中，让我们来了解如何操作
用它们制作精灵。

###### 用图像制作精灵

使用`sprite`方法使用您学习的相同格式创建一个图像精灵
早。以下是如何使用`dungeon.png`图像创建精灵。
（`dungeon.png`是512×512像素的背景图像。）
```js
dungeon = g.sprite("images/dungeon.png");
```
就这样！现在，而不是显示为一个简单的彩色矩形，
精灵将显示为512乘512的图像。没有必要
指定宽度或高度，因为Hexi数字表示我们为你
自动根据图像的大小。你可以使用所有其他的
sprite属性，像`x`，`y`，`width`和`height`，就像你一样
会用普通的矩形小精灵。 

以下是创建地下城的`setup`函数的代码
背景，退出门，玩家和宝藏，并将它们全部添加到
`gameScene`组。 
```js
//地牢背景
dungeon = g.sprite("images/dungeon.png");

//出口门
exit = g.sprite("images/door.png");
exit.x = 32;

//玩家精灵
player = g.sprite("images/explorer.png");
player.x = 68;
player.y = g.canvas.height / 2 - player.halfWidth;

//创建宝藏
treasure = g.sprite("images/treasure.png");

//将它放在画布左边的旁边
//g.stage.putCenter(treasure, 208, 0);

//在宝藏上创建一个`pickedUp` 属性来帮助我们
//了解玩家是否已经领取了宝藏
treasure.pickedUp = false;

//创建`gameScene`组并添加小精灵
gameScene = g.group(dungeon, exit, player, treasure);
```
（作为一个稍微更有效的改进
这个代码的原始版本，`group`创建`gameScene`和groups
精灵在一个单一的步骤。）

看起来熟悉？没错，唯一改变的代码是
创建精灵的线条。这种模块化是Hexi的特色，可让您快速创建
游戏原型使用简单的形状，你可以很容易地换出
随着您的游戏理念的发展，您会看到详细的图像 其余的代码在
游戏可以保持原样。

###### 微调收容区域

对这个新版本Treasure做了一个小小的改进
猎人是新的方式，精灵被包含在城墙内
地牢。它们被包含在自然匹配艺术品的2.5D视角的方式中，如此屏幕截图中的绿色方块所示：

![Treasure Hunter](/tutorials/screenshots/11.png)

这是一个非常简单的修改。所有你需要做的是供应
用包含定义大小的自定义对象的`contains`方法
包含矩形的位置。就是这样：
```js
g.contain(
  player,
  {
    x: 32, y: 16,
    width: g.canvas.width - 32,
    height: g.canvas.height - 32
  }
);
```
只需调整`x`, `y`, `width` 和 `height` 值即可
包含区域看起来很自然，你正在制作的游戏。

##### 使用纹理图集

如果你正在研究一个复杂的大型游戏，那么你就需要一个快速而又复杂的游戏
有效的方式来处理图像。纹理图集可以帮助您做到
这个。纹理图集实际上是两个紧密相连的独立文件
有关：

- 包含您的所有图像的单个PNG ** tileset **图像文件
  想在你的游戏中使用。（tileset图像有时被称为a
  spritesheet。）
- 描述这些子图像大小和位置的JSON文件
  在瓷砖中。

使用纹理地图集是一个很大的节省时间。你可以安排
以任何顺序设置tileset的子图像并保留JSON文件
追踪它们的大小和位置。这真的很方便
因为这意味着子图像的大小和位置不是
硬编码到您的游戏程序中。如果您更改了tileset，
如添加图像，调整大小或删除图像，只需重新发布即可
JSON文件和您的游戏将使用该更新的数据来显示
图像正确。如果你将会做出比a更大的事情
非常小的游戏，你一定会使用纹理图集。

tileset JSON数据事实上的标准是这样的格式
由一个名为 [Texture Packer](https://www.codeandweb.com/texturepacker) 的流行软件工具输出（Texture Packer的"Essential" 许可证是免费的）。即使你
不要使用Texture Packer，类似的工具如 [Shoebox](http://renderhjs.net/shoebox/)会以相同的格式输出JSON文件。让我们了解如何使用它来制作纹理
纹理打包器的地图集，以及如何将其加载到游戏中。

###### 准备图像

您首先需要为游戏中的每个图像创建单独的PNG图像。
你已经拥有了寻宝猎人，所以你们都准备好了。打开纹理
打包器并选择**{JS}** 配置选项。拖动您的游戏图像
进入其工作区。您还可以将纹理打包器指向包含的任何文件夹
你的图片。纹理打包器会自动排列图像
单个瓷砖图像，并给他们与原来相匹配的名字
图像文件名称。它会默认给它们一个2像素的填充。

![Texture Packer](/tutorials/screenshots/12.png)

地图集中的每个子图像都称为 **frame**。虽然
它只是一个大的图像，纹理地图集有5帧。每个的名称
框架与原始PNG文件名称相同：“dungeon.png”，
“blob.png”，“explorer.png”，“treasure.png”和“door.png”。这些
帧名称用于帮助地图集引用每个子图像。

完成后，请确保数据格式设置为JSON（哈希）和
单击发布按钮。选择文件名和位置，然后保存
发布文件。你将得到一个PNG文件和一个JSON文件。在
这个例子我的文件名是`treasureHunter.json`和
`treasureHunter.png`。做
您的生活更轻松，只需将这两个文件保存在项目的`images`中
夹。（将JSON文件视为图像文件的额外元数据。）

纹理打包机常常是一个痛苦的使用，因为你需要全部
这些设置恰到好处地让它正确发布而无需告知
你有错误。而且，它会试图诱骗你升级到
付费版本使用默认设置，不受免费支持
版。所以你需要明确地关掉这些（正如我所描述的那样
以上）为它工作没有错误。不过，这是值得的努力
最后 - 所以不断尝试，并在这个存储库中发布问题，如果你
得到不可能的卡住！

###### 加载纹理图集

要将纹理图集加载到游戏中，只需包含JSON文件即可
在Hexi的资产阵列当你初始化游戏。
```js
let thingsToLoad = [
  "images/treasureHunter.json",
  "sounds/chimes.wav"
];
let g = hexi(512, 512, setup, thingsToLoad);
g.scaleToWindow();
g.start();
```
就这样！您不必加载PNG文件 - Hexi就是这么做的
自动在后台。你需要告诉JSON文件
Hexi哪些瓷砖镶框（子图像）来显示。

现在，如果你想使用纹理图集的框架来制作一个
精灵，你可以这样做：
```js
anySprite = g.sprite("frameName.png");
```
Ga将创建精灵并从中显示正确的图像
纹理地图集的tileset。

以下是如何在Treasure Hunter中使用创建精灵的方法
纹理地图集框架：
```js
//地牢背景
dungeon = g.sprite("dungeon.png");

//出口门
exit = g.sprite("door.png");
exit.x = 32;

//玩家精灵
player = g.sprite("explorer.png");
player.x = 68;
player.y = g.canvas.height / 2 - player.halfWidth;

//创建宝藏
treasure = g.sprite("treasure.png");
```
Hexi知道那些纹理地图集的框架名称，而不是个人
图像，并直接从拼图显示它们。

如果您需要访问游戏中的纹理图集的JSON文件，
你可以像这样得到它：
```js
jsonFile = g.json("jsonFileName.json");
```
看一下`tutorials`文件夹中的`treasureHunterAtlas.js`文件
看一个如何加载纹理图集并使用它的实例
制作精灵。

#### 外星舰队

本系列教程中的下一个示例游戏是Alien Armada。你可以吗
摧毁60个外国人，然后摧毁地球？点击
下面的图像链接来玩游戏：

[![Alien Armada](/tutorials/screenshots/13.png)](https://gitcdn.xyz/repo/kittykatattack/hexi/master/tutorials/04_alienArmada.html)

使用箭头键移动并按下空格键进行拍摄。该
外星人从屏幕顶端下降
随着游戏进展而增加频率。以下是游戏的玩法：

![Alien Armada gameplay](/tutorials/screenshots/14.png)

Alien Armada展示了一些你一定会想要的新技术
在你的游戏中使用：

- 加载并使用自定义字体。
- 在游戏资产加载时显示加载进度条。
- 射击子弹。
- 创建多个图像状态的精灵。
- 生成随机敌人。
- 从游戏中删除精灵。
- 显示比赛分数。
- 重置并重新开始游戏。

你会发现完整的评论Alien Armada源代码
`tutorials` 文件夹。一定要看看它，以便你可以看到
所有这些代码在适当的上下文中。其总体结构是相同的
到宝藏猎人，加上这些新技术。让我们
了解它们是如何实施的。

##### 加载并使用自定义字体

Alien Armada使用名为`emulogic.ttf`的自定义字体来显示
得分在屏幕的右上角。字体文件是
预先加载资产数组中的其余资产文件（声音和图像）
初始化游戏。 
```js
let thingsToLoad = [
  "images/alienArmada.json",
  "sounds/explosion.mp3",
  "sounds/music.mp3",
  "sounds/shoot.mp3",
  "fonts/emulogic.ttf" // < - 自定义字体
];
let g = hexi(480, 320, setup, thingsToLoad, load);
g.scaleToWindow();
g.start();
```

要使用这种字体，请在游戏的`setup`中创建一个`text` 精灵
功能。`text`方法的第二个参数是a
描述字体点大小和名称的字符串：“20px emulogic”。  
```js
scoreDisplay = g.text("0", "20px emulogic", "#00FF00", 400, 10);
```
您可以加载和使用TTF，OTF，TTC或WOFF格式的任何字体。

##### 加载进度条

Alien Armada加载了三种MP3声音文件：一种是拍摄声音，一种是
爆炸声和音乐。音乐声音大小约为2 MB
在慢速网络连接上，这个声音可能需要几秒钟的时间
加载。发生这种情况时，玩家只会在Alien Armada看到空白的画布
负载。有些玩家可能会认为游戏已经冻结，所以游戏
有用地实施一个加载栏来通知
资产正在加载的玩家。这是一个从左到右扩展的蓝色矩形
显示一个数字，告诉你游戏资产的百分比
加载到目前为止。

![Loading progress bar](/tutorials/screenshots/16.png)

这是Hexi发动机内置的一项功能。 
Hexi有一个可选的装载状态，可以在游戏资产运行时运行
加载。您可以决定在装载过程中发生什么
州。你所需要做的就是编写一个应该有代码的函数
在资产加载时运行，并告诉Hexi这是什么名字
功能是。Hexi的引擎会自动运行该功能
直到资产完成加载。

让我们来了解一下Alien Armada的工作原理。游戏代码告诉
Hexi在装载状态下使用称为`load` 的函数。它的确如此
这通过列出`load`作为最后的参数
在Hexi的初始化构造函数中。（在下面的代码中查找`load`）：
```js
let g = hexi(480, 320, setup, thingsToLoad, load); //<- It's here!
```
这告诉Hexi在资产中循环运行`load`函数
正在加载。 

这是来自Alien Armada的`load`函数。它实现了一个
`loadingBar`对象，这是显示扩展蓝条和
加载的文件的百分比。
```js
function load(){
  g.loadingBar();
}

```
资产加载后，`setup`状态会自动运行。 

你会在Hexi的`core.js`文件中找到`loadingBar`代码。它的
本意是一个非常简单的例子，你可以用它作为基础
编写自己的自定义加载动画，如果你想。你可以运行任何代码
就像`load`函数一样，所以完全取决于你决定什么
应该会发生或在您的游戏加载时显示的内容。

##### 射击子弹

你怎么能制造大炮射击子弹？ 

当你按下空格键时，大炮向敌人发射子弹。
子弹从大炮炮塔的末端开始，然后向上穿行
每帧7像素的画布。如果他们撞到了外星人，外星人
爆炸。如果一颗子弹失踪并飞过舞台的顶端，那么
游戏代码将其删除。

![Firing bullets](/tutorials/screenshots/17.png)

为了在你的游戏中实施子弹射击系统，你首先要做的
需要的是一个数组来存储所有的子弹精灵。
```js
bullets = [];
```
这个`bullets`数组在游戏的`setup`函数中被初始化。

然后你可以使用Hexi的自定义“射击”方法让任何精灵发射
子弹在任何方向。以下是您可以使用的一般格式
实施“射击”方法。
```js
g.shoot(
  cannon,//射手
  4.71,//拍摄角度（4.71）
  cannon.halfWidth,//炮的子弹x位置
  0,// Bullet在canon上的y位置
  g.stage,//应该添加项目符号的容器
  7,//子弹速度（每帧像素）
  bullets, //用于存储子弹的数组

  //返回应该出现的精灵的函数
  //用于制作每个子弹
  () => g.sprite("bullet.png")
);
```
第二个参数确定以弧度表示的角度
子弹应该旅行。在这个例子中使用的弧度4.71。0是
在右边，1.57下降，3.14在左边。 

第三和第四个参数是子弹的开始x和y位置
佳能。第五个参数是子弹应该是的容器
添加到，第六个是子弹应该放置的阵列
成。

最后一个参数是一个返回应该是的精灵的函数
用作子弹。在这个例子中，项目符号是使用。创建的
来自游戏的加载纹理图集的“bullet.png”框架。
```js
() => g.sprite("bullet.png")
```
将此功能替换为您自己的功能以创建任何类型的自定义
子弹你可能需要。

你的子弹什么时候会被解雇？你可以调用`shoot`方法
每当你想制作子弹时，在你的代码中的任何一点。在外星人
舰队，当玩家按下空格键时会发射子弹。所以
游戏通过在空格栏内调用`shoot` 来实现这一点
`press`方法。就是这样：

```js
g.spaceBar.press = () => {

  //射击子弹
  g.shoot(
    cannon,            //大炮
    4.71,              //射击角度（4.71）
    cannon.halfWidth,  //炮的子弹x位置
    0,                 //Bullet在canon上的y位置
    g.stage,           //应该添加项目符号的容器
    7,                 //子弹速度（每帧像素）
    bullets,           //用于存储子弹的数组

    //返回应该出现的精灵的函数
    //用于制作每个子弹
    () => g.sprite("bullet.png")
  );

  //播放射击声音。
  shootSound.play();
};
```

你可以看到`press`方法也可以让`shootSound`播放。
（上面的代码在游戏的`setup`函数中被初始化。）

还有一件事你需要做：你必须让子弹移动。
你可以在游戏的循环`play`功能中使用一些代码来做到这一点。使用Hexi的
`move`方法并提供`bullets`数组作为参数：
```js
g.move(bullets);
```
`move`方法自动循环遍历所有的精灵
数组并使用它们的'vx`和'vy`速度值更新它们的x和y位置。

所以现在你知道子弹是如何创建和动画的。但是什么时候发生
他们打了一个外星人？

##### 精灵状态

当子弹击中外星人时，会出现黄色爆炸图像。这个
通过给每个外星人精灵两个状态创建简单的效果：一个“正常”
状态和“被摧毁”状态。外国人是与他们的国家创建的
设置为“正常”。如果他们被击中，他们的状态将变为“被摧毁”。

![The sprite's states](/tutorials/screenshots/18.png)

这个系统如何工作？

首先，让我们来看看这里显示的Alien Armada瓷砖：

![The Alien Armada tileset](/tutorials/screenshots/19.png)

你可以看到两个图像框架，它们定义了这两个状态：`alien.png`
和`explosion.png`。在创建精灵之前，先创建一个
列出这两个框架的数组： 
```js
let alienFrames = [
  "alien.png", 
  "explosion.png"
];
```
接下来使用`alienFrames`数组初始化`alien`精灵。
```js
alien = g.sprite(alienFrames);
```
如果您愿意，可以将这两个步骤合并为一个，如下所示：
```js
alien = g.sprite([
  "alien.png", 
  "explosion.png"
]);
```
这会将精灵加载两帧。帧`0`是`alien.png`
帧，帧`1`是'explosion.png`帧。帧'0'是
默认情况下显示在第一次创建精灵时。 

您可以使用精灵的`show`方法在其上显示任何其他帧号
精灵，就像这样：
```js
alien.show(1);
```
上面的代码将外星人设置为第一帧，这就是
`explosion.png`框架。

为了让你的代码更具可读性，定义一个好主意
你的精灵状态在一个特殊的 `states`对象中。给每个州一个
名称，其值与该状态的帧号相对应。
以下是你如何定义外星人的两种状态： `normal` 和
`destroyed`:
```js
alien.states = {
  normal: 0,
  destroyed: 1
};
```
`alien.states.normal` 现在具有值`0`，并且
`alien.states.destroyed`现在具有值`1`。这意味着你可以
像这样显示外星人的`normal`状态：
```js
alien.show(alien.states.normal);
```
并像这样显示外星人的`destroyed`状态：
```js
alien.show(alien.states.destroyed);
```
这使得你的代码更具可读性，因为你可以告诉
一目了然哪个精灵状态正在显示。

（注意：Hexi也有一个低级别的 `gotoAndStop`方法
`show`完全一样的东西。尽管你可以免费使用 `gotoAndStop`
游戏代码，按照惯例它只在Hexi的渲染内部使用
发动机。）

##### 随机产生外星人

Alien Armada在14个随机选择的职位中的任何一个职位中生成外籍人
恰好在舞台的顶部边界之上。外星人首先出现
很少，但逐渐开始以不断增加的速度出现。这使得游戏逐渐变得越来越困难。我们来看看这两个功能是如何实现的。

##### 外星人定时器

当游戏开始时，第一个新的外星人在100之后产生
帧已经过去。一个名为`alienFrequency`的变量，已初始化
游戏的“设置”功能用于帮助追踪这一点。它的
初始化为100。
```js
alienFrequency = 100;
```
另一个名为`alienTimer`的变量用于计算数量
在先前生成的外星人之间经过的帧，
和下一个。 
```js
alienTimer = 0;
```
`alienTimer`在`play`功能（游戏循环）中每帧更新1次。
当“alienTimer”达到“alienFrequency”的值时，一个新的外星人
精灵生成。这是`play`函数的代码
做这个。（这段代码省略了生成外星人的实际代码
精灵 - 我们会在未来看看）
```js
//添加一个到alienTimer
alienTimer++;

//如果`alienTimer`等于`alienFrequency`，则创建一个新的外星人
if(alienTimer === alienFrequency) {

  // ...创建外星人：请参阅前面提供的缺失代码...

  //将alienTimer设置回零
  alienTimer = 0;

  //减少一个 `alienFrequency`逐渐增加
  //外星人创造的频率
  if(alienFrequency > 2){  
    alienFrequency--;
  }
}
```
你可以在上面的代码中看到`alienFrequency`减少1
精灵创建完成后。这将使下一个外星人比我们早出现1帧
以前的外星人，这就是为什么外星人坠落速度缓慢
增加。在精灵之后，你还可以看到`alienTimer`被设置回0
已经被创建，以便它可以重新开始计数
下一个新的外星人。 

##### 随机开始位置

在我们产生任何外星人之前，我们需要一个阵列来存储所有的外星人
精灵。在`setup`中初始化一个名为`aliens`的空数组
功能为此目的。
```js
aliens = [];
```
然后每个外星人都在`play`功能中创建，在里面
我们在上面看过的'if'陈述。这段代码有很多工作要做：

- 它设置外星人的图像帧和状态。 
- 它设置外星人的速度（`vx`和`vy`）。 
- 它将外星人定位在顶级边界上方的任意水平位置。
- 最后，它将外星人推入`aliens` 数组。 

以下是完成所有这些工作的完整代码：
```js
//添加一个到alienTimer
alienTimer++;

//如果`alienTimer`等于`alienFrequency`，则创建一个新的外星人
if(alienTimer === alienFrequency) {

  //创建外星人。
  //从纹理地图集中分配两个帧作为 
  //外星人的两个国家
  let alienFrames = [
    "alien.png", 
    "explosion.png"
  ];


  //用框架初始化外星人精灵
  let alien = g.sprite(alienFrames);

  //定义外部对应的一些状态
  //到它的两个框架。
  alien.states = {
    normal: 0,
    destroyed: 1
  };
  
  
  //在屏幕边界上方设置其y位置
  alien.y = 0 - alien.height;
  
  //给外星人分配一个随机的x位置
  alien.x = g.randomInt(0, 14) * alien.width;
  
  //设置其速度
  alien.vy = 1;
  
  //将外星人推入“外星人”阵列
  aliens.push(alien);

  //将alienTimer设置回零
  alienTimer = 0;

  //减少一个“alienFrequency”逐渐增加
  //外星人创造的频率
  if(alienFrequency > 2){  
    alienFrequency--;
  }
}
```
你可以在上面的代码中看到外星人的'y`位置
在舞台顶部边界之上的视线之外。
```js
alien.y = 0 - alien.height;
```
然而，这个`x` 的位置是随机的。 
```js
alien.x = g.randomInt(0, 14) * alien.width;
```
此代码将其置于15个可能的随机位置（0到14）之一
舞台的顶部。以下是这些职位的说明：

![The Alien Armada tileset](/tutorials/screenshots/20.png)

最后，非常重要的是，代码将外星人精灵压入`aliens` 数组。
```js
aliens.push(alien);
```
所有这些代码开始以稳步增长的速度抽出外星人。

#### 移动外星人

我们如何让外星人移动？以完全相同的方式创造了
子弹移动。你会注意到上面的代码
每个外星人都用`vy` （垂直速度）值1初始化。
```js
alien.vy = 1;
```
当这个值适用于外星人的'y'位置时，它会使外星人向下移动，朝向舞台的底部，
速度为每帧1个像素。游戏中的所有外星精灵都在
 `aliens`数组。所以为了让它们全部移动，你需要循环
通过 `aliens`数组中的每个精灵，每个帧添加它们
`vy`值到他们`y`的位置。在`play`中有这样的代码
函数可以工作：
```js
aliens.forEach(alien => {
  alien.y += alien.vy;
});
```
不过，使用Hexi便捷的内置`move` 函数更容易。只是
用你想要移动的精灵阵列提供`move` ，就像
这个：
```js
g.move(aliens);
```
这会自动更新外星人的位置及其速度。

#### 让外星人爆炸

现在你知道如何改变外星人的状态，你如何使用
这个技能来制造爆炸效果？这是简化的代码
来自Alien Armada，告诉你如何做到这一点。使用`hitTestRectangle`来
检查外星人和子弹之间的碰撞。如果检测到碰撞，
删除子弹，显示外星人的 `destroyed`状态，然后移除
延迟一秒后的外星人。
```js
if (g.hitTestRectangle(alien, bullet)) {

  //删除子弹精灵。
  g.remove(bullet);

  //显示外星人的'摧毁'状态。
  alien.show(alien.states.destroyed);

  //等待1秒（1000毫秒） 
  //删除外星人精灵。
  g.wait(1000, () => g.remove(alien));
}
```
您可以使用Hexi的通用`remove`功能从游戏中删除任何精灵，如下所示：
```js
g.remove(anySprite);
```
您可以选择使用它一次删除多个精灵
列出在参数中删除的精灵，如下所示：
```js
g.remove(spriteOne, spriteTwo, spriteThree);
```
你甚至可以用它来删除一组精灵中的所有精灵。只是
提供sprite数组作为`remove`唯一的参数：
```js
g.remove(arrayOfSprites);
```
这将使得精灵从屏幕上消失，并且
将它们从他们所在的数组中清空。

Hexi还有一个方便的方法叫做`wait`，它可以运行一个函数
在您指定的任何延迟（毫秒）后。异形舰队
游戏代码使用`wait`在一秒延迟后移除外星人，
喜欢这个：
```js
g.wait(1000, () => g.remove(alien));
```
这允许外星人为其中一个显示“爆炸”图像状态
第二次在它从游戏中消失之前。

这些是使外星人爆炸的基本技术
并在游戏相撞时从游戏中移除外星人和子弹。
但在Alien Armada中使用的实际代码稍微复杂一些。那是
因为代码使用嵌套的`filter`循环遍历所有项目符号
和外星人，以便他们可以互相检查
碰撞。该代码在碰撞时也会发出爆炸声
发生，并将分数更新为1.这里是来自的所有代码
游戏的`play`功能可以做到这一点。（如果你是JavaScript的新手
`filter`循环，你可以 [read about how to use them here.](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Array/filter))
```js
//检查外星人和子弹之间的碰撞。
//通过`aliens` 数组中的每个外星人进行过滤。
aliens = aliens.filter(alien => {

  //一个变量来帮助检查外星人是否
  //活着或死亡。
  let alienIsAlive = true;

  //过滤所有的子弹。
  bullets = bullets.filter(bullet => {

    //检查外星人和子弹之间的碰撞。
    if (g.hitTestRectangle(alien, bullet)) {

      //删除子弹精灵。
      g.remove(bullet);

      //显示外星人的'摧毁'状态。
      alien.show(alien.states.destroyed);

      //你也可以使用帧号，
      //喜欢这个：
      //alien.show(1);

      //播放爆炸声。
      explosionSound.play();

      //阻止外星人移动。
      alien.vy = 0;

      //将alienAlive设置为false以便它可以
      //从数组中移除。
      alienIsAlive = false;

      //等待1秒（1000毫秒） 
      //删除外星人精灵。
      g.wait(1000, () => g.remove(alien));

      //更新分数。
      score += 1;

      //从子弹阵列中移除子弹。
      return false;

    } else {

      //如果没有碰撞，请保留子弹
      //子弹数组。
      return true;
    }
  });

  //将`alienIsAlive`的值返回给 
  //过滤循环。如果这是 `true`，外星人会
  //保存在 `aliens`数组中。 
  //如果它是'false'，它将从`aliens`数组中移除。
  return alienIsAlive;
});
```
只要过滤器循环返回 `true`,，当前精灵正在
选中将保留在数组中。如果有碰撞，但是，
循环返回 `false` ，并且当前外星人和子弹将从他们的数组中被移除。 

这就是游戏的碰撞效果！

#### 显示分数

由Alien Armada推出的另一个新功能是一个动态分数
显示。每次外星人被击中，得分在右上角
的游戏画面增加一个。这个怎么用？

Alien Armada初始化了一个名为`scoreDisplay`的`text`精灵
游戏的`setup`函数。
```js
scoreDisplay = g.text("0", "20px emulogic", "#00FF00", 400, 10);
```
你在前面的章节中看到了
每次外星人都会在游戏的`score`变量中加入1
击中：
```js
score += 1;
```
为了明显地更新分数，你需要做的就是设置`score`
值作为`scoreDisplay`的内容，如下所示：
```js
scoreDisplay.content = score;
```
这就是它的全部！

#### 结束并重置游戏

游戏结束有两种方式。任一玩家射下60
外星人，在这种情况下，玩家获胜。或者，外星人之一必须旅行
超越舞台的底部边缘，在这种情况下，外星人获胜。 

`play`函数中的一个简单的if语句检查这一点。如果
任一条件变为`true`，`winner`设置为任一条件
"player" 或 "aliens" ，游戏的`state` 变为 `end`。
```js
//如果分数与该值相匹配，则玩家获胜
//'scoreNeededToWin`，这是60
if (score === scoreNeededToWin) {

  //将玩家设置为赢家。
  winner = "player";

  //将游戏状态改为“结束”。
  g.state = end;
}

//如果其中一个达到底部，外星人会赢
//舞台。
aliens.forEach(alien => {

  //检查'外星人'的'y'位置是否更大
  //比“舞台”的“高度”
  if (alien.y > g.stage.height) { 

    //将外星人设置为胜利者。
    winner = "aliens";

    //将游戏状态改为“结束”。
    g.state = end;
  }
});
```
`end`函数暂停游戏，以便动画冻结。它
然后显示`gameOverMessage`，它将是“地球”
保存！“或”地球毁灭！“，取决于结果
触摸，音乐`volume` 也设置为50％。然后在一个
延迟3秒钟，调用名为`reset`的函数。这是
完成所有这一切的`end`函数：
```js
function end() {

  //暂停游戏循环。
  g.pause();
  
  //通过消息文本创建游戏。
  gameOverMessage = g.text("", "20px emulogic", "#00FF00", 90, 120);

  //将音乐音量减半。
  // 1是全音量，0是无音量，0.5是半音量。
  music.volume = 0.5;

  //显示“Earth Saved！” 如果玩家获胜。
  if (winner === "player") {
    gameOverMessage.content = "Earth Saved!";
    gameOverMessage.x = 120;
  }

  //显示“地球毁灭！” 如果外星人赢了。
  if (winner === "aliens") {
    gameOverMessage.content = "Earth Destroyed!";  
  }

  //等待3秒钟，然后运行“重置”功能。
  g.wait(3000, () => reset());
}
```
`reset`函数将所有的游戏变量都重置为它们的
起始值。它也将音乐音量恢复到1.它使用
`remove'功能可以从中删除任何剩余的精灵
`aliens`和`bullets`数组，以便这些数组可以
当游戏重新开始时重新填充。`remove`也用于
删除`gameOverMessage`，并且`cannon`精灵重新居中
在舞台的底部。最后，游戏 `state`被重新设置为
`play`，游戏循环通过调用Hexi的`resume`来取消暂停
方法。
```js
function reset() {

  //重置游戏变量。
  score = 0;
  alienFrequency = 100;
  alienTimer = 0;
  winner = "";

  //将音乐设置回完整音量。
  music.volume = 1;

  //删除剩下的外星人和子弹精灵。
  //通用的`remove`方法将循环
  //精灵阵列中的所有精灵，将其删除
  //从它们的父容器中取出，并将它们从数组中拼接出来。
  g.remove(aliens);
  g.remove(bullets);

  //你也可以使用通用的`remove`函数来删除。
  //一个精灵。
  g.remove(gameOverMessage);

  //重新定位大炮
  g.stage.putBottom(cannon, 0, -40);

  //将游戏状态改回“play”。
  g.state = play;
  g.resume();
}
```
这是再次开始游戏所需的所有代码。你可以玩
外星舰队无数次，只要你喜欢，它会重置并重新启动
本身就像这样无休无止。

### 飞扬的仙女

飞扬的仙女是对有史以来最臭名昭着的游戏之一的敬意：[Flappy
Bird](http://en.wikipedia.org/wiki/Flappy_Bird)。点击
下面的图像链接来玩游戏：

[![FlappyFairy](/tutorials/screenshots/21.png)](https://gitcdn.xyz/repo/kittykatattack/hexi/master/tutorials/04_flappyFairy.html)

点击“go”按钮，游戏将在全屏模式下启动。丝锥
在屏幕上的任何地方，让仙女飞起来，帮助她导航
通过缝隙在15根柱子上到达终点。五彩缤纷的足迹
仙女飞过迷宫时，仙女跟随着尘土。
如果她撞到一个绿色街区，她会在一阵沙尘中爆炸。
但如果她能驾驭越来越窄的差距
所有15根柱子，她到达一个巨大的浮动“完成”标志

![Flappy Fairy gameplay](/tutorials/screenshots/22.png)

如果你能制作出像Flappy Fairy这样的游戏，你几乎可以制作任何游戏
其他类型的2D动作游戏。除了使用你所有的技术
已经了解到，Flappy Fairy推出了一些令人兴奋的新产品：

- 以全屏模式启动游戏。
- 做一个可点击的按钮。 
- 创建一个动画精灵。
- 使用`tilingSprite`来制作滚动背景。
- 使用粒子效果。

你会在中找到完整的评论Flappy仙子源代码
`tutorials` 文件夹。一定要看看它，以便你可以看到
所有这些代码在适当的上下文中。其总体结构是相同的
到本教程中的其他游戏，并增加了这些新技术。让我们
了解它们是如何实施的。

#### 制作按钮

当你按下“Go”按钮时，游戏开始。“Go”按钮是一个特殊的精灵
称为`button` 。`button` 精灵有3个图像帧状态：up，over和
下。你可以用这样的三种状态创建一个`button`：
```js
goButton = g.button([
  "up.png",
  "over.png",
  "down.png"
]);
```
`up.png`是一个图像，它显示了按钮在不是时的样子
与指针交互。`over.png`显示按钮的外观
就像指针位于它上面一样，而`down.png`就是那个图像
当指针在按钮上按下时显示。

![Button states](/tutorials/screenshots/23.png)

（'down.png'图像略微向下偏移，所以它
看起来像被按下。）你可以分配你喜欢的任何图像
到这些状态，`button`将根据指针与它的交互方式自动显示它们。 

（注意：如果你的游戏是只触摸的，你可能只有两个按钮状态：上下，在这种情况下，只分配两个图像帧，Hexi会认为它们是指向上和向下状态。）

按钮有特殊的方法，你可以定义：`press`，
`release`，`over`，`out`和`tap`。你可以分配你喜欢的任何代码
这些方法。例如，以下是您如何更改游戏的方法
用户释放`playButton`时的状态：
```js
goButton.release = () => {
  g.state = setupGame;
};
```
按钮也有一个名为`enabled`的布尔值(true/false)属性
你如果你想禁用按钮，可以设置为`false`。（设置为 `enabled`
以`true`重新启用它。）您也可以使用按钮的`state`
属性来查明按钮状态当前是否是`"up"`, `"over"`
或 `"down"`。（这些状态值是字符串。）

重要！你可以给任何**精灵提供一个按钮的特性
将它的`interact`属性设置为`true`，如下所示：
```js
anySprite.interact = true;
```
这将使精灵`press`，`release`，`over`，`out`和`tap`
方法和与普通按钮相同的`state`属性。意即
你可以使任何精灵可点击，这对于一个真正有用的
各种互动游戏。

您还可以使`stage`对象交互，从而转变整体 
游戏画面变成交互式按钮：
```js
g.stage.interact = true;
```
有关如何使用按钮的更多详细信息，请参阅`buttons.html`文件
在`examples`文件夹中。

<a id='animatingsprites'> </a>
####动画精灵

Flappy仙女的一个整洁的特点是仙女角色掀动她的翅膀
当她飞起来的时候。这个动画是通过快速显示3创建的
连续循环中的简单图像。每个图像显示略有不同
动画的框架，如下所示：

![Animation frames](/tutorials/screenshots/24.png)

这三幅图像仅仅是游戏纹理图集中的三个普通帧，被称为
`0.png`，`1.png`和`2.png`。但是，你怎么能把这样的一系列帧变成精灵动画呢？

首先，创建一个定义动画帧的数组，例如
这个：
```js
let fairyFrames = [
  "0.png", 
  "1.png", 
  "2.png"
];
```
然后使用这些框架创建一个精灵，如下所示：
```js
let fairy = g.sprite(fairyFrames);
```
或者，如果您愿意，您可以将其合并为一个步骤：
```js
let fairy = g.sprite([
  "0.png", 
  "1.png", 
  "2.png"
]);

```
任何具有多个图像帧的精灵都会自动变成一个
动画精灵。如果你想要动画帧开始播放，
只需调用精灵的`playAnimation`方法即可：
```js
fairy.playAnimation();
```
这些帧会自动连续循环播放。如果你不想要他们
循环，将`loop`设置为`false`。
```js
fairy.loop = false;
```
使用`stopAnimation`方法停止动画：
```js
fairy.stopAnimation();
```
如果你想知道精灵的动画是否是当前的
玩，使用布尔（真/假）`玩'属性来找出。

您希望动画的播放速度有多快？你可以设置
动画的每秒帧数（`fps`）如下所示：
```js
fairy.fps = 24;
```
精灵动画的帧频独立于游戏的帧
率。这给你很多灵活性来微调精灵
动画。

如果你不想在动画中使用所有精灵的图像帧，只有其中的一部分？例如，假设您有一个30帧的精灵，但您只想播放10到15帧作为动画的一部分。为包含两个数字的数组提供`playAnimation`方法：要播放的序列的第一帧和最后一帧。
```js
animatedSprite.playAnimation([10, 15]);
```
现在只有10到15之间的帧将作为动画的一部分进行播放。做
这更具可读性，您可以将序列定义为一个数组
描述那些动画帧实际上做了什么。例如，也许
他们定义了角色的步行周期。你可以创建一个名为的数组
定义这些帧的`walkCycle`：
```js
let walkCycle = [10, 15];
```
然后用`playAnimation`来使用该数组，如下所示：
```js
animatedSprite.playAnimation(walkCycle);
```
这是更多的代码可写，但更可读！

有关Hexi精灵动画系统的更多细节以及您可以做什么
有了它，请参阅`keyframeAnimation.html`，
`examples`文件夹中的`textureAtlasAnimation.html`和`animationStates.html`文件。

#### 让仙女飞翔

现在你知道如何制作一个精灵，Flappy Fairy是如何制作的
当你点击游戏画面时会触发飞行动画？

代表重力的 `0.05`的值被从中减去
仙女的`y` 在 `play` 函数中定位每一帧。这是
将神仙拉到屏幕底部的重力效应。 
```js
fairy.vy += -0.05;
fairy.y -= fairy.vy;
```
但是当你点击屏幕时，仙女飞起来。这是多亏了
Hexi的内置 `pointer` 对象。它有一个你可以定义的 `tap`方法
执行任何你喜欢的动作。在Flappy Fairy中，每次点击时， `tap`方法会将仙女的垂直速度 `vy`提高1.5个像素。
```js
g.pointer.tap = () => {
  fairy.vy += 1.5;
};  
```
Hexi内置的`pointer`对象也有`press`和`release`方法
你可以用同样的方式定义。它也有布尔（真/假）
`isUp`，`isDown`和`tapped`属性，你可以用它来查找
指针的状态，如果你需要的话。

但是你会注意到，仙女只在她的时候才甩掉翅膀
开始飞起来，并停止扑动，当她失去动力和
开始下降。为了使这项工作，你需要知道仙女是否
目前正在上升，或正在下降，基于变化
仙女的垂直速度（vy）值。游戏实现了一个磨合良好的游戏
旧的伎俩来帮助解决这个问题。`play`功能捕捉
仙女的速度在这个当前帧中被称为`oldVy`的新值。但
它只有在仙女的位置发生变化后才会这样做*。 
```js
function play(){

  // ...
  // ...所有移动仙子的代码都是先来...
  // ...

  //然后，仙女的位置改变后，捕捉
  //她这个当前帧的速度
  fairy.oldVy = fairy.vy;
}
```
这意味着当下一个游戏框架摆动时，`oldVy`仍然会存储来自*前一帧*的仙子速度值。这意味着你
可以用这个数值来计算出仙女速度的变化
前一帧到当前帧。如果她开始上升（如果“vy”是
大于`oldVy`），扮演仙女的动画： 
```js
if (fairy.vy > fairy.oldVy) {
  if(!fairy.playing) {
    fairy.playAnimation();
  }
}
```
如果她开始下楼，停止动画并显示
仙女的第一帧。
```js
if (fairy.vy < 0 && fairy.oldVy > 0) {
  if (fairy.playing) fairy.stopAnimation();
  fairy.show(0);
}
```
这就是仙女飞行的方式！

#### 制作滚动背景

Flappy Fairy的一个有趣的新功能是它具有无限滚动功能
云从右到左移动的背景。

![Scrolling background](/tutorials/screenshots/25.png)

背景移动的速度比绿柱子慢，而且
造成了云层距离更远的错觉。（这是一个
浅，伪3D效果称为**paralax scrolling**）。 

背景只是一个图像。

![Scrolling background](/tutorials/screenshots/26.png)

该图像的设计使得无缝 **tile seamlessly**：
顶部和左侧的云与右侧的云匹配
和底部。这意味着你可以连接多个相同的实例
形象，他们会出现创造一个单一的，不间断的连续
图片。([Image from OpenGameArt.](opengameart.org/content/cartoony-sky)) 

因为这对游戏非常有用，Hexi有一个精灵类型
称为一个`tilingSprite`，这是专为这样的无限
滚动效果。以下是如何创建`tilingSprite`：
```js
sky = g.tilingSprite(
  "sky.png"              //要使用的图像
  g.canvas.width,        //宽度
  g.canvas.height,       //高度
);
```

你想要使用的图像的第一个参数，和最后两个
参数是精灵的宽度和高度。 

平铺精灵具有与普通精灵相同的属性，并添加了两个新属性：`tileX`和`tileY`。这两个属性可让您设置精灵左上角的图像偏移量。如果你想让拼贴精灵连续滚动，只需在游戏循环的每一帧中增加一些小的`tileX`值，如下所示：
```js
sky.tileX -= 1;
```
这就是你需要做的无限滚动
背景。

#### 粒子效应

你如何创造像火，烟，魔法和爆炸的效果？ 
你制造许多小小的精灵; 数十，数百或数千个。
然后对这些精灵施加一些物理或引力约束 
这样他们的行为就像你正在试图模拟的元素一样。您
还需要给他们一些关于他们应该如何出现的规则 
消失，他们应该形成什么样的模式。这些很小
精灵被称为粒子。您可以使用它们来制作广泛的范围
特效游戏。

Hexi有一个多用途的内置方法，叫做`ceateParticles`，可以
创造出你需要的多种粒子效果。这里的
使用它的格式：
```js
createParticles(
  pointer.x,                           //粒子的起始x位置
  pointer.y,                           //粒子的起始y位置
  () => sprite("images/star.png"),     //粒子函数
  g.stage,                             //将粒子添加到的容器 
  20,                                  //粒子数量
  0.1,                                 //重力
  true,                                //随机间距
  0, 6.28,                             //最小/最大角度e
  12, 24,                              //最小/最大尺寸
  1, 2,                                //最小/最大速度
  0.005, 0.01,                         //最小/最大刻度速度
  0.005, 0.01,                         //最小/最大alpha速度
  0.05, 0.1                            //最小/最大转速
);
```
你可以看到大多数参数描述了一个范围之间的范围 
应该用来更改精灵的最小值和最大值 
速度，旋转，缩放或alpha。您也可以分配数量
应该创建的粒子，并添加可选的重力。 
你可以通过自定义第三个参数来制作使用任何精灵的粒子。
只需提供一个函数返回你想要使用的精灵的种类
对于每个粒子：
```js
() => ("images/star.png"),
```
如果您提供具有多个框架的精灵，则使用`createParticles` 
方法会自动为每个粒子选择一个随机帧。
最小和最大角度值对于定义角度非常重要 
当它们从原点辐射出来时，粒子的圆形扩散。 
对于完全的圆形爆炸效果，使用最小角度0和 
最大角度为6.28。
```js
0, 6.28,
```
（这些值是弧度;度数的等效值是0和360.） 
0从3点钟位置开始，直接指向右侧。3.14
是9点的时钟位置，6.28会让你再次回到0。
如果你想限制粒子范围到一个更窄的角度， 
提供描述该范围的最小值和最大值。这里是
值可以用来限制角度与比萨饼切片 
地壳指向左边。
```js
2.4, 3.6,
```
你可以使用这样的约束角度范围来创建一个粒子
流，就像那些用来制造喷泉或火箭发动机的火焰。 
（您将会看到如何前进。）随机间隔值 
（第六个参数）确定粒子是否应该分开 
在这个范围内均匀（`false`）或随机（`true`）。
仔细选择粒子的精灵并进行精细调整 
每个参数，你可以使用这个通用的`createParticles`方法 
模拟从液体到火的一切。在Flappy Fairy中，它被使用了
创造仙尘。

##### 仙女爆炸

当飞扬的仙女击中一个街区时，她消失在一阵灰尘中。 

![Fairy dust explosion](/tutorials/screenshots/27.png)

这种效果如何起作用？

在我们创建爆炸效果之前，我们必须定义一个数组
列出我们想要用于每个粒子的图像。
正如你在上面学到的，`createParticles`方法将会随机 
如果精灵包含多个帧，则在精灵上显示一帧。 
为了使这个工作，首先定义一个纹理地图集框架的数组 
你想用于仙女的粉尘爆炸：
```js
dustFrames = [
  "pink.png",
  "yellow.png",
  "green.png",
  "violet.png"
];
```
当仙女撞到一块绿色块时发生爆炸。
游戏循环在`hitTestRectangle`的帮助下完成 
方法。代码循环遍历`blocks.children`数组并进行测试
每个绿色块和仙女之间的碰撞。如果`hitTestRectangle`
返回`true`，循环退出并调用一个碰撞对象
`fairyVsBlock`变成`true`。
```js
let fairyVsBlock = blocks.children.some(block => {
  return g.hitTestRectangle(fairy, block, true);  
});
```
`hitTestRectangle`的第三个参数必须为`true` ，以便碰撞
检测是使用雪碧的全局坐标（`gx` 和 `gy`）来完成的。
这是因为仙女是 `stage`的子集，但每个街区都是一个子集。
的`blocks`组。这意味着它们不共享相同的局部坐标空间。
使用块精灵的全局坐标力`hitTestRectangle`
使用它们相对于画布的位置

如果`fairyVsBlock`是`true`，并且仙女目前可见，那么 
碰撞代码运行。它使仙女看不见，创造粒子
爆炸，并在延迟3秒后调用游戏的`reset` 函数。
```js
if (fairyVsBlock && fairy.visible) {

  //让仙女看不见
  fairy.visible = false;

  //创建仙尘爆炸
  g.createParticles(
    fairy.centerX, fairy.centerY, // x和y位置
    () => g.sprite(dustFrames),   //粒子精灵
    g.stage,                      //将粒子添加到的容器
    20,                           //粒子数量
    0,                            //重力
    false,                        //随机间距
    0, 6.28,                      //最小/最大角度
    16, 32,                       //最小/最大尺寸
    1, 3                          //最小/最大速度
  );
  
  //停止跟踪仙子的尘埃发射器
  dust.stop();

  //等待3秒钟，然后重置游戏
  g.wait(3000, reset);
}
```

##### 使用粒子发射器

粒子发射器只是一个简单的计时器，可以在其中创建粒子 
固定间隔。这意味着，而不是仅仅调用
`createParticles`方法一次，发射器定期调用它。
Hexi有一个内置的`particleEmitter`方法，让你轻松做到这一点。
以下是如何使用它：
```js
let particleStream = g.particleEmitter(
  100,                                      //间隔
  () => g.createParticles(                  //`particleEffect`函数
    //分配粒子参数...
  )
);
```

`particleEmitter`方法仅包含`createParticles`方法。 
它的第一个参数是一个以毫秒为单位的数字，它决定了方式 
通常应该创建粒子。第二个说法是
`createParticles`方法，你可以自定义你喜欢的方法。 
`particleEmitter`方法用`play`和`stop`方法返回一个对象 
您可以使用它来控制粒子流。你可以使用它们
就像你用来控制一个精灵的`play`和`stop`方法一样 
动画。
```js
particleStream.play();
particleStream.stop();
```
发射器对象也具有“播放”属性 
取决于发射器的当前状态，`true` 或者 `false`。（见
`examples`文件夹中的`particleEmitter.html`文件以获取更多详细信息
如何创建和使用粒子发射器。）

一个粒子发射器用于飞翼仙女，使仙女发出一个 
当她拍动她的翅膀时，多彩多姿的粒子流。该
粒子被限制在2.4和3.6弧度之间的角度，所以 
他们在仙女的左边发射出一个锥形的楔子。 

![Emitting fairy dust](/tutorials/screenshots/28.png)

粒子流随机发出粉红色，黄色，绿色或紫色 
粒子，每个粒子都是纹理图集上的独立框架。

以下是创建此效果的代码： 
```js
dustFrames = [
  "pink.png",
  "yellow.png",
  "green.png",
  "violet.png"
];

//创建发射器
dust = g.particleEmitter(
  300,                                   //间隔
  () => {                         
      g.createParticles(                 //函数
      fairy.x + 8,                       //x 位置
      fairy.y + fairy.halfHeight + 8,    //y 位置
      () => g.sprite(dustFrames),        //粒子精灵
      g.stage,                           //将粒子添加到的容器            
      3,                                 //粒子数量
      0,                                 //重力
      true,                              //随机间距
      2.4, 3.6,                          //最小/最大角度
      12, 18,                            //最小/最大尺寸
      1, 2,                              //最小/最大速度
      0.005, 0.01,                       //最小/最大刻度速度
      0.005, 0.01,                       //最小/最大alpha速度
      0.05, 0.1                          //最小/最大转速
    );
  }
);
```
你现在可以用`play`和`stop`方法控制`dust`发射器。

#### 创建和移动支柱

现在你知道FLAPY精灵是如何实现Hexi的一些特殊特征的。
一些有趣的和有用的效果。但是，如果你是新的游戏
编程，你可能还想知道世界是如何飞飞的仙女
通过创建。让我们快速查看创建的代码。
移动仙女必须导航的绿色支柱
完成标志。

游戏中有十五个绿色支柱。每五根柱子
顶部和底部部分之间的间隙变得较窄。前五
柱子有四块，下五块有三块。
最后五个有两个街区的空隙。这使得游戏越来越多。
像飞舞的仙女飞得更困难。间隙的确切位置是
每一根柱子都是随机的，每次玩游戏都是不同的。每个支柱
间隔384像素，这就是它们的样子。
他们就在一起

![The green pillars](/tutorials/screenshots/29.png)

你可以看到差距从左边的四个空间逐渐变窄 
下降到两个在右边。 

所有组成支柱的街区都在一个叫做 `group` 的地方 `blocks`。
```js
blocks = g.group();
```
嵌套for循环创建每个块并将其添加到`blocks`容器。 
外循环运行15次; 一次创造每个支柱。内部循环
运行八次; 一次用于支柱中的每个块。块只是
如果他们没有占用随机选择的范围，则增加 
差距。外部循环每五次运行一次，间隙的大小就会缩小一个。
```js
//这些支柱之间的间隙的初始大小应该是多少？
let gapSize = 4;

//有多少支柱？
let numberOfPillars = 15;

//循环15次制造15个支柱
for (let i = 0; i < numberOfPillars; i++) {

  //随机将间隙放置在支柱内的某处
  let startGapNumber = g.randomInt(0, 8 - gapSize); 

  //每隔五分钟减少一次`gapSize`。这是
  //什么使差距逐渐变窄
  if (i > 0 && i % 5 === 0) gapSize -= 1; 

  //如果它不在数字范围内，则创建一个块
  //由差距占据
  for (let j = 0; j < 8; j++) {
    if (j < startGapNumber || j > startGapNumber + gapSize - 1) {
      let block = g.sprite("greenBlock.png");
      blocks.addChild(block);

      //将每个支柱间隔384个像素。第一支柱将是
      //放置在512的x位置
      block.x = (i * 384) + 512;
      block.y = j * 64;
    }
  }

  //创建柱子后，添加完成图像
  //最后
  if (i === numberOfPillars - 1) {
    finish = g.sprite("finish.png");
    blocks.addChild(finish);
    finish.x = (i * 384) + 896;
    finish.y = 192;
  }
}
```
代码的最后一部分为世界添加了大的 `finish` 精灵， 
Flappy Fairy将会看看她是否能够把它贯彻到底。

游戏循环将每组块向右移动2个像素 
框架，但只有在完成精灵离开屏幕时：
```js
if (finish.gx > 256) {
  blocks.x -= 2;
}
```
当 `finish`精灵滚动到画布的中心时， 
`blocks` 容器将停止移动。注意代码使用了
 `finish` 精灵的全局x位置（`gx`）来测试它是否在里面 
画布的区域。因为全球坐标是相对的
画布，而不是父容器，他们真的很有用 
只是这种情况下，你想要找到一个 
嵌套的精灵在画布上的位置。

请确保您查看完整的Flappy Fairy源代码
`examples`文件夹，以便您可以在适当的上下文中看到所有这些代码。

### 集成HTML、CSS

Hexi与HTML和CSS无缝协作。你可以自由地混合Hexi精灵和
代码与HTML元素，并使用Hexi的架构来建立一个HTML
基于应用。而且，您可以使用HTML构建丰富的用户
界面为您的Hexi游戏。

它是如何工作的？Hexi采取完全不干涉的方式。只要写简单的旧HTML和CSS，但是你喜欢，
然后在你的Hexi代码中引用你的HTML。就这样！Hexi
不会重新发明轮子，因此您可以编写尽可能多的低级HTML / CSS代码并将其融合 
无论您选择何种Hexi应用程序。

你可以在这个代码库中找到一个可用的例子，在 [`html` folder in Hexi's `examples`](https://github.com/kittykatattack/hexi/tree/master/examples/38_html) 。
这是一个简单的猜数字游戏：

![Number guessing game](/tutorials/screenshots/32.png)

包含按钮和文本输入字段的灰色框是HTML
元素。这些HTML元素，包括按钮，都是完全样式的
使用CSS。动态的文字和图像是Hexi精灵。

还有
一个看不见的`<div>`元素，其大小完全相同，
和Hexi的画布完全一样。大的``div>`元素
漂浮在画布上并包含灰色框，按钮和输入
领域。 

让我们快速看看这是如何工作的。`main.html`文件看起来像
这个：
```html
<!doctype html>
<meta charset="utf-8">
<title>Html integration</title>
<link rel="stylesheet" href="style.css">
<body>

<!-- UI -->
<div id="ui">
  <div id="box">
    <button>Guess!</button>
    <input id="input" type="text" placeholder="X..." maxlength="10" autofocus>
  <div>
</div>

<!-- Hexi -->
<script src="../../src/modules/pixi.js/bin/pixi.js"></script>
<script src="../../bin/modules.js"></script>
<script src="../../bin/core.js"></script>

<!-- Main application file -->
<script src="main.js"></script>
</body>
```
重要的部分是'UI'部分，就在`<body>`标签的下面。一个
带有`ui`的`div`用于包围盒子，按钮和输入。

这个魔法发生在`style.css`文件中。这是最重要的
部分：
```css
canvas
  { position : relative
  }

#ui
  { position : absolute
  ; left : 0
  ; top : 0
  ; width : 512px
  ; height : 512px

  ; z-index: 1
  }
```

Hexi的`canvas`设置为`relative`，`ui` div设置为
`absolute`。`ui`也被设置为**完全相同的宽度和高度，`512px`，
作为Hexi的画布。非常重要的是，`ui`具有`1`的`z-index`
强制它在画布上方显示。其他HTML元素（
框，按钮和输入栏）都是绝对相对的
到`ui` div  - 查看完整的CSS代码以获取详细信息。

要访问Hexi代码中的按钮和输入字段，只需创建
在Hexi的`setup`函数中引用它们：
```js
function setup() {

  //Html元素
  var button = document.querySelector("button");
  button.addEventListener("click", buttonClickHandler, false);
  var input = document.querySelector("#input");

  //...其余的设置代码创建Hexi sprites ...
```
然后创建一个普通的函数来处理按钮点击，
喜欢这个：
```js
function buttonClickHandler(event) {

  //从HTML文本输入字段捕获播放器的输入
  if (input.value) playersGuess = parseInt(input.value);

  //...其余代码...
}
```
`input.value`可以让你访问用户输入的任何内容
输入字段。这只是普通的旧式香草Web API代码 - 没有任何东西
特别！。您可以使用该值来更改任何Hexi精灵属性。
看看源代码的细节，但没有任何意外。

但是示例代码确实有一个窍门。整个Hexi
应用程序可以扩展并在浏览器中自行对齐。这意味着
Hexi的画布和UI div都放大了**和**保持一致。他们
如果用户更改浏览器窗口的大小，甚至可以重新缩放和重新对齐。怎么样
那样有用吗？这是执行此操作的JavaScript代码（在`main.js`中）
文件，在Hexi的标准初始化代码之后）：
```js
//缩放Hexi的画布
g.scaleToWindow();

//缩放html UI <div>容器
scaleToWindow(document.querySelector("#ui"));
window.addEventListener("resize", function(event){ 
  scaleToWindow(document.querySelector("#ui"));
});
```
Hexi的画布由Hexi引擎在内部缩放，但是UI层
使用全局的`scaleToWindow` 函数进行缩放。（你可以找到
关于`scaleToWindow` 函数[here](https://github.com/kittykatattack/scaleToWindow)。）

HTML和Hexi之间的这种松散集成意味着你可以自由地自定义这一点，无论你如何
喜欢。如果你想要，你可以做疯狂的低级HTML / CSS编程，混合逻辑
与你的Hexi精灵一起，并设计任何类型的自定义布局
需要。这只是HTML！而且，是的，你可以编写你的HTML
如果你愿意，可以使用Angular，React或[Elm](http://elm-lang.org)（Go Elm !!）。




