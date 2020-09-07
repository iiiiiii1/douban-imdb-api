douban-imdb-api
---------------
一个基于豆瓣、`IMDB`、烂番茄评分的电影/电视剧双语(中英)数据`api`接口，根据豆瓣电影/电视剧`id`，可直接获取其主演、导演、类型、编剧、评分、海报等全部中英文数据。

使用示例
----
### 接口地址

    #后面的23333为豆瓣电影/电视剧id
    https://www.querydata.org/api/movie?id=23333

### 接口演示

    #请求示例
    GET https://www.querydata.org/api/movie?id=1302425
    
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

问题反馈
----
如果使用过程中，有部分id获取不到信息，请留言即可，并附上id号。
