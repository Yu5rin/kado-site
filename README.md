# slideinacalendar-site

[SlideinaCalendar](https://github.com/Yu5rin/SlideinaCalendar) の公開ページ。

Google の OAuth 同意画面を**本番**に切り替えるには、ホームページ URL と
プライバシーポリシー URL が要る。本体のリポジトリは private で、
要件書や実働日のデータが入っているため公開できない。この2枚だけを分けて置いている。

| ファイル | 役割 |
|---|---|
| `index.html` | アプリの紹介。同意画面の「アプリケーションのホームページ」に入れる |
| `privacy.html` | プライバシーポリシー。同意画面の「プライバシーポリシー リンク」に入れる |

## 公開の設定

Settings → Pages で、Source を `Deploy from a branch`、Branch を `main` / `/ (root)` にする。

公開後の URL。

```
https://yu5rin.github.io/slideinacalendar-site/
https://yu5rin.github.io/slideinacalendar-site/privacy.html
```

## Google 側に入れる値

[ブランディング](https://console.cloud.google.com/auth/branding)に次を入れて保存し、
[対象](https://console.cloud.google.com/auth/audience)で「アプリを公開」。

| 欄 | 値 |
|---|---|
| アプリケーションのホームページ | `https://yu5rin.github.io/slideinacalendar-site/` |
| [アプリケーション プライバシー ポリシー] リンク | `https://yu5rin.github.io/slideinacalendar-site/privacy.html` |
| 承認済みドメイン | `yu5rin.github.io` |

承認済みドメインは [Search Console](https://search.google.com/search-console) での
所有確認が要る。`https://yu5rin.github.io/slideinacalendar-site/` を URL プレフィックスで
登録し、HTML ファイルをこのリポジトリの直下に置いて確認する方法が手早い。

## 中身を変えるとき

プライバシーポリシーは本体の実装に合わせて書いてある。**書いてあることと動きが
食い違うとまずい。** データの扱いを変えたらこちらも直すこと。
