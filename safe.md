数列极限的四则运算法则有这么一条：<br>

$$\lim_{n\rightarrow\infty}(a_n+b_n)=\lim_{n\rightarrow\infty}a_n+\lim_{n\rightarrow\infty}b_n$$

运用上面的法则，来看下面这道题：<br>

$$\lim_{n\rightarrow\infty}(\frac{1}{\sqrt {n^2+1}}+\frac{1}{\sqrt {n^2+2}}+...+\frac{1}{\sqrt {n^2+n}})$$

很自然的，我们有：原式＝

$$\lim_{n\rightarrow\infty}\frac{1}{\sqrt{n^2+1}}+\lim_{n\rightarrow\infty}\frac{1}{\sqrt{n^2+2}}+...+\lim_{n\rightarrow\infty}\frac{1}{\sqrt{n^2+n}}=0+0+...+0=0$$

一切看上去似乎毫无任何破绽，有破绽吗？<br>

我们知道，数列极限的性质中，有一个“迫敛性定理”，也叫作“夹逼准则”，是这样叙述的：<br>

> 设收敛数列${a_n},b_n$都以$a$为极限，数列$c_n$满足：存在正数$N_0$，当$n>N_0$时有$a_n<=c_n<=b_n$，则数列$c_n$收敛，且$\lim_{n\rightarrow\infty}{c_n}=a$.



运用迫敛性定理，再次计算上题：<br>

$$1=\lim_{n\rightarrow\infty}\frac{n}{\sqrt{n^2+n}}=\lim_{n\rightarrow\infty}(\frac{1}{\sqrt {n^2+n}}+\frac{1}{\sqrt {n^2+n}}+...+\frac{1}{\sqrt {n^2+n}})<\\\lim_{n\rightarrow\infty}(\frac{1}{\sqrt {n^2+1}}+\frac{1}{\sqrt {n^2+2}}+...+\frac{1}{\sqrt {n^2+n}})\\<\lim_{n\rightarrow\infty}(\frac{1}{\sqrt {n^2+1}}+\frac{1}{\sqrt {n^2+1}}+...+\frac{1}{\sqrt {n^2+1}})=\lim_{n\rightarrow\infty}\frac{n}{\sqrt{n^2+1}}=1$$

此时得到的答案是１.<br>

事实上，**这道题的答案就是１**，那么第一种解法在哪里出问题了呢？<br>

仔细观察题干，当$n\rightarrow\infty$时，括号里面的项数会随之增加到无穷多项，从而题目就等价于求解**无穷多个无穷小之和**，这是**极限的未定式**的一种，叫做$\infty*0$型，这类式子（即“未定式”）的极限不确定，可以是0，是其他数，也可以不存在，它的极限不一定等于0，也就不满足四则运算法则，所以解法１不可行.<br>

下面的栗子同样如此：<br>

$$1=\lim_{n\rightarrow\infty}1=\lim_{n\rightarrow\infty}n\frac{1}{n}=\lim_{n\rightarrow\infty}\frac{1}{n}+\lim_{n\rightarrow\infty}\frac{1}{n}+...+\lim_{n\rightarrow\infty}\frac{1}{n}=0+0+...+0=0$$

当把１拆成$n$个$\frac{1}{n}$之和时，$\frac{1}{n}$的个数会随着$n\rightarrow\infty$而趋于$\infty$，这也是上面的$\infty*0$未定式型.<br>



通过这个栗子，我们要谨记：**极限的四则运算法则只对有限项成立，当推广到无限项时则不一定成立，因为此时会出现未定式，而未定式不能使用四则运算.**<br>

***

现在来总结下极限的７种未定式，它们分别是：<br>

（1）0/0



（2）∞/∞



（3）0·∞（栗子）



（4）∞-∞



（5）0^0



（6）∞^0



（7）1^∞



对于这些未定式，都不能运用极限的四则运算！<br>

![](/home/fantasy/Desktop/sxfx/1.jpg)

![](/home/fantasy/Desktop/sxfx/2.jpg)

***

写了一大堆，其实最初的想法来源是陈纪修老师的教材上的一道题，现在来一起看一下这道题：<br>

* 设$a_n>0$，$\lim_{n\rightarrow\infty}a_n=a$，求证$\lim_{n\rightarrow\infty}\sqrt[n]{a_1a_2...a_n}$

![](/home/fantasy/Desktop/sxfx/3.jpg)<br>

在第一个证明的倒数第二行，即

$$\lim_{n\rightarrow\infty}｜\frac{a_1+a_2+...+a_n}{n}-a｜=\lim_{n\rightarrow\infty}\frac{(a_1-a)+(a_2-a)+...+(a_n-a)}{n}=0$$

这里计算出来的那个０，并不是运用四则运算法则将其拆开，因为这里也是有无穷多项，虽然拆开计算的结果也是０，但是这只是巧合罢了，正确的做法是：<br>

由已知$\lim_{n\rightarrow\infty}a_n=a$，并且在前一步已经证明了当$a=0$时，$\lim_{n\rightarrow\infty}\frac{a_1+a_2+...+a_n}{n}=0=a$，即**$a_n$**是无穷小量时所证引理结论成立.<br>

而当$a!=0$时，$a_n-a$便是无穷小量（理由：在题干中，将已知的$\lim_{n\rightarrow\infty}a_n=a$中的$a$移到左侧即得$\lim_{n\rightarrow\infty}(a_n-a)=0$)，既然$a_n-a$是无穷小量了，那就可以套用刚刚证明的结论了（这个结论通俗点说就是：若$a_n$的极限是$a$，**如果$a_n$是无穷小量**，即$a=0$，**则有$\lim_{n\rightarrow\infty}\frac{a_1+a_2+...+a_n}{n}=a=0$，用的就是它等于０这一点）**，现在的无穷小量是$a_n-a$，那么就应该有$\lim_{n\rightarrow\infty}\frac{(a_1-a)+(a_2-a)+...+(a_n-a)}{n}=0$.