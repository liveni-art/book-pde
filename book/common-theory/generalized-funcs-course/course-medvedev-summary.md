# Краткая версия
Краткая версия конспект курса по обобщённым функциям.

$$
\newcommand{\R}{\mathbb{R}}
\newcommand{\C}{\mathbb{C}}
\newcommand{\D}{\mathcal{D}}
\newcommand{\Dp}{\mathcal{D}'}
\newcommand{\Ss}{\mathcal{S}}
\newcommand{\Ssp}{\mathcal{S}'}
\newcommand{\E}{\mathcal{E}}
\newcommand{\Ep}{\mathcal{E}'}
$$

---

## 1. Основные пространства тестовых функций

### Пространство $\D(\R^n)$ — финитные гладкие функции
$$
\D(\R^n) = \{\varphi \in C^\infty(\R^n) \mid \operatorname{supp} \varphi \text{ — компакт}\}
$$
**Носитель:** $\operatorname{supp} \varphi = \overline{\{x \mid \varphi(x) \neq 0\}}$

**Сходимость в $\D$:** $\varphi_k \to \varphi$, если:
- $\exists R > 0$: $\operatorname{supp} \varphi_k \subset B_R$ $\forall k$
- $\forall \alpha$: $D^\alpha \varphi_k \rightrightarrows D^\alpha \varphi$ (равномерно)

### Пространство $\Ss(\R^n)$ — быстроубывающие функции (Шварца)
$$
\Ss = \left\{f \in C^\infty \mid \forall \alpha, \beta:\ \sup_{x} |x^\beta D^\alpha f(x)| < \infty\right\}
$$
**Сходимость в $\Ss$:** $\varphi_k \to \varphi$, если $\forall \alpha, \beta$: $x^\beta D^\alpha \varphi_k \rightrightarrows x^\beta D^\alpha \varphi$

### Пространство $\E(\R^n) = C^\infty(\R^n)$
**Сходимость:** равномерная на компактах всех производных.

### Вложения
$$
\D \subset \Ss \subset \E, \quad \overline{\D} = \Ss \text{ (в топологии } \Ss\text{)}
$$

---

## 2. Обобщённые функции (распределения)

### Определение
**Обобщённая функция** на $F$ ($F = \D, \Ss, \E$) — линейный непрерывный функционал $f: F \to \C$.

Обозначение: $\langle f, \varphi \rangle$ или $(f, \varphi)$.

Пространства: $\Dp, \Ssp, \Ep$.

**Вложения:** $\Ep \subset \Ssp \subset \Dp$ (все плотные).

### Регулярные и сингулярные ОФ
- **Регулярная:** $\langle f, \varphi \rangle = \int f(x)\varphi(x)\,dx$, где $f \in L^1_{\text{loc}}$
- **Сингулярная:** не представима в таком виде (например, $\delta$)

### Равенство ОФ
$f = g$ на области $\Omega$, если $\langle f - g, \varphi \rangle = 0$ $\forall \varphi \in \D$ с $\operatorname{supp} \varphi \subset \Omega$.

### Носитель ОФ
$\operatorname{supp} f = \R^n \setminus O_f$, где $O_f$ — наибольшая открытая область, где $f = 0$.

**Примеры:**
- $\operatorname{supp} \delta = \{0\}$
- $\operatorname{supp} \theta = [0, +\infty)$
- $\delta_S$: $\langle \delta_S, \varphi \rangle = \int_S \varphi\,dS$, $\operatorname{supp} \delta_S = S$

### Сходимость ОФ
$f_k \to f$ в $\Fp$ (слабая сходимость), если $\langle f_k, \varphi \rangle \to \langle f, \varphi \rangle$ $\forall \varphi \in \F$.

---

## 3. Операции над ОФ

### Умножение на гладкую функцию
Для $f \in \Dp$, $g \in C^\infty$:
$$
\langle gf, \varphi \rangle = \langle f, g\varphi \rangle
$$
**Примеры:**
- $g(x)\delta(x) = g(0)\delta(x)$
- $x \cdot \text{v.p.}\frac{1}{x^2} = \text{v.p.}\frac{1}{x}$

### Производная ОФ
$$
\langle D^\alpha f, \varphi \rangle = (-1)^{|\alpha|} \langle f, D^\alpha \varphi \rangle
$$
**Свойства:**
- Линейность: $D^\alpha(\alpha f + \beta g) = \alpha D^\alpha f + \beta D^\alpha g$
- Коммутативность: $D^\alpha D^\beta f = D^\beta D^\alpha f$
- $\operatorname{supp} D^\alpha f \subset \operatorname{supp} f$
- Формула Лейбница: $(gf)' = g'f + gf'$

**Примеры:**
- $\theta' = \delta$
- $\delta'(\varphi) = -\varphi'(0)$
- $g(x)\delta'(x) = -g'(0)\delta(x) + g(0)\delta'(x)$
- $(\text{v.p.}\frac{1}{x})' = -\text{v.p.}\frac{1}{x^2}$
- $(\ln|x|)' = \text{v.p.}\frac{1}{x}$

### Связь с классической производной
Для кусочно-гладкой $f$:
$$
f'_{\text{об}} = \{f'\} + \sum_k [f]_{x_k} \delta(x - x_k)
$$
где $[f]_{x_k} = f(x_k+0) - f(x_k-0)$ — скачок.

---

## 4. Тензорное произведение

### Определение
Для $f \in \Dp(\R^n)$, $g \in \Dp(\R^m)$:
$$
\langle f \otimes g, \varphi(x,y) \rangle = \langle f(x), \langle g(y), \varphi(x,y) \rangle \rangle
$$

### Свойства
1. Коммутативность: $f \otimes g = g \otimes f$
2. Билинейность
3. Ассоциативность: $(f \otimes g) \otimes h = f \otimes (g \otimes h)$
4. $D_x^\alpha(f \otimes g) = D^\alpha f \otimes g$
5. $\operatorname{supp}(f \otimes g) = \operatorname{supp} f \times \operatorname{supp} g$

### Примеры
- $\delta(x) \otimes \delta(y) = \delta(x,y)$
- $1 \otimes f(x) = f(x)$ (не зависит от второй переменной)
- $\delta(at - |x|) = \theta(t) \otimes \delta(at+x) + \theta(t) \otimes \delta(at-x)$

---

## 5. Свёртка

### Определение (для функций)
$$
(f * g)(x) = \int_{\R^n} f(t)g(x-t)\,dt
$$

### Условия существования в $\Dp$
Свёртка $f * g$ определена, если:
- $f$ или $g$ финитны
- $\operatorname{supp} f$ и $\operatorname{supp} g$ ограничены с одной стороны (на $\R$)
- Более общие условия (Владимиров §8)

### Определение для ОФ
$$
\langle f * g, \varphi \rangle = \langle f(x) \otimes g(y), \varphi(x+y) \rangle
$$

### Свойства
1. Коммутативность: $f * g = g * f$
2. Билинейность
3. $D^\alpha(f * g) = D^\alpha f * g = f * D^\alpha g$
4. **Не ассоциативна!** (скобки важны)
5. $f * \delta = f$

### Примеры
- $\theta(x) * \theta(x) = x\theta(x)$
- $\theta(x-a) * \theta(x-b) = (x-a-b)\theta(x-a-b)$
- $\frac{\partial}{\partial t}\theta(at-|x|) = a\,\delta(at-|x|)$

---

## 6. Преобразование Фурье обычных функций

### Определение
$$
F[f](\xi) = \hat{f}(\xi) = \int_{\R^n} f(x) e^{i\langle \xi, x \rangle}\,dx
$$

### Свойства
- $F[f] \in C(\R^n)$, $|F[f](\xi)| \leq \|f\|_{L^1}$
- Дифференцирование: $F[D^\alpha f] = (-i\xi)^\alpha F[f]$
- Умножение на $x^\alpha$: $F[x^\alpha f] = i^{|\alpha|} D^\alpha_\xi F[f]$
- Сдвиг: $F[f(x-x_0)] = e^{i\langle x_0, \xi \rangle} F[f]$
- Свёртка: $F[f * g] = F[f] \cdot F[g]$

### Примеры
- $F[e^{-x^2/2}] = \sqrt{2\pi}\,e^{-\xi^2/2}$
- $F[e^{iax}] = 2\pi\delta(\xi-a)$

---

## 7. Преобразование Фурье ОФ

### Определение
Для $f \in \Ssp$:
$$
\langle F[f], \varphi \rangle = \langle f, F[\varphi] \rangle \quad \forall \varphi \in \Ss
$$

$F: \Ssp \to \Ssp$ — изоморфизм.

### Обратное преобразование
$$
F^{-1}[f](x) = \frac{1}{(2\pi)^n} F[f(-\xi)](x)
$$

### Таблица

| $f(x)$ | $F[f](\xi)$ |
|--------|-------------|
| $\delta(x)$ | $1$ |
| $1$ | $(2\pi)^n \delta(\xi)$ |
| $\delta^{(k)}(x)$ | $(-i\xi)^k$ |
| $x^k$ | $2\pi i^k \delta^{(k)}(\xi)$ |
| $\text{v.p.}\frac{1}{x}$ | $-\pi i\,\text{sign}\,\xi$ |
| $\text{sign}\,x$ | $2i\,\text{v.p.}\frac{1}{\xi}$ |
| $\theta(x)$ | $\pi\delta(\xi) - i\,\text{v.p.}\frac{1}{\xi}$ |

### Свойства
- $F[D^\alpha f] = (-i\xi)^\alpha F[f]$
- $F[x^\alpha f] = i^{|\alpha|} D^\alpha F[f]$
- $F[f * g] = F[f] \cdot F[g]$
- $F[f \otimes g] = F[f] \otimes F[g]$

---

## 8. Решение дифференциальных уравнений в ОФ

### Уравнения вида $x^m y = 0$
**Теорема:** Общее решение в $\Dp$:
$$
y = \sum_{k=0}^{m-1} c_k \delta^{(k)}(x), \quad c_k \in \R
$$

**Примеры:**
- $xy = 0 \Rightarrow y = C\delta(x)$
- $x^2 y = 0 \Rightarrow y = C_0 \delta(x) + C_1 \delta'(x)$
- $(x-1)y = 0 \Rightarrow y = C\delta(x-1)$
- $x(x-1)y = 0 \Rightarrow y = C_1\delta(x) + C_2\delta(x-1)$

### Уравнения с правой частью
**Пример:** $xy = 1 \Rightarrow y = \text{v.p.}\frac{1}{x} + C\delta(x)$

**Пример:** $x^2 y''' = 0 \Rightarrow y = c_0 \frac{x^2}{2}\theta(x) + c_1 x\theta(x) + c_2\frac{x^2}{2} + c_3 x + c_4$

---

## 9. Фундаментальное решение

### Определение
$\varepsilon \in \Dp$ — фундаментальное решение оператора $L(D)$, если:
$$
L(D)\varepsilon = \delta
$$

$\varepsilon$ определено с точностью до решения однородного уравнения $L(D)\varepsilon_0 = 0$.

### Теорема Мальгранжа-Эренпрейса
Всякое уравнение $L(D)\varepsilon = \delta$ имеет решение в $\Dp(\R^n)$.

### Метод решения через ФР
Если $L(D)u = f$ и свёртка $\varepsilon * f$ существует, то:
$$
u = \varepsilon * f
$$

### ФР для ОДУ с постоянными коэффициентами
Для $L\left(\frac{d}{dt}\right) = \frac{d^n}{dt^n} + a_1\frac{d^{n-1}}{dt^{n-1}} + \ldots + a_n$:
$$
\varepsilon(t) = Z(t)\theta(t)
$$
где $Z(t)$ — решение задачи Коши:
$$
LZ = 0, \quad Z(0) = Z'(0) = \ldots = Z^{(n-2)}(0) = 0, \quad Z^{(n-1)}(0) = 1
$$

**Пример:** $L = \frac{d}{dt}$: $\varepsilon(t) = \theta(t)$

### ФР оператора Коши-Римана
$$
\frac{\partial}{\partial \bar{z}} = \frac{1}{2}\left(\frac{\partial}{\partial x} + i\frac{\partial}{\partial y}\right)
$$
$$
\varepsilon(z) = \frac{1}{\pi z} = \frac{1}{\pi(x+iy)}
$$

### Метод Фурье для нахождения ФР
**Пример:** $L = \frac{d}{dx}$, $L\varepsilon = \delta$
$$
F[L\varepsilon] = 1 \Rightarrow -i\xi F[\varepsilon] = 1 \Rightarrow F[\varepsilon] = \frac{i}{\xi}
$$
$$
\varepsilon = F^{-1}\left[\pi\delta + i\,\text{v.p.}\frac{1}{\xi}\right] = \theta(x)
$$

---

## 10. Важные формулы и тождества

### Основные тождества с $\delta$
- $\delta(ax) = \frac{1}{|a|}\delta(x)$
- $x^k \delta^{(m)}(x) = (-1)^k \frac{m!}{(m-k)!} \delta^{(m-k)}(x)$ при $m \geq k$
- $x^m \delta^{(m)}(x) = (-1)^m m!\,\delta(x)$

### Производные v.p.
- $\left(\text{v.p.}\frac{1}{x}\right)' = -\text{v.p.}\frac{1}{x^2}$
- $\left(\text{v.p.}\frac{1}{x^2}\right)' = -2\,\text{v.p.}\frac{1}{x^3}$

### Интегральные тождества
- $\langle \text{v.p.}\frac{1}{x}, \varphi \rangle = \text{v.p.}\int \frac{\varphi(x)}{x}\,dx = \lim_{\varepsilon \to 0} \int_{|x|>\varepsilon} \frac{\varphi(x)}{x}\,dx$
- $\langle \text{pf}\frac{1}{x^2+y^2}, \varphi \rangle = \int_{x^2+y^2<1} \frac{\varphi(x,y)-\varphi(0,0)}{x^2+y^2}\,dxdy + \int_{x^2+y^2>1} \frac{\varphi(x,y)}{x^2+y^2}\,dxdy$