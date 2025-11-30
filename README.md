
douban-imdb-api
---------------

本项目是一个基于豆瓣、`IMDB`、烂番茄评分的电影/电视剧双语(中英)数据`api`接口，根据豆瓣电影/电视剧`id`，可直接获取其主演、导演、类型、编剧、评分、海报等全部中英文数据，适合用于各种影视相关需求的开发调用。
    
接口使用
----
    
    #网页中使用API获取数据的案例网页：
    https://api.wmdb.tv/testapi 可根据代码自行整合API至自己的网站中！

    #根据豆瓣id查询数据，doubanid为id，若数据库没有数据则会从维基百科等接口获取数据。doubanUrl/subject/1428581/ 最后数字1428581为doubanid
    https://api.wmdb.tv/movie/api?id=doubanid

    #支持id、imdbId、doubanId，至少需要传递其中一个
    https://api.wmdb.tv/api/v1/movie?imdbId=tt6264654
    https://api.wmdb.tv/api/v1/movie?doubanId=1302425
    
    #全文模糊搜索，根据匹配分数排序
    https://api.wmdb.tv/api/v1/movie/search?q=英雄本色&limit=10&skip=0&lang=Cn&year=2002
    q为必填，其他为选填，limit和skip用于分页，lang用于返回指定语言的查询数据，支持Cn或者En，year支持限定年份，例如q=英雄&year=2002，则只会返回张艺谋导演、李连杰主演的那一部英雄，可用于各种使用片名+年份精准获取数据的场景！

该api为测试阶段，如果全文搜索没有数据的，可使用/movie/api接口，根据豆瓣id查询数据。

相关项目
----
图片云处理服务器：[查看地址](https://github.com/bookyo/image-server-node) 可云处理图片成各种大小各种格式图片，带缓存，带自动删除冷门图片。

图片鉴黄接口：[查看地址](https://github.com/iiiiiii1/checkimage) 可判断各种类型图片的色情值。

磁力接口：[查看地址](https://github.com/iiiiiii1/magnet-vip) 可自动将磁力链接转换成种子文件提供下载，并返回磁力和磁力对应的种子的详细信息，包含文件列表信息、大小和`hashInfo`。
