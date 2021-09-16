# Normal
通常のdocsに乗っているか、ほぼ周知の内容です。<br>
これはここ以外でも乗っている内容可能性が高いです。

# Base
ベースURLは<br>
https://discord.com/api/<br>
となります。

# /users/@me
https://discord.com/api/users/@me
## 説明
TokenをHeaderに渡すと、情報を得ることができます。
## サンプルコード
Python
```py
import requests

headers = {
  "Authorization": ""
}

response = requests.get(url="https://discord.com/api/users/@me", headers=headers)

print(response.json())
```
## ヘッダー
### Authorization(String)
Tokenの指定です。
## 成功レスポンス
レスポンスコード: 200(Success)<br>
レスポンスJson(例)
```json
{
  "id": "Stringj ID",
  "username": "String Name",
  "avatar": "String Avatar Hash",
  "discriminator": "String Discriminator",
  "public_flags": 0,
  "flags": 0,
  "banner": "String Banner Hash",
  "banner_color": "String Banner Color Hash",
  "accent_color": "String User Color Hash",
  "bio": "String BIO Unicode",
  "locale": "String Country Code (2 alphabed)",
  "nsfw_allowed": Boolean NSFW Access Permission,
  "mfa_enabled": Boolean 2fa Enable Check,
  "email": "String Login Email",
  "verified": Boolean Email Verify Status,
  "phone": "String Reg Phone"
}
```

## 失敗レスポンス
レスポンスコード: 421(レート制限)<br>
レスポンスコード: 403(権限無し)<br>
レスポンスJson(例)
```py
{
  "message": "401: Unauthorized",
  "code": 0
}
```
