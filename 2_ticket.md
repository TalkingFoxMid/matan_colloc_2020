**2) Необходимое условие интегрируемости функции по Риману.**

**Теорема (необходимое условие интегрируемости).**

Если $f$ - интегрируема на $[a, b]$, то $f$ - ограничена на $[a, b]$.

$\;$

*Доказательство.* О/п: Пусть $f$ - интегрируема и не ограничена на
$[a, b]$.

$\;$

Распишем по Коши:

$$\forall\epsilon>0\;\;\exists\delta(\epsilon)>0,\;\forall\tau,d<\delta(\epsilon)\;\;\forall\lbrace\xi\rbrace_{i=0}^{n-1}$$

$$\vert\sigma(\tau,\lbrace\xi\rbrace_i)-I\vert<\epsilon$$

Возьмём
$\epsilon=1\;\;\exists\delta(1)>0\;\;\forall\tau:d<\delta(1)\;\;\forall\lbrace\xi_i\rbrace$,
подставим в неравенство и ограничим слева:

$$\;\;\vert\sigma(\tau,\lbrace\xi_i\rbrace)\vert-\vert{I}\vert\leq\vert\sigma(\tau,\lbrace\xi_i\rbrace)-I\vert<1 \label{eq:1}$$

Т.к. $f$ - не ограничена =\> при разбиении на одном из отрезков она не
ограничена.

Распишем интегральную сумму:

$$\sigma(\tau,\lbrace{\xi_i}\rbrace)=f(\xi_0)\cdot\triangle{x_0}+\underbrace{\overset{n-1}{\underset{i=1}{\sum}}f(\xi_i)\cdot\triangle{x_i}}_{\sigma_1}$$

Подставим в последнее неравенство и снова ограничим слева меньшим
значением:

$$\vert{f(\xi_0)}\vert\cdot\triangle{x_0}-\vert{\sigma_1}\vert-\vert{I}\vert\leq\vert{f(\xi_0)\cdot\triangle{x_0}+\sigma_1}\vert-\vert{I}\vert<1$$

Перенесём в правую часть и поделим на $\triangle{x_0}$:

$$\vert{f(\xi_0)}\vert<\frac{\vert\sigma_1\vert+\vert{I}\vert+1}{\triangle{x_0}}$$

$\forall\xi_n\in[a_1, b_1]$ =\> ограничена - противоречие.

$\heartsuit\;\;$Условие *необходимое*, но *не
достатоное*.$\;\;\heartsuit$
