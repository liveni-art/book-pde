# Конспект курса: Обобщенные функции

## Обобщённые функции. Носитель. Пространство $\mathcal{D}(\mathbb{R}^n)$

**Уравнение Навье–Стокса:**

$$
\frac{\partial \vec{v}}{\partial t} = -(\vec{v} \cdot \nabla)\vec{v} + \nu \Delta \vec{v} - \frac{1}{\rho}\nabla p + \vec{f}
$$

### Носитель функции

**Определение.** Носитель функции $\varphi$:

$$
\operatorname{supp} \varphi = \overline{\{x \in \mathbb{R}^n \mid \varphi(x) \neq 0\}}
$$

Например, $\operatorname{supp} \omega = B_R(x)$ — носитель сосредоточен в шарике $B_R(x)$.

> Носитель = множество, вне которого функция равна нулю (для гладких функций).

**Определение.** Нулевое множество функции $\varphi$:

$$
O_\varphi = \mathbb{R}^n \setminus \operatorname{supp} \varphi \quad \text{(открытое множество)}
$$

### Пространство $\mathcal{D}(\mathbb{R}^n)$

$\mathcal{D}(\mathbb{R}^n)$ — совокупность всех бесконечно дифференцируемых **финитных** функций в $\mathbb{R}^n$, т.е.

$$
\mathcal{D}(\mathbb{R}^n) = \{\varphi \mid \varphi \in C^\infty(\mathbb{R}^n),\ \operatorname{supp} \varphi \subseteq B_R(x) \text{ для некоторого } R\}
$$

### Структура линейного пространства на $\mathcal{D}(\mathbb{R}^n)$

1) $\varphi, \psi \in \mathcal{D}(\mathbb{R}^n)$, $\forall \alpha, \beta \in \mathbb{R}$

2) $\alpha\varphi + \beta\psi$ — гладкая, т.е. $\in C^\infty(\mathbb{R}^n)$, т.к. $\varphi, \psi \in C^\infty$

3) Носитель $\alpha\varphi + \beta\psi$ содержится в $B_k \supset B_{k_1} \cup B_{k_2}$, где $B_{k_1}, B_{k_2}$ — носители $\varphi$ и $\psi$ соответственно.

4) $\alpha\varphi + \beta\psi$ — финитная.

5) Т.е. $\mathcal{D}(\mathbb{R}^n)$ — **векторное (линейное) пространство**.

### Топология на $\mathcal{D}(\mathbb{R}^n)$ через сходимость

Хотим ввести топологию. Введём её через сходимость последовательностей.

**Определение.** Последовательность $\varphi_k \in \mathcal{D}(\mathbb{R}^n)$ называется **сходящейся** к $\varphi \in \mathcal{D}(\mathbb{R}^n)$, если:

1) $\exists R > 0: \forall k \in \N \quad \operatorname{supp} \varphi_k \subset B_R$ (носители равномерно ограничены)

2) $\forall$ мультииндекса $\alpha = (\alpha_1, \ldots, \alpha_n)$:

$$
D^\alpha \varphi_k \to D^\alpha \varphi \quad \text{равномерно в } \mathbb{R}^n
$$

---

### Задача 6.2 (Владимиров)

Пусть

$$
\chi(x) = \begin{cases} 1, & \text{при } -2\varepsilon \leq x \leq 2\varepsilon \\ 0, & \text{при } |x| > 2\varepsilon \end{cases}
$$

*[График: ступенчатая функция, равная 1 на $[-2\varepsilon, 2\varepsilon]$ и 0 вне этого интервала]*

Возьмём $w_\varepsilon(x) \in \mathcal{D}(\mathbb{R}^1)$ — «шапочку» (гладкую финитную функцию).

*[График: гладкий «колокол» с носителем в $[-\varepsilon, \varepsilon]$, максимум в нуле]*

Определим свёртку:

$$
y(x) = \int_{-\infty}^{\infty} \chi(y)\, w_\varepsilon(x - y)\, dy
$$

**Доказать:**

1) $y(x)$ — основная функция из $\mathcal{D}(\mathbb{R}^1)$

2) $0 \leq y(x) \leq 1$

3) $y(x) \equiv 1$ при $-\varepsilon \leq x \leq \varepsilon$

4) $y(x) \equiv 0$ при $|x| > 3\varepsilon$

---

## Пространство быстроубывающих функций $\mathcal{S}$ (лекция 3)

### Определение пространства $\mathcal{S}$

$\mathcal{S}$ — множество всех $f \in C^\infty(\mathbb{R}^n)$ таких, что $f(x) \to 0$ при $|x| \to \infty$, причём вместе со всеми производными.

**Пространство быстроубывающих функций:**

$$
\mathcal{S} = \left\{f \in C^\infty \;\middle|\; \forall \alpha = (\alpha_1, \ldots, \alpha_n),\ \forall \beta = (\beta_1, \ldots, \beta_n):\ x^\beta D^\alpha f(x) \xrightarrow{|x| \to \infty} 0\right\}
$$

где $x^\beta = x_1^{\beta_1} x_2^{\beta_2} \cdots x_n^{\beta_n}$.

> Функция и все её производные стремятся к нулю **быстрее любой степени** $\dfrac{1}{|x|}$.

### Примеры

1) $f(x) = 1 \notin \mathcal{S}$ — не стремится к 0.

2) $e^{-|x|^2} \in \mathcal{S}$ — быстро убывает.

---

## Свойства $\mathcal{S}$

3) $e^{|x|} \notin \mathcal{S}$ — не стремится к 0.

4) $e^{-|x|} \notin \mathcal{S}$ — т.к. не гладкая (в нуле излом).

### Утверждение

$$
\mathcal{D} \subset \mathcal{S}
$$

### Упражнение

$\mathcal{S}$ — векторное пространство.

### Топология на $\mathcal{S}$

Хотим наделить $\mathcal{S}$ топологией.

**Определение.** Последовательность $\{\varphi_k\}_k \subset \mathcal{S}$ **сходится** к $\varphi \in \mathcal{S}$, если:

$$
\forall \alpha = (\alpha_1, \ldots, \alpha_n),\ \forall \beta = (\beta_1, \ldots, \beta_n): \quad x^\beta D^\alpha \varphi_k \to x^\beta D^\alpha \varphi \quad \text{равномерно в } \mathbb{R}^n
$$

**Пространство $\mathcal{S}$ с такой топологией** называется **основным пространством $\mathcal{S}$** (пространство Лорана Шварца).

---

### К задаче о свёртке

Для доказательства нужно показать, что:

1.1) $y(x)$ — бесконечно дифференцируема

1.2) $y(x)$ — финитная (следует из условия 4)

### Задачи

> Задачи — в тетради с заданиями (решения этих задач там есть).

**2 лекция** (разбор задач 6.2, 6.3 был, см. в задачнике)

**Д/з:** 6.1с, 6.6, 6.7

### Обобщённая функция Дирака

> Обобщённая функция — дельта-функция Дирака показала (пример обобщённой функции, не являющейся обычной).


## Утверждение. $\mathcal{D} \subset \mathcal{S}$ плотно (относительно топологии в $\mathcal{S}$)

$$
\overline{\mathcal{D}} = \mathcal{S} \quad \text{(замыкание } \mathcal{D} \text{ в } \mathcal{S}\text{)}
$$

---

## Семинар

### Утверждения об умножении на гладкую функцию

- **Для $\mathcal{D}$:** $\varphi \in \mathcal{D}$, $a \in C^\infty \Rightarrow a\varphi \in \mathcal{D}$
- **Для $\mathcal{S}$:** $\varphi \in \mathcal{S}$, $a \in C^\infty \not\Rightarrow a\varphi \in \mathcal{S}$

**Контрпример:**

$$
\varphi = e^{-|x|^2}, \quad a(x) = e^{|x|^2}
$$

$$
a\varphi \equiv 1 \notin \mathcal{S}
$$

---

### Упражнение 6.11 (Владимиров)

**Условие:** $\varphi \in \mathcal{S}$, $p$ — многочлен $\Rightarrow \varphi \cdot p \in \mathcal{S}$

**Решение:**

1) $\varphi \cdot p \in C^\infty$ (как произведение двух гладких функций)

2) $\forall \alpha = (\alpha_1, \ldots, \alpha_n)$, $\beta = (\beta_1, \ldots, \beta_n)$:

$$
x^\beta D^\alpha(\varphi \cdot p(x)) \xrightarrow{|x| \to \infty} 0
$$

Пусть $p(x) = \displaystyle\sum_{|\alpha| \leq m} a_\alpha x^\alpha$, $\deg p = m$, где:

- $|\alpha| = \alpha_1 + \ldots + \alpha_n$ — длина мультииндекса
- $x^\alpha = x_1^{\alpha_1} \cdot x_2^{\alpha_2} \cdots x_n^{\alpha_n}$

Тогда:

$$
D^\alpha(\varphi(x) p(x)) = D^\alpha\!\left(\sum_{|\alpha| \leq m} a_\alpha x^\alpha \varphi(x)\right) = \sum_{|\alpha| \leq m} a_\alpha D^\alpha(x^\alpha \varphi(x)) \quad (*)
$$

По формуле Лейбница:

$$
D^\alpha(x^\alpha \varphi(x)) = \sum_{|\xi| \leq |\alpha|} C^{|\xi|+|\eta|} D^\xi \varphi(x) \cdot D^\eta x^\alpha
$$

Подставляя в $(*)$:

$$
(*) = \sum_{|\alpha| \leq m} a_\alpha \sum_{|\xi| \leq |\alpha|} C^{|\xi|+|\eta|} D^\xi \varphi(x) \cdot D^\eta x^\alpha = \sum_{|\xi| \leq |\alpha|} r_\xi(x) D^\xi \varphi(x)
$$

где $r_\xi(x)$ — многочлен.

Следовательно:

$$
x^\beta D^\alpha(\varphi(x) p(x)) = x^\beta \sum_{|\xi| \leq |\alpha|} r_\xi(x) D^\xi \varphi(x) = \sum_{|\xi| \leq |\alpha|} S_\xi(x) D^\xi \varphi(x) \xrightarrow{|x| \to \infty} 0
$$

т.к. $\varphi(x) \in \mathcal{S}$.

---

## Согласованность со сходимостью в $\mathcal{D}$ (согласованность топологии)

$\mathcal{D} \subset \mathcal{S}$. Пусть $\varphi_k \to \varphi$ в $\mathcal{D}$, тогда:

1) $\exists R > 0$: $\operatorname{supp} \varphi_k \subset B_R(\rho)$ $\forall k > k_0$

2) $\forall \alpha = (\alpha_1, \ldots, \alpha_n)$: $D^\alpha \varphi_k \to D^\alpha \varphi$ равномерно в $B_R(\rho)$

$$
\Rightarrow \max_{B_R(\rho)} |D^\alpha \varphi_k - D^\alpha \varphi| \to 0
$$

$$
\Rightarrow \forall \alpha = (\alpha_1, \ldots, \alpha_n),\ \beta = (\beta_1, \ldots, \beta_n):
$$

$$
\max_{\mathbb{R}^n} |x^\beta D^\alpha \varphi_k(x) - x^\beta D^\alpha \varphi(x)| = \max_{B_R(\rho)} |x^\beta D^\alpha \varphi_k - x^\beta D^\alpha \varphi|
$$

$$
\leq \underbrace{\max_{B_R(\rho)} |x^\beta|}_{\text{огранич.}} \cdot \max_{B_R(\rho)} |D^\alpha \varphi_k(x) - D^\alpha \varphi(x)| \to 0
$$

$$
\Rightarrow x^\beta D^\alpha \varphi_k \to x^\beta D^\alpha \varphi \text{ равномерно} \iff \varphi_k \to \varphi \text{ в } \mathcal{S}
$$

---

### Упражнение 6.12 (Владимиров)

**Утверждение.** Пусть $a \in C^\infty(\mathbb{R}^n)$ и

$$
|D^\alpha a(x)| \leq C(1+|x|^m)^{|\alpha|}
$$

Тогда $\varphi \in \mathcal{S}'(\mathbb{R}^n) \Rightarrow a\varphi \in \mathcal{S}'(\mathbb{R}^n)$.

**Упражнение\*:** показать, что $x^\beta D^\alpha(a\varphi) \to 0$.

---

### Дополнительная задача

**Дано:** $\varphi \in C^\infty(\mathbb{R}^n)$, $\varphi = 0$ при $x < a$, $\varphi$ ограничена вместе со всеми своими производными.

**Доказать:** $\varphi(x) e^{-\delta x} \in \mathcal{S}$, где $\delta > 0$, $\delta \in \mathbb{R}$.

*[Рисунок: функция, равная нулю при $x < a$, затем плавно возрастающая]*



<!-- <11-15> -->
## Продолжение доказательства дополнительной задачи

Имеем оценку:

$$
\leq \sum_{i \leq \alpha} |c_i| \, |\varphi^{(i)}(x)| \, |e^{-\delta x}| \leq \sum_{i \leq \alpha} |c_i| M_i |e^{-\delta x}|
$$

где $M_i = \sup |\varphi^{(i)}|$, $N_i = |c_i| M_i = \text{const}$.

Тогда:

$$
= \sum_{i \leq \alpha} N_i |x|^\beta e^{-\delta x}
$$

### При $x \to -\infty$:

$\varphi^{(i)}(x) = 0 \Rightarrow x^\beta \varphi^{(i)}(x) e^{-\delta x} = 0$ при $x \to -\infty$.

### При $x \to +\infty$:

$$
|x^\beta (\varphi(x) e^{-\delta x})^{(\alpha)}| \leq \sum_{i \leq \alpha} N_i |x|^\beta e^{-\delta x}
$$

Сумма стремится к 0 при $x \to +\infty$ (экспонента убывает быстрее любого многочлена).

---

## Домашнее задание

- **6.1 пункт 3**
- **6.10**
- **Вопрос:** $\operatorname{supp} D^\alpha \varphi \stackrel{?}{=} \operatorname{supp} \varphi$

---

## Конструкция δ-функции (аппроксимация)

Возьмем "шапочку" для построения δ-функции:

$$
\varphi_\varepsilon(x) = C_\varepsilon e^{-\frac{\varepsilon^2}{\varepsilon^2 - x^2}}
$$

*[График: гладкий "колокол" с носителем на $[-\varepsilon, \varepsilon]$, максимум $e^{-1}$ в нуле]*

Хотим добиться условия нормировки:

$$
\int_{\mathbb{R}} \varphi_\varepsilon(x) \, dx = 1
$$

При $\varepsilon \to 0$ функция "сжимается" к нулю, образуя последовательность, сходящуюся к δ-функции.

### Вычисление нормировочной константы

$$
\int_{\mathbb{R}} C_\varepsilon \left(e^{-\frac{\varepsilon^2}{\varepsilon^2-x^2}}\right) dx = C_\varepsilon \int_{\mathbb{R}} e^{-\frac{\varepsilon^2}{\varepsilon^2-x^2}} dx
$$

$$
= C_\varepsilon \int_{-\varepsilon}^{\varepsilon} \exp\left(-\frac{\varepsilon^2}{\varepsilon^2-x^2}\right) dx = \varepsilon C_\varepsilon \int_{-\varepsilon}^{\varepsilon} \exp\left(-\frac{1}{1-\left(\frac{x}{\varepsilon}\right)^2}\right) d\left(\frac{x}{\varepsilon}\right)
$$

Замена: $t = \frac{x}{\varepsilon}$, $-1 \leq t \leq 1$:

