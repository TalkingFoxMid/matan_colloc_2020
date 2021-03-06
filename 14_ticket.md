---
title: Множество площади 0
---

14) Понятие кривой площади 0. Доказать, что непрерывная и спрямляемая кривая имеют площадь 0. {#понятие-кривой-площади-0.-доказать-что-непрерывная-и-спрямляемая-кривая-имеют-площадь-0. .unnumbered}
=============================================================================================

$D$ - множество площади ноль (плоское множество жордановой меры 0),
если:
$$\forall \varepsilon > 0 \; \exists R \text{ - многоугольник}: D \subseteq R \land \mathcal{S} (R) < \varepsilon$$

Критерий квадрируемости' {#критерий-квадрируемости .unnumbered}
------------------------

*Ограниченная плоская фигура $D$ квадрируема $\iff$\
$\partial D$ - множество площади ноль.* ($\partial$ - граница множества)

#### Доказательство:  {#доказательство .unnumbered}

$$\begin{gathered}
    R = \overline{Q \setminus P} \supseteq \partial D \\
    \mathcal{S}(R) = \mathcal{S}(Q) - \mathcal{S}(P) < \varepsilon \\
    R \cup P = Q \\
    \accentset{\circ}{R} \cap \accentset{\circ}{P} = \emptyset\end{gathered}$$

Утверждение:  {#утверждение .unnumbered}
------------

*Любая спрямляемая кривая - множество площади 0*

#### Доказательство:  {#доказательство-1 .unnumbered}

Зададим спрямляемую кривую $\gamma$ следующим образом.
$$\begin{gathered}
    |\gamma| = l \\
    \gamma = \begin{cases} x=x(t) \\ y=y(t) \end{cases}, t \in [\alpha, \beta] \\
    \frac{l}{n} = |M_i M_{i+1}|\end{gathered}$$ $K_i$ - квадрат с
центром $M_i$ и стороной $a=\frac{2l}{n}$;
$M_{i-1},M_{i+1} \in \overline{K_i}$

r0.4 ![image](kek.png){width="40%"}

$$\begin{gathered}
    R = \bigcup_{i=0}^{n}K_i\\
    \mathcal{S}(R) \leq \sum_{n = 0}^{n}\mathcal{S}(K_i) = \frac{4l^2}{n^2} \cdot (n+1) \xrightarrow[n \to \infty]{} 0 \\
    \forall \varepsilon > 0 \; \exists N_\varepsilon \in \mathbb{N}: \forall n > N_\epsilon \\
    \mathcal{S}(R) < \varepsilon\end{gathered}$$

#### Пояснение:  {#пояснение .unnumbered}

Зададим спрямляемую (шо ето такое - смотри \<ссыль на билет 12\>) кривую
через параметрическое уравнение, возьмём её длину $|\gamma|=l$.\
$n$ - число точек разбиения кривой, отсюда $\frac{l}{n}$ - расстояние
между двумя соседними точками.

Затем построим квадраты с центрами в точках разбиения и сторонами
$\frac{2l}{n}$, чтобы предыдущая и последующая точки относительно центра
каждого квадрата попали внутрь или на границу квадрата.

Теперь возьмём в качестве многоугольника $R$ из *определения множества
площади ноль* объединение всех построенных квадратов, тогда
$\mathcal{S}(R)$ не будет превосходить суммы всех площадей квадратов.

В свою очередь сумма всех площадей квадратов равна квадрату их стороны
$\frac{2l}{n}$, умноженному на их количество ($n+1$ в формуле из-за
начальной/конечной точки разбиения).

Устремим $n$ к бесконечности, тогда очевидно, что сумма всех площадей
квадратов будет стремиться к 0.

Отсюда получается, что площадь многоугольника меньше любого
$\varepsilon$, а это удовлетворяет *определению множества площади ноль*.

Утверждение:  {#утверждение-1 .unnumbered}
------------

*Пусть*
$$\gamma = \begin{cases} x=x \\ y=f(x) \end{cases},\;x \in [a, b],\;f\text{ - непрерывная}$$
*Тогда $\gamma$ имеет площадь 0*
