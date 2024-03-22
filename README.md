# 1. 目的

# 2. プログラムについて
## 2-1.フォルダ構成
### 2-1-1. distributions
確率分布クラスをまとめたフォルダ。continuousフォルダに連続型の確率分布クラス、discreteフォルダに離散型の確率分布クラスがまとめられている。

それぞれの確率分布クラスは基底クラスを継承しており（連続型はContinuousDistributionBase、離散型はDiscreteDistributionBase）、
おのおのの基底クラスは抽象クラスAbstractDistributionを継承している。
### 2-1-2. extensions
拡張メソッドクラスをまとめたフォルダ。今回は階乗や順列、組み合わせなどの演算メソッドを拡張クラスとして実装している。
## 2-2. 特記事項
### 2-2-1. 積分計算について
本プログラムでは連続型関数の定積分は台形近似を用いて計算している。台形近似は数値積分におけるポピュラーな積分近似の方法の一つである。

分割単位を $\Delta x$ とすると、積分区間 $[a, b]$ の定積分の近似式は下記で与えられる。

$$\int_{a}^{b}f(x)dx \approx \sum_{k=0}^{n-1}\cfrac{(f(k) + f(k + 1))\Delta x}{2}$$

また、広義積分については、十分に大きい値 $N$ を定義し、下記で示される式にて計算している。

$$\int_{-\infty}^{\infty}f(x)dx \approx \int_{-N}^{N}f(x)dx$$