$$
= C_\varepsilon \cdot \varepsilon \int_{-1}^{1} \exp\left(-\frac{1}{1-t^2}\right) dt = C \cdot C_\varepsilon \cdot \varepsilon = 1
$$

где $C = \displaystyle\int_{-1}^{1} \exp\left(-\frac{1}{1-t^2}\right) dt$ — константа.

Отсюда $C_\varepsilon = \dfrac{1}{C \cdot \varepsilon}$.

---

## Решение дополнительной задачи (полное)

**Доказать:** $\varphi(x) e^{-\delta x} \in \mathcal{S}(\mathbb{R})$, где $\varphi \in C^\infty(\mathbb{R})$, $\varphi = 0$ при $x < a$, $\varphi$ ограничена вместе со всеми производными.

**Решение:**

1) $\varphi(x) e^{-\delta x} \in C^\infty(\mathbb{R})$ — очевидно (произведение гладких функций).

2) $\forall \alpha, \beta \in \mathbb{N}$:

$$
x^\beta D^\alpha(\varphi(x) e^{-\delta x}) \xrightarrow{|x| \to \infty} 0
$$

По формуле Лейбница (обобщенная):

$$
(\varphi(x) e^{-\delta x})^{(\alpha)} = \sum_{i \leq \alpha} C_\alpha^i \, \varphi^{(i)}(x) \, (e^{-\delta x})^{(\alpha-i)}
$$

где $(e^{-\delta x})^{(\alpha-i)} = (-1)^{\alpha-i} \delta^{\alpha-i} e^{-\delta x}$.

Тогда:

$$
= \sum_{i \leq \alpha} [(-\delta)^{\alpha-i} C_\alpha^i] \, \varphi^{(i)}(x) e^{-\delta x}
$$

где коэффициенты — константы.

Следовательно:

$$
x^\beta D^\alpha(\varphi(x) e^{-\delta x}) = \sum_{i \leq \alpha} c_i \, \varphi^{(i)}(x) \, x^\beta e^{-\delta x}
$$

Так как $\exists M_i > 0$: $|\varphi^{(i)}(x)| \leq M_i$ $\forall i \in \mathbb{N} \cup \{0\}$, то:

$$
|x^\beta (\varphi(x) e^{-\delta x})^{(\alpha)}| = \left|\sum_{i \leq \alpha} c_i \, \varphi^{(i)}(x) e^{-\delta x}\right| \leq \sum_{i \leq \alpha} |c_i| M_i |x|^\beta e^{-\delta x} \to 0
$$

при $|x| \to \infty$ (экспонента доминирует).

---

## Свойства носителя и пространств

### 1. Свойство носителя линейной комбинации

$$
\operatorname{supp}(\alpha\varphi + \beta\psi) \subseteq \operatorname{supp}\varphi \cup \operatorname{supp}\psi
$$

### 2. $\mathcal{S}$ — векторное пространство

(лекция 04, всё видео)

---

## Обобщённые функции (распределения)

**Лемма (du Bois-Reymond или основная лемма вариационного исчисления):**

Если $\displaystyle\int_{\mathbb{R}^n} f(x)\varphi(x) \, dx = 0$ $\forall \varphi \in \mathcal{D}(\mathbb{R}^n)$, то $f = 0$ п.в. на $\mathbb{R}^n$.

**Следствие:** если $f, g \in L_{\text{loc}}^1$, то $f = g$ п.в. $\Leftrightarrow$ $f$ и $g$ порождают один и тот же обобщённый функционал (т.е. $\displaystyle\int f\varphi = \int g\varphi$ $\forall \varphi \in \mathcal{D}$).

---

### Определение обобщённой функции

Пусть $F$ — одно из пространств $\mathcal{D}$, $\mathcal{S}$ или $\mathcal{E}$.

**Обобщённая функция на $F$** — всякий линейный непрерывный функционал $f: F \to \mathbb{C}$.

Обозначение: $\langle f, \varphi \rangle \in \mathbb{C}$ — это $f(\varphi)$ (или $f[\varphi]$).

**Типы функционалов:**

- **Регулярные** — когда представляются в виде $\langle f, \varphi \rangle = \displaystyle\int f\varphi \, dx$
- **Сингулярные** — когда не регулярны (например, δ-функция Дирака: $\langle \delta, \varphi \rangle = \varphi(0)$)

### Свойства функционала

1) **Линейность:**

$$
\langle f, \alpha\varphi + \beta\psi \rangle = \int_{\mathbb{R}^n} f(\alpha\varphi + \beta\psi) \, dx = \alpha \int_{\mathbb{R}^n} f\varphi \, dx + \beta \int_{\mathbb{R}^n} f\psi \, dx
$$

2) **Непрерывность:**

Опр. непрер-ти: $f: V \to W$ непрерывна $\Leftrightarrow$ $\{v_k\} \subset V$: $v_k \to 0 \Rightarrow f(v_k) \to 0$.

Для линейных функционалов: $(\forall k)\{v_k\} \subset V$: $v_k \to v \Rightarrow f(v_k) \to f(v)$.

**Теорема Рисса** (о представлении функционала):

$$
\lim_{k \to \infty} f(v_k) = f\left(\lim_{k \to \infty} v_k\right)
$$

$\forall f \in L_{\text{loc}}^1(\mathbb{R}^n)$ $f$ порождает регулярную обобщённую функцию:

$$
\langle f, \varphi \rangle := \int_{\mathbb{R}^n} f\varphi \, dx, \quad \forall \varphi \in \mathcal{D}
$$

---

## Семинар (04) (всё видео)

### Вложение пространств

$$
E = C^\infty
$$

$$
\mathcal{D} \subset \mathcal{S} \subset E
$$

$$
E' \subset \mathcal{S}' \subset \mathcal{D}'
$$

(плотные вложения)

### Топологические понятия

- $A$ плотно в $B$ $\Leftrightarrow$ $\overline{A} \supset B$
- $A$ всюду плотно в $B$ — $\forall x \in A$, $\forall$ окр-ти $U_\varepsilon(x)$ $\exists b \in B$, что $b \in U_\varepsilon(x)$

### Регулярные функционалы

$$
\langle f, \varphi \rangle = \int_{\mathbb{R}^n} f\varphi \, dx
$$

где $f \in L_{\text{loc}}^1(\mathbb{R}^n)$.

### Главное значение интеграла (v.p.)

$$
\text{v.p.} \int_{\text{неособ.}} = \lim_{x \to x_0} \int_{\text{инт.}}
$$

(когда вырезается точка, в которой интеграл не определён и берётся предел)

**Пример:**

$$
\left\langle \text{v.p.}\frac{1}{x}, \varphi \right\rangle = \text{v.p.} \int_{\mathbb{R}} \frac{\varphi(x)}{x} \, dx
$$

### Свойства функционала v.p.$\frac{1}{x}$

1) Линейность $V$

2) Непрерывность $V$

$\Rightarrow$ (линейная обобщённая функция относительно $\varphi$):

$$
\varphi_k \to 0 \text{ в } \mathcal{D} \Rightarrow \left\langle \text{v.p.}\frac{1}{x}, \varphi_k \right\rangle \to 0 \text{ в } \mathbb{R}
$$

*Сингулярность:* $\not\exists f \in L_{\text{loc}}^1(\mathbb{R})$: $\left\langle \text{v.p.}\dfrac{1}{x}, \varphi \right\rangle = \displaystyle\int_{\mathbb{R}} f\varphi \, dx$.

Это приводит к контрпримеру (сингулярный функционал).


## Проверка, что v.p. $\frac{1}{x}$ — обобщённая функция

**Проверить:**
1) v.p. $\frac{1}{x}$ — обобщённая ф-я
2) v.p. $\frac{1}{x}$ — сингулярная обобщённая ф-я

### 1) Проверка линейности и непрерывности функционала

(провер. лин. и непрер. ф-ала)

Следует просто из линейности интеграла.

**Проверка непрерывности в $\mathcal{D}$:**

$\varphi_k \to 0$ в $\mathcal{D}$ $\Rightarrow$ $\langle f, \varphi_k \rangle \to 0$

Условия сходимости в $\mathcal{D}$:

1) $\exists R$: $\operatorname{supp} \varphi_k \subset B_R(\rho)$, т.е. $\varphi_k = 0$ вне $B_R(\rho)$

2) $\varphi_k^{(\alpha)}(x) \to 0$ равномерно на $B_R(\rho)$, т.е. $\max\limits_{[-R,R]} \varphi_k^{(\alpha)} \to 0$

Вычислим:

$$
\left\langle \text{v.p.}\frac{1}{x}, \varphi_k \right\rangle = \text{v.p.} \int_{\mathbb{R}} \frac{\varphi_k(x)}{x} dx = \text{v.p.} \int_{-R}^{R} \frac{\varphi_k(x)}{x} dx
$$

**Применяем теорему Лагранжа** (т.о. усредн.):

$\forall x$ $\exists \xi$ между $x$ и $0$, т.ч. $\varphi_k(x) - \varphi_k(0) = \varphi_k'(\xi)(x-0) = x\varphi_k'(\xi)$

где $\xi = \xi(x)$ — непрерывная ф-я.

Отсюда:

$$
\varphi_k(0) = \varphi_k(x) - x\varphi_k'(\xi)
$$

Подставляем в интеграл:

$$
\text{v.p.} \int_{-R}^{R} \frac{\varphi_k(0) + x\varphi_k'(\xi)}{x} dx = \text{v.p.} \int_{-R}^{R} \frac{\varphi_k(0)}{x} dx + \int_{-R}^{R} \frac{x\varphi_k'(\xi)}{x} dx
$$

Первый интеграл (v.p.) равен нулю (нечётная функция), второй:

$$
\int_{-R}^{R} \varphi_k'(\xi) dx \to 0 \quad \text{при } k \to \infty
$$

т.к. $\varphi_k' \to 0$ равномерно.

---

## Продолжение доказательства сингулярности

Из предыдущего:

$$
C_\varepsilon A_\varepsilon B = \frac{\sqrt{\varepsilon}}{C} A_\varepsilon \cdot B \to 0
$$

где $C_\varepsilon = \dfrac{1}{\varepsilon \cdot C}$

Противоречие с $C = 1$.

$$
\Rightarrow \not\exists f \in L_{\text{loc}}^1(\mathbb{R})
$$

---

## Домашнее задание

**Д/З:**

1) **Владимиров 6.22** (обязательно)

   Подсказка: $\delta$ — послед-ть ф-ций, проверить:
   - 1) проверка на обобщённую ф-ю
   - 2) ...
   
   Связал, не сровнялся.

2) **6.25** (обяз.)

   $$
   \left\langle \delta, \frac{1}{x^2}, \varphi \right\rangle = \text{v.p.} \int \frac{\varphi(x)}{x^2} dx
   $$
   
   - 1) проверить, что это обобщённая ф-я из $\mathcal{D}$
   - 2) сингулярная? (подсказка: вычисл. значение эфф.)

---

## Доказательство сингулярности δ-функции

**Доказать, что δ-ф-я — сингулярная.**

От противного:

Пусть $\exists f \in L_{\text{loc}}^1(\mathbb{R}^n)$, такая, что $\langle \delta, \varphi \rangle = \displaystyle\int_{\mathbb{R}^n} f \cdot \varphi \, dx = \varphi(0)$.

Рассмотрим $\varphi = w_\varepsilon = \exp\left(-\dfrac{\varepsilon^2}{\varepsilon^2 - |x|^2}\right)$.

Тогда:

$$
\langle \delta, w_\varepsilon \rangle = \int_{\mathbb{R}^n} f \cdot \exp\left(-\frac{\varepsilon^2}{\varepsilon^2 - |x|^2}\right) dx = w_\varepsilon(0) = e^{-1}
$$

С другой стороны:

$$
\left|\int_{B_\varepsilon(0)} f \cdot \exp\left(-\frac{\varepsilon^2}{\varepsilon^2 - |x|^2}\right) dx\right| \leq \max_{B_\varepsilon(0)} \exp\left(-\frac{\varepsilon^2}{\varepsilon^2 - |x|^2}\right) \cdot \int_{B_\varepsilon(0)} |f| dx
$$

где максимум равен $e^{-1}$.

Отсюда:

$$
w_\varepsilon(0) = e^{-1} \leq e^{-1} \int_{B_\varepsilon(0)} |f| dx \quad \Rightarrow \quad \int_{B_\varepsilon(0)} |f| dx \geq 1 \quad \forall \varepsilon > 0
$$

Но:

$$
\lim_{\varepsilon \to 0} \int_{B_\varepsilon} |f| dx = \lim_{\varepsilon \to 0} \varepsilon^n \int_{B_1(0)} f\left(\frac{x}{\varepsilon}\right) d\left(\frac{x}{\varepsilon}\right) \leq \lim_{\varepsilon \to 0} \varepsilon^n \cdot C = 0
$$

т.к. $f \in L_{\text{loc}}^1(\mathbb{R}^n)$.

Противоречие: $0 \geq e^{-1}$.

---

## Главное значение интеграла для $\frac{1}{x}$

**v.p. ф-я $\dfrac{1}{x}$**

Действие этой обобщённой ф-ции на ф-цию $\varphi \in \mathcal{D}$:

$$
\text{v.p.}\frac{1}{x} = \text{v.p.} \int_{\mathbb{R}} \frac{dx}{x} = \lim_{\varepsilon \to 0} \left(\int_{-\infty}^{-\varepsilon} \frac{dx}{x} + \int_{\varepsilon}^{\infty} \frac{dx}{x}\right)
$$

$$
= \lim_{\varepsilon \to 0} \int_{|x| \geq \varepsilon} \frac{1}{x} dx
$$

*[График функции $1/x$ с вырезанной окрестностью нуля $[-\varepsilon, \varepsilon]$]*

$$
\left\langle \text{v.p.}\frac{1}{x}, \varphi \right\rangle = \text{v.p.} \int_{\mathbb{R}} \frac{\varphi}{x} dx
$$

синг. обобщ. ф-я из $\mathcal{D}'$.

---

## Продолжение доказательства

Условие получаем на $C_\varepsilon$:

$$
C_\varepsilon = \frac{1}{\varepsilon \cdot C} \xrightarrow[\varepsilon \to 0]{} \infty
$$

Возьмём носитель ф-ии:

$$
\left\langle \text{v.p.}\left(\frac{1}{x}\right), x\varphi_\varepsilon \right\rangle = \text{v.p.} \int \frac{x\varphi_\varepsilon}{x} dx = \int_{\mathbb{R}} \varphi_\varepsilon(x) dx = 1
$$

(способ сокращения на $\frac{1}{x}$)

Если $\exists f \in L_{\text{loc}}^1(\mathbb{R})$, такая, что:

$$
\left\langle \text{v.p.}\frac{1}{x}, x\varphi_\varepsilon \right\rangle = \int_{\mathbb{R}} f x \varphi_\varepsilon
$$

(локально интегрируемая ф-я)

Тогда по **неравенству Коши-Буняковского** (Коши-Шварца):

$$
\left|\left\langle \text{v.p.}\frac{1}{x}, x\varphi_\varepsilon \right\rangle\right| = \left|\int_{\mathbb{R}} f x \varphi_\varepsilon dx\right| \leq \left(\int_{-\varepsilon}^{\varepsilon} f^2 dx\right)^{1/2} \left(\int_{-\varepsilon}^{\varepsilon} x^2 \varphi_\varepsilon^2 dx\right)^{1/2}
$$

