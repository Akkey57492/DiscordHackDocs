# Normal
通常のdocsに乗っているか、ほぼ周知の内容です。
これはここ以外でも乗っている内容です。

# Base
ベースURLは
https://discord.com/api/
となります。

# /users/@me
## 説明
このAPIは、tokenの情報を取得できます。
パスワード以外の基本情報です。
## サンプルコード
```py
import requests

headers = {
  "Authorization": ""
}

response = requests.get(url="https://discord.com/api/users/@me", headers=headers)

print(response.json())
```
## 成功レスポンス
- レスポンスコード: 200(Success)
## 失敗レスポンス
- レスポンスコード: 421(RateLimit)
- レスポンスコード: 403(Forbidden)
