# ログイン

VRChatのAuthCookieを用いたログインを実装しています。

![ログイン画面](./img/login.png){ width="400" }

アプリケーションを起動すると上記ウィンドウが表示されるため、ウィンドウの指示に従い、以下の操作を行います。

1. [VRChatへログイン](https://vrchat.com/home/login)
    - 通常通りログインします。
1. [AuthCookieの取得](https://vrchat.com/api/1/auth)
    - 以下のように表示されているものを `authcookie` から末尾の `"` の前までコピーしてウィンドウにペーストします。

    ![AuthCookieの取得](./img/authcookie.png)
1. 入力欄にペーストして認証ボタンをクリック
    - 入力欄に `authcookie_xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx` と入力されていることを確認し、認証ボタンをクリックすることで認証が行われます。

## 認証情報について

入力された認証情報は `Base64` でエンコードを行い実行されているユーザーのプロファイル配下に保存されます。

具体的なパスは以下の通りです。

`%localappdata%/じゅううん/AvatarManager*/`