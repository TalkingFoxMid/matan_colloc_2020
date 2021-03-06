# 11.Замена переменной в определенном интеграле

###### tags: `Матан-колоквиум` 
#### Формулировка:

Пусть функция $u=g(t)$ имеет непрерывную производную на отрезке $[a,b]$ и 

$$\inf_{t\in[m,M]}   g(t) = A\\
{\sup_{t\in[m,M]}}   g(t) = B$$

причем $g(a) = A$, $g(b) = B$. Тогда

$\int_A^B{f(u)du} = \int_a^b{f[g(t)]g'(t)dt}$

при условии, что функция $f$ непрерывна на отрезке $[A,B]$.

#### Доказательство:

Пусть $F(x)$ - некоторая первообразная функции $f(x)$. Функции $F(x)$ и $u=g(t)$ дифференцируемы на отрезках $[A,B]$ и $[a,b]$ соответственно. Согласно правилу вычисления производной сложной функции,

$\frac{d}{dt}F(g(t)) = F'(g(t))g'(t)$.

Учитывая, что $F'(g(t)) = F'(u)$ при $u = g(t)$ и что $F'(u) = f(u)$, получим

$\frac{d}{dt}F(g(t)) = f(g(t))g'(t)dt$.

Таким образом, функция $F(g(t))$ является на отрезке
$[a, b]$ первообразной для функции $f(g(t))g'(t)$ и, следовательно,

$\int_a^b{f(g(t))g'(t)dt} = F(g(b)) - F(g(a))=F(B)-F(A).$

В итоге, с одной стороны,

$\int_A^B{f(u)du}=F(B)-F(B)$, так как $F'(u) = f(u)$

а, с другой стороны,

$F(B)-F(A) =\int_a^b{f(g(t))g'(t)dt},$

что и требовалось доказать.