$$
= C_\varepsilon \left(\int_{-\varepsilon}^{\varepsilon} x^2 \exp\left(-\frac{2\varepsilon^2}{\varepsilon^2 - x^2}\right) dx\right) = C_\varepsilon \left(\int_{-1}^{1} t^2 e^{-\frac{2}{1-t^2}} dt\right)^{1/2}
$$

где $A = \left(\displaystyle\int_{-\varepsilon}^{\varepsilon} f^2 dx\right)^{1/2}$, $B = \left(\displaystyle\int_{-1}^{1} t^2 e^{-\frac{2}{1-t^2}} dt\right)^{1/2}$.

<!--21-25-->


## Лекция 7 (видео 7)

### Определение. Обобщённая функция обращается в 0 на области

**Опр.** Обобщённая ф-я $f$ **обращается в 0** на области $\Omega \subset \mathbb{R}^n$, если

$$
\langle f, \varphi \rangle = 0 \quad \forall \varphi \in \mathcal{D}(\mathbb{R}^n): \operatorname{supp} \varphi \subset \Omega
$$

**Обозн.:** $f = 0$ на $\Omega$ — почти везде.

---

### Пространство $\mathcal{F}'$

$\mathcal{F}'$ — пространство линейных непрерывных функционалов.

Оно линейно: $\forall f, g \in \mathcal{F}'$, $\forall \alpha, \beta \in \mathbb{R}$:

$$
\alpha f + \beta g \in \mathcal{F}'
$$

---

### Равенство обобщённых функций

**Опр.** Обобщённые ф-ции $f$ и $g$ называются **равными в области $\Omega$**, если обобщённая ф-я $f - g = 0$ на $\Omega$ (т.е. $\forall x \in \Omega$).

---

### Нулевое множество

**Опр.** **Нулевым мн-вом** обобщённой ф-ции $f$ называется объединение всех областей $\Omega \subset \mathbb{R}^n$, таких что $f = 0$ в $\Omega$.

**Обозначение:** $O_f$

---

## Носитель обобщённой функции

**Опр.** Носителем обобщённой ф-ции $f$ называется $\mathbb{R}^n \setminus O_f$:

$$
\operatorname{supp} f = \mathbb{R}^n \setminus O_f
$$

**Утв.:**
- $O_f$ — открытое мн-во
- $\operatorname{supp} f$ — замкнутое

---

### Финитные обобщённые функции

**Опр.** Обобщённая ф-я называется **финитной**, если $\operatorname{supp} f$ — финитный, т.е. $\operatorname{supp} f$ — компакт.

---

## Примеры

### 1. Дельта-функция финитна

$$
O_\delta = \mathbb{R}^n \setminus \{0\}
$$

$$
\operatorname{supp} \delta = \{0\}
$$

$$
\delta \in \mathcal{D}': \quad \langle \delta, \varphi \rangle = \varphi(0) \quad \forall \varphi \in \mathcal{D}(\mathbb{R}^n)
$$

---

### 2. Функция Хевисайда

$$
\theta(x) = \begin{cases} 1, & x \geq 0 \\ 0, & x < 0 \end{cases}
$$

*[График: ступенчатая функция, 0 при $x < 0$, 1 при $x \geq 0$]*

$$
\theta \in L_{\text{loc}}^1(\mathbb{R})
$$

$$
\operatorname{supp} \theta = [0, +\infty) \quad \text{(как обобщённой ф-ции)}
$$

Действие на тестовую функцию:

$$
\langle \theta, \varphi \rangle = \int_{\mathbb{R}} \theta \varphi \, dx = \int_{0}^{\infty} \varphi \, dx
$$

Если рассматривать обобщённую ф-ю как обычную, то все её свойства сохраняются.

$$
\forall \Omega \subset \mathbb{R} \setminus [0, +\infty) = (-\infty, 0)
$$

$$
\forall \varphi \in \mathcal{D}: \operatorname{supp} \varphi \subset \Omega \quad \Rightarrow \quad \langle \theta, \varphi \rangle = \int_{0}^{\infty} 0 \, dx = 0
$$

---

### 3. Носитель δ-функции

Если $\operatorname{supp} \varphi \subset \Omega \subset \mathbb{R}^n \setminus \{0\}$, то:

$$
\langle \delta, \varphi \rangle = \varphi(0) = 0
$$

(доказали: $\delta(\varphi) = 0$ в $\Omega$ $\Leftrightarrow$ $\delta = 0$ в $\Omega$)

т.е. $\Omega \subset O_\delta$

$$
\forall \Omega \subset \mathbb{R}^n \setminus \{0\}
$$

$$
\Rightarrow O_\delta = \mathbb{R}^n \setminus \{0\}
$$

$$
\Rightarrow \operatorname{supp} \delta = \{0\} \quad (= \mathbb{R}^n \setminus O_\delta)
$$

---

### 4. δ-функция простого слоя (тоже сингулярна)

$$
\delta_S \in \mathcal{D}'
$$

$$
\langle \delta_S, \varphi \rangle = \int_S \varphi(x) \, dS
$$

где $S$ — поверхность в $\mathbb{R}^n$, $\forall \varphi \in \mathcal{D}(\mathbb{R}^n)$

индуцированная мера Лебега на $S$

*(поверхностный интеграл)*

*[Рисунок: поверхность S в $\mathbb{R}^n$ — сфера]*

---

## Алгоритм поиска носителя

1) $\operatorname{supp} \delta = ?$

   $\varphi \in \mathcal{D}$: $\operatorname{supp} \varphi \subset \Omega \subset \mathbb{R}^n \setminus \{0\}$

2) Находим 0-мн-во

3) Берём объединение всех 0-областей

4) Дополнение к нему

---

## Продолжение доказательства для v.p. $\frac{1}{x}$

$$
= \text{v.p.} \, \varphi_k(0) \int_{-k}^{k} \frac{dx}{x} + \text{v.p.} \int_{-k}^{k} \varphi_k'(\xi) \, dx
$$

$$
= \text{v.p.} \left( \varphi_k(0) \cdot \int_{-k}^{k} \frac{dx}{x} \right) + \text{v.p.} \int_{-k}^{k} \varphi_k'(\xi) \, dx \quad \text{①}
$$

**Упр.:** $g \to 0$, тогда $① = \text{v.p.} \displaystyle\int_{-k}^{k} \varphi_k'(\xi) \, dx = \displaystyle\int_{-k}^{k} \varphi_k'(\xi) \, dx$

$$
|①| \leq \int_{-k}^{k} |\varphi_k'(\xi)| \, dx \leq \max_{[-k,k]} |\varphi_k'| \cdot |2k|
$$

$$
\text{v.p.} \int_{-k}^{k} \frac{dv}{x} \, dx
$$

$$
\lim_{\varepsilon \to 0} \int_{-k}^{-\varepsilon} \frac{dx}{x} + \lim_{\varepsilon \to 0} \int_{\varepsilon}^{k} \frac{dx}{x}
$$

$$
= \lim_{\varepsilon \to 0} \big( \ln \varepsilon - \ln(-k) \big) + \lim_{\varepsilon \to 0} \big( \ln k - \ln \varepsilon \big)
$$

**Упр.:** $\varphi_\varepsilon = x \widehat{w}_\varepsilon$ (модир. шапочки)

$$
\widehat{w}_\varepsilon = C_\varepsilon w_\varepsilon; \quad \int_{k} \widehat{w}_\varepsilon = 1
$$

$$
\langle \text{v.p.} \frac{1}{x}, \varphi_\varepsilon \rangle \not\to 0
$$

<!-- <26-30> -->

## Домашнее задание 9/3 (после видео [07])

- 6.19 [2]
- 6.15.2
- 3) д-ть, что $e^{-ax} \theta(x) \to \theta(x)$ в $\mathcal{S}'(\mathbb{R})$ при $a \to 0^+$

---

## Линейные преобразования в обобщённых функциях

$$
x = Ay + b \quad \text{— лин. преобр-е}
$$

$A$ — невырождена (базис переходя в базис) (диффеоморфизм) ($\det A \neq 0$)

$$
\langle f(y), \varphi(y) \rangle = \int_{\mathbb{R}^n} f(y) \varphi(y) \, dy
$$

---

## Носитель функции $\theta$

$$
\theta = 0 \quad \forall \Omega \subset (-\infty; 0) \quad \text{(как обобщ.)}
$$

$$
\Rightarrow O_\theta = (-\infty, 0)
$$

$$
\operatorname{supp} \theta = \mathbb{R} \setminus O_\theta = [0; \infty)
$$

---

## Пространства обобщённых функций $\mathcal{D}'$ и $\mathcal{S}'$

Пусть $\mathcal{F} = \mathcal{D}$ или $\mathcal{S}$. Определим топологию на $\mathcal{F}'$ как **слабую топологию**, т.е.

**Опр.** Послед-ть $\{f_k\}_{k \in \mathbb{N}} \subset \mathcal{F}'$ называется **сходящейся** к $f \in \mathcal{F}'$, если

$$
\lim_{k \to \infty} \langle f_k, \varphi \rangle = \langle f, \varphi \rangle \quad \forall \varphi \in \mathcal{F}
$$

(это **слабая сходимость**)

**Т** (полнота пр-ва $\mathcal{F}'$). Ф-л $f$ на $\mathcal{F}$ определённая на ф-ле $\langle f, \varphi \rangle := \lim_{k \to \infty} \langle f_k, \varphi \rangle$ $\forall \varphi \in \mathcal{F}$ является линейным и непрерывным, т.е. $f \in \mathcal{F}'$.

---

## Антисимметричные обобщённые функции

$$
A = \operatorname{diag}(-1, \ldots, -1)
$$

$$
\langle f(-x), \varphi(x) \rangle = \langle f(x), \varphi(-x) \rangle
$$

### Пример:

**1)** $\delta(ax) = \dfrac{1}{|a|^n} \delta(x)$ при $a \neq 0$

**Доказательство:**

$$
\langle \delta(ax), \varphi(x) \rangle = \frac{1}{|a|^n} \left\langle \delta(x), \varphi\left(\frac{x_1}{a}, \ldots, \frac{x_n}{a}\right) \right\rangle
$$

$$
= \frac{1}{|a|^n} \varphi(0) = \frac{1}{|a|^n} \langle \delta(x), \varphi(x) \rangle
$$

$$
\boxed{\delta(ax) = \frac{\delta(x)}{|a|^n}}
$$

**2)** $\displaystyle\sum_{k=0}^{\infty} a_k \delta(x-k)$ сходится в $\mathcal{S}'(\mathbb{R}^n)$, где $a_k$ — ф-ции, такие что $|a_k| \leq C(1+|k|)^m$ $\forall m \in \mathbb{N}$

$$
\left\langle \sum_{k=0}^{\infty} a_k \delta(x-k), \varphi(x) \right\rangle = \sum_{k=0}^{\infty} a_k \varphi(k) \in \mathbb{R}
$$

где $\varphi \in \mathcal{S}(\mathbb{R}^n)$

---

## Продолжение доказательства сходимости ряда

$$
\left|\sum_{k=0}^{\infty} a_k \varphi(k)\right| = |a_0 \varphi(0)| + \left|\sum_{k=1}^{\infty} a_k \varphi_k\right| \leq
$$

$$
\leq |a_0 \varphi(0)| + \left|\sum_{k=1}^{\infty} a_k \varphi(k)\right| \leq |a_0 \varphi(0)| + \sum_{k=1}^{\infty} |a_k \varphi(k)| \leq |a_0 \varphi(0)| + \sum_{k=1}^{\infty} \frac{C(1+|k|)^m}{|k|^{n+2}}
$$

Если $\varphi \in \mathcal{S}$, то $|\varphi(x)| \leq \dfrac{1}{|x|^{n+2}}$

$$
= |a_0 \varphi(0)| + C \sum_{k=1}^{\infty} \frac{1}{|k|^2} + C_m^1 \frac{|k|}{|k|^{n+2}} + \ldots + \frac{|k|^m}{|k|^{n+2}}
$$

(при $n = m+2$)

Ряд сходится.

---

## Линейная замена переменных

$$
y \mapsto Ay + b
$$

$$
\langle f(Ay+b), \varphi(y) \rangle = \int_{\mathbb{R}^n} f(Ay+b) \varphi(y) \, dy \quad \text{①}
$$

Замена координат: $x = Ay + b$

$$
\text{①} = \int_{\mathbb{R}^n} f(x) \varphi(A^{-1}(x-b)) \frac{dx}{|\det A|}
$$

Якобиан: $y = A^{-1}x - A^{-1}b$

$$
= \int_{\mathbb{R}^n} \frac{f(x)}{|\det A|} \varphi(A^{-1}(x-b)) \, dx
$$

(легко считается если знать внешнюю алгебру Грассмана)

$$
\forall \varphi \in \mathcal{D}(\mathbb{R}^n)
$$

### Примеры

**1)** сдвиг, $A = E$

$$
\langle f(y+b), \varphi(y) \rangle = \langle f(x), \varphi(x-b) \rangle
$$

$$
\langle \delta(x-y), \varphi(x) \rangle = \langle \delta(x), \varphi(x+y) \rangle = \varphi(y)
$$

**2)** масштаб, $A = \operatorname{diag}(a_{11}, \ldots, a_{nn})$

$$
\langle f(Ay), \varphi(y) \rangle = \frac{1}{|a_{11} \cdots a_{nn}|} \left\langle f(x), \varphi\left(\frac{x_1}{a_{11}}, \ldots, \frac{x_n}{a_{nn}}\right) \right\rangle
$$

<!-- 31-35 -->
## Лекция 9 (1-ая часть)

Пусть $f \in L^1_{\text{loc}}(\mathbb{R}^n)$, тогда $\forall g \in C^\infty(\mathbb{R}^n)$: $gf \in L^1_{\text{loc}}$.

$$
\int_K |gf| \, dx < \infty \quad \text{если} \quad \int_K |f| \, dx < \infty
$$

**Определение.** $B_{\text{loc}}(\mathbb{R}^n) := \{g \mid g|_K \text{ — ограничена } \forall K \Subset \mathbb{R}^n\}$ (компакт).

---

### Произведение обобщённой функции на гладкую

**Произведение** ОФ $f \in \mathcal{D}'(\mathbb{R}^n)$ на $g \in C^\infty(\mathbb{R}^n)$ — называется ОФ $gf$, действует на $\varphi \in \mathcal{D}(\mathbb{R}^n)$ по формуле:

$$
\langle gf, \varphi \rangle = \langle f, g\varphi \rangle, \quad g\varphi \in \mathcal{D}(\mathbb{R}^n)
$$

**Замечание:** это не работает для ОФ из $\mathcal{S}'(\mathbb{R}^n)$ (а пока только для $\mathcal{D}'$), потому что если $\varphi \in \mathcal{S}$ и $g \in C^\infty$, то $g\varphi \notin \mathcal{S}$.

---

## Примеры

### 1) $g(x)\delta(x)$

$$
\langle g(x)\delta(x), \varphi(x) \rangle = \langle \delta(x), g(x)\varphi(x) \rangle = g(0)\varphi(0)
$$

где $g \in C^\infty$, $\delta \in \mathcal{D}'$.

$$
= g(0)\langle \delta(x), \varphi(x) \rangle = \langle g(0)\delta(x), \varphi(x) \rangle
$$

(т.к. линейность обобщённых функций)

$$
\Rightarrow g(x)\delta(x) = g(0)\delta(x)
$$

