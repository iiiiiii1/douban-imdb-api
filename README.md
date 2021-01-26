
douban-imdb-api
---------------

    提示：本项目会尽量长期维护下去，使用过程中有任何问题请留言，还请大佬们右上角给个Star鼓励下。

本项目是一个基于豆瓣、`IMDB`、烂番茄评分的电影/电视剧双语(中英)数据`api`接口，目前分为数据接口和图片接口，可根据自身需求选择使用。

#### 数据接口

根据豆瓣电影/电视剧`id`，可直接获取其主演、导演、类型、编剧、评分、海报等全部中英文数据，适合用于各种影视相关需求的开发调用。

#### 图片接口

根据豆瓣电影/电视剧`id`，可直接获取其主演、导演、类型、编剧、评分、海报等全部中英文数据，并智能算出海报突出的颜色作为背景，结合海报一起合成影视数据展示图片，适合用于各种自媒体、公众号发帖贴图使用，非常美观。

![截图][1]

相关项目
----

图片鉴黄接口：https://github.com/iiiiiii1/checkimage 可判断各种类型的色情值。

更新日志
----

#### 2020.10.24

 - 重新设计数据表，查询速度大大加快

#### 2020.10.09

 - 修复部分参数获取不到的问题
 - 改善api的稳定性及获取速度

#### 2020.09.13

 - 修复生成图片 烂番茄指数不显示的问题
 - 修复英文资料中的分类获取错误

接口地址
----

#### 数据接口

    #后面的1302425为豆瓣电影/电视剧id，自己根据实际情况修改
    https://movie.querydata.org/api?id=1302425

该接口直接会返回中英文信息。

#### 图片接口

    注意：此功能使用chrome无头浏览器技术生成，第一次获取耗时较长，请耐心等待，请勿连续请求，15S内仅能请求一次。

    #中文接口，后面的1302425为豆瓣电影/电视剧id，自己根据实际情况修改
    https://movie.querydata.org/api/generateimage?id=1302425&lang=Cn

    #英文接口，后面的1302425为豆瓣电影/电视剧id，自己根据实际情况修改
    https://movie.querydata.org/api/generateimage?id=1302425&lang=En

该接口直接会返回对应的中英文信息展示图片，且`lang`为选填，不填默认返回中文信息。

请求示例
----

