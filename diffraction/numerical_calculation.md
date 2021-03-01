# 回折積分の数値計算法


## 概要

- この節では、コンピュータを用いて回折積分を計算するための効率的な方法について説明する。
- 回折積分の理論式は[理論編](./theory.md)を参照のこと。
- また、数値計算に用いるフーリエ変換に関する事項は[離散フーリエ変換](./fourier_transform.md)を参照。


## 高速畳み込み

- 2平面$z=0$および$z=z$における伝播を表すRayleigh-Sommerfeldの回折積分公式は

$$
    U(x, y, z) = \int U(xi, eta, 0) \frac{\exp(j k r')}{r'} \mathrm{d}\xi \mathrm{d}\eta
$$

- となるのだった。
- ただし、$r'=\sqrt{ (x-\xi)^2 + (y-\eta)^2 + z^2 }$である。
- これは畳み込みとして書き直すことができ、

$$
    U(x, y, z) = U(xi, eta, 0) * \frac{\exp(j k r)}{\sqrt{ (x-\xi)^2 + (y-\eta)^2 + z^2 }} \mathrm{d}\xi \mathrm{d}\eta
$$

## 角スペクトル法 (Angular Spectrum Method) 




