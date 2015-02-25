+++
date = "2015-02-25T11:43:17+09:00"
title = "Interact.jlを使ってみる"
tags = [ "julia" ]

+++

[Interact.jl](https://github.com/JuliaLang/Interact.jl)を使って，
多項式曲線フィッティングをインタラクティブにしてみた．  

<div style="text-align:center">
<img src=/images/fitting.gif>
</div>

Gadflyと組み合わせると，グラフがグリグリ動いてとても楽しい．  
見た目もわかりやすくて，非常に良いですね．  

例では，多項式の次数を$M$，L2正則化の係数を$\lambda=10^{\lambda_p}$としてます．  
コードは[こちら](http://nbviewer.ipython.org/github/peakbook/julia_notebook/blob/master/interact/fitting.ipynb)．
nbviewerではもちろんインタラクティブにはならないので悪しからず．


