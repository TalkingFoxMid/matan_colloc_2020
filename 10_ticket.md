**10) Формула интегрирования по частям для определённого интеграла.**

Пусть $u=u(x)$ и $v=v(x)$ - две функции, непрерывные со своими первыми
производными на сегменте $[a, b]$

Возьмем дифференциал от их произведения:

$$\label{eq:1}
d[u(x)v(x)] = u(x)dv(x)+v(x)du(x)=u(x)v'(x)dx+v(x)u'(x)dx.$$

Интегрируя это тождество в пределах от $a$ до $b$, получим

$$\int_a^b d[u(x)v(x)] = \int_a^b u(x)v'(x)dx + \int_a^b v(x)u'(x)dx$$

Но по формуле Ньютона-Лейбница

$$\int_a^b d[u(x)v(x)]=u(x)v(x) |_a^b$$

Таким образом, равеноство [\[eq:1\]](#eq:1){reference-type="eqref"
reference="eq:1"} примет следующий вид:

$$u(x)v(x)|_a^b = \int_a^b u(x)v'(x)dx + \int_a^b v(x)u'(x)dx$$

Откуда

$$\label{eq:2}
\int_a^b u(x)v'(x)dx = u(x)v(x)|_a^b-\int_a^b v(x)u'(x)dx$$

Это формула интегрирования по частям в определенном интеграле

Так как, $du = u'(x)dx$ и $dv = v'(x)dx$, то формулу
[\[eq:2\]](#eq:2){reference-type="eqref" reference="eq:2"} можно
записать в более компактном виде:

$$\int_a^b udv = uv|_a^b-\int_a^b vdu$$

При этом, надо иметь в виду, что границы интегрирования относятся к
независимой переменной $x$.

**Пример**

Вычислить $$\int_0^\pi x\cos xdx$$

Положим $x = u$, $\cos xdx = dv$. Тогда $du = dx$, $v=\sin x$.

Применяя формулу интегрирования по частям, найдем:

$$\int_0^\pi x\cos xdx = x\sin x|_0^\pi - \int_0^\pi \sin xdx = \cos x|_0^\pi = -2$$
так как $$x\sin x|_0^\pi = \pi \sin\pi-0*\sin 0 = 0$$