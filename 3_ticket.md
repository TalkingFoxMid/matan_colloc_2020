**3) Определение сумм Дарбу и интегралов Дарбу, их свойства**

Пусть $f(x)$ - ограничена на $[a, b]$. Разобъем отрезок на частичные
отрезки, т. е. введём разбиение $\uptau = \{x\}_{n=1}^N\;$ и диаметр
разбиения ${d = max\Delta x\ \forall\\i =\overline{0,n - 1}}$.

Рассмотрим функцию на $i$-ом отрезке $[x_i, x_{i+1}]$. Поскольку $f(x)$
- ограничена на $[a, b]$, то она ограничена и на каждом частичном
отрезке, следовательно, можно найти
${\underset{x\in{[x_i, x_{i+1}]}}{\sup{f(x)}}}$ и
${\underset{x\in{[x_i, x_{i+1}]}}{\inf{f(x)}}}$. Обозначим их таким
образом: $M_i={\underset{x\in{[x_i, x_{i+1}]}}{\sup{f(x)}}}$ и
$m_i={\underset{x\in{[x_i, x_{i+1}]}}{\inf{f(x)}}}$. Теперь составим
интегральные суммы, но вместо произвольного значения будем брать в одном
случае $M_i$, а в другом $m_i$
$$S(\uptau)=\sum_{i=0}^{n-1}M_i\Delta x_i\quad s(\uptau)=\sum_{i=0}^{n-1}m_i\Delta x_i$$
$S(\uptau)$ - верхняя сумма Дарбу, $s(\uptau)$ - нижняя сумма Дарбу.

**Свойства сумм Дарбу**

-   Для произвольного разбиения и произвольного выбора точек
    справедливо:
    $$\forall\{\uptau\}\;\forall\{\upxi\}\quad s(\uptau) \leq \sum_{i=0}^{n-1}f(\upxi)\Delta x_i \leq S(\uptau)$$
    Доказательство:

    По определению $m_i$ и $M_i$, для каждого частичного отрезка и любой
    точки $\upxi$ из этого отрезка выполняется:
    $$m_i \leq f(\upxi) \leq M_i$$ Домножим это неравенство на
    $\Delta x$: $$m_i\Delta x \leq f(\upxi)\Delta x \leq M_i\Delta x$$
    Поскольку неравенство српаведливо для каждого частичного отрезка, мы
    имеем $n$ штук таких неравенств, теперь их сложим и придем к
    утверждению свойства:
    $$s(\uptau) \leq \sum_{i=0}^{n-1}f(\upxi)\Delta x_i \leq S(\uptau)$$

```{=html}
<!-- -->
```
-   $$\forall\uptau \quad {\underset{\{\upxi_i\}}\sup{\sigma(\uptau, \{\upxi_i\})}}=S(\uptau) \quad {\underset{\{\upxi_i\}}\inf{\sigma(\uptau, \{\upxi_i\})}}=s(\uptau)$$То
    есть для любого разбиения $\uptau$, $\sup$ интегральных сумм по
    выбору точек равен верхней сумме Дарбу, а $\inf$ - нижней сумме
    Дарбу.

    Доказательство:

    Распишем супремум по определению:

    $${\underset{\{\upxi_i\}}\sup{\sigma(\uptau, \{\upxi_i\})}}=S(\uptau)\Longleftrightarrow \begin{cases}   1)\forall\{\upxi_i\}\quad {\sigma(\uptau, \{\upxi_i\})} \leq S(\uptau)  \\    2)\forall\varepsilon\; \exists{\{\upxi_i^\varepsilon\}}\quad \sigma{(\uptau, \{\upxi_i^\varepsilon\})} > S(\uptau)- \varepsilon\end{cases}$$

    Первое условие выполняется по определению верхней суммы Дарбу,
    теперь нужно построить такую интегральную сумму
    $\sigma{(\uptau, \{\upxi_i^\varepsilon\})}$ для которой будет
    выполняться второе условие. Для этого рассмотрим $M_i$ на каждом
    частичном отрезке:

    $$M_i = {\underset{\upxi_i\in{[x_i, x_{i+1}]}}{\sup{f(x)}}}\Longleftrightarrow \begin{cases}    1) \forall\upxi_i\in{[x_i, x_{i+1}]} \quad f(\upxi_i) \leq M_i \\    2)\forall\varepsilon \; \exists{\upxi_i^\varepsilon} \quad f({\upxi_i^\varepsilon}) > M_i - \frac{\varepsilon}{b-a} \end{cases}$$

    Теперь мы знаем, какими должны быть точки $\upxi_i^\varepsilon$. То
    есть мы построили для $\sigma{(\uptau, \{\upxi_i^\varepsilon\})}$
    каждую точку $\upxi_i^\varepsilon$, и теперь можем рассмотреть эту
    интегральную сумму:

    $$\sigma{(\uptau, \{\upxi_i^\varepsilon\})} = \sum_{i=0}^{n-1}f(\upxi_i^\varepsilon)\Delta x_i$$
    Согласно условию (2) в определении $M_i$ как
    ${\underset{\upxi_i\in{[x_i, x_{i+1}]}}{\sup{f(x)}}}$, справедливо
    следующее:
    $$\sum_{i=0}^{n-1}f(\upxi_i^\varepsilon)\Delta x_i > \sum_{i=0}^{n-1}{(M_i - \frac{\varepsilon}{b-a})\Delta x_i} =  \sum_{i=0}^{n-1}M_i\Delta x_i - \sum_{i=0}^{n-1}\frac{\varepsilon}{b-a}\Delta x_i$$
    Поскольку $\frac{\varepsilon}{b-a}$ это константа, можно эту
    величину вынести за снак суммы, а в сумме останутся длины всех
    частичных отрезков, а сумма всех этих отрезков равна изначальному
    отрезку $[a, b]$:
    $$\sum_{i=0}^{n-1}M_i\Delta x_i - \sum_{i=0}^{n-1}\frac{\varepsilon}{b-a}\Delta x_i = S(\uptau) - \varepsilon$$
    Мы показали, что
    $\forall\varepsilon\; \exists{\{\upxi_i^\varepsilon\}}\quad \sigma{(\uptau, \{\upxi_i^\varepsilon\})} > S(\uptau)- \varepsilon$,
    т. е. выполняется второе условие того, что
    ${\underset{\{\upxi_i\}}\sup{\sigma(\uptau, \{\upxi_i\})}}=S(\uptau)$.
    Свойство доказано. Для инфинума доказывается по аналогии.

