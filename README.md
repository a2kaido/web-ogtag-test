# web-ogtag-test
facebook ogタグの検証用リポジトリです

## 検証に使ったデバッガ

https://developers.facebook.com/tools/debug/sharing/

## 検証に使ったページ一覧

https://a2kaido.github.io/web-ogtag-test/

## 検証結果

* 空文字は、設定してないのと同じ扱い
* descriptionか、og:descriptionに空ではない文字列が入っていたらdescriptionとして採用される
* descriptionとog:descriptionが未設定の場合(空文字含む)、なぜかページ内の`<p>タグ`がdescriptionとして採用される
  * `<p>タグ`の中である程度文字数があるものが採用される
* descriptionと、og:descriptionに文字列が入っていたらog:descriptionが優先的に採用される

## 結論

空文字ではなくて、適切な文言を設定しましょう。

