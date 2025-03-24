---

marp: true
theme: my-theme
math: mathjax
paginate: true
header: 'Header content'
footer: 'Footer content'

---

<!-- _class: top -->

<!-- CSSファイルに /* @theme my-theme */ と最初に書かれていることを確認 -->

# Marpでプレゼンテーション

---

## Marpとは？

*   Markdownでプレゼンテーション資料を作成できるツールです。
*   シンプルな記法で、美しいスライドを作成できます。
*   HTML, PDF, PPTX形式でエクスポート可能です。

---

## 画像の挿入

![width:500](https://labs.fleuraison.net/wp-content/uploads/marp.png)

* Marpのロゴです。
* `width:500`のほかにも様々なコマンドがあります。

---

## 数式の記述

$$
v = v_0 + at
$$

$$
x = v_0t + \frac{1}{2}at^2
$$

$$
v^2 - v_0^2 = 2ax
$$

* 等加速度運動の公式です。
* LaTeX形式で記述可能です。

---

## リスト

*   順序なしリスト
    *   入れ子も可能

1.  順序付きリスト
2.  順序付きリスト
    1.  入れ子も可能

---

## テーブル

| ヘッダー1 | ヘッダー2 |
| -------- | -------- |
| セル1    | セル2    |
| セル3    | セル4    |
| セル5    | セル6    |
| セル7    | セル8    |

---

## リンク

[Marpの文法まとめ](https://qiita.com/pocket8137/items/27ede821e59c12a1b222)

[Marpの画像文法まとめ](https://briboo-pc.hatenablog.jp/entry/2023/12/27/%E3%80%90Marp%E3%80%91%E3%82%B9%E3%83%A9%E3%82%A4%E3%83%89%E3%81%AE%E4%B8%AD%E3%81%AB%E7%94%BB%E5%83%8F%E3%82%92%E6%8C%BF%E5%85%A5%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95)

↑クリックできます

---

## サンプルコード

```python
def hello_world():
    print("Hello, Marp!")

hello_world()
```

---

## スライドの分割

`---` を使うと、スライドを分割できます。

---

## コメント

`<!-- コメント -->` は表示されません。

<!-- これはコメントです -->

---

<!-- _class: top -->

# Marpを使うためのセットアップ

---

## Markdownファイルの作成

Markdownファイルを作成し、Marp記法でコンテンツを記述

※普通のMarkdown形式で書けば問題なし

---

## 変換 (Marp for VS Code)

VSCode mdファイルの右上にあるMarpロゴのボタンを押して、

`Export slide deck`を選ぶ

---

<!-- _class: top -->

# オプション設定

---

## テーマの作成

必要に応じてCSSを作成して、カスタムテーマを定義可能

```css
/* @theme my-theme */
@import 'default';

section {
  background-color: #eee;
}

...
```

---

### 作ったテーマの適用

1. VSCodeの設定を開く
2. `markdown.marp.themes` を検索
3. `./{ファイル名}.css` と入力 (現在のワークスペースから見た**相対パス**)

---

## PDFにブックマークを追加

PDFにブックマークを追加する設定

1. VSCodeの設定を開く
2. `markdown.marp.pdf.outlines` を検索
3. お好みの設定を選択

---

### ブックマーク設定項目

PDFに追加するブックマークの設定項目

| 設定     | 説明                             |
| -------- | -------------------------------- |
| `off`    | ブックマークを追加しない           |
| `pages`  | ページ数をブックマークとして追加     |
| `headings` | h1, h2, h3をブックマークとして追加 |
| `both`   | `pages` と `headings` の両方を追加 |

---

## 出力形式を変更

1. VSCodeの設定を開く
2. `markdown.marp.exportType` を検索
3. お好みの形式を選択
   - デフォルトはPDF形式
   - 他にもHTML, PPTX, PNG, JPEGが選択可能

---

<!-- _class: top -->

# まとめ

Marpを使うと、簡単にプレゼンテーション資料を作成できます。

ぜひお試しください！
