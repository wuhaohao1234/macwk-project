# macwk 资源站分析

测试官网

https://macwk.com/soft/all/p1

## 接口分析

1. 获取所有资源

地址

```shell
$ curl https://api.macwk.com/api/items/soft
```
请求方式: get
query参数
```js

meta=total_count%2Cfilter_count

sort=-modified_on

offset=20

limit=100 //这里显示请求数量

filter%5Bperfect%5D%5Beq%5D=1

fields=icon.filename_disk.%2A%2Cmodified_on%2Cslug%2Cos_version%2Cversion%2Ctitle%2Ctitle_des%2Cdescription%2Csize%2Ciscrack%2Clanguage%2Cgallery.gallery_id.filename_disk.%2A&status=published

```

response返回值分析
```json
{
    "meta": {
        "total_count": 1238,
        "filter_count": 113
    },
    "data": [
        {
            "title_des": "API文档和代码片段管理",
            "size": "22650000",
            "slug": "dash",
            "title": "Dash",
            "version": "6.2.2 (992)",
            "description": "Dash for mac 破解版是一款功能强大的API文档浏览器和代码片段管理器，内置了丰富的API文档，多达150多种，可以在线下载各种开发API和文档资料，可以让您集中管理API文档，包括离线下载、搜索、查阅，包括各种主流的编程语言和框架，如Cocos2D, Cocos3D, Corona, CSS, HTML, Java, Objective-C, JavaScript, jQuery, Vue,React等, 不需要在到处下载 API 文档，Dash 已经自动集成了，并支持集成到Webstrom、Xcode、Alfred等软件中，非常的强大！开发者必备的API文档参考工具。",
            "icon": {
                "filename_disk": "dash-2.png"
            },
            "iscrack": true,
            "language": [
                "en"
            ],
            "modified_on": "2022-01-14 03:01:49",
            "os_version": "1012_h",
            "gallery": [
                {
                    "gallery_id": {
                        "filename_disk": "dash-screen-01-1.jpg"
                    }
                },
                {
                    "gallery_id": {
                        "filename_disk": "dash-screen-02-1.jpg"
                    }
                },
                {
                    "gallery_id": {
                        "filename_disk": "dash-screen-03-1.jpg"
                    }
                },
                {
                    "gallery_id": {
                        "filename_disk": "dash-screen-04.jpg"
                    }
                },
                {
                    "gallery_id": {
                        "filename_disk": "dash-screen-05.jpg"
                    }
                },
                {
                    "gallery_id": {
                        "filename_disk": "dash-screen-06.jpg"
                    }
                }
            ]
        }
    ]
}

```
gallery 参数为产品的轮播图展示

所有借口返回值见: resource.json

2. 单个资源的接口

地址
```shell
$ curl https://api.macwk.com/api/items/soft_version
```
query参数
```
sort=sort
filter%5Bsoftid%5D%5Beq%5D=23
fields=%2A
status=published
```
response

```json
{
    "data": [
        {
            "cby": "di",
            "created_on": "2022-01-14 02:56:26",
            "download": [
                {
                    "url": "https://macwk.lanzout.com/iQDuUyr8jgj",
                    "name": "蓝奏云盘",
                    "type": 1
                }
            ],
            "id": 1180923,
            "language": [
                "en"
            ],
            "os_version": "1013_h",
            "size": "22650000",
            "softid": 23,
            "sort": 1,
            "team": "tnt",
            "version": "6.2.2 (992)"
        },
        {
            "cby": "di",
            "created_on": "2021-12-23 03:23:56",
            "download": [
                {
                    "url": "https://macwk.lanzout.com/i29y0xw2c3c",
                    "name": "蓝奏云盘",
                    "type": 1
                }
            ],
            "id": 1180637,
            "language": [
                "en"
            ],
            "os_version": "1013_h",
            "size": "22650000",
            "softid": 23,
            "sort": 2,
            "team": "tnt",
            "version": "6.2.1 (990)"
        },
        {
            "cby": "di",
            "created_on": "2021-11-11 00:18:12",
            "download": [
                {
                    "url": "https://macwk.lanzoui.com/i8TF8wdk2bi",
                    "name": "蓝奏云盘",
                    "type": 1
                }
            ],
            "id": 13143,
            "language": [
                "en"
            ],
            "os_version": "1013_h",
            "size": "21780000",
            "softid": 23,
            "sort": 3,
            "team": "tnt",
            "version": "6.2.0 (988)"
        },
        {
            "cby": "di",
            "created_on": "2021-02-07 03:45:20",
            "download": [
                {
                    "type": 1,
                    "name": "蓝奏云盘",
                    "url": "https://macwk.lanzous.com/iCJNSlf94pe"
                }
            ],
            "id": 8728,
            "language": [
                "en"
            ],
            "os_version": "1014_h",
            "size": "15810000",
            "softid": 23,
            "sort": 10,
            "team": "tnt",
            "version": "5.5.2"
        },
        {
            "cby": "di",
            "created_on": "2019-11-13 02:46:14",
            "download": [
                {
                    "type": 1,
                    "name": "蓝奏云盘",
                    "url": "https://macwk.lanzous.com/i7cbnkd",
                    "password": null
                },
                {
                    "type": 0,
                    "name": "奶牛快传",
                    "url": "https://macwk.cowtransfer.com/s/f31dd99c551d43",
                    "password": null
                },
                {
                    "type": 2,
                    "name": "城通网盘",
                    "url": "https://sn9.us/file/19991453-407513247",
                    "password": null
                }
            ],
            "id": 1116,
            "language": [
                "en"
            ],
            "os_version": "1012_h",
            "size": "13800000",
            "softid": 23,
            "sort": 11,
            "team": "tnt",
            "version": "4.6.7"
        }
    ],
    "public": true
}
```

这里尤其注意：softid为23