**Лемма:** $f = g$ как обобщённые функции, когда $\forall \varphi \in \mathcal{D}$: $\langle f, \varphi \rangle = \langle g, \varphi \rangle$.

---

### 2) $x \cdot \text{v.p.}\dfrac{1}{x^2} = \text{v.p.}\dfrac{1}{x}$

$\forall \varphi \in \mathcal{D}$ имеем:

$$
\left\langle x \cdot \text{v.p.}\frac{1}{x^2}, \varphi \right\rangle = \left\langle \text{v.p.}\frac{1}{x^2}, x\varphi \right\rangle =
$$

$$
= \text{v.p.} \int_{-\infty}^{\infty} \frac{x\varphi(x) - 0 \cdot \varphi(0)}{x^2} \, dx = \text{v.p.} \int_{-\infty}^{\infty} \frac{x\varphi(x)}{x^2} \, dx =
$$

$$
= \left\langle \text{v.p.}\frac{1}{x}, \varphi \right\rangle
$$

---

### 3) $\text{pf}\left(\dfrac{1}{x^2+y^2}\right) \in \mathcal{D}'(\mathbb{R}^2)$

$$
\left\langle \text{pf}\left\{\frac{1}{x^2+y^2}\right\}, \varphi \right\rangle = \int_{x^2+y^2<1} \frac{\varphi(x,y) - \varphi(0,0)}{x^2+y^2} \, dx \, dy + \int_{x^2+y^2>1} \frac{\varphi(x,y)}{x^2+y^2} \, dx \, dy
$$

*[Рисунок: круг единичного радиуса в $\mathbb{R}^2$]*

**Владимиров 6.30:**

$$
\left\langle (x^2+y^2) \cdot \text{pf}\frac{1}{x^2+y^2}, \varphi \right\rangle = \left\langle \text{pf}\frac{1}{x^2+y^2}, (x^2+y^2)\varphi \right\rangle =
$$

$$
= \int_{x^2+y^2<1} \frac{(x^2+y^2)\varphi(x,y) - (x^2+y^2)\varphi(0,0)\big|_0}{x^2+y^2} \, dx \, dy +
$$

$$
+ \int_{x^2+y^2>1} \frac{(x^2+y^2)\varphi(x,y)}{x^2+y^2} \, dx \, dy \quad \text{}
$$

$$
\text{②} = \int_{x^2+y^2<1} \varphi(x,y) \, dx \, dy + \int_{x^2+y^2>1} \varphi(x,y) \, dx \, dy = \langle 1, \varphi \rangle
$$

$$
\forall \varphi \in \mathcal{D}
$$

$$
= \int_{\mathbb{R}^2} \varphi(x,y) \, dx \, dy
$$

т.е.

$$
(x^2+y^2) \, \text{pf}\frac{1}{x^2+y^2} = 1
$$

---

### Домашнее задание

Доказать, что

$$
x \cdot \text{v.p.}\frac{1}{x} = x^2 \, \text{v.p.}\frac{1}{x^2} = x^3 \, \text{v.p.}\frac{1}{x^3} = 1
$$

---

## Дифференцирование обобщённых функций

**1D-вид интегрирования по частям:**

$$
\int_{-\infty}^{\infty} f \, d\varphi = \int_{-\infty}^{\infty} \varphi \, df
$$

$$
\int_{-\infty}^{\infty} f' \varphi \, dx = \int_{-\infty}^{\infty} \varphi \, df = \varphi f \Big|_{-\infty}^{\infty} - \int_{-\infty}^{\infty} f \, d\varphi
$$

**Итог по частям:** $f \in C^k(\mathbb{R}^n)$, $\varphi \in \mathcal{D}(\mathbb{R}^n)$, тогда $\forall \alpha$, $|\alpha| \leq k$:

$$
\int_{-\infty}^{\infty} f^{(n)} \varphi \, dx = (-1)^n \int_{-\infty}^{\infty} f \, \varphi^{(n)} \, dx
$$

$$
\int_{\mathbb{R}^n} D^\alpha f(x) \, \varphi(x) \, dx = (-1)^{|\alpha|} \int_{\mathbb{R}^n} f(x) \, D^\alpha \varphi(x) \, dx
$$

---

### Определение производной ОФ

$f$ и $D^\alpha f$ локально интегрируемы $\Rightarrow$ они порождают ОФ из $\mathcal{D}(\mathbb{R}^n)$, причём

$$
\langle D^\alpha f, \varphi \rangle = (-1)^{|\alpha|} \langle f, D^\alpha \varphi \rangle
$$

**Опр.** Производной ОФ $f \in \mathcal{D}'$ называется ОФ $D^\alpha f \in \mathcal{D}'$:

$$
\langle D^\alpha f, \varphi \rangle = (-1)^{|\alpha|} \langle f, D^\alpha \varphi \rangle
$$

---

### Свойства обобщённой производной

$$
\langle D^\alpha f, \varphi \rangle = (-1)^{|\alpha|} \langle f, D^\alpha \varphi \rangle
$$

**1) Линейность:**

$$
\langle D^\alpha f, \alpha\varphi + \beta\psi \rangle = (-1)^{|\alpha|} \langle f, D^\alpha(\alpha\varphi + \beta\psi) \rangle
$$

$$
= (-1)^{|\alpha|} \langle f, \alpha D^\alpha \varphi \rangle + (-1)^{|\alpha|} \langle f, \beta D^\alpha \psi \rangle
$$

$$
= (-1)^{|\alpha|} \alpha \langle f, D^\alpha \varphi \rangle + (-1)^{|\alpha|} \beta \langle f, D^\alpha \psi \rangle = \alpha \langle D^\alpha f, \varphi \rangle + \beta \langle D^\alpha f, \psi \rangle
$$

*[9 лекция, 2-ая часть — после перерыва]*

**2) Непрерывность:**

$$
(D^\alpha f, \varphi) = (-1)^{|\alpha|} (f, D^\alpha \varphi)
$$

<!-- 36-40 -->
## Свойства обобщённой производной

**Св-ва дифф-я:**

1) $D^\alpha: \mathcal{D}'(\mathbb{R}^n) \to \mathcal{D}'(\mathbb{R}^n)$ — линейное, непрерывное отображение

2) Всякая ОФ дифференцируема, причём бесконечное число раз

3) $D^\beta D^\alpha f = D^\alpha D^\beta f$

4) $\operatorname{supp} D^\alpha f \subset \operatorname{supp} f$

5) $\forall f \in \mathcal{D}'(\mathbb{R}^n)$, $g \in C^\infty(\mathbb{R}^n)$:

$$
\frac{\partial}{\partial x_i}\big(g(x) f(x)\big) = \frac{\partial g(x)}{\partial x_i} f(x) + g(x) \frac{\partial f(x)}{\partial x_i}
$$

(формула Лейбница)

---

## Примеры

### Функция Хевисайда

$$
\theta(x) = \begin{cases} 1, & x \geq 0 \\ 0, & x < 0 \end{cases}
$$

*[График: ступенчатая функция, 0 при $x < 0$, 1 при $x \geq 0$]*

**Обычная производная:**

$$
\theta'(x) = \begin{cases} 0, & x \neq 0 \\ \text{не опр.}, & x = 0 \end{cases}
$$

**Обобщённая производная** [сингулярная]:

$$
\theta'(x) = \delta(x) = \begin{cases} 0, & x \neq 0 \\ \infty, & x = 0 \end{cases}
$$

**Доказательство:** $\forall \varphi \in \mathcal{D}'$:

$$
\langle \theta', \varphi \rangle = (-1)^1 \langle \theta, \varphi' \rangle = -\int_0^\infty \varphi' \, dx = -\int_0^{+\infty} d\varphi = -\varphi\Big|_0^{+\infty} = +\varphi(0) = \langle \delta, \varphi \rangle
$$

---

### Пример 2 ($g \in C^\infty$)

$$
g(x)\delta'(x) = -g'(0)\delta(x) + g(0)\delta'(x)
$$

**Вспомним:**

$$
\langle \delta', \varphi \rangle = (-1) \cdot \langle \delta, \varphi' \rangle = -\varphi'(0)
$$

(поэтому $\delta'$ так и обозначается — $\delta'$!)

**Через формулу Лейбница:**

$$
(g(x)\delta(x))' = g'(x)\delta(x) + g(x)\delta'(x)
$$

Но $g(x)\delta(x) = g(0)\delta(x) \Rightarrow (g(x)\delta(x))' = (g(0)\delta(x))' = g(0)\delta'(x)$

Отсюда:

$$
g(0)\delta'(x) = g'(0)\delta(x) + g(x)\delta'(x)
$$

---

### Пример 3

$$
(g(x)\theta(x))' = g(x)\delta(x) + g'(x)\theta(x)
$$

по формуле Лейбница тоже.

---

### Пример 4

$$
\frac{d}{dx} \text{v.p.}\frac{1}{x} = -\text{v.p.}\frac{1}{x^2}
$$

$\forall \varphi \in \mathcal{D}$:

$$
\left\langle \frac{d}{dx} \text{v.p.}\frac{1}{x}, \varphi \right\rangle = -\left\langle \text{v.p.}\frac{1}{x}, \varphi' \right\rangle = -\text{v.p.} \int_{-\infty}^{\infty} \frac{\varphi'(x)}{x} \, dx = -\lim_{\varepsilon \to 0} \int_{\mathbb{R} \setminus [-\varepsilon, \varepsilon]} \frac{\varphi'(x)}{x} \, dx
$$

Интегрируем по частям на $\mathbb{R} \setminus [-\varepsilon, \varepsilon]$:

$$
= -\lim_{\varepsilon \to 0} \left[ \frac{\varphi(x)}{x}\bigg|_{-\infty}^{-\varepsilon} + \frac{\varphi(x)}{x}\bigg|_{\varepsilon}^{\infty} - \int_{-\infty}^{-\varepsilon} \varphi(x)\left(-\frac{1}{x^2}\right) dx - \int_{\varepsilon}^{\infty} \varphi(x)\left(-\frac{1}{x^2}\right) dx \right]
$$

$$
= -\lim_{\varepsilon \to 0} \left[ \frac{\varphi(-\varepsilon)}{-\varepsilon} - \frac{\varphi(\varepsilon)}{\varepsilon} + \int_{\mathbb{R} \setminus [-\varepsilon, \varepsilon]} \frac{\varphi(x)}{x^2} \, dx \right]
$$

Добавляем и вычитаем $\dfrac{2\varphi(0)}{\varepsilon}$:

$$
= -\lim_{\varepsilon \to 0} \left[ \frac{-\varphi(-\varepsilon) - \varphi(\varepsilon) + 2\varphi(0)}{\varepsilon} + \left(\int_{-\infty}^{-\varepsilon} + \int_{\varepsilon}^{\infty}\right) \frac{\varphi(x) - \varphi(0)}{x^2} \, dx \right]
$$

Первое слагаемое $\to -\varphi'(0) + \varphi'(0) = 0$, второе даёт $-\left\langle \text{v.p.}\dfrac{1}{x^2}, \varphi \right\rangle$.

Итого:

$$
\frac{d}{dx} \text{v.p.}\frac{1}{x} = -\text{v.p.}\frac{1}{x^2} \quad \text{(как обобщённая ф-я)}
$$

> **Замечание:** v.p. — это перенормировка. Может ли она зависеть от того, какая особенность (какого рода)?

---

## Лекция 10

Пусть $f \in C^1(x \leq x_0) \cap C^1(x > x_0)$. Тогда:

$$
f'_{\text{об}} = \{f'\} + [f]_{x_0} \, \delta(x - x_0)
$$

где:
- $f'_{\text{об}}$ — обобщённая производная
- $\{f'\}$ — обычная (классическая) производная
- $[f]_{x_0}$ — скачок функции в точке $x_0$

---

### Скачок функции $1/x$ в нуле

$$
\left[\frac{1}{x}\right]_0 = \frac{1}{x}(0^+) - \frac{1}{x}(0^-) = \infty + \infty = \infty
$$

$$
\left[\frac{1}{x}\right]_x = \begin{cases} 0, & x \neq 0 \\ \infty, & x = 0 \end{cases} \quad \text{(сингулярная)}
$$

как обобщённая ф-я. $\dfrac{1}{x}$ — непрерывна $\forall x \neq 0$.

---

## Домашнее задание

1) $\left[\dfrac{1}{x}\right]_x' = \delta(x)$ (доказать) (?)

2) $x^2 \cdot \text{v.p.}\dfrac{1}{x^3} = \text{v.p.}\dfrac{1}{x}$

