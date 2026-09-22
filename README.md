# kado-site

[Kado](https://github.com/Yu5rin/Kado) の公開ページ。

Google の OAuth 同意画面を**本番**に切り替えるには、ホームページ URL と
プライバシーポリシー URL が要る。その2枚だけをここに分けて置いている。

本体のリポジトリと分けてあるのは、Google に登録した URL を本体の都合から
切り離しておくため。本体側でフォルダ構成を変えても、ここの URL は動かない。

| ファイル | 役割 |
|---|---|
| `index.html` | アプリの紹介。同意画面の「アプリケーションのホームページ」に入れる |
| `privacy.html` | プライバシーポリシー。同意画面の「プライバシーポリシー リンク」に入れる |

## 公開の設定

Settings → Pages で、Source を `Deploy from a branch`、Branch を `main` / `/ (root)` にする。

公開後の URL。

```
https://yu5rin.github.io/kado-site/
https://yu5rin.github.io/kado-site/privacy.html
```

## Google 側に入れる値

[ブランディング](https://console.cloud.google.com/auth/branding)に次を入れて保存し、
[対象](https://console.cloud.google.com/auth/audience)で「アプリを公開」。

| 欄 | 値 |
|---|---|
| アプリケーションのホームページ | `https://yu5rin.github.io/kado-site/` |
| [アプリケーション プライバシー ポリシー] リンク | `https://yu5rin.github.io/kado-site/privacy.html` |
| 承認済みドメイン | `yu5rin.github.io` |

## 所有確認のファイル

承認済みドメインには [Search Console](https://search.google.com/search-console) での
所有確認が要る。`googlebb0482883758bfcb.html` がその確認用ファイル。

**消さないこと。** 消すと所有確認が外れ、同意画面の承認済みドメインも無効になる。

## 中身を変えるとき

プライバシーポリシーは本体の実装に合わせて書いてある。**書いてあることと動きが
食い違うとまずい。** データの扱いを変えたらこちらも直すこと。