#### 数据接口

    #请求方式
    GET https://movie.querydata.org/api?id=1302425
    
    #请求结果
    {
        "id": "5f54ecc0fc1f587649984f63",
        "originalName": "喜劇之王",
        "imdbVotes": 6139,
        "imdbRating": "7.3",
        "rottenVotes": null,
        "rottenRating": null,
        "doubanId": "1302425",
        "imdbId": "tt0188766",
        "alias": "King of Comedy",
        "doubanVotes": 701869,
        "doubanRating": "8.7",
        "year": "1999",
        "type": "Movie",
        "duration": 5340,
        "dateReleased": "1999-02-13T08:00:00.000+08:00",
        "data": [
            {
                "genre": "喜剧/剧情/爱情",
                "name": "喜剧之王",
                "lang": "Cn",
                "language": "粤语",
                "poster": "https://image.querydata.org/movie/poster/1599401149839-g84102.jpg",
                "description": "尹天仇（周星驰 饰）一直醉心戏剧，想成为一名演员，平时除了做跑龙套以外，还会在街坊福利会里开设演员训练班。此时舞小姐柳飘飘在妈妈桑的带领下来到这里要求学做戏，原来柳飘飘有一段非常不愉快的经历，在尹天仇...",
                "country": "香港"
            },
            {
                "genre": "Comedy/Drama/Romance",
                "name": "King of Comedy",
                "lang": "En",
                "language": "Cantonese",
                "poster": "https://image.querydata.org/movie/poster/1599401152444-168dc1.jpg",
                "description": "A bar girl hires a struggling actor to give her acting lessons so that she can feign a greater interest in her customers. The longer they work together, the more they find they have in common.",
                "country": "Hong Kong"
            }
        ],
        "director": [
            {
                "data": [
                    {
                        "name": "周星驰",
                        "lang": "Cn"
                    },
                    {
                        "name": "Stephen Chow",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "李力持",
                        "lang": "Cn"
                    },
                    {
                        "name": "Lik-Chi Lee",
                        "lang": "En"
                    }
                ]
            }
        ],
        "actor": [
            {
                "data": [
                    {
                        "name": "田启文",
                        "lang": "Cn"
                    },
                    {
                        "name": "Kai Man Tin",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "周星驰",
                        "lang": "Cn"
                    },
                    {
                        "name": "Stephen Chow",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "林子善",
                        "lang": "Cn"
                    },
                    {
                        "name": "Chi-Sing Lam",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "冯勉恒",
                        "lang": "Cn"
                    },
                    {
                        "name": "Min Hun Fung",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "郑文辉",
                        "lang": "Cn"
                    },
                    {
                        "name": "Man-Fai Cheng",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "张柏芝",
                        "lang": "Cn"
                    },
                    {
                        "name": "Cecilia Cheung",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "莫文蔚",
                        "lang": "Cn"
                    },
                    {
                        "name": "Karen Mok",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "吴孟达",
                        "lang": "Cn"
                    },
                    {
                        "name": "Man Tat Ng",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "李兆基",
                        "lang": "Cn"
                    },
                    {
                        "name": "Siu-Kei Lee",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "成龙",
                        "lang": "Cn"
                    },
                    {
                        "name": "Jackie Chan",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "李思捷",
                        "lang": "Cn"
                    },
                    {
                        "name": "Sze-Chit Lee",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "陈宝骏",
                        "lang": "Cn"
                    },
                    {
                        "name": "Po-Chun Chan",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "戴龙",
                        "lang": "Cn"
                    },
                    {
                        "name": "Lung Dai",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "袁富华",
                        "lang": "Cn"
                    },
                    {
                        "name": "Fu-wah Yuen",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "叶竞生",
                        "lang": "Cn"
                    },
                    {
                        "name": "Bobby Yip Kin Sang",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "徐志雄",
                        "lang": "Cn"
                    },
                    {
                        "name": "Terence Tsui",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "侯焕玲",
                        "lang": "Cn"
                    },
                    {
                        "name": "Woon Ling Hau",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "郑祖",
                        "lang": "Cn"
                    },
                    {
                        "name": "Joe Cheng",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "胡立成",
                        "lang": "Cn"
                    },
                    {
                        "name": "Licheng Hu",
                        "lang": "En"
                    }
                ]
            }
        ],
        "writer": [
            {
                "data": [
                    {
                        "name": "周星驰",
                        "lang": "Cn"
                    },
                    {
                        "name": "Stephen Chow",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "曾瑾昌",
                        "lang": "Cn"
                    },
                    {
                        "name": "Kan-Cheung Tsang",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "冯勉恒",
                        "lang": "Cn"
                    },
                    {
                        "name": "Min Hun Fung",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "李敏",
                        "lang": "Cn"
                    },
                    {
                        "name": "Erica Lee",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "郑文辉",
                        "lang": "Cn"
                    },
                    {
                        "name": "Man-Fai Cheng",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "梁嘉杰",
                        "lang": "Cn"
                    },
                    {
                        "name": "Ka-Kit Leung",
                        "lang": "En"
                    }
                ]
            }
        ]
    }

#### 图片接口

    #请求方式
    GET https://movie.querydata.org/api/generateimage?id=1302425
    
    #请求结果
    {
        "success": 1,
        "image": "https://image.querydata.org/movie/poster/1599842781369-5f54ecc0fc1f587649984f63.png"
    }

获取后，直接下载该图片地址即可。


  [1]: https://movie.querydata.org/img/generateimage_api.png