3) $x^3 y''' = 0$ — найти решения в $\mathcal{D}'$

---

## Теорема о связи классической и обобщённой производных кусочно-гладкой функции

**Тв.** $\forall$ кусочно-гладкой функции $f: \mathbb{R} \to \mathbb{C}$:

$$
f'_{\text{об}} = f'_{\text{кл}} + \sum_k [f]_{x_k} \, \delta(x - x_k)
$$

где скачок:

$$
[f]_{x_k} = f(x_k + 0) - f(x_k - 0) = \lim_{h \to 0^+} f(x_k + h) - \lim_{h \to 0^+} f(x_k - h)
$$

---

## Уравнение $x^m y = 0$ в $\mathcal{D}'$

**Утв.:** $x^m y = 0$, где $x, y \in \mathcal{D}'$.

Тогда общее решение имеет вид:

$$
y = \sum_{k=0}^{m-1} c_k \, \delta^{(k)}, \quad c_k \in \mathbb{R}
$$

**Доказательство:**

$$
\left\langle x^m \cdot \sum_{k=0}^{m-1} c_k \delta^{(k)}, \varphi \right\rangle = \left\langle \sum_{k=0}^{m-1} c_k \, x^m \delta^{(k)}, \varphi \right\rangle = \sum_{k=0}^{m-1} c_k \langle x^m \delta^{(k)}, \varphi \rangle = \sum_{k=0}^{m-1} c_k \langle \delta^{(k)}, x^m \varphi \rangle = \ldots
$$

(продолжение следует — применение формулы $\langle \delta^{(k)}, \psi \rangle = (-1)^k \psi^{(k)}(0)$ к $\psi = x^m \varphi$).

<!-- 41-45 -->
## Продолжение решения уравнения

$$
= \sum_{k=0}^{m-1} c_k (-1)^k \langle \delta(x), x^m \varphi(x) \rangle^{(k)} \quad \text{②}
$$

$$
\text{②} = \sum_{k=0}^{m-1} c_k (-1)^k \left\langle \delta(x), \sum_{i=0}^k C_i^k (x^m)^{(i)} \varphi^{(k-i)} \right\rangle
$$

$$
= \sum_{k=0}^{m-1} c_k (-1)^k \left\langle \delta(x), \sum_{i=0}^k C_i^k \frac{m!}{(m-i)!} x^{m-i} \varphi^{(k-i)} \right\rangle
$$

$$
= \sum_{k=0}^{m-1} \sum_{i=0}^k (-1)^k c_k C_i^k \frac{m!}{(m-i)!} \langle \delta(x), x^{m-i} \varphi^{(k-i)} \rangle \bigg|_{x=0} = 0
$$

---

## Найти общее решение

**Найти общее решение:**

$$
x^2 y'' = 0 \quad \text{в } \mathcal{D}'
$$

**Решение:**

$$
y = c_0 \frac{x^2}{2} \theta(x) + c_1 x \theta(x) + c_2 \frac{x^2}{2} + c_3 x + c_4
$$

где $\theta$ — функция Хевисайда.

---

### Решение через дельта-функции

$$
x^2 y'' = 0 \text{ в } \mathcal{D}' \iff y'' = \sum_{k=0}^{2-1} c_k \delta^{(k)} = c_0 \delta(x) + c_1 \delta'(x)
$$

$$
y'' = c_0 \delta(x) + c_1 \delta'(x)
$$

---

## Интегрирование дельта-функции

Интегрируем $\delta(x)$:

$$
\theta'(x) = \delta(x)
$$

$$
y'' = c_0 \theta(x) + c_1 \delta(x) + c_2
$$

**Проверка:**

$$
\theta = (x\theta(x) + c)' = (x\theta)' = \theta + x\delta(x) = \theta + 0 \cdot \delta(x)
$$

Отсюда:

$$
y' = c_0 x\theta(x) + c_1 \theta(x) + c_2 x + c_3
$$

$$
y = \frac{c_0 x^2 \theta(x)}{2} + c_1 x \theta(x) + \frac{c_2 x^2}{2} + c_3 x + c_4
$$

---

## Домашнее задание

**Д/З:**

1. с предыдущей лекции — 4-ое задание
2. с этой лекции — все задания (письменно)
3. видео [11]

*подробнее не выписано*

---

## Сходимость в $\mathcal{D}(\mathbb{R}^n)$

$\varphi_k$ сходится в $\mathcal{D}(\mathbb{R}^n)$ к функции $\varphi \in \mathcal{D}$, если:

$$
\{f_k\} \xrightarrow[k \to \infty]{} f \quad \text{в } \mathcal{D}' \text{ (ОФ)}, \text{ если}
$$

$$
\langle f_k, \varphi \rangle \to \langle f, \varphi \rangle \quad \forall \varphi \in \mathcal{D}
$$

$$
\{\varphi_k\}_k \xrightarrow[k \to \infty]{} \varphi \quad \text{в } \mathcal{D} \text{ (если)}
$$

$$
\forall \alpha \quad D^\alpha \varphi_k \rightrightarrows D^\alpha \varphi
$$

---

## Теорема о разложении

**Т-ма из Гельфанда, Шилова:**

$$
\varphi(x,y) \in \mathcal{D}(\mathbb{R}^{n+m}) \text{ аппроксимируется:}
$$

$$
\sum_{i=1}^L \varphi_i(x) \psi_i(y), \quad \text{где } \varphi_i \in \mathcal{D}(\mathbb{R}^n), \quad \psi_i \in \mathcal{D}(\mathbb{R}^m)
$$

$$
L \to \infty
$$

$$
\lim_{L \to \infty} \sum_{i=1}^L \varphi_i(x) \psi_i(y) = \varphi(x,y)
$$

т.е. в-вом вида $\displaystyle\sum_{i=1}^L \varphi_i(x) \psi_i(y)$ плотно в $\mathcal{D}(\mathbb{R}^{n+m})$.

---

## Лекция [видео 11]

### Тензорное произведение функций

Тензорное произведение ф-ий $f(x)$ и $g(y)$:

$$
h = f \otimes g(x,y) = f(x)g(y): \mathbb{R}^{n+m} \to \mathbb{Z} \quad \text{мн-во значений}
$$

**Пример:** $e^{x+y} = e^x e^y$

Если $f \in L^1_{\text{loc}}(\mathbb{R}^n)$, $g \in L^1_{\text{loc}}(\mathbb{R}^m)$, тогда $f \otimes g(x,y)$ тоже $\in L^1_{\text{loc}}(\mathbb{R}^{n+m})$.

---

### Тензорное произведение обобщённых функций

Тогда:

$$
(f \otimes g(x,y), \varphi(x,y)) = \int_{\mathbb{R}^{n+m}} f(x)g(y)\varphi(x,y) \, dx \, dy \quad \text{①}
$$

$$
\text{①} = \int_{\mathbb{R}^n} f(x) \left( \int_{\mathbb{R}^m} g(y)\varphi(x,y) \, dy \right) dx = \langle f(x), \langle g(y), \varphi(x,y) \rangle \rangle
$$

Пусть $f \in \mathcal{D}'(\mathbb{R}^n)$, $g \in \mathcal{D}'(\mathbb{R}^m)$, тогда их тензорное произведение — это ОФ $f \otimes g \in \mathcal{D}'(\mathbb{R}^{n+m})$, действующая по ф-ле:

$$
(f \otimes g, \varphi(x,y)) = (f(x), (g(y), \varphi(x,y))) \quad \forall \varphi \in \mathcal{D}(\mathbb{R}^{n+m})
$$

(о-во корректности опр-я — в лекции)

---

## Свойства тензорного произведения

**Св-ва тенз. пр-я:**

1) $f \otimes g = g \otimes f$ (коммутативность)

2) $(\alpha f + \beta g) \otimes h = \alpha(f \otimes h) + \beta(g \otimes h)$

билинейность и билинейность — и коммут-ть

3) $(f \otimes g) \otimes h = f \otimes (g \otimes h)$ — ассоциативность

4) $\forall \alpha \quad D_x^\alpha (f(x) \otimes g(y)) = D_x^\alpha f(x) \otimes g(y)$

5) $\forall a \in C^\infty(\mathbb{R}^n) \quad a(x)(f(x) \otimes g(y)) = (a(x)f(x)) \otimes g(y)$

6) $\operatorname{supp}(f \otimes g) = \operatorname{supp} f \times \operatorname{supp} g$

---

## Домашнее задание

**Д/З:**

1) $\varphi_{L,k}(x) = \left\langle g(y), \displaystyle\sum_{i=0}^L \varphi_i(x) \psi_{i,k}(y) \right\rangle \to 0$, тогда $\varphi_{i,k}(x) \psi_{i,k}(y) \to 0$ в $\mathcal{D}$

2) $\operatorname{supp}(f \otimes g) = \operatorname{supp} f \times \operatorname{supp} g$


<!-- 46-50 -->

## Сходимость в $\mathcal{D}(\mathbb{R}^n)$

$\varphi_k$ сходится в $\mathcal{D}(\mathbb{R}^n)$ к функции $\varphi \in \mathcal{D}$, если:

$$
\{f_k\} \xrightarrow[k \to \infty]{} f \quad \text{в } \mathcal{D}' \text{ (ОФ)}, \text{ если}
$$

$$
\langle f_k, \varphi \rangle \to \langle f, \varphi \rangle \quad \forall \varphi \in \mathcal{D}
$$

$$
\{\varphi_k\}_k \xrightarrow[k \to \infty]{} \varphi \quad \text{в } \mathcal{D} \text{ (если)}
$$

$$
\forall \alpha \quad D^\alpha \varphi_k \rightrightarrows D^\alpha \varphi
$$

---

## Теорема о разложении

**Теорема из Гельфанда, Шилова:**

$$
\varphi(x,y) \in \mathcal{D}(\mathbb{R}^{n+m}) \text{ аппроксимируется:}
$$

$$
\sum_{i=1}^L \varphi_i(x) \psi_i(y), \quad \text{где } \varphi_i \in \mathcal{D}(\mathbb{R}^n), \quad \psi_i \in \mathcal{D}(\mathbb{R}^m)
$$

$$
L \to \infty
$$

$$
\lim_{L \to \infty} \sum_{i=1}^L \varphi_i(x) \psi_i(y) = \varphi(x,y)
$$

т.е. функциями вида $\displaystyle\sum_{i=1}^L \varphi_i(x) \psi_i(y)$ плотно в $\mathcal{D}(\mathbb{R}^{n+m})$.

---

## Семинар (видео [12])

### Домашнее задание

**Д/З:** #8.4 (Владимиров) — по индукции

*(во Владимире $\otimes$ обозначает $f \otimes g$ — это $f \cdot g$)*

---

### Тензорное произведение с единицей

$f(x) \in \mathcal{D}'(\mathbb{R}^n)$, $1 \in \mathcal{D}'(\mathbb{R}^n)$

$f \otimes 1$ — не зависит от $y$.

$\forall \varphi(x,y) \in \mathcal{D}(\mathbb{R}^{n+m})$:

$$
(f(x) \otimes 1(y), \varphi(x,y)) = (f(x), (1(y), \varphi(x,y))) \quad \text{(по опр.)}
$$

$$
= \left(f(x), \int_{\mathbb{R}^n} \varphi(x,y) \, dy\right)
$$

Пусть $f \in L^1_{\text{loc}}(\mathbb{R}^n) \Rightarrow (1(y) \otimes f(x), \varphi(x,y)) = (1(y), (f(x), \varphi(x,y))) = \displaystyle\int_{\mathbb{R}^m} (f(x), \varphi(x,y)) \, dy$

$$
\Rightarrow \left(f(x), \int_{\mathbb{R}^m} \varphi(x,y) \, dy\right) = \int_{\mathbb{R}^m} (f(x), \varphi(x,y)) \, dy
$$

---

## Пример: $\delta(at - |x|)$

Пусть $\delta(at - |x|) \in \mathcal{D}'(\mathbb{R}^2)$, $a > 0$.

**Определение по формуле:**

$$
\delta(at - |x|) = \theta(t) \otimes \delta(at + x) + \theta(t) \otimes \delta(at - x)
$$

(функция Хевисайда)

Вычислим:

$$
(\theta(t) \otimes \delta(at+x), \varphi(t,x)) = (\theta(t), (\delta(at+x), \varphi(t,x))) = (\theta(t), \varphi(t, -at)) = \int_0^{+\infty} \varphi(t, -at) \, dt
$$

Аналогично:

$$
(\theta(t) \otimes \delta(at-x), \varphi(t,x)) = \int_0^{+\infty} \varphi(t, at) \, dt
$$

---

## Функция $\theta(at - |x|)$

$$
\theta(at - |x|) = \begin{cases} 1, & |x| \leq at \\ 0, & |x| > at \end{cases}
$$

Выше показано:

$$
(\theta(t) \otimes \delta(at+x), \varphi(t,x)) = \int_0^{+\infty} \varphi(t, -at) \, dt
$$

$$
(\theta(t) \otimes \delta(at-x), \varphi(t,x)) = \int_0^{+\infty} \varphi(t, at) \, dt
$$

**Носитель** $\operatorname{supp} \theta(at - |x|)$ — **конус будущего**.

*[График: конус в плоскости $(t,x)$ с границами $x = -at$ и $x = at$]*

---

### Производная $\dfrac{\partial}{\partial t} \theta(at - |x|)$

Посчитаем и докажем, что:

$$
\frac{\partial}{\partial t} \theta(at - |x|) = a \, \delta(at - |x|)
$$

Пусть $\varphi(t,x) \in \mathcal{D}(\mathbb{R}^2) \Rightarrow$

$$
\left(\frac{\partial}{\partial t} \theta(at - |x|), \varphi(t,x)\right) = -1 \cdot \left(\theta(at - |x|), \frac{\partial}{\partial t} \varphi(t,x)\right)
$$

$$
= -\int_{\mathbb{R}_t \times \mathbb{R}_x} \theta(at - |x|) \frac{\partial}{\partial t} \varphi(t,x) \, dt \, dx = -\int_{-\infty}^0 dx \int_{-x/a}^{\infty} \frac{\partial \varphi}{\partial t} \, dt + \int_0^{+\infty} dx \int_{x/a}^{+\infty} \frac{\partial \varphi}{\partial t} \, dt
$$

$$
= -\int_{-\infty}^0 \left(\varphi(t,x)\Big|_{t=-x/a} - 0\right) dx - \int_0^{+\infty} \left(0 - \varphi(t,x)\Big|_{t=x/a}\right) dx
$$

$$
= -\int_{-\infty}^0 \left(0 - \varphi\left(-\frac{x}{a}, x\right)\right) dx - \int_0^{+\infty} \left(0 - \varphi\left(\frac{x}{a}, x\right)\right) dx
$$

$$
= \int_{-\infty}^0 \varphi\left(-\frac{x}{a}, x\right) dx + \int_0^{+\infty} \varphi\left(\frac{x}{a}, x\right) dx
$$

Замена переменной $\tau = -x/a$ в первом интеграле и $\tau = x/a$ во втором:

$$
= -a \int_{-\infty}^0 \varphi(\tau, -a\tau) \, d\tau + a \int_0^{+\infty} \varphi(\tau, a\tau) \, d\tau
$$

$$
= a \left(\int_0^{+\infty} \varphi(\tau, -a\tau) \, d\tau + \int_0^{+\infty} \varphi(\tau, a\tau) \, d\tau\right)
$$

$$
= a \big((\theta(t) \otimes \delta(at+x), \varphi(t,x)) + (\theta(t) \otimes \delta(at-x), \varphi(t,x))\big)
$$

$$
= (a \, \delta(at - |x|), \varphi(t,x))
$$

$$
\boxed{\Rightarrow \quad \frac{\partial}{\partial t} \theta(at - |x|) = a \, \delta(at - |x|)}
$$

<!-- 51-55 -->

## Решение уравнений в $\mathcal{D}'(\mathbb{R})$

**Решить** (над $\mathcal{D}'(\mathbb{R})$):

### 1) $y'' = \delta$

**Решение:**

$$
y' = \theta + C_0
$$

$$
y = x\theta(x) + C_0 x + C_1
$$

**Известные формулы:**

- $\theta' = \delta$
- $(x\theta(x))' = \theta(x)$
- $\varphi\delta(x) = \varphi(0)\delta(x)$
- $\left(\text{v.p.}\frac{1}{x}\right)' = -\text{v.p.}\frac{1}{x^2}$
- $\left(\text{v.p.}\frac{1}{x^2}\right)' = -2\text{v.p.}\frac{1}{x^3}$

---

### Домашнее задание

Доказать:

$$
\left(\text{v.p.}\frac{1}{x^2}\right)' = -2\text{v.p.}\frac{1}{x^3}
$$

---

### Решение уравнения $x^2 y''' = 0$ в $\mathcal{D}'$

Решение (было в Д/З когда-то):

$$
y = c_0 \frac{x^2}{2}\theta(x) + c_1 x\theta(x) + c_2 \frac{x^2}{2} + c_3 x + c_4
$$

---

### Решение неоднородного уравнения

Решить ур-е:

$$
x^2 y''' = \text{v.p.}\frac{1}{x} \quad \text{(общее реш-е)}
$$

Неоднородное ур-е:

**Общее решение** = $\Sigma$ частного решения неоднородного + общее решение однородного

$$
x^2 y''' = \text{v.p.}\frac{1}{x}
$$

$$
y''' = \frac{1}{x^2} \text{v.p.}\frac{1}{x} = \text{v.p.}\frac{1}{x^3}
$$

---

## Продолжение решения

$$
x^2 \text{v.p.}\frac{1}{x^3} = \text{v.p.}\frac{1}{x} \quad \Rightarrow \quad \text{v.p.}\frac{1}{x^3} = \frac{1}{x^2} \text{v.p.}\frac{1}{x}
$$

$$
\left(x^2 \text{v.p.}\frac{1}{x^3}, \varphi\right) = \left(\text{v.p.}\frac{1}{x}, \varphi\right)
$$

$$
\left(\text{v.p.}\frac{1}{x^3}, x^2\varphi\right) = \text{v.p.} \int_{\mathbb{R}} \frac{x^2 \varphi}{x^3} dx \quad \text{①}
$$

$$
\text{①} = \text{v.p.} \int_{\mathbb{R}} \frac{\varphi}{x} dx = \left(\text{v.p.}\frac{1}{x}, \varphi\right)
$$

$$
\left(\text{v.p.}\frac{1}{x^2}\right)' = -2\text{v.p.}\frac{1}{x^3} \quad \Rightarrow \quad \text{v.p.}\frac{1}{x^3} = -\frac{1}{2} \left(\text{v.p.}\frac{1}{x^2}\right)'
$$

Отсюда:

$$
y''' = \left(-\frac{1}{2} \text{v.p.}\frac{1}{x^2}\right)'
$$

