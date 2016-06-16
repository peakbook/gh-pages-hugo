+++
date = "2016-01-15T14:44:25+09:00"
title = "Regularization"
tags = ["regularization","machine learning","julia"]
+++

次の最小化問題を
[Julia](ihttp://julialang.org/)+[Convex](https://github.com/JuliaOpt/Convex.jl)+[Gadfly](https://github.com/dcjones/Gadfly.jl)+[Interact](https://github.com/JuliaLang/Interact.jl)
を使って可視化してみた．  
$$
\\begin{align}
        \text{L1正則化:} \hspace{2em}& \\underset{\\boldsymbol{w}\\in\\mathbb{R}^d}{\\operatorname{minimize}} \\hat{L}(\\boldsymbol{w}) + \\lambda \\| \boldsymbol{w} \\|_1 \\\\
        \text{L2正則化:} \hspace{2em}& \\underset{\\boldsymbol{w}\\in\\mathbb{R}^d}{\\operatorname{minimize}} \\hat{L}(\\boldsymbol{w}) + \\frac{\\lambda}{2} \\| \boldsymbol{w} \\|_2^2\\\\
        \text{損失関数:} \hspace{2em}& \\hat{L}(\\boldsymbol{w}) = \frac{1}{2}\\|\\boldsymbol{X}\\boldsymbol{w}-\\boldsymbol{y}\\|_2^2
\\end{align}
$$
なお，行列$\\boldsymbol{X}$とベクトル$\\boldsymbol{y}$は以下のように設定した($d=2$)．
$$
\\boldsymbol{X} = 
\\left[
    \\begin{array}{cc}
    1 & 0.5 \\\\
    0 & 1 
  \\end{array}
\\right],\\;\\;
\\boldsymbol{y} = 
\\left[
    \\begin{array}{c}
    1.75  \\\\
    0.5 
  \\end{array}
\\right].
$$
ソースコードは[こちら](https://github.com/peakbook/julia_notebook/blob/master/machine_learning_with_sparsity_inducing_regularizations/L1_L2_comparison.ipynb)．


<div style="text-align:center">
<video controls autoplay width="540" height="400" >
<source src="/videos/regularization.webm" >
</video>
</div>
