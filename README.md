# 課題（中間課題１）

複数のページで構成される「自己紹介ページ」を記述しなさい。公開され、外部から参照されることを想定して、特に企業の採用担当者が読んだときに興味を持ってもらえるような内容にすること。これには、略歴、所属ゼミ、現在の研究課題の意義・手法・期待される結論、SRC の発表原稿へのリンク、活動が取り上げられた記事へのリンクなどを含むであろう。

## 条件

- HTML/CSS によって、論理構造と物理属性が分離されていること。
- CSS は、HTML で直接記述することなく、スタイルシートファイルを読み込んでいること。


# CSS における class の利用

同じタグであっても、ものによって物理属性を変化させたいことがある。

例：
- 同じ ```<tr>``` タグだが、テーブルの偶数行と奇数行で表示を変化させたい（ http://src.tama.ac.jp?conf=SRC2016S ）
- 特定の段落だけに色を付けたい

このようなとき、HTML 側でタグに「class」属性を与えておく（ここでも、物理属性は記述しないことに注目）

例：```<tr class='odd'> ... </tr><tr class='even'> ... </tr>```

CSS 側では、属性を ```タグ.クラス名``` で指定する。

例：
```
tr.odd { background-color: green; }
tr.even { background-color: yellow; }
```

クラス名だけ指定すると、タグを問わず同一のクラスに同じ属性をいっせいに指定できる。

例：```<h1 class='important'>``` も ```<p class='important'>``` も全部赤くしたい。

```
.important { color: red; }
```



参照：
- [w3school の class selector の解説]( https://www.w3schools.com/cssref/sel_class.asp )

# 復習（本当にファイナル）

git で https を使って push/pull をかけたい場合には、```user.email``` と ```user.name``` を設定しておく必要がある。これが面倒な人は、ssh による認証・転送を検討するとよい。

そのリポジトリだけに設定したい：

```
git config user.email "29988777xx@tama.ac.jp"
git config user.name "tamataro"
```

そのコンピュータで git を使うのは自分だけで、全てのリポジトリに設定したい：

```
git config --global user.email "29988777xx@tama.ac.jp"
git config --global user.name "tamataro"
```

# git で課題を提出する流れ

- tnext から課題リンクに飛ぶ
- 画面の説明に沿って、宿題（assignment）を受け取る
- 自分の課題リポジトリを開く
- clone のためのリンクをコピーする
- 自分のコンピュータの htdocs フォルダで ```git clone``` する
- 自分のコンピュータ上でファイルを編集する
- 自分のコンピュータの htdocs フォルダの中の課題リポジトリフォルダに移動する
- ```git add -A``` で変更ファイルを全て追加する
- 適当な区切りで ```git commit -m '......'``` でコメントをつけてコミットする
- ```git push``` でプッシュする

# 表示確認

xampp が正しくインストールされ、apache がサーバとして動作していれば

http://localhost/各自のリポジトリ名/style.html

で、このリポジトリの style.html ファイルが表示されるはずである。今回の「各自のリポジトリ名」は、css-final-ユーザ名 である。
