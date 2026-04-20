[study-notes](../README.md) > HTML

---

# HTMLメモ

HTMLに関する知識をまとめる。

---

## 📋 内容
#### グローバル属性
参考：https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Global_attributes

| 要素       | 説明      | URL |
| ----       | ----    | ---- |
| class=""   | 要素の再利用可能なクラスの属性。スペース区切りで複数書ける | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/nav |
| id=""      | 全体で単一の要素を識別するための属性 | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Global_attributes/id |
| tabindex="" | "0"でタブ到達可能、"-1"でタブ到達不可能 | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Global_attributes/tabindex 
| hidden     | 要素を非表示にする | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Global_attributes/hidden
| data-*=""  | カスタムデータ属性で、HTMLElement.datasetプロパティの*でアクセス可能にする | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Global_attributes/data-*

#### フローコンテンツ
参考：https://developer.mozilla.org/ja/docs/Web/HTML/Guides/Content_categories#%E3%83%95%E3%83%AD%E3%83%BC%E3%82%B3%E3%83%B3%E3%83%86%E3%83%B3%E3%83%84

| 要素     | 説明      | URL |
| ----    | ----      | ---- |
| \<a>    | hrefを用いてリンク先へ移動する | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/a |
| \<ul>   | 順序なしリスト（箇条書き） | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/ul |
| \<ol>   | 順序ありリスト（数）   | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/ol |
| \<li>   | \<ul>\<ol>の子要素   | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/li |
| \<p>    | テキストブロック            | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/p |
| \<header> | 導入部、ナビゲーションコンテンツ、ロゴ、検索フォームなどのヘッダー要素 | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/header 

#### 区画分類
参考：https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/section#%E4%BD%BF%E7%94%A8%E4%B8%8A%E3%81%AE%E3%83%A1%E3%83%A2

| 要素       | 説明      | URL |
| ----       | ----    | ---- |
| \<nav>     | メニュー、目次等のナビゲーションコンテンツ | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/nav |
| \<article> | 商品、記事、コメントなど不可分の1つ1つ | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/article
| \<aside>   | 文章に対しての補足など。直接的な重要性が低い | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/aside
| \<main>    | WEB・アプリの中心的な機能・コンテンツ | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/main
| \<div>     | CSSでスタイルを付けるための意味を定義しないまとまり| https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/div |
| \<span>    | CSSでスタイルを付けるための意味を定義しないまとまり| https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/span |
| \<section> | 見出しh1～h6要素で意味を定義するまとまり | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/section

（divはブロックレベルコンテンツ、spanはインラインレベルコンテンツ。）

その他用語
| 用語      | 説明      | URL  | 
| ----    | ----    | ---- |
| ブロックレベルコンテンツ   | 要素ごとに改行。親の幅分使う。縦に並ぶ | https://developer.mozilla.org/ja/docs/Glossary/Block-level_content |
| インラインレベルコンテンツ | 改行されない。必要な分だけ幅を使う。横に並ぶ | https://developer.mozilla.org/ja/docs/Glossary/Inline-level_content |
| サイドバー                | Webページの横に表示され、情報や操作を補助するペイン（枠）| https://developer.mozilla.org/ja/docs/Mozilla/Add-ons/WebExtensions/user_interface/Sidebars |
| コールアウトボックス       | 操作に対してよく出る、注意・エラー・ヒントなど重要な情報を強調するUIパターン | -
| ナビゲーションコンテンツ | ヘッダーやパンくずリストなど他のページへの導線 | -
#### 引用
| 要素          | 説明     | URL |
| ----          | ----    | ---- |
| \<blockquote> | 引用を内包するときに使用する | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/blockquote
| \<cite>       | 引用元をマークアップするときに使用する | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/cite

#### キャプション付の図
| 要素          | 説明     | URL |
| ----          | ----    | ----|
| \<figure>     | 図のブロックを表す際に使用する。キャプションがつけられる | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/figure
| \<img>        | 画像を埋め込む                                       | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/img
| \<figcaption> | \<figure>内のキャプションを書く                       | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/figcaption

#### 検索フォーム
| 要素          | 説明     | URL |
| ----          | ----    | ----|
| \<search>    | 検索やフィルターであることを表すコンテナ | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/search
| \<form>      | Webサーバーへの送信情報を含む区間 | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/form
| ^            | action属性は送信先のURLを指定する | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/form#action
| ^            | method属性はHTTPメソッド（post/get/dialog）を指定する | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/form#method
| \<input>     | ユーザー操作可能なコントロールを作成する               | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/input |
| ^            | type属性で、テキストボックスやチェックボックスなど様々な型を使用できる | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/input#input_%E3%81%AE%E5%9E%8B
| \<label>     | \<input>等のユーザーインターフェースのキャプション。for属性で紐づけてクリックに反応させられる | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/label
| \<button>    | 操作可能要素でフォームの送信やダイアログの表示ができる | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/button |

#### ポップオーバー
- 参考
  - https://developer.mozilla.org/ja/docs/Web/API/Popover_API

| 用語          | 説明          | URL |
| ポップオーバー | コンテンツの上にコンテンツを表示すること | https://developer.mozilla.org/ja/docs/Web/API/Popover_API
| モーダル      | ポップオーバー表示中に後ろのコンテンツが反応しないようにする | ^
| 非モーダル    | ポップオーバー表示中も後ろのコンテンツが反応する | ^

#### 強調表示
- 参考
  - https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/b#%E4%BD%BF%E7%94%A8%E4%B8%8A%E3%81%AE%E3%83%A1%E3%83%A2
| 要素        | 説明      | URL  |
| ----          | ----    | ----|
| \<strong>   | 重要な単語や文章の強調（デフォで太字） | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/strong
| \<em>       | 文章内の軽い強調（デフォで斜体） | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/em
| \<mark>    | 検索結果に対して検索文字を強調するなど（デフォでマーク） | https://developer.mozilla.org/ja/docs/Web/HTML/Reference/Elements/mark

#### ロール
| 用語          | 説明          | URL |
| ----    | ----    | ---- |
| bannerロール | サイト全体で共通のヘッダー要素 | https://developer.mozilla.org/ja/docs/Web/Accessibility/ARIA/Reference/Roles/banner_role
| genericロール | ロールとしての役割がないもの（意図的には使わない） | https://developer.mozilla.org/ja/docs/Web/Accessibility/ARIA/Reference/Roles/generic_role


## 別ページ移す
スクリーンリーダー：画面の内容を音声で読み上げてくれるソフト
