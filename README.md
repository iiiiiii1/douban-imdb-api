
douban-imdb-api
---------------

本项目是一个基于豆瓣、`IMDB`、烂番茄评分的电影/电视剧双语(中英)数据`api`接口，根据豆瓣电影/电视剧`id`，可直接获取其主演、导演、类型、编剧、评分、海报等全部中英文数据，适合用于各种影视相关需求的开发调用。

相关说明
----

由于旧接口数据越来越多，性能受到少许影响，目前整体全部重写，读取速度从原来几百毫秒降低至30MS，支持名称模糊查询、imdbId、doubanId查询及近30个api，目前暂时放出少许接口，其它会慢慢测试并逐步开放。

对于旧接口，数据获取接口已替换成新数据库接口，用法一样，旧api：[查看地址](/old-api.md)。

## 自媒体专用图片生成：
![1637210006558-5fa652fb0cea9b0e1eba060a](https://user-images.githubusercontent.com/20472717/142352696-321b3f2c-cf04-408e-b9e9-9be47e67a24f.png)
![1637210344774-5fa652fb0cea9b0e1eba060a](https://user-images.githubusercontent.com/20472717/142352851-f1a89dbb-7dbd-425e-8b80-33c86ffdb3bf.png)

相关提示
----
很多朋友直接调用接口获取的海报image(wmdb).querydata.org等地址的图片，导致服务器每个月消耗至少8T的流量，服务器有点扛不住，所以后面会经常更换图片域名。

建议大家获取数据后，将图片本地化即可，这里顺便提供一个图片云处理服务器，直接处理图片为webp格式，体积极小，加载极快，也可直接通过API调用海报。

#### 调用示例

    https://imageserver.querydata.org/api?url=https://wmdb.querydata.org/movie/poster/no-poster.jpg&width=200&format=webp
    
    #参数详解
    url为海报地址，已经做了白名单，仅支持wmdb.querydata.org中的图片处理。
    width和height参数为海报长宽，至少需要存在一个，当仅存在其中一个时，则会保留图片宽高比自动处理！
    format为返回类型，支持jpg、png和webp，推荐使用webp，程序会判断浏览器是否支持webp，支持webp返回webp，不支持返回jpg！webp加载实在太快了！

本源码已开源，可在下方相关项目中看见github地址，也可直接使用我们搭建好的服务。
    
更新日志
----
#### 2021.12.22
- 修复生成自媒体分享图片的BUG，现在返回和生成都正常了！

#### 2021.11.25
- 新增图片处理服务API，方便大家更智能的调用图片，详情可查看接口使用！

#### 2021.11.18
- 图片生成接口全新上线，重新构建代码，效率更高！使用方式请查看接口使用！

#### 2021.11.15
- 新增前端使用API的案例页面，方便大家整合API进自己的项目中！页面地址https://api.wmdb.tv/testapi .
- 最近经常有人恶意请求页面，影响部分人使用，现添加请求限制，并暂时关闭/api/v1/movie接口！

#### 2021.11.06
- 全文搜索接口新增了更多参数，可以更精准的获取到想要的数据！新增了limit,skip,lang,year参数，具体使用请查看接口使用。

#### 2021.11.05
- 新增TOP250接口，支持IMDB和douban两种类型TOP250，支持语言选择、分页。
- 修复了IMDBID和doubanID对应问题。

#### 2021.10.28

 - 重写api，新增根据原标题+别名+剧情+多语言标题综合模糊全文搜索（根据匹配分数排序）、imdbId、doubanId查询及近30个api。

#### 2020.10.24

 - 重新设计数据表，查询速度大大加快

#### 2020.10.09

 - 修复部分参数获取不到的问题
 - 改善api的稳定性及获取速度

#### 2020.09.13

 - 修复生成图片 烂番茄指数不显示的问题
 - 修复英文资料中的分类获取错误


接口使用
----
    
    #网页中使用API获取数据的案例网页：
    https://api.wmdb.tv/testapi 可根据代码自行整合API至自己的网站中！

    #根据豆瓣id查询数据，doubanid为id，若数据库没有数据则会从维基百科等接口获取数据。doubanUrl/subject/1428581/ 最后数字1428581为doubanid
    https://api.wmdb.tv/movie/api?id=doubanid
    
    #自媒体/微博/网页引用分享等专用图片生成接口
    https://api.wmdb.tv/movie/api/generateimage?doubanId=1306123&lang=En
    doubanId是必填项，lang可选En或者Cn，分别对应英文版和中文版
    返回为json：{"image":"https://wmdb.querydata.org/movie/poster/1637210344774-5fa652fb0cea9b0e1eba060a.png","success":1}
    image就是生成的分享图片！

    #支持id、imdbId、doubanId，至少需要传递其中一个
    https://api.wmdb.tv/api/v1/movie?imdbId=tt6264654
    https://api.wmdb.tv/api/v1/movie?doubanId=1302425
    
    #全文模糊搜索，根据匹配分数排序
    https://api.wmdb.tv/api/v1/movie/search?q=英雄本色&limit=10&skip=0&lang=Cn&year=2002
    q为必填，其他为选填，limit和skip用于分页，lang用于返回指定语言的查询数据，支持Cn或者En，year支持限定年份，例如q=英雄&year=2002，则只会返回张艺谋导演、李连杰主演的那一部英雄，可用于各种使用片名+年份精准获取数据的场景！
    
    #TOP250接口
    https://api.wmdb.tv/api/v1/top?type=Imdb&skip=0&limit=50&lang=Cn
    type为必填，可选Douban或Imdb，skip和limit为分页使用，lang调用指定语言的数据，支持Cn或者En

该api为测试阶段，如果全文搜索没有数据的，可使用/movie/api接口，根据豆瓣id查询数据。

## 赞助支持
本项目 CDN 加速及安全防护由 [Tencent EdgeOne](https://edgeone.ai/zh?from=github) 赞助

[![EdgeOne Logo](https://edgeone.ai/media/34fe3a45-492d-4ea4-ae5d-ea1087ca7b4b.png)](https://edgeone.ai/zh?from=github)

相关项目
----
图片云处理服务器：[查看地址](https://github.com/bookyo/image-server-node) 可云处理图片成各种大小各种格式图片，带缓存，带自动删除冷门图片。

图片鉴黄接口：[查看地址](https://github.com/iiiiiii1/checkimage) 可判断各种类型图片的色情值。

磁力接口：[查看地址](https://github.com/iiiiiii1/magnet-vip) 可自动将磁力链接转换成种子文件提供下载，并返回磁力和磁力对应的种子的详细信息，包含文件列表信息、大小和`hashInfo`。
