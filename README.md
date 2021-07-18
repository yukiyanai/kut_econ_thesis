# kut_econ_thesis

これは、高知工科大学経済・マネジメント学群に提出する卒業論文を R Markdown で書くためのテンプレートです。正しく使うと[このファイル](kut_econ_thesis_rmd_sample.pdf)のようなフォーマットの文書ができます。自由に利用してください。

以下の4つのファイルを配布します。

- Rmd ファイルのテンプレート：[kut_econ_thesis_rmarkdown.Rmd](kut_econ_thesis_rmarkdown.Rmd) 
- フォーマットを規定するtex ファイル：[kut_econ_thesis_lualatex.tex](kut_econ_thesis_lualatex.tex)
- bibファイルのサンプル：[myrefs.bib](myrefs.bib)
- 正しくknit できたPDFのサンプル：[kut_econ_thesis_rmd_sample.pdf](kut_econ_thesis_rmd_sample.pdf)

詳しい使い方はテンプレート内に書いてあるので、よく読んで使ってくたさい。


## 準備

###  Rで **bookdown** パッケージをインストールする。
```
install.packages("bookdown", dependencies = TRUE)
```

### LaTeX一式をインストールする

- インストール方法については [TeX Wiki](https://texwiki.texjp.org/?TeX%E5%85%A5%E6%89%8B%E6%B3%95) を参照。
- LaTeX 自体を使う予定がないなら、**tinytex** でもよい。既にLaTeXが入っているパソコンに追加でtinytex を入れてはいけない！
```
install.packages("tinytex")
tinytex::install_tinytex()
```

###  卒論用の R Project を作る

R Studio から通常どおりにプロジェクトを作る。既存のプロジェクトを使ってもかまわない。


### プロジェクトフォルダの中に必要なファイル作る・保存する

1. 卒論本体の Rmd ファイル
  - テンプレート（`kut_econ_thesis_rmarkdown.Rmd`）に従って書く。
2. `kut_econ_thesis_lualatex.tex`
3. `myrefs.bib`（このファイル名で、中身は自分で作る）
4. `jecon-unicode.bst`：武田史郎さんが作ったものを使う。[ココ](https://github.com/ShiroTakeda/jecon-bst/tree/master/unicode) から入手する。

### IPAexフォントをインストールする

- 既にインストールされているならこの作業は不要
- インストール方法はテンプレートファイルに書いてある

---

**あとは研究して執筆するのみ！**
