# BiliBili Video Player 传入参数整理


#### 引言

若寻找关于 HTML中`<iframe>`标签的内容 请挪步 [W3S](https://www.w3school.com.cn/tags/tag_iframe.asp) [菜鸟教程](https://www.runoob.com/jsref/dom-obj-frame.html) 

部分信息来自 [王陸 - 关于博客园内嵌入bilibili视频](https://www.cnblogs.com/wkfvawl/p/12268980.html)

因官方未给出播放器参数的官方文档，为便于查阅，MonianHello 在此处整理了部分内容。

[bilibili-API-collect](https://socialsisteryi.github.io/bilibili-API-collect/)

如有补充可提交issue

<u>MonianHello 2021.2</u>

#### 播放器地址

##### (Old)bilibili html5 player

`http://player.bilibili.com/player.html`

例

`http://player.bilibili.com/player.html?bvid=BV1ux41147Eh&danmaku=0&autoplay=1`

##### (New)bilibili new player

`http://www.bilibili.com/blackboard/newplayer.html`

例

`http://www.bilibili.com/blackboard/newplayer.html?bvid=BV1ux41147Eh&danmaku=0&autoplay=1`

#### 传入参数说明

|     参数     | 数据类型 |                     说明                     |
| :----------: | :------: | :------------------------------------------: |
|     bvid     |  字符串  |            BV号(需要添加"BV"字符)            |
|     aid      |   整型   |            av号(无需添加"av"字符)            |
|     cid      |   整型   |               视频标识号(可选)               |
|     page     |   整型   | 第几个视频, 起始下标为 1(超出默认为1) (可选) |
|   as_wide    |  布尔型  |               是否宽屏 (可选)                |
|   autoplay   |  布尔型  |             是否自动播放 (可选)              |
|   danmaku    |  布尔型  |             是否打开弹幕 (可选)              |
| high_quality |  布尔型  |  ==[仅旧版本可用]== 是否播放最高画质 (可选)  |
|     ...      |   ...    |                  待补充...                   |

#### 注释

> 参见 [王陸 - 关于博客园内嵌入bilibili视频](https://www.cnblogs.com/wkfvawl/p/12268980.html)

##### 获取aid、bvid和cid

Bilibili网页端转发视频的时候直接可以看到嵌入代码 

从嵌入代码中可以直接得到aid、bvid和cid

##### aid/bvid与cid区别

aid为视频的av号，bvid为视频的BV号。

但是每个av(BV)号下不一定只有1p

所以B站用cid来管理视频的真正id

那么也可以说如果视频只有1p，那么cid就无用了 

在此建议使用page代替cid

#####  仅旧版本可用 最高画质的说明

如视频有 360p 720p 1080p 三种

默认或者 high_quality=0 是最低 360p

high_quality=1 是最高1080p




