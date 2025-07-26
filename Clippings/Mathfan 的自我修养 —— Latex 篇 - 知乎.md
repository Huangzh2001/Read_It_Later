---
id: f4896923-023e-4b53-b854-81a323e1d428
created: 星期五, 九月 20日 2024, 5:59:49 下午
updated: 星期一, 十一月 25日 2024, 6:27:01 晚上
---

# Mathfan 的自我修养 —— Latex 篇 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/mathfan-latex-192031d0b80)
[Read Original](https://zhuanlan.zhihu.com/p/720441726)

## Highlights

> 当然也会遇到那种无法对齐的状况
> J
> [
> y
> ]
> =
> ∫
> 0
> r
> |
> π
> x
> [
> ρ
> g
> h
> 2
> +
> 2
> σ
> 1
> +
> y
> ˙
> 2
> ]
> ⏟
> F
> (
> y
> ˙
> ,
> y
> ;
> x
> )
> d
> x
> +
> 2
> π
> r
> Δ
> σ
> l
> ⏟
> ϕ
> (
> l
> ;
> r
> )
> J[\color{blue}y]= \int_0^r\underbrace{\vphantom{\Bigg|}\pi \color{darkorange}x\Big[\ \rho g\color{orange}h^2+2\color{red}\sigma\sqrt{1+\color{blue}{\dot y}^2}\ \Big]}_{F(\dot y,y;x)}dx+ \underbrace{2\pi \color{orange}r\Delta\color{red}\sigma \color{darkblue}l}_{\phi(l;r)}\\
> 我们只需为其添加一个虚拟高度体即可
> \underbrace{\vphantom{[虚拟高度]}{[内容]}}_{[下标]}
> J
> [
> y
> ]
> =
> ∫
> 0
> r
> |
> π
> x
> [
> ρ
> g
> h
> 2
> +
> 2
> σ
> 1
> +
> y
> ˙
> 2
> ]
> ⏟
> F
> (
> y
> ˙
> ,
> y
> ;
> x
> )
> d
> x
> +
> |
> 2
> π
> r
> Δ
> σ
> l
> ⏟
> ϕ
> (
> l
> ;
> r
> )
> J[\color{blue}y]= \int_0^r\underbrace{\vphantom{\Bigg|}\pi \color{darkorange}x\Big[\ \rho g\color{orange}h^2+2\color{red}\sigma\sqrt{1+\color{blue}{\dot y}^2}\ \Big]}_{F(\dot y,y;x)}dx+ \underbrace{\vphantom{\Bigg|}2\pi \color{orange}r\Delta\color{red}\sigma \color{darkblue}l}_{\phi(l;r)}\\
> 此处我为后者添加了一个\Bigg| 的虚拟高度，这样两者便能对齐了 [⤴️](https://omnivore.app/me/mathfan-latex-192031d0b80#985b00fc-dc92-4bab-8761-01dbe6c971e8)  ^985b00fc

