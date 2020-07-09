## 申明
本项目与Google的Flutter没有任何关系，Flutter英文字面意思为震动，FlutterGo即为用Go来实现移动端的多平台共振。
## 愿景
实现类似Flutter的跨平台开发功能，超越Flutter，解决Flutter无法解决的各种兼容问题。
## 方案
专业的事情交给专业的人来做，原生负责UI实现，GoLang包揽所有业务逻辑，整体按照MVP开发模式来进行。
## Google Flutter的优缺点
|        | Flutter |
| :----: |  :---- |
| 优点 | 1、使用全新的类似游戏开发的引擎来进行页面渲染，流畅性不错 |
|  | 2、可全部使用Flutter也可Native+Flutter结合，比较灵活 |
|  | 3、动态编译运行速度快 |
| 缺点 | 1、万年长谈，兼容性不好 |
|  | 2、生态不行 |
|  | 3、风格与原生迥异 |
|  | 4、内存占用过多 |
|  | 5、耗电大 |
|  | 6、UI绘制相当吃力 |
## FlutterGo的优缺点
|        | FlutterGo |
| :----: |  :---- |
| 优点 | 1、UI回归原生，控件没有任何坑 |
|  | 2、Go语言生态不错，只实现业务逻辑毫无难度 |
|  | 3、支持CPU密集型运算 |
|  | 4、上手容易 |
| 缺点 | 1、需要原生绘制UI |
## 对比总结
总得来讲，让原生来实现UI是最正确的事，业务逻辑按照MVP开发模式使用GoLang来实现完全可取，期待各位的加入
## FlutterGo编译环境准备
  1.准备GoLang环境
  
    请自行查阅相关文档
    
  2.获取GoMobile源码
  
    go get golang.org/x/mobile/cmd/gomobile
    
  3.配置NDK环境变量：NDK_HOME
  
  4.初始化GoMobile
    
    gomobile init
    
  5.编译Android AAR包
    
    进入go workspace即src文件夹下
    gomobile bind -target=android FlutterGo
    
  6.编译iOS Framework库
  
    进入go workspace即src文件夹下
    gomobile bind -target=ios FlutterGo
