---
author: "RyoNak"
last_modified_at: 2024-08-24
tags:
- documentation
---

## Task List at GitHub Repository Push

- [ ] poetry managed packagesを`requirements.txt`へ出力する
- [ ] ~~*hoge*~~

<strong > &#9654;&nbsp; `requirements.txt`へ出力</strong>

```zsh
% poetry export --without-hashes --format=requirements.txt --output requirements.txt
```

## Referncesの記載方法

- `references.bib`に下記例の形式で記載をする
- ポスト中で使用する場合は `@2020現代数理統計学` のように使用する．使用した場合，ポストの末尾にreference一覧が自動的に出力される


```json
@article{knuth84,
  author = {Knuth, Donald E.},
  title = {Literate Programming},
  year = {1984},
  issue_date = {May 1984},
  publisher = {Oxford University Press, Inc.},
  address = {USA},
  volume = {27},
  number = {2},
  issn = {0010-4620},
  url = {https://doi.org/10.1093/comjnl/27.2.97},
  doi = {10.1093/comjnl/27.2.97},
  journal = {Comput. J.},
  month = may,
}

@book{2020現代数理統計学,
  author = {竹村彰通},
  title = {現代数理統計学},
  year = {2020},
  isbn = {9784780608601},
  url = {https://books.google.co.jp/books?id=OY8dzgEACAAJ},
  month = nov,
  publisher = {学術図書出版社}
}
```

<strong > &#9654;&nbsp; Reference出現位置をコントールしたい場合</strong>

- ポスト（`.qmd`ファイル）の任意の位置に以下のようなブロックを記述すると，レンダリング時にその場所にreference listが表示される

```md
References
----------
::: {#refs}
:::
```

## Mathjax関連

<strong > &#9654;&nbsp; 式番号の文中引用</strong>

引用したいmathjax equationに対して，以下のようにラベル付をします．

```latex
<div class="math display" style="overflow: auto">
$$
\frac{1}{(1-q)^r} = \sum_{k=0}^\infty \frac{(k+r-1)!}{(r-1)!k!}q^{k}
$${#eq-comb-seq}
</div>
```

その後，文中で `@eq-comb-seq` とすると引用することができます．



## Quarto FAQ

<strong > &#9654;&nbsp;Q: icon fieldで利用可能なiconのリストはどこでみれるのか？</strong>

- [Bootstrap Icons](https://icons.getbootstrap.com/)
