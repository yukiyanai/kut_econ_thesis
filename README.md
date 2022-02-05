# kut_econ_thesis

これは、高知工科大学経済・マネジメント学群に提出する卒業論文を R Markdown で書くためのテンプレートです。正しく使うと[このファイル](kut_econ_thesis_sample.pdf)のようなフォーマットの文書ができます。自由に利用してください。

- 2021年度から卒論のフォーマットが変更になりました。これに合わせてテンプレートも改変しました。（2021-11-27）
- Windows で正しく動作するように、[.latexmkrc](.latexmkrc) を追加しました。(2022-02-05)


以下の5つのファイルを配布します。

- Rmd ファイルのテンプレート：[kut_econ_thesis.Rmd](kut_econ_thesis.Rmd) 
- フォーマットを規定するtex ファイル：[kut_econ_template.tex](kut_econ_template.tex)
- bibファイルのサンプル：[myrefs.bib](myrefs.bib)
- latexmk の設定ファイル：[.latexmkrc](.latexmkrc) 
- 正しくknit できたPDFのサンプル：[kut_econ_thesis_sample.pdf](kut_econ_thesis_sample.pdf)

詳しい使い方はテンプレート内に書いてあるので、よく読んで使ってください。

## 準備

### IPAexフォントをインストールする

- 既にインストールされているならこの作業は不要
- インストール方法はテンプレートファイルに書いてある


###  Rで必要なパッケージをインストールする。

**bookdown** パッケージが必要なのでインストールする。他にも追加パッケージのインストールを促されたら、指示に従ってインストールする（RStudio を使っているなら、ポップアップの指示を読んで"Yes" をクリックすればよい）。
```
install.packages("bookdown", dependencies = TRUE)
```


### LaTeX一式をインストールする

- インストール方法については [TeX Wiki](https://texwiki.texjp.org/?TeX%E5%85%A5%E6%89%8B%E6%B3%95) を参照。
- LaTeX 自体を使う予定がないなら、**tinytex** でもよい。ただし、**既にLaTeXが入っているパソコンに追加でtinytex を入れてはいけない**！
```
install.packages("tinytex")
tinytex::install_tinytex()
```

###  卒論用の R Project を作る

R Studio からいつもどおりプロジェクトを作る。既存のプロジェクトを使ってもかまわない。


### プロジェクトフォルダの中に必要なファイル作る・保存する

1. 卒論本体の Rmd ファイルを作る
  - テンプレート（`kut_econ_thesis.Rmd`）に従って書く
  - ファイル名は自由に付けてよい
  - 本文、分析用コード、図表を作るコードをすべてこのファイルに書く
2. `kut_econ_template.tex` を1のRmdファイルと同じフォルダ（同じ階層）に保存する
3. `myrefs.bib` を作り、1のRmdファイルと同じフォルダ（同じ階層）に保存する
  - 必ずこのファイル名にする（ファイル名を変える場合は tex テンプレートの修正が必要）
  - ファイル自体はここで配布するものではなく、ZoteroやJabRefなどを使って自分で作る
4. `jecon.bst` を1のRmdファイルと同じフォルダ（同じ階層）に保存する
  - 武田史郎さんが作った文献スタイルファイル
  - [ココ](https://github.com/ShiroTakeda/jecon-bst/) から入手する
    - **誤って HTML ファイルを保存しないように注意**

## Windows ユーザ（と一部のUbuntuユーザ？）への注意

Windows でテンプレのRmd ファイルを knit しようとすると、upbibtex の代わりに bibtex が使われてしまい、bbl ファイルが作成できなくなるようです。latexmk の設定がうまく読み込めていないことが原因だと思われます（Ubuntu でうまくいかない場合も同様）。この問題への対応として、配布する .latexmkrc をknit する Rmd ファイルと同じフォルダに保存してください。ファイル名は変えない（先頭のドットを消さない、余分な拡張子を付けない）ように注意してください。
---

あとは研究して執筆するのみ。

**Enjoy & good luck!**
