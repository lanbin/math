# 极限

## 简单的解法

最简单的解决方法是，将趋近的目标带入式子中，如果得出的是一个有效的值，则即为极限的值。

比如极限(1)
$$
\lim_{n \rightarrow 2} x+2 = 4
$$


## 趋近无穷

当x趋近于正无穷时，可以保留变化最大的项进行简化，类似于求导。

比如极限(2):
$$
\lim_{n \rightarrow + \infty} \frac{x^2+x}{4x^2-5} = ?
$$
可以简化成(3):
$$
\lim_{n \rightarrow +\infty} \frac{x^2}{4x^2} = \frac{1}{4}
$$



## 因式拆分

类似这样的：
$$
\lim_{z \rightarrow 2} \frac{z^2 + 2z -8}{z^4 - 16}
$$
可以拆分,然后得出：
$$
\lim_{z \rightarrow 2} \frac{(z+4)(z-2)}{(z^2+4)(z+2)(z-2)} =\frac{6}{8+4} = \frac{1}{2}
$$


## 根号

类似这样的：
$$
\lim_{n \rightarrow \infty} \sqrt{x^2+4x+1} -x
$$
要消除根号，可以使用**共轭**(conjugate)的方式:
$$
(a+b)(a-b)
$$
例如，这样：
$$
\lim_{n \rightarrow \infty} (\sqrt{x^2+4x+1} -x )\ast \frac{\sqrt{x^2+4x+1} + x}{\sqrt{x^2+4x+1} + x}
$$
相乘，并消除最大项得：
$$
\lim_{n \rightarrow \infty} \frac{x^2 + 4x + 1 - x^2}{\sqrt{x^2+4x+1} + x} \ast \frac{\frac{1}{x}}{\frac{1}{x}}
$$
各种合并之后得：
$$
\lim_{n \rightarrow \infty} \frac{4 + \frac{1}{x}}{\sqrt{1 + \frac{4}{x} + \frac{1}{x^2}} +1}
$$
当x趋近于无穷的时候，x为分母的式子均趋近于0，所以得：
$$
\lim_{n \rightarrow \infty} \frac{4 + 0}{\sqrt{1 + 0 + 0} + 1} = 2
$$
综上所述：
$$
\lim_{n \rightarrow \infty} \sqrt{x^2+4x+1} -x = 2
$$


## 三角函数

类似这样的问题： 
$$
\lim_{n \rightarrow 0} \frac{\cot 2x}{\csc x}
$$


三角函数参考公式：
$$
\csc x = \frac{1}{\sin x}
$$

$$
\cot 2x = \frac{1}{\tan 2x} = \frac{\cos 2x}{\sin 2x}
$$


$$
\sin 2x = 2 \sin x \cos x
$$

$$
\cos 0 = 1
$$


式子(13)可得：
$$
\lim_{n \rightarrow 0} \frac{\cot 2x}{\csc x} = \lim_{n \rightarrow 0} \frac{\cos 2x \ast \sin x}{\sin 2x} = \lim_{n \rightarrow 0} \frac{\cos 2x \sin x}{2\sin x\cos x} =  \lim_{n \rightarrow 0} \frac{\cos 2x }{2\cos x}
$$
根据(17)可得
$$
\lim_{n \rightarrow 0} \frac{\cot 2x}{\csc x} =  \frac{1}{2}
$$


## 夹逼定理



如果有下列三个函数：
$$
g(x) \leq f(x) \leq h(x)
$$
那么，当：
$$
\lim_{x \to a} g(x) = L 
$$

$$
\lim_{x \to a} h(x) = L
$$

时，可以得出：
$$
\lim_{x \to a} f(x) = L
$$
因为，__f(x)__总是大于g(x)且总是小于__h(x)__，那么当__g(x)__和__h(x)__极限一样时，__f(x)__极限也会等于他们的值。

 

### 实际应用，证明:


$$
\lim_{x \to 0} \frac{\sin x} {x} = 1
$$
参考：
$$
\sin x < x < \tan x
$$
推导：
$$
\frac{\sin x}{|\sin x|} < \frac{x} {|\sin x|} < \frac{\frac{\sin x}{\cos x}}{|\sin x|}
$$
对绝对值计算需要改变自己的绝对值符号，得出：
$$
1 < \frac{|x|} {|\sin x|} < \frac{1}{|\cos x|}
$$


对不等式求倒数，而且__sin x__于__x__肯定是同符号的，所以可以去掉绝对值符号：
$$
1 > \frac{\sin x}{x} > \cos x
$$
不等式的两端：
$$
\lim_{x \to 0} 1 = 1
$$

$$
\lim_{x \to 0} \cos x = 1
$$

根据夹逼定理：
$$
\lim_{x \to 0} \frac{\sin x}{x} = 1
$$






























































