# DXUI-Library
### 此库来之不易，使用请标明作者。
**共同维护良好的开源环境！**<br>
**QQ: 2441987560<br>
WeChat: yangzhen2441987560<br>
Email: 2441987560@qq.com**<br>
**欢迎通过各种方式提出宝贵的意见，每个周末我都会查看，有不懂的也可以找我交流。**<br><br>

一个 **超级简单、动画华丽** 的界面库<br>
取“DXUI”这个名字是因为此界面库使用Direct 2D图形库来绘制，使用Wic库实现加载图片及部分功能，使用DWrite库来绘制处理文字。<br>
* 1.控件样式可以90%自定义，并且有完善的透明度支持。<br>
* 2.支持线性与非线性的贝塞尔曲线参数动画，仅通过一行代码即可实现一个华丽的控件动画。<br>
* 3.局部刷新技术，背景图再大，上层控件动画也能流畅播放。<br>
* 4.非常简单，开发者只需要考虑如何找到好看的颜色，仅通过几行代码即可添加控件。<br>
* 5.高兼容性，无需考虑硬件支持问题，就算不支持，可无缝切换到WARP软件光栅化器，效率优于GDI。<br>
* 6.比GDI/GDI+更高的绘图质量，界面更清晰大方。<br>
* 8.极其完善的高DPI支持，再也不用担心系统缩放模糊的问题。<br><br>
预览图：<br><br>
**注意：这里的内存占用与任务管理器显示的不一致，实际远小于这个值。**<br>
* **DXUI - 示例程序预览图：**<br>
![main](https://github.com/IDXGI/DXUI-Library/blob/master/preview%20pictures/main.jpg)<br>
* **百词斩UI - DXUI示例程序预览图：**<br>
![ncz0](https://github.com/IDXGI/DXUI-Library/blob/master/preview%20pictures/ncz0.jpg)<br>
![ncz2](https://github.com/IDXGI/DXUI-Library/blob/master/preview%20pictures/ncz2.jpg)<br><br>
目前已经基本完善并能正常使用，显然我知道颜色及某些需要手动填入是比较繁琐的，后期准备向简化这部分努力。<br>
要高考了，等高考完再考虑更。<br><br>


**————————220126 更新内容————————**<br>
1.大规模代码重构及 BUG 修复。<br>
2.新增 Button_WaterWave，可以更方便地创建 Google 风格的按钮。<br>
3.新增 DClipRect，可以占用更少的内存及速度实现对子控件的裁剪。<br>
4.新增 DCombinedCon，通过继承的方式，可以实现用户自定义控件，自己处理控件响应。<br>
5.简化的用户代码的过程，减少了不必要的参数传递，并且不用再加入 Windows 消息处理回调，与DXUI的消息回调合并，真正做到很少的代码实现华丽的界面。<br>
6.新增 DString 类，实现文本窄字符和宽字符支持，即 wchar 和 char 可以轻松使用及转换。<br>
7.实现了 G++ 的编译，去除了对 VS 和 Windows SDK 的依赖。<br>
8.在 Windows 8 及以上的系统中，使用 Flip 呈现模型，极大地减少了绘制时 GPU 占用。<br>
9.优化了 64 位程序编译时的问题。<br>
10.增加 TextBox 插入符隐显动画，像呼吸一样隐显，更加自然。<br>
11.设计了 DXUI Designer，来简化控件位置、大小参数的填写，以及处理窗口大小改变时控件的位置。<br><br>

实在是累，代码量增加到了 14000 行，马上就要高考了，近期不会再更新了。<br>
**————————210221 更新内容————————**<br>
1.中等规模代码重构，图形库由D2D1.0升级为D2D1.1。<br>
2.启用Windows窗口混合的局部刷新功能，节省大部分场景下的GPU占用。<br>
3.优化控件局部刷新，减少了小部分场景下的GPU占用。<br>
4.更换TextBox与ScrollView的非线性滚动动画、插入符动画的参数，观感更加丝滑。<br>
5.较明显地优化了内存占用。<br>
6.DTransparentWindow与DWindow类合并，DWindow增加设置可以运行时无缝切换为透明窗口。<br>
7.控件背景增加实时高斯模糊选项，能动态反映出底层控件的改变。<br>
8.优化多线程调用的问题，不同线程调用更加安全。<br>
9.显示更新区域选项改为多彩闪烁，正在更新的控件更清楚。<br>
10.冗杂的零碎BUG修复。<br>
11.示例程序重新设计，将多个曾经的示例UI结合到一起，美观度++。<br><br>

一个人维护这1w+行代码实在太累了，但此库也逐渐走向成熟，设计思想也得到提升。这个假期还有一些计划好的目标，比如增加设计工具自动生成样式数据，增加控件阴影等没有实现。快开学了，要全力学习了。暑假应该可以继续更新。<br>
**————————200915 更新内容————————**<br>
1.DScrollView的BUG修复。<br>
2.DScrollView可以定位到某一位置，并且定位过程支持动画滚动。<br>
3.SetStateType()的小BUG修复。<br>
**————————2000713 更新内容————————**<br>
1.增加了DScrollView，轻松的实现滚动界面。<br>
2.优化了DTextBox及DScrollView的滚动动画，更加平滑。<br>
3.其它的一些小BUG修复。<br>
**————————200626 更新内容————————**<br>
1.解决了Win7、Win7 SP1显示不全的问题。<br>
**————————200523 更新内容————————**<br>
1.增加了GifBox，可以一行代码从文件或资源读取gif文件，并轻松播放。<br>
2.ImageBox增加了CopyFromMemory()函数。<br>
3.增加了Win10背景动态高斯模糊效果，在低版本系统无效果。<br>
4.自动设置进程的高DPI感应，如果忘记在工程设置感应也无大碍。<br>
5.一些小BUG修复及小幅优化了性能。<br>
6.作者用它编写了LightMusic播放器，用到了很多新特性，应该会发上来，看看有没有时间。<br>
**————————200424 更新内容————————**<br>
1.修复了许多的小BUG(忘了是啥了，也懒得写)，代码量由7k+增至1w+。<br>
2.TextBox增加可选平滑滚动动画、插入符动画。增加某些输入法(如微软拼音)的组合字符串实时显示。<br>
3.增加DSolidColorBox、DLinearColorBox和DRadialColorBox用来显示单调颜色、线性渐变与梯度渐变。并且后两者支持渐变起始位置和终点位置的动画。<br>
4.增加窗口阴影的透明度动画，一行代码即可实现。<br>
5.增加DTransparentWindow，与DWindow完全一样的使用方法，但可以来实现异形窗口，此类创建的窗口可没有背景色，只显示控件。<br>
6.优化TextBox字符处理部分的稳定性。<br>
7.每个控件增加整体的透明度TotalOpacity，并与填充颜色、描边颜色等透明度互不干扰，TotalOpacity也支持动画。<br>
8.优化绘制功能的性能，改进了绘制结构，在高强度绘制时有明显改善。<br>
9.优化了日常绘制时的卡顿感，还原对应帧率的真实体验。<br>
10.为确保稳定性，通知给调用者的控件消息都自动转为主线程再通知，防止调用者处理时不在同一线程而出错。<br>
11.每个动画启动时都可以设置AID，动画结束时，会发送Control_EndOfAnimation消息来通知用户，并会把启动时的AID传递过去，可据此进行处理。<br>
<br>
由于不在住所，所以没有修改示例程序的代码，旧代码可能会有些小地方不兼容。最新的程序ChatUI会在晚些时候发布。<br>
**————————200316 更新内容————————**<br>
1.根据方程的建议简化了部分冗余代码。<br>
2.修正用户手动SetState和修改TextBox文本不会触发消息的问题。<br>
3.TextBox增加GetLength()类函数。<br>
4.修正TextBox文本的裁剪区域为超出一半描边宽度的问题。<br>
5.优化了重叠的控件在动画时的更新区域。<br>
6.示例程序增加一个重叠的TextBox。<br>
**————————200315 更新内容————————**<br>
1.修复各种大大小小的BUG。<br>
2.更改控件消息的传递方式，不在WndProc里。更简洁、直接。<br>
3.简化控件消息。<br>
4.增加设置窗口阴影。<br>
5.优化动画流畅度。<br>
6.增加了控件 位置、大小、不透明度、圆角半径的动画，并且可选用贝塞尔曲线参数实现非线性动画。<br>
7.ImageBox新增一行代码实现软件多线程高斯模糊功能。<br>
8.示例程序增加了多种华丽的非线性动画。<br>
写完几个大的功能再更新吧，更新好麻烦呀。<br>
**————————191130 更新内容————————**<br>
1.修复文本框在接收文本时单击鼠标左键会无限期假死的问题。<br>
2.修改了示例程序控件的部分参数，更加美观。<br>
期中成绩优秀，最近更新没有那么积极。<br>
**————————191102 更新内容————————**<br>
1.修复文本框插入符不能左右移动的问题。<br>
2.创建渲染线程时，自动先把第一帧画上，防止显示窗口时白屏一下。<br>
3.示例程序的控件样式优化，更加美观。文本框也添加了文字颜色过渡动画。<br>
本周还是只有一天时间，而且面临期中考试，近期不会有大的更新（我太难了）。<br>
**————————191019 更新内容————————**<br>
1.修复线程锁的问题，用户可多线程调用此库。<br>
2.大幅优化ImageBox加载图片后占用的内存。<br>
3.控件被析构后，自动释放，不用再每次手动释放。<br>
4.enum语法改为C++11新特性enum class。<br>
5.修复Label在 高速修改内容 同时 鼠标在移动 时会造成动画闪烁的问题，修复后无论修改多快都完美流畅显示。<br>
6.示例程序左下角新增 系统CPU占用 和 程序内存占用 信息，并单独开了一个线程来更新信息。由于获取这些信息，示例程序代码量增到500行。<br>
7.示例程序改为静态编译，在没有VC++运行库的电脑上也能运行。<br>
因为本周只有一天时间，只优化了一些小问题，预计下次更新一周后，更新步入正轨。<br>
**————————191004 更新内容————————**<br>
1.修复了当窗口大小超出屏幕大小时，窗口坐标计算出错导致窗口无法显示的问题。问题出在示例程序上，库没有问题。<br>
由于国庆回去后段考，认真在家复习，国庆暂不更新。预计下一次更新为2周后，要添加控件的位置、大小、不透明度的动画，然后给ImageBox增加高斯模糊功能及模糊半径的动画。<br>
**————————190922 更新内容————————**<br>
1.ImageBox实现圆角功能。<br>
2.优化控件绘制时逻辑，不透明度为0时不绘图。<br>
3.TextBox的插入符颜色和宽度支持自定义。<br>
**————————190921 更新内容————————**<br>
1.优化了在客户区拖动窗口的实现方式，新方法没有任何特殊限制。<br>
2.优化ImageBox的加载函数，理论支持图片大小可达系统极限值，且上层控件动画依然流畅。还优化了加载失败后的处理。<br>
3.优化了示例程序的控件参数，使其更自然、流畅。还增加了一些控件，更好地展示此库的简单、美观。更新后示例程序去掉注释和换行，依旧只有350行左右。<br>
**———————————————————————**<br>