$$
y'' = -\frac{1}{2} \text{v.p.}\frac{1}{x^2}
$$

$$
y'' = \left(\frac{1}{2} \text{v.p.}\frac{1}{x}\right)'
$$

$$
y' = \frac{1}{2} \text{v.p.}\frac{1}{x} = \frac{1}{2} (\ln|x|)'
$$

$$
y = \frac{1}{2} \ln|x| \quad \text{— частное реш-е}
$$

**Заметка:** $\ln|x| \in L^1_{\text{loc}}(\mathbb{R})$

$$
(\ln|x|, \varphi) := \text{v.p.} \int_{\mathbb{R}} \ln|x| \, \varphi \, dx
$$

ОФ $\ln|x|$ определена.

**Утв.:** $(\ln|x|)' = \text{v.p.}\frac{1}{x}$ в $\mathcal{D}'(\mathbb{R})$

---

## Вычисление производной $\ln|x|$

$$
((\ln|x|)', \varphi) = -(\ln|x|, \varphi') = -\text{v.p.} \int_{\mathbb{R}} \ln|x| \, \varphi' \, dx \quad \text{①}
$$

$$
\text{①} = \text{v.p.} \int_{\mathbb{R}} (\ln|x|)' \, \varphi \, dx = \text{v.p.} \int_{\mathbb{R}} \frac{\varphi}{x} \, dx = \left(\text{v.p.}\frac{1}{x}, \varphi\right)
$$

$$
\left[ (f, \varphi) = \text{v.p.} \int_{\mathbb{R}} f \varphi \, dx \right]
$$

(одинаково для всех)

---

### Общее решение

$$
y = \frac{1}{2} \ln|x| + c_0 \frac{x^2}{2} \theta(x) + c_1 \theta(x) + c_2 \frac{x^2}{2} + c_3 x + c_4
$$

$\uparrow$ общее решение

---

### Замечание о решениях

Если $x \neq 0$, то $\text{v.p.}\frac{1}{x} = \frac{1}{x}$ — рег. ОФ

