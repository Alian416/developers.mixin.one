# 注册 Mixin Network 用户

### `POST /users` 

请求 Body 数据

| 参数 | 类型 | 介绍 |
| :----- | :----: | :---- |
| session_secret | String | base64 之后的 Ed25519 公钥 |
| full_name | String | 用户名 |

curl 示例

```
$$XIN:curl$$ "https://api.mixin.one/users" -X POST --data '{"full_name":"Bot User","session_secret":"MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDMTuli9K9k7F+L7Rq34se23nQeV2yvjVGCZyRTbp8qNASnRq6N679ZflgVxNUsr2qkHN4eqvafrQ9IIcRXfofMlWWIU6MrgVVD0UEVyH4jKA5gUr4smU/SDnVLqb3TojYMELIKHgqnrjqDJ0b+vMUG1Iix4fi+CvjSiJzsWPOavQIDAQAB"}'
```

返回数据

```json
{
  "data":{
    "user_id":"06aed1e3-bd77-4a59-991a-5bb5ae6fbb09",     // 用户 Id
    "session_id":"a34c07a9-755d-4b54-94c5-e45e9a2dd43e",  // 会话 Id
    "pin_token":"",                                       // 用于加密 PIN 
    "full_name":"Bot User",                               // 昵称
    "biography":"",                                       // 简介
    "avatar_url":"",                                      // 头像
    "created_at":"2018-05-03T06:03:56.867971412Z",        // 创建时间
  }
}
```