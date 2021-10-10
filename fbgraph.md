### 异常返回信息
```
{
  "code": 1,
  "error": ""
}
```

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
removeUserCookie 需要删除授权用户的Cookie
actID
```


### 创建Page
http://skylerluxury.com/graph/create_page
```
返回值
{
  "code": 0,
  "data": {
    "page_id": "2352353245262"
  }
}

参数说明
proxy
cookie
useragent
name 名称
category 分类ID
description 描述
```

### 关闭Page通知
http://skylerluxury.com/graph/close_page_notification
```
返回值
{
  "code": 0
}

参数说明
proxy
cookie
useragent
pageName
pageID
```

### 查看账号质量
http://skylerluxury.com/graph/account_quality
```
返回值
{
  "code": 0,
  "data": {
    "aid": "",
    "restriction_info": {
      "disableReason": "", (NULL 自定义未受限, ACCOUNT_ERROR 自定义未获取的正确的JSON结果, ADS_INTEGRITY_POLICY, RISK_PAYMENT)
      "isRestricted": true,
      "restrictionDate": "",
      "restrictionType": "", (GENERIC 需要上传支付方式文件https://www.facebook.com/help/contact/391647094929792或者需要确认账户, ALR, ALE)
      "validStatus": 0 (1-验证卡, 2-验证账号)
    }
  }
}

参数说明
proxy
cookie
useragent
aid (NOTE: 可选)
```

### 绑定信用卡
http://skylerluxury.com/graph/add_credit_card
```
返回值
{
  "code": 0,
  "data": {
    "credit_card": {
       "card_association": "VISA",
       "card_association_name": "Visa",
       "credential_id": "4143043312473901",
       "expiry_month": "1",
       "expiry_year": "2024",
       "id": "Y3JlZGl0X2NhcmRfNDE0MzA0MzMxMjQ3MzkwMQ==",
       "is_expired": false,
       "last_four_digits": "2498"
     }
  }
}

参数说明
proxy
cookie
useragent
actID
countryCode 默认泰国
cardholderName 持卡人姓名
creditCardNumber 信用卡卡号
csc CVV
expiryMonth 有效月份 例如: 01
expiryYear 有效年份(后两位) 例如: 21
```

### 绑定信用卡成功后查询计费阈值
http://skylerluxury.com/graph/billing_threshold
```
返回值
{
    "code": 0,
    "data": {
        "currency": "THB",
        "formatted_amount_no_symbol": "70.00"
    }
}

参数说明
proxy
cookie
useragent
actID
```
