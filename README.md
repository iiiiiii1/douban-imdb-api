douban-imdb-api
---------------
一个基于豆瓣、`IMDB`、烂番茄评分的电影/电视剧双语(中英)数据`api`接口，根据豆瓣电影/电视剧`id`，可直接获取其主演、导演、类型、编剧、评分等全部数据。

使用示例
----
### 接口地址

    #后面的111111为豆瓣电影/电视剧id
    https://www.querydata.org/api/movie?id=111111

### 接口演示

    #以下影视连接为https://movie.douban.com/subject/25907124
    https://www.querydata.org/api/movie?id=25907124
    
    #请求结果
    {
        "id": "5f54e4a4fc1f587649984eac",
        "originalName": "姜子牙",
        "imdbVotes": 0,
        "imdbRating": "",
        "rottenVotes": null,
        "rottenRating": null,
        "doubanId": "25907124",
        "imdbId": "tt11177804",
        "alias": "Legend of Deification",
        "doubanVotes": 0,
        "doubanRating": "",
        "year": "2020",
        "type": "Movie",
        "duration": 6600,
        "dateReleased": "2020-10-01T08:00:00.000+08:00",
        "data": [
            {
                "genre": "剧情/动画/奇幻",
                "name": "姜子牙",
                "lang": "Cn",
                "language": "中文",
                "poster": "https://image.querydata.org/movie/poster/1599399074442-7cg511.jpg",
                "description": "动画电影《姜子牙》的故事发生于封神大战之后。昆仑弟子姜子牙，率领众神战胜狐妖，推翻了残暴的商王朝，赢得封神大战的胜利，即将受封为众神之长。在巅峰时刻，他却因一时之过被贬下凡间。失去神力，被世人唾弃。为...",
                "country": "中国"
            },
            {
                "genre": "Animation/Family/Fantasy",
                "name": "Jiang Zi Ya",
                "lang": "En",
                "language": "Chinese",
                "poster": "https://image.querydata.org/movie/poster/1599399076347-22ag5e.jpg",
                "description": "Atop the ruins of war, top commander JIANG ZIYA is given the task to banish the Nine-tailed Fox Demon who threatens all mortals' very existence. When he discovers the Nine-tailed Fox's life...\n                    See full summary »",
                "country": "China"
            }
        ],
        "director": [
            {
                "data": [
                    {
                        "name": "程腾",
                        "lang": "Cn"
                    },
                    {
                        "name": "Teng Cheng",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "李炜",
                        "lang": "Cn"
                    },
                    {
                        "name": "Li Wei",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "李夏",
                        "lang": "Cn"
                    },
                    {
                        "name": "Xia Li",
                        "lang": "En"
                    }
                ]
            },
            {
                "data": [
                    {
                        "name": "王昕",
                        "lang": "Cn"
                    },
                    {
                        "name": "",
                        "lang": "En"
                    }
                ]
            }
        ],
        "actor": [
            {
                "data": [
                    {
                        "name": "王昕",
                        "lang": "Cn"
                    },
                    {
                        "name": "",
                        "lang": "En"
                    }
                ]
            }
        ],
        "writer": []
    }
