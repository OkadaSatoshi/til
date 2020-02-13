# URI(Uniform Resource Identifier)の概要

URLから拡張された概念。一定の書式でなんらかのリソースを一意に識別するための統一書式。
サブセットとして、URL, URNがある。（どちらもURIであるという理解）

[RFC3986 日本語訳の複製](https://triple-underscore.github.io/rfc-others/RFC3986-ja.html#section-1.1.3)によると,
> 個々のスキームは、"名前" あるいは "位置指定子" のどちらか一方に分類される必要はない。

と書いてあるので、個々のURIはURLorURNのどちらかに分類されるわけではなく、両方の性質を持ったものも存在する、ということなのかな。

# URIの構造

scheme, authority, path, query, fragmentに分かれている
schemeとpathは必須。

例えば、以下のようなURIがあるとする  
(URL)foo://example.com:8042/over/there?name=ferret#nose  
(URN)urn:example:animal:ferret:nose

構造は以下のようになる(URNの方合ってるか自信ない)
|scheme|authority|path|query|fragment|
| :---: | :---: | :---:| :---: | :---: |
|foo:|//example.com:8042|/over/there|?name=ferret|#nose|
|urn:|example:|animal:|ferret:|nose|

# 疑問

- URL, URNどちらの性質も持たないURIも存在するのだろうか？

# 参考

[RFC3986 日本語訳の複製](https://triple-underscore.github.io/rfc-others/RFC3986-ja.html)
