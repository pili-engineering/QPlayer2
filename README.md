# QPlayer2



Qplayer2是一款跨平台的播放器SDK,除了基础的播放器能力外，更致力于各种应用场景的对接。SDK 包含2个库：

1. qplayer2-core:提供播放器的核心能力。
2. qplayer2-ext：一个基于应用层框架组件，更好的实现播放器场景下的UI/手势/场景切换等。

### 支持的平台

 Platform | Build Status
 -------- | ------------
 Android | 正式版已发布 
 IOS | 敬请期待 
 Windows | 敬请期待 
 Mac | 敬请期待 
### qplayer2-core 功能列表

| 能力                  | 亮点                                                         | 备注                             |
| --------------------- | ------------------------------------------------------------ | -------------------------------- |
| 媒体资源组成形式      | 一个媒体资源支持多url，比如一个音频url和一个视频url组成一个媒体资源,提升拉流速度和解封装速度 |                                  |
| 播放协议及视频类型    | http/https/rtmp flv/m3u8/mp4/flac/wav(PCM_S24LE)             | 新增协议和视频类型请联系技术支持 |
| 解码                  | 除了软解/硬解/自动解码方式外 新增混解方式，提升硬解首帧速度  |                                  |
| 色盲模式              | 能在业务场景中更好的服务视觉有障碍的客户                     |                                  |
| 倍速                  | 变速不变调                                                   |                                  |
| 清晰度切换            | 通用清晰度切换方案，无缝切换，即使媒体资源gop不对齐          |                                  |
| seek                  | 支持精准/关键帧 seek 两种方式                                |                                  |
| 指定起播位置          | 从指定位置开始播放                                           |                                  |
| 起播方式              | 起播播放/起播暂停 设置起播暂停时，起播后首帧渲染出来就停止画面 |                                  |
| 预加载                | 提前加载点播视频，获得更好的首帧体验                         |                                  |
| SEI数据回调           | 所有解码方式都支持                                           |                                  |
| 纯音频播放/纯视频播放 | 播放只有单音频流或者只有单视频流的视频                       |                                  |
| APM埋点上报           | 用于整体大盘的性能监测                                       |                                  |
| VR视频                | 支持Equirect-Angular类型的vr视频播放                         |                                  |



### qplayer2-ext 能力介绍

| 能力               | 亮点                                                         | 备注 |
| ------------------ | ------------------------------------------------------------ | ---- |
| 场景切换定制       | 当一个播放器有直播点播场景时，且2个场景的业务逻辑完全不同时，通过场景定制，能更丝滑的在2套逻辑中切换 |      |
| 播放面板定制       | 统一控制面板的显示隐藏，不同的视频场景中 可快速切换面板      |      |
| 播放器上层浮窗定制 | 拥有统一的浮窗展示隐藏动画和布局规范，更快的实现各类弹窗     |      |
| 播放器上层手势     | 支持多种手势判定回调，上层只需关心业务逻辑                   |      |



### Android

目前发布的是beta版本，欢迎大家试用，目前不建议使用该sdk 到正式环境中，正式版本会在不久的将来发布，如有意见也欢迎大家来提。

##### 引入依赖

```groovy
implementation("com.qiniu:qplayer2-core:0.0.7")
implementation("com.qiniu:qplayer2-ext:0.0.7") //如果无需qplayer2-ext能力可以不引入 不影响core的使用
```



##### 鉴权

如需使用该套sdk到其他工程中，请联系我们的技术支持开通帐号。



##### API文档

请查阅document目录下的api文档



##### Demo介绍

1. demo工程内的 长视频播放页 是基于qplayer2-ext + qplayer2-core来实现的
2. demo工程内的 短视频视频播放页 是仅基于qplayer2-core来实现的
3. 体验demo下载：http://fir.qnsdk.com/4rg5?release_id=62cfc82af945487ca599c6c0



#### 技术支持与交流

产品及服务咨询：400-808-9176

问题反馈：如有问题请提交issue

