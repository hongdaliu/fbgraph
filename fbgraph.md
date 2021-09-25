
### 多用户授权
http://skylerluxury.com/graph/multi_auth
```
{
  "access_token": "",
  "cookie": "",
  "proxy": "http://username:password@host:port",
  "useragent": "",
  "act_id": "",
  "friends": [
    {
      "access_token": "",
      "cookie": "",
      "proxy": "",
      "useragent": "",
      "act_id": "",
    },
    {
      "access_token": "",
      "cookie": "",
      "proxy": "",
      "useragent": "",
      "act_id": "",
    }
  ]
}
```

### 删除指定授权用户
http://skylerluxury.com/graph/remove_user_role
```
返回值
{
  "code": 0
}

参数说明
proxy
cookie
useragent
removeUserID 需要删除授权用户的USER_ID
actID
```


### 创建Page
http://skylerluxury.com/graph/create_page
```
返回值
{
  "code": 0,
  "page_id": "2352353245262"
}

参数说明
proxy
cookie
useragent
name 名称
category 分类ID
description 描述
```
