## V2EX-API
请求 API 的 URL 为 `https://www.v2ex.com/api/`

默认情况下，请求方式均为GET请求，每个 IP 每小时可以发起的 API 请求数被限制在 120 次
### 获取社区信息
  * `/site/info.json`
```
{
    "title": "V2EX",                    // 社区名称
    "slogan": "way to explore",         // 社区口号
    "description": "创意工作者们的社区", // 社区描述
    "domain": "www.v2ex.com"            // 社区域名
}
```

### 获取社区状态
* `/site/stats.json`
```
{
    "topic_max": 362572,  // 话题数量
    "member_max": 235408  // 用户数量
}
```
### 获取节点信息
* `/nodes/show.json?id=` （id 参数必须）通过节点 id 获取信息
* `/nodes/show.json?name=` （name 参数必须）通过节点名称获取信息
* `/nodes/all.json` 获取全部节点信息
```
{
    "id": 1,
    "name": "babel",
    "url": "http://www.v2ex.com/go/babel",
    "title": "Project Babel",
    "title_alternative": "Project Babel",
    "topics": 1119,
    "stars": 352,
    "header": "Project Babel - 帮助你在云平台上搭建自己的社区",
    "footer": "Project Babel 是用 Python 语言写成的，运行于 Google App Engine 云计算平台上的社区软件。",
    "created": 1272206882,
    "avatar_mini": "//v2ex.assets.uxengine.net/navatar/c4ca/4238/1_mini.png?m=1494924246",
    "avatar_normal": "//v2ex.assets.uxengine.net/navatar/c4ca/4238/1_normal.png?m=1494924246",
    "avatar_large": "//v2ex.assets.uxengine.net/navatar/c4ca/4238/1_large.png?m=1494924246"
}
```

### 获取用户信息
* `/members/show.json?id=` （id 参数必须）通过用户 id 获取用户信息
* `/members/show.json?username=` （username 参数必须）通过用户名称获取用户信息
```
// 得到用户的基本信息
{
    "status": "found",
    "id": 126679,
    "url": "http://www.v2ex.com/member/igaozp",
    "username": "igaozp",
    "website": "",
    "twitter": "",
    "psn": "",
    "github": "igaozp",
    "btc": "",
    "location": "",
    "tagline": "",
    "bio": "",
    "avatar_mini": "//v2ex.assets.uxengine.net/avatar/75cc/4c25/126679_mini.png?m=1495115425",
    "avatar_normal": "//v2ex.assets.uxengine.net/avatar/75cc/4c25/126679_normal.png?m=1495115425",
    "avatar_large": "//v2ex.assets.uxengine.net/avatar/75cc/4c25/126679_large.png?m=1495115425",
    "created": 1436623834
}
```

### 获取主题信息
* `/topics/hot.json` 获取社区每天最热的10个主题
* `/topics/show.json?id=` （id 参数必须）通过主题 id 获取主题的信息
* `/topics/show.json?username=` （username 参数必须） 通过用户名称获取用户的主题列表
* `/topics/show.json?node_name=` （node_name 参数必须） 通过节点名称获取该节点下的主题列表
* `/topics/show.json?node_id=` （id 参数必须） 通过节点 id 获取该节点下的主题列表
```
{
        // 主题的基本信息
        "id": 369998,
        "title": "求教：如果想挖优秀的 Python ，什么才算是有吸引力的条件?",
        "url": "http://www.v2ex.com/t/369998",
        "content": "除了与能力相匹配的工资（ 20K+）、五险一金、双休、下午茶、高大上的办公环境、各种好相处的同事、早 10 晚 6:30 的工作时间（不加班）之外，还需要什么？求大神们赐教~~~~~",
        "content_rendered": "除了与能力相匹配的工资（ 20K+）、五险一金、双休、下午茶、高大上的办公环境、各种好相处的同事、早 10 晚 6:30 的工作时间（不加班）之外，还需要什么？求大神们赐教~~~~~",
        "replies": 74,
        // 主题作者的相关信息
        "member": {
            "id": 236187,
            "username": "131452p",
            "tagline": "",
            "avatar_mini": "//v2ex.assets.uxengine.net/gravatar/2c2d8f49c0e73ee73515e49483325f58?s=24&d=retro",
            "avatar_normal": "//v2ex.assets.uxengine.net/gravatar/2c2d8f49c0e73ee73515e49483325f58?s=48&d=retro",
            "avatar_large": "//v2ex.assets.uxengine.net/gravatar/2c2d8f49c0e73ee73515e49483325f58?s=73&d=retro"
        },
        // 主题发布节点的相关信息
        "node": {
            "id": 90,
            "name": "python",
            "title": "Python",
            "title_alternative": "Python",
            "url": "http://www.v2ex.com/go/python",
            "topics": 7102,
            "avatar_mini": "//v2ex.assets.uxengine.net/navatar/8613/985e/90_mini.png?m=1497939308",
            "avatar_normal": "//v2ex.assets.uxengine.net/navatar/8613/985e/90_normal.png?m=1497939308",
            "avatar_large": "//v2ex.assets.uxengine.net/navatar/8613/985e/90_large.png?m=1497939308"
        },
        "created": 1498012527,
        "last_modified": 1498012527,
        "last_touched": 1498098068
    },
```

### 获取主题回复
* `/replies/show.json?topic_id=` （topic_id 参数必须） 通过主题 id 获取该主题下的所有回复
```
{
    // 主题回复的基本信息
    "id": 4447209,
    "thanks": 0,
    "content": "工作流程怎么样？\r\nPM 会不会随意改需求？",
    "content_rendered": "工作流程怎么样？\r<br />PM 会不会随意改需求？",
    "member": {
        "id": 124253,
        "username": "joeHuang",
        "tagline": "None",
        "avatar_mini": "//v2ex.assets.uxengine.net/avatar/29b5/0fbb/124253_mini.png?m=1437789219",
        "avatar_normal": "//v2ex.assets.uxengine.net/avatar/29b5/0fbb/124253_normal.png?m=1437789219",
        "avatar_large": "//v2ex.assets.uxengine.net/avatar/29b5/0fbb/124253_large.png?m=1437789219"
    },
    "created": 1498013146,
    "last_modified": 1498013146
}
```
