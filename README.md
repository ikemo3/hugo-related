# hugo-related

[Hugo][]で、関連記事を明示的に指定するためのテーマです。

## 前提条件

[Theme Components][]を使用するため、[Hugo][] 0.42以上が必要です。

## 使い方

### あるセクションの記事→別のセクションの同じタグを持つ記事

例えば`/manual/hugo`という記事があった場合、
別のセクションで`hugo`というタグが付いているものを引っ張って、表示します。

これを設定するためには、`/manual/_index.md`のFront Matterに、
以下のように書きます(YAMLの場合)
キーの`invered`は固定で、配列に入っている方がセクション名を表します。

```yaml
inverted: ["inverted"]
```

### あるセクションの記事のタグ→別のセクションの記事

逆に、`/inverted/`以下の記事でタグに`hugo`を持つものから、
`/manual/hugo`にリンクするには、`/inverted/_index.md`に以下のように記載します。

```yaml
tagref: ["manual"]
```

## ライセンス

MITライセンスです。

[Hugo]: https://gohugo.io/
[Theme Components]: https://gohugo.io/themes/theme-components/
