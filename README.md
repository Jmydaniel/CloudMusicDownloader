# CloudMusicDownloader

只想简单的保存一首音乐而不希望登录账号或下载客户端? CloudMusicDownloader(LUD) 可以帮助您以最简单的方式找到您想要的歌曲并以本地.mp3格式呈现给您!

**请注意, CloudMusicDownloader(LUD)不会尝试破解网易云音乐的正常机制，你只能下载/转换自己有权播放的歌曲**

~~由于MucheXD对这个项目已经摆烂的开发态度~~，某些功能可能会有严重Bug。你可以提交一个Issue，然后猜猜MucheXD会不会修 :P

---

## 使用方法

本程序部分功能接入网易云官方API，使用时请确保网络环境。如果网络环境较差，则部分功能使用时可能造成程序假死(未响应)及其它未知异常。

### 载入

#### 在线检索

1.`载入`功能可以帮助你找到你想要的歌曲。在菜单栏找到`载入`以打开载入功能区。

2.在左侧的下拉框中，你可以选择搜索的模式。在右侧输入框输入搜索内容后点击`搜索`，程序会自动提交搜索请求并向你展示结果。

> 如果没有你需要的结果，请更换关键词或点击`更多结果`

> 需要注意，由于网易云对外部API调用的限制，目前无法载入歌单与专辑，但可以读取其信息。

3.找到你需要的结果，点击右侧的`选择`，然后你就可以在待选列表功能区中找到解析出的所有单曲。

> 如果选择下载的歌曲只提供试听版本，"选择"按钮将被"选择试听"取代

4.点击右侧的`详细信息`可获取歌曲的歌词/MV链接等，你可以选择复制歌词或将歌词附加到下载。

#### 缓存检索

1.在`载入`功能区中下拉左侧下拉框，选择`本地缓存`。

2.如果你需要自定义载入缓存文件(.uc/.uc!)，在右侧输入框中输入该路径，否则请直接点击`搜索`，程序会自动检索网易云音乐桌面端的默认缓存位置。

3.点击`选择`，然后你就可以在待选列表中找到解析出的所有单曲。

> 所谓"缓存"，是指网易云音乐桌面端在播放歌曲过程中生成的临时文件，其质量等均由播放时的客户端设置决定。如果找不到你需要的缓存文件，请尝试打开网易云音乐桌面端播放你需要的歌曲一遍。

> 如果你选择载入本地缓存，那么此过程将无需连接互联网。

#### 匹配歌曲信息

网易云音乐客户端生成缓存文件的文件名是一串字符串，此时你可以通过匹配歌曲信息功能获取该文件的歌名/作者等信息。

1.选择缓存文件(参见"缓存检索")，此时在待选列表中会增加一个按钮`匹配信息`

2.点击`匹配信息`即可自动为列表中的缓存文件匹配歌曲信息

> 此过程需要连接互联网

> 匹配以文件名为依据，格式为"[歌曲ID]-[比特率]-[随机后缀]"。这是默认的网易云生成规则，但如果你更改了文件名，匹配功能将失效。

### 附带歌词的下载

本程序支持获取对应歌曲的歌词，附加的歌词将与歌曲一同保存到同一目录下，可以由支持lrc歌词格式的播放器识别。

在`待选列表`功能区切换`附词...`下拉框以选择合适版本的歌词，当选择后，当前所有加载于本页的歌曲均会附加歌词下载标签。

### 选择并下载

1.在待选列表勾选你需要输出的歌曲，点击开始下载即可。

2.你可以在`当前任务`中找到工作信息，包括工作进度，工作速度(仅下载)等。

3.下载完成后，点击上方`打开目录`即可找到输出的文件。

> 不建议一次性下载太多项，否则可能被网易云服务器封禁IP地址。

> 如果项来源是本地缓存，那么该过程即使不连接互联网也能进行

> 如果选择下载的歌曲不是开放歌曲，那么可能显示"无法获取下载内容大小"

### 设置

- 该功能正在开发中，已被隐藏，接下来可能不被开发，具体视用户需求决定。

## 关于程序

### 效率测试 (缓存转换)

>总文件数: 300
>
>总大小: 972MB
>
>LUD_V0.4.2+运行用时(不附词): 8090ms
>
>NMTC运行用时: 122290ms
>
>LUD_V0.4.2+效率(不附词): 8.3ms/MB
>
>NMTC效率: 124.7ms/MB(快速模式)
>
>LUD_V0.3.0数据: 318/981MB/9640ms/9.8ms/MB
>
>效率提升(较NMTC): 93.3%
>
>效率提升(较V0.3.0): 15.3%
>
>结果哈希值: 相同

### NMTC替换解决方案

本程序几乎可以完美替换原解决方案NMTC，且有一定的效率提升与附加功能。

要载入缓存文件，请参阅[缓存检索](https://github.com/MucheXD/CloudMusicDownloader#缓存检索)

效率提升：参阅[效率测试](https://github.com/MucheXD/CloudMusicDownloader#效率测试)

+ LUD额外支持匹配歌曲信息功能。
+ LUD支持移动设备端的缓存文件 (.uc!)

### 环境说明

以下列出建议的运行环境

> Runtime: Microsoft Visual C++ 2015-2019 Redistributable
>
> System: Windows 10 / Windows 11
>
> RAM: 128MB+ (free)

如果您下载的是单文件版本，则需要附加QT运行时库

### 制作与版权

#### 程序制作者

+ 代码逻辑/UI界面: MucheXD 100%

+ 内部图标提供方: iconfont (https://www.iconfont.cn/)

+ 字体: 默认为微软雅黑，但是非嵌入式的。调用文件: .ui

#### 版权与许可证

本程序最新版本使用以下编译器或支持库

+ VisualStudio 2022

+ QT 6.7.2

详细许可证内容请参阅其对应的官方网站
