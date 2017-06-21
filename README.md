### 获取社区信息
#### /site/info.json
```
{
    "title": "V2EX",                    // 社区名称
    "slogan": "way to explore",         // 社区口号
    "description": "创意工作者们的社区", // 社区描述
    "domain": "www.v2ex.com"            // 社区域名
}
```

### 获取社区状态
#### /site/stats.json
```
{
    "topic_max": 362572,  // 话题数量
    "member_max": 235408  // 用户数量
}
```
### 获取节点信息
#### /nodes/show.json?id= （id参数必须）通过节点 id 获取信息
#### /nodes/show.json?name= （name参数必须）通过节点名称获取信息
#### /nodes/all.json 获取全部节点信息
```
{
    "id": 1,  // 节点id
    "name": "babel",  // 节点缩略名
    "url": "http://www.v2ex.com/go/babel",  // 节点URL
    "title": "Project Babel",  // 节点名称
    "title_alternative": "Project Babel",  // 备选节点名称
    "topics": 1119,  // 主题数量
    "stars": 352,  // 该节点关注人数
    "header": "Project Babel - 帮助你在云平台上搭建自己的社区",  // 节点头部信息
    "footer": "Project Babel 是用 Python 语言写成的，运行于 Google App Engine 云计算平台上的社区软件。",  // 节点脚部信息
    "created": 1272206882,  // 节点创建时间
    "avatar_mini": "//v2ex.assets.uxengine.net/navatar/c4ca/4238/1_mini.png?m=1494924246",  // 节点的小图标
    "avatar_normal": "//v2ex.assets.uxengine.net/navatar/c4ca/4238/1_normal.png?m=1494924246",  // 节点的标准图标
    "avatar_large": "//v2ex.assets.uxengine.net/navatar/c4ca/4238/1_large.png?m=1494924246"  // 节点的大图标
}
```