```{=html}
<!-- -->
```
-   При измельчении разбиения верхняя сумма Дарбу может разве лишь
    уменьшится, а нижняя сумма - увеличиться. Пусть $\uptau'$ -
    измельчение разбиения $\uptau$, тогда формулировка будет выглядеть
    таким образом:
    $$\forall\uptau'\supset\uptau \quad S(\uptau') \leq S(\uptau) \; s(\uptau') \geq s(\uptau)$$
    Доказательство:

    Пусть $\uptau' = \uptau \cup \{y\}, \quad y\in{[x_i, x_{i+1}]}$, то
    есть измельчение получено путем добавления одной точки $y$ в
    изначальное разбиение. Пусть эта точка добавлена в $k$-ый отрезок.
    Рассмотрим разность $S(\uptau) - S(\uptau')$.

    Если рассматривать эти суммы на каждом частичном отрезке, то все
    слагаемые совпадают и сократяться кроме того, где мы добавили точку.
    То есть от изначального разбиения $S(\uptau)$ останется слагаемое на
    том отрезке, где добавили точку, а в измельчении $S(\uptau')$ этот
    же частичный отрезок разобъется на два других отрезка.

    Обозначим $M_k$ - $\sup$ на частичном отрезке разбиения $S(\uptau)$.
    Поскольку в измельчении $S(\uptau')$ частичный отрезок разбился на
    две части, обозначим $M_k^L$ - $\sup$ на первой(левой) части и
    $M_k^R$ - $\sup$ на второй(правой) части.

    Таким образом, имеем:
    $$S(\uptau) - S(\uptau') = M_k(x_{k+1}-x_k) - (M_k^L(y - x_{k+1}) + M_k^R(x_{k+1} - y))$$
    Поскольку $M_k^L$ и $M_k^R$ - супремумы на новых отрезках,
    полученных разбиением старого, то $M_k^L \leq M_k$ и
    $M_k^R \leq M_k$. Тогда ${-M_k^L \geq -M_k}$ и ${-M_k^R \geq -M_k}$.
    Тогда
    справедливо:$$M_k(x_{k+1}-x_k) - (M_k^L(y - x_{k+1}) + M_k^R(x_{k+1} - y)) \geq M_k(x_{k+1}-x_k) - (M_k(y - x_{k+1}) + M_k(x_{k+1} - y))$$
    Вынесем в правой скобке $M_k$:
    $$M_k(x_{k+1}-x_k) - M_k(y - x_{k+1} + x_{k+1} - y) = M_k(x_{k+1}-x_k) - M_k(x_{k+1}-x_k) = 0$$
    Таким образом, получили, что
    $$S(\uptau) - S(\uptau') \geq0, \quad S(\uptau) \geq S(\uptau')$$
    Для нижней суммы Дарбу доказываеться по аналогии.

```{=html}
<!-- -->
```
-   Теперь пусть $\uptau' = \uptau \cup \{y\}_{k=1}^p$, $d$ - диаметр
    изначального разбиения $\uptau$,
    $M={\underset{x\in{[a, b]}}{\sup{f(x)}}}$,
    $m={\underset{x\in{[a, b]}}{\inf{f(x)}}}$. Тогда справедлива оценка:
    $$0 \leq S(\uptau) -S(\uptau') \leq (M-m)pd, \quad 0 \leq s(\uptau') - s(\uptau) \leq (M-m)pd$$
    Доказательство:

    По аналогии с предыдущим свойством, отличаются только $p$ отрезков,
    следовательно остальные сократяться. Перенумеруем так, чтобы $y_1$
    входил в первый отрезок, $y_2$ в 2-ой отрезок, \..., $y_p$ в $p$-ый
    отрезок, тогда справедливо:
    $$\sum_{k=1}^{p}S(\uptau) - S(\uptau') = \sum_{k=1}^{p}M_k(x_{k+1}-x_k) - \sum_{k=1}^{p}(M_k^L(y - x_{k+1}) + M_k^R(x_{k+1} - y))$$
    Оценим $M_k, M_k^R$ и $M_k^L$ таким образом:
    $$M_k \leq M, \quad -M_k^L \leq -m, \; -M_k^R \leq -m$$ Теперь можем
    оценить все выражение: $$\begin{gathered}
    \sum_{k=1}^{p}M_k(x_{k+1}-x_k) - \sum_{k=1}^{p}(M_k^L(y - x_{k+1}) + M_k^R(x_{k+1} - y)) \leq \\ \leq M\sum_{k=1}^{p}\Delta x_k - m\sum_{k=1}^{p}\Delta x_k = (M-m)\sum_{k=1}^{p}\Delta x_k = (M-m)pd\end{gathered}$$
    Для нижних сумм Дарбу доказывается аналогично.

```{=html}
<!-- -->
```
-   Для любых абсолютно разных разбиений нижняя сумма Дарбу меньше
    верхней суммы Дарбу
    $$\forall\uptau',\uptau'' \quad s(\uptau') \leq S(\uptau'')$$
    Доказательство:

    Введеме разбиние $\uptau$ которое будет разбиением $\uptau'$ и
    $\uptau''$, то есть: $$\uptau = \uptau' \cup \uptau''$$ Как мы уже
    знаем, при измельчении разбиения нижняя сумма Дарбу может разве лишь
    увеличиться: $$s(\uptau') \leq s(\uptau)$$ В то же время, по
    определению на одном и том же разбииени нижняя сумма Дарбу меньше
    верхней суммы Дарбу: $$s(\uptau') \leq s(\uptau) \leq S(\uptau)$$
    $\uptau$ - размельчение $\uptau''$, поэтому
    $S(\uptau) \leq S(\uptau'')$. Применим это неравенство к
    предыдущему:
    $$s(\uptau') \leq s(\uptau) \leq S(\uptau) \leq   S(\uptau'')$$
    Свойство доказано.

**Верхний и нижний интеграл Дарбу**

Мы знаем, что
$\forall\uptau', \uptau'' \quad s(\uptau') \leq S(\uptau'')$.
Зафиксируем разбиение $\uptau'$ и будем перебирать всевозможные
разбиения $\uptau''$, при этом условие все еще выполняется, но поскольку
мы перебрали всевозможные разбиения $\uptau''$, значит, что
$\{S(\uptau)\}$ - ограничено снизу, следовательно, имеет точную нижную
грань. Обозначим её как $I^*$
$$s(\uptau') \leq S(\uptau'') \Rightarrow \exists\;{\underset{\{\uptau\}}\inf\{{S(\uptau)}\}} = I^*$$
$I^*$ - верхний интеграл Дарбу. Поскольку $I^*$ - точная верхняя грань,
$I^*$ меньше или равен какой-либо грани, в нашем случае меньше или равен
$S(\uptau)$. То есть:
$$\forall\uptau', \uptau'' \quad s(\uptau') \leq I^* \leq S(\uptau'')$$
Теперь зафиксируем $\uptau''$ и будем перебирать $\uptau'$. Поскольку от
этого неравенство не измениться, то есть
$\forall \uptau' \quad s(\uptau') \leq I^*$, то можно сделать вывод, что
$\{s(\uptau)\}$ - ограничено сверху константой $I^*$. Следовательно
существует точная грань $\{s(\uptau)\}$, обозначим ее как $I_*$. $I_*$ -
нижний интеграл Дарбу.
$$s(\uptau') \leq I^* \Rightarrow \exists\;{\underset{\{\uptau\}}\sup\{{s(\uptau)}\}} = I_*$$
В то же время $I^*$ это какая-то верхняя грань множества $s(\uptau)$, а
$I_*$ - это точная верхняя грань, то есть наименьшая из всех верхних
граней. Тогда справедливо: $$I_* \leq I^*$$