$$
x^2 y''' = \frac{1}{x} \quad \text{в } \mathbb{R} \setminus \{0\} \quad \longleftarrow \quad \text{реш-е: } y = \frac{1}{2} \ln|x| + c_2 \frac{x^2}{2} + c_3 x + c_4
$$

т.е., в сравнении решений:

в точке $0$ возникла гетерь $\left[c_0 \frac{x^2}{2} \theta(x) + c_1 \theta(x)\right]$

$\theta$: $\_\_\_\_\_\_\_$

**Вывод:** (чудесный!) реш-я над ОФ содержат в себе чудеса решений над обычными ф-ями.

---

## Домашнее задание

**Решить** (над $\mathcal{D}'(\mathbb{R})$):

1) $xy' = \text{v.p.}\frac{1}{x}$

2) $xy' = 1$

---

## Лекция (видео [14] — 4-ый час)

### Определение свёртки

Пусть $f, g \in L^1_{\text{loc}}(\mathbb{R}^n)$. Их **свёртка** — это (это свёртка локально интегрируемых ф-й):

$$
(f * g)(x) = \int_{\mathbb{R}^n} f(t) g(x-t) \, dt = \int_{\mathbb{R}^n} g(t) f(x-t) \, dt,
$$

если эти интегралы $\exists$.

---

### Важное замечание

**НЕВЕРНО**, что $\forall f, g \in L^1_{\text{loc}}(\mathbb{R}^n) \Rightarrow f * g \in L^1_{\text{loc}}(\mathbb{R}^n)$

**Случаи, когда $f * g \in L^1_{\text{loc}}$:**

1) $f$ — финитна или $g$ — финитна

2) $f, g \in L^1(\mathbb{R}^n)$

3) $f \in L^1(\mathbb{R}^n)$, $g$ — ограничена на $\mathbb{R}^n$ (или наоборот)

---

## Доказательство для $L^1$

Пусть $f, g \in L^1(\mathbb{R})$. Тогда $\|f\|_{L^1}, \|g\|_{L^1} < \infty$

(т.е. $\displaystyle\int_{\mathbb{R}} |f| dx < \infty$)

Тогда:

$$
\|f * g\|_{L^1} = \int_{\mathbb{R}} |f * g(x)| \, dx = \int_{\mathbb{R}} \left|\int_{\mathbb{R}} f(t) g(x-t) \, dt\right| dx \quad \text{①}
$$

$$
\text{①} \leq \int_{\mathbb{R}} \int_{\mathbb{R}} |f(t)| \, |g(x-t)| \, dt \, dx = \int_{\mathbb{R}} \int_{\mathbb{R}} |f(t)| \, |g(x-t)| \, dx \, dt
$$

(по теореме Фубини)

$$
= \int_{\mathbb{R}} |f(t)| \left(\int_{\mathbb{R}} |g(x-t)| \, dx\right) dt = \int_{\mathbb{R}} |f(t)| \left(\int_{\mathbb{R}} |g(x-t)| \, d(x-t)\right) dt
$$

$$
= \int_{\mathbb{R}} |f(t)| \cdot \|g\|_{L^1(\mathbb{R})} \, dt = \|g\|_{L^1} \cdot \int_{\mathbb{R}} |f(t)| \, dt = \|g\|_{L^1} \|f\|_{L^1} < \infty
$$

Следовательно, $f * g \in L^1(\mathbb{R}^n)$.

---

### Случай локальной интегрируемости

$f * g \in L^1_{\text{loc}}(\mathbb{R}^n)$

$$
\int_K |f * g(x)| \, dx = \int_K \left|\int_{\mathbb{R}^n} g(t) f(x-t) \, dt\right| \leq \int_K \int_{\mathbb{R}^n} |g(t)| \, |f(x-t)| \, dt
$$

Если $g$ ограничена, то:

$$
= C \int_K \|f\|_{L^1(\mathbb{R}^n)} \, dt = C \|f\|_{L^1(\mathbb{R}^n)} \int_K dt
$$

$$
\Rightarrow C \|f\|_{L^1} \mu(K) < \infty
$$

(где $K \subset \mathbb{R}^n$ ограниченное)

<!-- 56-60 -->
## Свёртка обобщённых функций

Пусть $f, g, f*g \in L^1_{\text{loc}}(\mathbb{R}^n)$, $\varphi \in \mathcal{D}(\mathbb{R}^n)$.

Тогда:

$$
((f*g)(x), \varphi(x)) = \int_{\mathbb{R}^n} \left(\int_{\mathbb{R}^n} f(\xi) g(x-\xi) \, d\xi\right) \varphi(x) \, dx \quad \text{}
$$

$$
\text{①} = \int_{\mathbb{R}^n} \int_{\mathbb{R}^n} f(\xi) g(\eta) \varphi(\xi+\eta) \, d\eta \, d\xi \quad \text{②}
$$

$$
\text{②} = (f(\xi) \otimes g(\eta), \varphi(\xi+\eta)) \quad \text{(*)}
$$

**Замечание:** ф-я $\varphi(\eta+\xi)$ не является финитной ф-ей от $\xi$ и $\eta$!

$$
\varphi(\xi+\eta) \notin \mathcal{D}(\mathbb{R}^n) \quad \text{хотя } \varphi(x) \text{ — финитна, } x \in \mathbb{R}^n
$$

$\xi + \eta \in \mathbb{R}^n + \mathbb{R}^n$

Пусть $n=1$, $\varphi \in \mathcal{D}(\mathbb{R}^n) \Rightarrow \operatorname{supp} \varphi = [a, b]$

$\Rightarrow \operatorname{supp} \varphi(\xi+\eta)$ — полоса между прямыми $\xi+\eta = a$ и $\xi+\eta = b$

т.к. $a \leq x \leq b$, $a \leq \xi+\eta \leq b$

---

## Условие корректности свёртки

А что делать, чтобы стало $\varphi(\xi+\eta) \in \mathcal{D}(\mathbb{R}^n)$?

Вспомним, что:

$$
\operatorname{supp} f(x) \otimes g(y) = \operatorname{supp} f(x) \times \operatorname{supp} g(y)
$$

(*) имеет смысл если $\varphi(\xi+\eta) \in \mathcal{D}(\mathbb{R}^n)$, т.е. если $\operatorname{supp} \varphi(\xi+\eta) \cap \operatorname{supp}(f(\xi) \otimes g(\eta))$ по огранич. мн-ву.

Тогда $\varphi(\xi+\eta)$ можно заменить на $\psi(\xi, \eta)$, где $\psi \in \mathcal{D}(\mathbb{R}^{2n})$.

$$
\Rightarrow (f*g(x), \varphi(x)) = (f(\xi) \otimes g(\xi), \varphi(\xi+\eta)) \in \mathcal{D}(\mathbb{R}^{2n})
$$

### Частные случаи

1) $f$ и $g$ — финитны

2) на $\mathbb{R}$, если $\operatorname{supp} f$ и $\operatorname{supp} g$ ограничены с одной стороны

3) более слабые условия (см. Владимиров §8)

---

## Свёртка ОФ $f$ и $g$

$$
(f(x) * g(x), \varphi(x)) = (f(x) \otimes g(y), \varphi(x+y)) = (f(x), (g(y), \varphi(x+y)))
$$

определение $f*g$ для ОФ [доказательство в видео]

---

## Свойства свёртки

**Св-ва свёртки:**

1) $f * g = g * f$

2) $f * g$ билинейна

3) $D^\alpha(f * g) = D^\alpha f * g = f * D^\alpha g$

4) $f * g$ не ассоциативна (!) (скобки важны)

**Замечание:** Свёртка с $\delta$-ф-ей всегда существует и $f(x) * \delta(x) = f(x)$

---

## Семинар (видео [14] — 2-ая часть)

### Примеры решения задач

**1)** $\theta(x-a) * \theta(x-b)$, $0 \leq a \leq b$

$\forall \varphi \in \mathcal{D}(\mathbb{R})$:

$$
(\theta(x-a) * \theta(x-b), \varphi(x)) = (\theta(x-a) \otimes \theta(y-b), \varphi(x+y))
$$

$$
= (\theta(x-a), (\theta(y-b), \varphi(x+y))) = \left(\theta(x-a), \int_0^{+\infty} \varphi(x+y+b) \, dy\right)
$$

$$
= \left(\theta(x-a), \int_0^{+\infty} \varphi(x+y+b) \, dy\right) = \left(\theta(x), \int_0^{+\infty} \varphi(x+y+a+b) \, dy\right)
$$

$$
= \int_0^{+\infty} \int_0^{+\infty} \varphi(x+y+a+b) \, dy \, dx = \int_0^{+\infty} \int_x^{+\infty} \varphi(r+a+b) \, dr \, dx
$$

**Замена:** $x+y = r$; потом меняем интеграл:

$$
= \int_0^{+\infty} \int_0^r \varphi(r+a+b) \, dx \, dr = \int_0^{+\infty} \varphi(r+a+b) \cdot r \, dr
$$

$$
= (\theta(r), r\varphi(r+a+b)) = (r\theta(r), \varphi(r+a+b))
$$

$$
= ((r-a-b)\theta(r-a-b), \varphi(r)) \Rightarrow
$$

$$
\boxed{\theta(x-a) * \theta(x-b) = (x-a-b)\theta(x-a-b)}
$$

Если $a = b = 0$:

$$
\boxed{\theta(x) * \theta(x) = x\theta(x)}
$$

---

**2)** $x\theta(t) * t\theta(x)$ — посчитать:

1) проверить $\operatorname{supp} x\theta(t) \cap \operatorname{supp} t\theta(x)$ — наличие

$$
\operatorname{supp}(x\theta(t) * t\theta(x)) = \{(x,y,t,r) \in \mathbb{R}^4 \mid x,y,t,r \in \mathbb{R}, \, y,t \geq 0\}
$$

$$
(x\theta(t) + t\theta(x), \varphi(xt)) = (x\theta(t) \otimes r\theta(y), \varphi(x+t))
$$

<!-- 61-65 -->

## Пример

Линейный дифференциальный оператор с постоянными коэффициентами:

$$
L(D) = D^{2,0} + 5D^{1,1} + \sqrt{3}\, D^{0,1} + \frac{1}{2} D^{0,2} + D^{0,0}
$$

Соответствие переменных $x, y$:

$$
D^{2,0} \to \frac{\partial^2}{\partial x^2}, \quad D^{1,1} \to \frac{\partial^2}{\partial x \partial y}, \quad D^{0,1} \to \frac{\partial}{\partial y}, \quad D^{0,2} \to \frac{\partial^2}{\partial y^2}, \quad D^{0,0}u = u \quad \text{(сама ф-я)}
$$

---

### Фундаментальное решение

**Определение.** Фундаментальное решение $L(D)$ — это ОФ $\varepsilon \in \mathcal{D}'(\mathbb{R}^n)$, такая что:

$$
L(D)\varepsilon(x) = \delta(x)
$$

**Замечание:** $\varepsilon$ определено с точностью до решения однородного ур-я $L(D)\varepsilon_0(x) = 0$.

---

### Теорема

Если $f \in \mathcal{D}'(\mathbb{R}^n)$ и свёртка $\varepsilon(x) * f(x)$ существует в $\mathcal{D}'(\mathbb{R}^n)$, то ур-е $L(D)u = f(x)$ имеет единственное обобщённое решение:

$$
u = \varepsilon(x) * f(x)
$$

---

## Пример: ОДУ с постоянными коэффициентами

$$
L\left(\frac{d}{dt}\right) = \frac{d^n}{dt^n} + a_1 \frac{d^{n-1}}{dt^{n-1}} + \ldots + a_{n-1}\frac{d}{dt} + a_n, \quad a_i \in \mathbb{R}
$$

**Утверждение:** $\varepsilon(t) = Z(t)\theta(t)$, где $Z(t)$ — решение задачи Коши:

$$
Z \in C^\infty(\mathbb{R}), \quad \begin{cases} L Z(t) = 0 \\ Z(0) = Z'(0) = \ldots = Z^{(n-2)}(0) = 0 \\ Z^{(n-1)}(0) = 1 \end{cases}
$$

**Доказательство** $L\varepsilon(t) = \delta(t)$:

$$
\varepsilon'(t) = Z'(t)\theta(t) + Z(t)\theta'(t) = Z'(t)\theta(t) + Z(t)\delta(t) = Z'(t)\theta(t) + Z(0)\delta(t) = Z'(t)\theta(t)
$$

$$
\varepsilon''(t) = Z''(t)\theta(t) + 2Z'(0)\delta(t) + Z(0)\delta'(t)
$$

---

## Продолжение доказательства

**Примечание:** если $d(x)$ — гладкая, то $d(x)\delta^{(k)}(x) = d(0)\delta^{(k)}(x)$.

$$
\varepsilon^{(n)}(t) = Z^{(n)}(t)\theta(t) + Z^{(n-1)}(0)\delta(t) = Z^{(n)}(t)\theta(t) + \delta(t)
$$

Тогда:

$$
L\varepsilon(t) = (LZ(t))\theta(t) + \delta(t) = \delta(t)
$$

т.к. $LZ(t) = 0$.

*[Д/З — ан-но будет]*

*[Доказано]*

---

### Теорема Мальгранжа-Эренпрейса

Всякое ур-е $L(D)\varepsilon(x) = \delta(x)$ имеет решение в $\mathcal{D}'(\mathbb{R}^n)$.

---

## Приложение к теории линейных дифференциальных операторов с постоянными коэффициентами

Линейный дифференциальный оператор порядка $m$ с постоянными коэффициентами — это оператор в виде:

$$
L(D) = \sum_{|\alpha|=0}^{m} a_\alpha D^\alpha, \quad \text{где } a_\alpha \in \mathbb{R}
$$

($\alpha$ — мультииндекс)

---

## Пример: финитная функция

$$
\omega_r(x,t) = \begin{cases} \exp\left(-\dfrac{r^2}{r^2 - x^2 - t^2}\right), & x^2 + t^2 < r^2 \\ 0, & x^2 + t^2 \geq r^2 \end{cases}
$$

$$
\operatorname{supp} \omega_r = \{(x,t) \mid x^2 + t^2 < r^2\}
$$

$$
\operatorname{supp} \omega_r(x+y, t+\tau) = \{(x,y,t,\tau) \mid (x+y)^2 + (t+\tau)^2 \leq r^2\}
$$

$$
\cap \operatorname{supp}(x\theta(t) \otimes r\theta(y)) = \operatorname{supp} x\theta(t) \times \operatorname{supp} r\theta(y) \quad \text{— неогранич. мн-во} \Rightarrow * \text{ не определена для этих ф-й}
$$

---

## Преобразование Фурье обобщённых функций

**Определение** [2:21, 14 мин]:

Пусть $f \in L^1(\mathbb{R}^n)$. Её **преобразование Фурье** — это:

$$
F[f(x)](\xi) = \int_{\mathbb{R}^n} f(x) e^{i\langle \xi, x \rangle} \, dx \quad \text{(обозн. } \hat{f}\text{)}
$$

### Свойства

- $F[f(x)](\xi) \in C(\mathbb{R}^n)$ (если $f \in L^1(\mathbb{R}^n)$)
- $|F[f(x)](\xi)| \leq \displaystyle\int_{\mathbb{R}^n} |f(x)| \, dx$

$\Rightarrow F[f(x)](\xi)$ порождает регулярную ОФ на $\mathcal{S}(\mathbb{R}^n)$ (ф-я медленного роста).

$$
(F[f(x)](\xi), \varphi(\xi)) = \int_{\mathbb{R}^n} F[f(x)](\xi) \varphi(\xi) \, d\xi \quad \forall \varphi \in \mathcal{S}(\mathbb{R}^n)
$$

По теореме Фубини:

$$
(F[f(x)](\xi), \varphi(\xi)) = (f(x), F[\varphi(\xi)](x)) \quad \forall \varphi \in \mathcal{S}(\mathbb{R}^n)
$$

<!-- 66-70 -->

## Определение преобразования Фурье для обобщённых функций

**Определение.** Преобразование Фурье ОФ $f \in \mathcal{S}'(\mathbb{R}^n)$ определяется по формуле:

$$
(F[f(x)](\xi), \varphi(\xi)) = (f(x), F[\varphi(\xi)](x)) \quad \forall \varphi \in \mathcal{S}(\mathbb{R}^n)
$$

(обозначение $\hat{f}$)

---

### Обратное преобразование Фурье

Обратное пр. Фурье ОФ $f \in \mathcal{S}'(\mathbb{R}^n)$:

$$
F^{-1}[f(\xi)](x) = \frac{1}{(2\pi)^n} F[f(-\xi)](x) = \frac{1}{(2\pi)^n} F[f(\xi)](-x)
$$

---

### Теорема

Преобразование Фурье ОФ из $\mathcal{S}'(\mathbb{R}^n)$ — это ОФ из $\mathcal{S}'(\mathbb{R}^n)$.

Более того, отображение $f \to F[f]$ — непрерывный изоморфизм (и даже гомеоморфизм) между $\mathcal{S}'(\mathbb{R}^n_x)$ и $\mathcal{S}'(\mathbb{R}^n_\xi)$.

$$
1 \xrightarrow{F} (2\pi)^n \delta
$$

---

## Примеры

**1)** $F[1] = (2\pi)^n \delta(x)$

**2)** $F[\delta(x-x_0)](\xi)$

$$
(F[\delta(x-x_0)](\xi), \varphi(\xi)) = (\delta(x-x_0), F[\varphi(\xi)](x)) =
$$

$$
= \left(\delta(x-x_0), \int_{\mathbb{R}^n} \varphi(\xi) e^{i\langle \xi, x \rangle} d\xi\right) = \int_{\mathbb{R}^n} \varphi(\xi) e^{i\langle \xi, x_0 \rangle} d\xi = (e^{i\langle \xi, x_0 \rangle}, \varphi(\xi))
$$

---

## Свойства преобразования Фурье (Владимиров, стр. 114)

(Видео 15, Лекция 15)

Если $f \in \mathcal{S}'(\mathbb{R}^n)$, то:

**1)** Дифференцирование в частотной области:

$$
D^\alpha_\xi F[f(x)](\xi) = F[(ix)^\alpha f(x)](\xi)
$$

**2)** Дифференцирование оригинала (переход к производной):

$$
F[D^\alpha f(x)](\xi) = (-i\xi)^\alpha F[f(x)](\xi)
$$

**Преобразование сдвига:**

**3)** Сдвиг аргумента:

$$
F[f(x-x_0)](\xi) = e^{i\langle x_0, \xi \rangle} F[f](\xi)
$$

**4)** Сдвиг в частотной области (модуляция):

$$
F[f](\xi + \xi_0) = F[f(x) e^{i\langle x, \xi_0 \rangle}](\xi)
$$

---

## Дополнительные свойства

**5)** Подобие (масштабирование):

$$
F[f(cx)](\xi) = \frac{1}{|c|^n} F[f]\left(\frac{\xi}{c}\right), \quad c \neq 0
$$

**6)** Преобразование Фурье тензорного произведения:

Если $f \in \mathcal{S}'(\mathbb{R}^n)$, $g \in \mathcal{S}'(\mathbb{R}^m)$, то:

$$
F[f(x) \otimes g(y)](\xi, \eta) = F[f(x)](\xi) \otimes F[g(y)](\eta)
$$

**7)** Преобразование Фурье свёртки:

Если $f \in \mathcal{S}'(\mathbb{R}^n)$, $g \in \mathcal{D}'(\mathbb{R}^n)$ (при условиях существования свёртки), то:

$$
F[f(x) * g(x)](\xi) = F[f(x)](\xi) \cdot F[g(x)](\xi)
$$

---

## Примеры (продолжение)

**$\delta(x)$**

**1)** $F[D^\alpha \delta(x)](\xi) = (-i\xi)^\alpha F[\delta(x)](\xi) = (-i\xi)^\alpha \cdot 1 = (-i\xi)^\alpha$

$F$ — линейный оператор из $\mathcal{S}'(\mathbb{R}^n_x) \to \mathcal{S}'(\mathbb{R}^n_\xi)$, непрерывный и даже изоморфизм.

$$
F[k f(x)](\xi) = k \cdot F[f(x)](\xi)
$$

---

## Продолжение вычислений

$$
\Rightarrow F[(-1)^{|\alpha|} D^\alpha \delta(x)] = \xi^\alpha \quad \xrightarrow{F^{-1}} \quad (-1)^{|\alpha|} D^\alpha \delta(x)
$$

$$
\Rightarrow F^{-1}[\xi^\alpha](x) = \frac{1}{(2\pi)^n} F[(-\xi)^\alpha](x) = \frac{1}{(2\pi)^n} F[\xi^\alpha](-x) \quad \text{(нет, } (-\xi)^\alpha \text{)}
$$

$$
\Rightarrow F[\xi^\alpha](x) = (-1) \cdot (-i)^{|\alpha|} D^\alpha \delta(x) \cdot (2\pi)^n
$$

$$
F[\xi^\alpha](x) = -(2\pi)^n (-i)^{|\alpha|} D^\alpha \delta(x)
$$

**В коробке (итог):**

$$
F[x^\alpha] = -(2\pi)^n (-i)^{|\alpha|} D^\alpha \delta(\xi)
$$

*(Примечание: $\alpha$ — мультииндекс, $\xi^\alpha$ — моном)*

---

### Функция sign

**2)** $\text{sgn } x = \begin{cases} \frac{x}{|x|}, & x \neq 0 \\ 0, & x = 0 \end{cases}$

*[График: -1 при x<0, 1 при x>0]*

Вычисление $F[\text{v.p.} \frac{1}{x}]$:

$$
(F[\text{v.p.} \frac{1}{x}](\xi), \varphi(\xi)) = (\text{v.p.} \frac{1}{x}, F[\varphi(\xi)](x))
$$

$$
= \left(\text{v.p.} \frac{1}{x}, \int_{-\infty}^{+\infty} \varphi(\xi) e^{ix\xi} d\xi\right) = \lim_{\varepsilon \to 0} \left(\int_{-\infty}^{-\varepsilon} + \int_{\varepsilon}^{+\infty}\right) \frac{1}{x} \dots
$$

Меняем порядок интегрирования:

$$
\int_{-\infty}^{+\infty} \varphi(\xi) \left( \int \frac{e^{ix\xi}}{x} dx \right) d\xi
$$

---

## Итоги по преобразованию Фурье

В коробке:

$$
F[\delta(x-x_0)](\xi) = e^{i\langle \xi, x_0 \rangle}
$$

В частности, при $x_0 = 0$:

$$
F[\delta(x)](\xi) = 1
$$

Обратное преобразование:

$$
\delta(x) = F^{-1}[1](\xi) = \frac{1}{(2\pi)^n} F[1]
$$

$$
\Rightarrow F[1] = (2\pi)^n \delta(x)
$$

---

## Домашнее задание

**Д/З:**
- Владимиров 8.31 1)
- 8.33 (2) $\to$ вычислить пр. Фурье $\theta(t-|x|)$
- 11.2 1)
- 11.5 1)


<!-- 71-75 -->
## Продолжение вычисления преобразования Фурье

**5)** $F\left[\text{v.p.}\frac{1}{x^2}\right](\xi) = F\left[-\frac{d}{dx}\text{v.p.}\frac{1}{x}\right](\xi)$

$$
= -(-i\xi) F\left[\text{v.p.}\frac{1}{x}\right](\xi) = i\xi \cdot \pi i \, \text{sign}\,\xi
$$

$$
= -\pi \xi \, \text{sign}\,\xi = -\pi |\xi|
$$

где $\text{sign}\,x = \dfrac{|x|}{x}$, $x \neq 0$.

---

## Таблица преобразований Фурье

(при $\hat{f}(\xi) = \displaystyle\int f(x) e^{-ix\xi} dx$):

| $f(x)$ | $\hat{f}(\xi)$ |
|--------|----------------|
| $\delta(x)$ | $1$ |
| $1$ | $(2\pi)^n \delta(\xi)$ |
| $\delta'(x)$ | $i\xi$ |
| $\delta''(x)$ | $-\xi^2$ |
| $x$ | $2\pi i \delta'(\xi)$ |
| $e^{iax}$ | $2\pi \delta(\xi - a)$ |
| $e^{-x^2/2}$ | $\sqrt{2\pi} \, e^{-\xi^2/2}$ |
| $D^\alpha \delta(x)$ | $(-i\xi)^\alpha$ |
| $\delta(x-x_0)$ | $e^{i\langle \xi, x_0 \rangle}$ |

---

## Нахождение фундаментального решения для $L = \dfrac{d}{dx}$

$$
L\varepsilon(x) = \delta(x)
$$

$$
F[L\varepsilon(x)](\xi) = 1
$$

$$
F\left[\frac{d}{dx}\varepsilon(x)\right](\xi) = 1
$$

$$
\Rightarrow -i\xi \, F[\varepsilon(x)](\xi) = 1
$$

$$
\Rightarrow F[\varepsilon(x)](\xi) = -\frac{1}{i\xi} = \frac{i}{\xi}
$$

Это функция, похожая на $\text{v.p.}\dfrac{1}{\xi}$.

$$
\Rightarrow i\left(-i\pi\delta + \text{v.p.}\frac{1}{\xi}\right) = \pi\delta + i\,\text{v.p.}\frac{1}{\xi}
$$

$$
\Rightarrow \varepsilon(x) = F^{-1}\left[\pi\delta + i\,\text{v.p.}\frac{1}{\xi}\right](x) = \frac{1}{2\pi} F\left[\pi\delta(-\xi) + i\,\text{v.p.}\frac{1}{-\xi}\right](x)
$$

$$
= \frac{1}{2\pi} \pi F[\delta(\xi)](x) - i F\left[\text{v.p.}\frac{1}{\xi}\right](x) = \frac{1}{2} - \frac{i}{2\pi} \cdot \pi i \, \text{sign}\,x
$$

$$
= \frac{1}{2} + \frac{1}{2}\text{sign}\,x = \theta(x)
$$

(это наш фундаментальное решение)

---

## Вычисление $F\left[\text{v.p.}\dfrac{1}{x}\right](\xi)$ (продолжение)

$$
\cdots = \int_{-\infty}^{+\infty} \varphi(\xi) \left(\lim_{\varepsilon \to 0} \left(\int_{-\infty}^{-\varepsilon} + \int_{\varepsilon}^{+\infty}\right) \frac{e^{i\xi x}}{x} dx\right) d\xi
$$

Используем формулу Эйлера $e^{i\xi x} = \cos\xi x + i\sin\xi x$:

$$
\frac{\cos x\xi}{x} \text{ — нечётная} \Rightarrow \int_{-\infty}^{-\varepsilon} \frac{\cos x\xi}{x} dx + \int_{\varepsilon}^{+\infty} \frac{\cos x\xi}{x} dx = 0
$$

$$
\lim_{x \to 0} \frac{\sin x\xi}{x\xi} = \xi
$$

$$
\Rightarrow \int_{-\infty}^{+\infty} \varphi(\xi) \int_{-\infty}^{+\infty} \frac{i\sin x\xi}{x} d\xi
$$

Известный интеграл Дирихле:

$$
\int_{-\infty}^{+\infty} \frac{\sin x\xi}{x} d\xi = \pi \, \text{sign}\,\xi
$$

$$
\Rightarrow i\pi \int_{-\infty}^{+\infty} \varphi(\xi) \, \text{sign}\,\xi \, d\xi = (\pi i \, \text{sign}\,\xi, \varphi(\xi)) = (\pi i \, \text{sign}\,x, \varphi(x))
$$

$$
\forall \varphi \in \mathcal{S}(\mathbb{R}^n)
$$

---

## Итоговые формулы

$$
\boxed{\pi i \, \text{sign}\,\xi = F\left[\text{v.p.}\frac{1}{x}\right](\xi)}
$$

---

### 3) $F[\text{sign}\,x](\xi) = ?$

$$
\pi i \, \text{sign}\,\xi = F\left[\text{v.p.}\frac{1}{x}\right](\xi)
$$

$$
\Rightarrow F^{-1}[\pi i \, \text{sign}\,\xi](x) = \text{v.p.}\frac{1}{x}
$$

$$
i\pi \cdot \frac{1}{2\pi} F[\text{sign}(-\xi)](x) = \text{v.p.}\frac{1}{x}
$$

$$
F[\text{sign}(\xi)](x) = -\frac{2}{i} \text{v.p.}\frac{1}{x} = 2i \, \text{v.p.}\frac{1}{x}
$$

---

### 4) $F[\theta(x)](\xi) = ?$

$$
1 = F[\delta(x)](\xi) = F[\theta'(x)](\xi) = (-i\xi) F[\theta(x)](\xi)
$$

$$
\Rightarrow F[\theta(x)](\xi) = -\frac{1}{i\xi} = i\frac{1}{\xi} = i\left(-i\pi\delta + \text{v.p.}\frac{1}{\xi}\right)
$$

$$
= \pi\delta + i\,\text{v.p.}\frac{1}{\xi}
$$

(функция, похожая на Владимиров 6.20)

---

## Консультация (предпоследнее видео)

### Задача 7.22.3

$$
d(x) y = 0, \quad d \in C(\mathbb{R}), \quad d > 0
$$

Найти решения в $\mathcal{D}'(\mathbb{R})$.

**Решение:**

$$
(d(x)y, \varphi(x)) = 0
$$

$$
\int_{\mathbb{R}} d(x) y \, \varphi(x) \, dx = 0
$$

Используем **теорему Стоуна-Вейерштрасса**: любую непрерывную функцию ($f \in C$) можно аппроксимировать многочленом.

$$
P_k(x) \to d(x) \quad \text{равномерно} \quad \text{(последовательность многочленов, т.к. } d(x) \in C(x)\text{)}
$$

Рассмотрим ур-е:

$$
((d(x) - P_k(x))y, \varphi(x)) = 0
$$

$$
\underbrace{(d(x)y, \varphi(x))}_{0} - (P_k(x)y, \varphi(x)) = -(P_k(x)y, \varphi(x)) \in \mathcal{D}'(\mathbb{R})
$$

Т.к. $P_k(x) > 0$ (без потери общности), $P_k \in C^\infty(\mathbb{R})$:

$$
\Rightarrow -(y, P_k(x)\varphi(x)) \quad \underbrace{P_k(x)\varphi(x)}_{\in C^\infty(\mathbb{R}) \subset \mathcal{D}(\mathbb{R})}
$$

---

## Фундаментальное решение

Уравнение $Lu = f$ решается в ОФ так:

$$
u = f * \varepsilon
$$

где $\varepsilon$ — фундаментальное решение (ФР), т.е. решение $L\varepsilon = f$ в обобщённых функциях (для линейных операторов).

---

## Домашнее задание

**Д/З:**
1. Владимиров 6.2
2. Владимиров 9.6: 4), 5); 9.9: 1), 2)

*[можно 9.11 ещё упомянуть он]*

---

## Темы для экзамена (2 часа)

1. **n-тая производная** (по базисам)
2. **Диффур без использования Фундаментального решения** (15д) (типа 7.25)
3. **Свёртка** (5д)
4. **Диффур, исп. фунд. решение и свёртка** (15д)
5. *[примерно как 11.3]*
6. (*) д-ть, что ОФ-функция на операторе (как 11.4)

См. 11.2

---

## Моё ДЗ к след. занятию (13.04)

Разобрать как решать §3-6 из (напр. примеры подобны из Владимиров)

<!-- 76-80 -->

## Продолжение решения 7.22.3

Итак:
$\forall \varphi_k(x) \quad p_k(x) > 0$

$$
\varphi(x) = \frac{\varphi_k(x)}{p_k(x)}
$$

$$
\Rightarrow 0 = -(y, \varphi(x)) \quad \forall \varphi(x) \in \mathcal{D}(\mathbb{R})
$$

$$
\Rightarrow \boxed{y = 0}
$$

---

## 7.22.4

$$
(x-1)y = 0
$$

$$
((x-1)y, \varphi(x)) = 0 \quad \forall \varphi \in \mathcal{D}
$$

Замена $x \to x+1$:

$$
(xy(x+1), \varphi(x)) = 0 \quad \forall \varphi \in \mathcal{D}
$$

$$
x \cdot y(x+1) = 0 \quad \Rightarrow \quad y(x+1) = C\delta(x)
$$

(из 7.22.1 видно)

$$
(\dots)
$$

$$
\Rightarrow y = C\delta(x-1)
$$

---

## 11.4 1)

$$
\frac{\partial}{\partial \bar{z}} = \frac{1}{2}\left(\frac{\partial}{\partial x} + i\frac{\partial}{\partial y}\right)
$$

**Оператор Коши-Римана**

[Продолжение решения:]

$$
\text{①} \int_{\mathbb{R}^2} \frac{1}{\pi} \frac{2 \cdot \frac{1}{n^2}}{(x^2+y^2+\frac{1}{n^2})^2} \varphi(x,y) dx dy
$$

$$
\text{①} \frac{2}{\pi} \int_{\mathbb{R}^2} \frac{1}{(x^2+y^2+\frac{1}{n^2})^2} \varphi(x,y) dx dy
$$

Замена: $x \to \frac{x}{n}, y \to \frac{y}{n}$

$$
\text{①} \frac{1}{\pi} \int_{\mathbb{R}^2} \frac{\varphi(\frac{x}{n}, \frac{y}{n})}{(x^2+y^2+1)^2} dx dy \xrightarrow{n \to \infty} \varphi(0,0) \iint \dots
$$

$$
\text{①} \frac{\varphi(0,0)}{\pi} \int_0^{2\pi} d\theta \int_0^\infty \frac{r dr}{(1+r^2)^2} = \varphi(0,0) \cdot 1
$$

(считается в полярных коорд.)

$$
= (\delta(x,y), \varphi(x,y))
$$

---

### Фундаментальное решение

$$
\mathcal{E} = \frac{1}{\pi(x+iy)} \quad \text{— ФР: } \frac{\partial}{\partial \bar{z}} \mathcal{E}(x,y) = \delta(x,y)
$$

$$
\frac{1}{\pi z}
$$

$$
\forall z \in \mathbb{C} \setminus \{0\} \in L^1_{\text{loc}}(\mathbb{R}^2)
$$

[1:28 видео консультации]

---

### Решение (ф-ла)

Избавление от комплексности в знаменателе (умножение на $(x-iy)$):

$$
\mathcal{E}(x,y) = \frac{1}{\pi} \frac{x-iy}{x^2+y^2}
$$

**Проекция:**

$$
\mathcal{E}_n(x,y) = \frac{1}{\pi} \cdot \frac{x-iy}{x^2+y^2+\frac{1}{n^2}}
$$

$$
\mathcal{E}_n(x,y) \xrightarrow[n \to \infty]{\text{равн.}} \mathcal{E}(x,y) \quad (\text{а } \mathcal{E}_n \in L_1(\mathbb{R}^2), \text{ даже } \in C^\infty(\mathbb{R}^2))
$$

Рассмотрим $\left(\frac{\partial}{\partial \bar{z}} \mathcal{E}_n(x,y), \varphi(x,y)\right) = -\left(\mathcal{E}_n(x,y) \frac{\partial}{\partial \bar{z}} \varphi(x,y)\right)$

$$
\text{①} -\int_{\mathbb{R}^2} \mathcal{E}_n(x,y) \frac{\partial}{\partial \bar{z}} \varphi(x,y) \, dx \, dy = \int_{\mathbb{R}^2} \frac{\partial}{\partial \bar{z}} \mathcal{E}_n(x,y) \, \varphi(x,y) \, dx \, dy
$$

[Продолж. сверху]

---

## 7.22.5

$$
x(x-1)y = 0 \quad \iff \quad (x-1)xy = 0
$$

Пусть $z = (x-1)y$. Тогда $x \cdot z = 0$.
Пусть $w = xy$. Тогда $(x-1)w = 0$.

$$
\Rightarrow z = (x-1)y = C_1 \delta(x)
$$

$$
w = xy = C_2 \delta(x-1)
$$

$$
\Rightarrow z = \begin{cases} (x-1)y = C_1 \delta(x) \\ xy = C_2 \delta(x-1) \end{cases}
$$

$$
xy - y = C_1 \delta(x) \quad \longrightarrow \quad y = C_2 \delta(x-1) + C_1 \delta(x)
$$

---

## 7.22.7

$$
(xy, \varphi) = (1, \varphi) = \int_{\mathbb{R}} \varphi(x) dx_1 = \text{v.p.} \int_{\mathbb{R}} \frac{x \varphi(x)}{x} dx
$$

Т.к. $x$ — гладкая:

$$
(y, \underbrace{x\varphi}_{\psi}) = \text{v.p.} \int_{\mathbb{R}} \frac{x\varphi(x) - 0 \cdot \varphi(0)}{x} dx
$$

$$
\Rightarrow (y, \varphi) = \text{v.p.} \int_{\mathbb{R}} \frac{\varphi(x) - \varphi(0)}{x} dx = \left(\text{v.p.}\frac{1}{x}, \psi\right)
$$

$$
\Rightarrow y = \text{v.p.}\frac{1}{x} + C\delta(x)
$$

(реш-е неоднородного + реш-е однородного)

---

## Продолжение (с предыдущей страницы)

$$
\text{①} \varphi(0) \cdot C + (y, x\varphi(x)), \quad \text{где } C = (y, \eta) \text{ и } \eta(x) \in \mathcal{D}
$$

$$
\text{и } \varphi(x) = \frac{\varphi(x) - \varphi(0)\eta(x)}{x} \in \mathcal{D}
$$

(см. реш-е задачи 6.7)

В силу $(*)$ имеем $(y, x\varphi) = 0$.

Тогда из $(**)$ имеем $(y, \varphi) = \varphi(0)(y, \eta(x)) = C \cdot (y, \eta(x)) \text{①} = \delta \cdot C$.

---

## 7.22.2

$$
d(x)y = 0, \quad \text{где } d \in C^\infty(\mathbb{R}^1) \text{ и имеет единств. нуль в точке } x=0 \text{ порядка } 1.
$$

(реш-е по сути будет повторять реш-е 7.22.1, т.к. 7.22.1 — частный случай, где $d(x)=x$).

---

## 7.22.1

Найти общее решение в $\mathcal{D}'(\mathbb{R}^1)$ ур-я:

$$
xy = 0
$$

**Решение:**

$y = y(x) = ?$

[Владимиров, стр. 98]. Пусть $\displaystyle\sum_{k=0}^m a_k(x) y^{(k)} = f(x)$, $a_k(x) \in C^\infty$, $f \in \mathcal{D}'(\mathbb{R}^1)$.

Его обобщ. реш-е — это ОФ $y \in \mathcal{D}'(\mathbb{R}^1)$, удовлетв. $\forall \varphi \in \mathcal{D}$:

$$
\left(\sum_{k=0}^m a_k y^{(k)}, \varphi\right) = \left(y, \sum_{k=0}^m (-1)^k (a_k \varphi)^{(k)}\right) = (f, \varphi)
$$

$a_1 = x$

$$
(a_1 \cdot y^{(0)}, \varphi) = (y, a_1 \varphi^{(0)}) = (0, \varphi)
$$

т.е. $(y, x\varphi) = 0 \quad \forall \varphi \in \mathcal{D} \quad (*)$

Найдём это $y$.

Имеем $(y, \varphi) = (y, \varphi(0)\eta(x) + \varphi(x) - \varphi(0)\eta(x))$, где $\eta \in \mathcal{D}$, $\eta \equiv 1$ на $[-\varepsilon, \varepsilon]$ и $\eta \equiv 0$ вне $[-3\varepsilon, 3\varepsilon]$.

$$
(**) (y, \varphi) = \varphi(0)(y, \eta(x)) + \left(y, x \cdot \frac{\varphi(x) - \varphi(0)\eta(x)}{x}\right) \text{①}
$$

<!-- 81 -->

## Задача 9.11 (Владимиров)

**Вычислить** $F[x^k \delta^{(m)}(x)]$ при $m \geq k$.

*(сделать преобразование Фурье)*

---

### 1) Пробуем строить напрямую

Используем определение преобразования Фурье для ОФ:

$$
(F[f(x)](\xi), \varphi) = (f(x), F[\varphi(\xi)](x))
$$

где Фурье обобщ. $f \in L^1$: $\displaystyle\int_{\mathbb{R}^n} f(x) e^{i\langle \xi, x \rangle} dx$ (скал. пр-е).

Применяем к нашей задаче:

$$
(F[x^k \delta^{(m)}](\xi), \varphi) = \left(x^k \delta^{(m)}, F[\varphi(\xi)](x)\right) \quad \text{①}
$$

$$
= \left(\delta^{(m)}, x^k F[\varphi(\xi)](x)\right) =
$$

---

### Используем свойство из задачи 7.3.6

$$
x^k \delta^{(m)} \quad \text{при } m \geq k \quad \Rightarrow \quad (-1)^k \, k! \, C_m^k \, \delta^{(m-k)}(x)
$$

*[свойство из задаче 7.3.6]*

Тогда ① превращается в:

$$
\text{①} = \left((-1)^k \cdot k! \cdot C_m^k \, \delta^{(m-k)}(x), \, F[\varphi(\xi)](x)\right)
$$

---

### Вычисляем Фурье

Итак:

$$
F\left[(-1)^k \cdot k! \cdot C_m^k \, \delta^{(m-k)}(x)\right] =
$$

$$
= (-1)^k \cdot k! \cdot \frac{m!}{k!(m-k)!} \, F[\delta^{(m-k)}] \quad \text{②}
$$

$$
= (-1)^k \cdot \frac{m!}{(m-k)!} \cdot (-i\xi)^{m-k}
$$

---

### Итоговый ответ

$$
\boxed{F[x^k \delta^{(m)}(x)](\xi) = (-1)^k \cdot \frac{m!}{(m-k)!} \cdot (-i\xi)^{m-k}, \quad m \geq k}
$$

---

## Итог по всему конспекту

Основные темы, которые были разобраны:

### Пространства тестовых функций
- $\mathcal{D}(\mathbb{R}^n)$ — финитные гладкие функции, носитель, сходимость
- $\mathcal{S}(\mathbb{R}^n)$ — быстроубывающие функции (Шварца), топология
- Вложения $\mathcal{D} \subset \mathcal{S} \subset \mathcal{E} = C^\infty$ и плотность $\overline{\mathcal{D}} = \mathcal{S}$

### Обобщённые функции (распределения)
- Определение как линейных непрерывных функционалов
- Регулярные и сингулярные ОФ
- $\delta$-функция Дирака, функция Хевисайда $\theta(x)$, $\text{v.p.}\frac{1}{x}$, $\text{pf}\frac{1}{x^2+y^2}$
- Носитель ОФ, финитные ОФ, $\delta$ простого слоя

### Операции над ОФ
- Дифференцирование (формула Лейбница, связь с классической производной через скачки)
- Умножение на гладкую функцию
- Свёртка (условия существования, свойства, неассоциативность)
- Тензорное произведение
- Замена переменных

### Преобразование Фурье
- Определение на $\mathcal{S}'$, свойства (сдвиг, дифференцирование, свёртка)
- Таблица: $F[\delta] = 1$, $F[1] = (2\pi)^n\delta$, $F[\text{v.p.}\frac{1}{x}] = \pi i\,\text{sign}\,\xi$, $F[\theta] = \pi\delta + i\,\text{v.p.}\frac{1}{\xi}$

### Дифференциальные уравнения в ОФ
- Фундаментальное решение $\varepsilon$: $L(D)\varepsilon = \delta$
- Теорема Мальгранжа-Эренпрейса
- Решение $Lu = f$ через свёртку: $u = \varepsilon * f$
- Уравнения вида $x^m y = 0$, $xy = 0$, $(x-1)y = 0$, $x(x-1)y = 0$

