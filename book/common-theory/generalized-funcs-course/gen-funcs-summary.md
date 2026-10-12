# Краткий конспект
Краткое инфо про обобщённые функции и сопутствующую теорию.

## 1. Пространства основных функций

### 1.1. Пространство $\mathcal{D}$ 
**Пространство $\mathcal{D} \equiv \mathcal{D}(\mathbb{R}^n)$ — пространство финитных бесконечно дифференцируемых функций.**
$$
\mathcal{D}(\mathbb{R}^n) = \{\varphi \in C^\infty(\mathbb{R}^n) \mid \operatorname{supp} \varphi \text{ — компакт}\}
$$
**Носитель (классической функции):** $\operatorname{supp} \varphi = \overline{\{x \mid \varphi(x) \neq 0\}}$

**Сходимость в $\mathcal{D}$:**  $\ \varphi_k \to \varphi$ при $k \to \infty$ , если:
- $\exists R > 0$:  $\quad \forall k:$  $\operatorname{supp} \varphi_k \subset B_R$ 

    (существует шарик $B_R$, в который укладываются носители всех функций из последовательности $\varphi_k$ )
- $\forall \alpha$: $\quad D^\alpha \varphi_k \rightrightarrows D^\alpha \varphi$ равномерно по $x$, $\quad$  где $\alpha -$ мультииндекс.

    (сама функция и все её произвозные сходятся равномерно к предельной функции и её производным соответственно)

    ("$\rightrightarrows$" здесь и далее означает равномерную сходимость)

### 1.2. Пространство $\mathcal{S}$
**Пространство $\mathcal{S} \equiv \mathcal{S}(\mathbb{R}^n)$ — пространство быстроубывающих функций (пространство Шварца).**
$$
\mathcal{S(\mathbb{R}^n)} = \left\{    \varphi \in C^\infty(\mathbb{R}^n)  \mid \forall \alpha, \beta:\ \sup_{x} |x^\beta D^\alpha f(x)| < \infty\right\},
$$
то есть, это множество бесконечно гладких в $\mathbb{R}^n$  функций, убывающих при $|x| \to \infty$ вместе со всеми производными быстрее любой степени $|x|^{-1}$.

**Сходимость в $\mathcal{S}$:**  $\ \varphi_k \to \varphi$ при $k \to \infty$ , если: 
- $\forall \alpha, \beta$: $\quad x^\beta D^\alpha \varphi_k \rightrightarrows x^\beta D^\alpha \varphi$ равномерно по $x$

### 1.3. Пространство $\mathcal{E}$
**Пространство $\mathcal{E} \equiv \mathcal{E}(\mathbb{R}^n) = C^\infty(\mathbb{R}^n)$ — пространство бесконечно дифференцируемых функцй**

**Сходимость в $\mathcal{E}$:** $\ \varphi_k \to \varphi$ при $k \to \infty$ , если для любого компактного множества $K \subset \mathbb{R}^n$ выполняется:
- $\forall \alpha$: $\quad D^\alpha \varphi_k \rightrightarrows D^\alpha \varphi$ равномерно по $x \in K$,$\quad$ где $\alpha -$ мультииндекс.

### 1.4. Вложения пространств основых функций
$$
\mathcal{D} \subset \mathcal{S} \subset \mathcal{E}
$$

---

## 2. Обобщённые функции 

### 2.1. Определение
**Обобщённая функция** на $\mathcal{F}$ $(\mathcal{F} = \mathcal{D}, \mathcal{S}, \mathcal{E}$) — это линейный непрерывный функционал $f: \mathcal{F} \to \mathbb{R}$.

Обозначение действия ОФ $f$ на $\varphi$: $\langle f, \varphi \rangle$ или $(f, \varphi)$.

Пространства обобщенных функций обозначаются соответственно: $\mathcal{D}', \mathcal{S}', \mathcal{E}'$.

**Вложения пространств ОФ:** $\mathcal{E}' \subset \mathcal{S}' \subset \mathcal{D}'$ (все вложения плотные).


### 2.2. Сходимость ОФ
$f_k \to f$ в $\mathcal{F}'$ (последовательность обобщенных функций $f_k$ сходится к обобщенной функции $f$), если $\langle f_k, \varphi \rangle \to \langle f, \varphi \rangle$ при $k \to \infty$  для любых $\varphi \in \mathcal{F}$, где $\mathcal{F} = \mathcal{D}, \mathcal{S}, \mathcal{E}$.


### 2.3. Равенство ОФ
$f = 0$ в области $\Omega$, если $\langle f, \varphi \rangle = 0 \quad \forall \varphi \in \mathcal{D}$ таких, что $\operatorname{supp}\varphi = \Omega$.

$f = g$ в области $\Omega$, если $\langle f - g, \varphi \rangle = 0$ $\forall \varphi \in \mathcal{D}$ таких, что $\operatorname{supp} \varphi = \Omega$.

$f = g$, если $\langle f - g, \varphi \rangle = 0$ $\forall \varphi \in \mathcal{D}$.

### 2.4. Носитель ОФ
**Нулевым множеством** $O_f$ обобщенной функции $f$ называется объединение всех областей $\Omega \subset \mathbb{R}^n$, таких, что $f = 0$ в $\Omega$.

**Носителем** обобщенной функции называется множество 

$$
\operatorname{supp} f = \mathbb{R}^n \setminus O_f.
$$

Если $\operatorname{supp} f$ - ограниченное множество, то $f$ называется **финитной ОФ**.

**Примеры носителей:**
- $\operatorname{supp} \delta = \{0\}$
- $\operatorname{supp} \theta = [0, +\infty)$
  
### 2.5. Регулярные и сингулярные ОФ
- **$f$ - регулярная ОФ**, если она представима в виде: $\langle f, \varphi \rangle = \int f(x)\varphi(x)\,dx$, где $f \in L^1_{\text{loc}}$
- **сингулярная,** если не представима в таком виде (например, $\delta$)

---

## 3. Операции над ОФ

### 3.1. Умножение на гладкую функцию
Для $f \in \mathcal{D}'$, $\alpha(x) \in C^\infty(\mathbb{R}^n)$:
$$
\langle \alpha f, \varphi \rangle = \langle f, \alpha\varphi \rangle
$$
**Примеры:**
- $\alpha(x)\delta(x) = \alpha(0)\delta(x)$
- $x \cdot \text{v.p.}\frac{1}{x^2} = \text{v.p.}\frac{1}{x}$

### 3.2. Производная ОФ 
Производной обобщённой функци $f \in \mathcal{D}'(\mathbb{R}^n)$ называется функцонал, действующий по формуле
$$
\langle D^\alpha f, \varphi \rangle = (-1)^{|\alpha|} \langle f, D^\alpha \varphi \rangle,
$$
где $\alpha$ - мультииндекс.

**Свойства:**
1. Линейность: $\langle D^\alpha f, \alpha \varphi + \beta \psi\rangle = \alpha \langle D^\alpha f, \varphi \rangle + \beta \langle D^\alpha f, \psi\rangle$
2. Непрерывность: $\langle D^\alpha f, \varphi \rangle  = \langle f, D^\alpha \varphi \rangle$

(из 1 и 2 понятно, что $D^\alpha : \mathcal{D}'(\mathbb{R}^n) \to \mathcal{D}(\mathbb{R}^n)$ - линейное непрерывное отображение)

3. Всякая ОФ дифференцируема, причём бесконечное число раз.
4. Коммутативность: $D^\alpha D^\beta f = D^\beta D^\alpha f$
5.  $\operatorname{supp} D^\alpha f \subset \operatorname{supp} f$
6. Формула Лейбница:  $\forall f \in \mathcal{D}'(\mathbb{R}^n), g \in C^{\infty}(\mathbb{R}^n): \quad (gf)' = g'f + gf'$

**Примеры производных:**
- $\theta' = \delta$
- $\delta'(\varphi) = -\varphi'(0)$
- $g(x)\delta'(x) = -g'(0)\delta(x) + g(0)\delta'(x)$
- $(\text{v.p.}\frac{1}{x})' = -\text{v.p.}\frac{1}{x^2}$
- $(\ln|x|)' = \text{v.p.}\frac{1}{x}$

### 3.3. Связь с классической производной
Для кусочно-гладкой $f \in \mathcal{D}'(\mathbb{R}^n)$:
$$
f'_{\text{об}} = f'_{кл} + \sum_k [f]_{x_k} \delta(x - x_k)
$$
где $[f]_{x_k} = f(x_k+0) - f(x_k-0)$ — скачок.

---

## 4. Тензорное произведение

### 4.1. Определение
Для $f \in \mathcal{D}'(\mathbb{R}^n)$, $g \in \mathcal{D}'(\mathbb{R}^m)$:
$$
\langle f \otimes g, \varphi(x,y) \rangle = \langle f(x), \langle g(y), \varphi(x,y) \rangle \rangle, \quad \varphi \in \mathcal{D}(\mathbb{R}^{n+m})
$$

### 4.2. Свойства
1. Коммутативность: $f \otimes g = g \otimes f$
2. Билинейность:$(\alpha f + \beta g)\otimes h = \alpha (f\otimes h) + \beta (g\otimes h)$
3. Бинепрерывность.
4. Ассоциативность: $(f \otimes g) \otimes h = f \otimes (g \otimes h)$
5. $\forall \alpha:\quad D_x^\alpha(f \otimes g) = D^\alpha f \otimes g$
6. $\forall a \in C^{\infty}(\mathbb{R}^{n}):$
   $$
   a(x)(f(x)\otimes g(y)) = (a(x)f(x))\otimes g(y)
   $$
7. $\operatorname{supp}(f \otimes g) = \operatorname{supp} f \times \operatorname{supp} g$

### 4.3. Примеры
- $\delta(x) \otimes \delta(y) = \delta(x,y)$
- $1 \otimes f(x) = f(x)$ (не зависит от второй переменной)
- $\delta(at - |x|) = \theta(t) \otimes \delta(at+x) + \theta(t) \otimes \delta(at-x)$

---

## 5. Свёртка классических функций

### 5.1. Определение
Пусть $f, g \in L^1_{loc}(\mathbb{R}^n)$. Тогда их **свёртка**:
$$
(f * g)(x) = \int_{\mathbb{R}^n} f(t)g(x-t)\ dt = \int_{\mathbb{R}^n} g(t)f(x-t)\ dt,
$$
если эти интегралы существуют.

### 5.2. Условия существования
Случаи, когда для функций из 5.1 выполняется $f * g \in L^1_{loc}$:
1. $f$ финитна или $g$ финитна
2. $f, g \in  L^1(\mathbb{R}^n)$
3. $f \in  L^1(\mathbb{R}^n)$, $g$ - ограничена на $\mathbb{R}^n$ (или наоборот)


## 6. Свёртка ОФ
### 6.1. Определение
Пусть  $f, g \in \mathcal{D}'(\mathbb{R}^n)$. Тогда их **свёртка**:
$$
\langle f * g, \varphi \rangle = \langle f(x) \otimes g(y), \varphi(x+y) \rangle
$$

### 6.2. Условия существования в $\mathcal{D}'$ 
Свёртка $f * g$ определена, если:
1. $f$ и $g$ финитны
2. $\operatorname{supp} f$ и $\operatorname{supp} g$ ограничены с одной стороны (на $\mathbb{R}$)
3. Более общие условия (Владимиров §8)


### 6.3. Свойства
1. Коммутативность: $f * g = g * f$
2. Билинейность
3. $D^\alpha(f * g) = D^\alpha f * g = f * D^\alpha g$
4. **Не ассоциативна!** (скобки важны)
5. $f * \delta = f$

### 6.4. Примеры
- $\theta(x) * \theta(x) = x\theta(x)$
- $\theta(x-a) * \theta(x-b) = (x-a-b)\theta(x-a-b)$

---

## 7. Преобразование Фурье классических функций

### 7.1. Определение
Пусть $f \in L^1(\mathbb{R}^n)$. Её **преобразование Фурье** - это:
$$
F[f](\xi) = \hat{f}(\xi) = \int_{\mathbb{R}^n} f(x) e^{i\langle \xi, x \rangle}\,dx
$$

### 7.2. Свойства
<!-- todo: проверить -->
1. $F[f] \in C^{\infty}(\mathbb{R}^n)$, $|F[f](\xi)| \leq \|f\|_{L^1}$.
   (Следовательно, $F[f(x)](\xi)$ порождает регулярную ОФ на $\mathcal{S}(\mathbb{R}^n)$)
2. Дифференцирование: $F[D^\alpha f](\xi) = (-i\xi)^\alpha F[f](\xi)$
3. Сдвиг: $F[f(x-x_0)] = e^{i\langle x_0, \xi \rangle} F[f]$
4. Свёртка: $F[f * g] = F[f] \cdot F[g]$

### 7.3. Примеры
- $F[e^{-x^2/2}] = \sqrt{2\pi}\,e^{-\xi^2/2}$
- $F[e^{iax}] = 2\pi\delta(\xi-a)$

---

## 8. Преобразование Фурье ОФ

### 8.1. Определение
**Преобразование Фурье** для $f \in \mathcal{S}'$: 
$$
\langle F[f], \varphi \rangle = \langle f, F[\varphi] \rangle \quad \forall \varphi \in \mathcal{S}
$$
**Обратное преобразование Фурье** для $f \in \mathcal{S}'$:
$$
F^{-1}[f] = \frac{1}{(2\pi)^n} F[f(-x)]
$$

**Замечание.** $F: \mathcal{S}' \to \mathcal{S}'$ — изоморфизм.


### 8.2. Свойства
$$
\begin{aligned}
D^\alpha F[f] &= F[(ix)^\alpha f], \\
F[D^\alpha f] &= (-i\xi)^\alpha F[f], \\
F[f(x - x_0)] &= e^{i(x_0, \xi)} F[f], \\
F[f](\xi + \xi_0) &= F\!\left[f(x)\, e^{i(x, \xi_0)}\right]\!(\xi), \\
F[f(cx)] &= \frac{1}{|c|^n}\, F[f]\!\left(\frac{\xi}{c}\right), \quad c \neq 0,\\
F[f(x) \otimes g(y)] &= F[f](\xi) \otimes F[g](\eta),\\
F[f * g] &= F[f] F[g], \text{$f$ или $g$ финитна} \\
\end{aligned}
$$


---

### 8.3. Примеры

| $f(x)$ | $F[f](\xi)$ |
|--------|-------------|
| $\delta(x)$ | $1$ |
| $1$ | $(2\pi)^n \delta(\xi)$ |
| $\delta^{(k)}(x)$ | $(-i\xi)^k$ |
| $\text{sign}\,x$ | $2i\,\text{v.p.}\frac{1}{\xi}$ |

## 9. Решение дифференциальных уравнений в ОФ

### 9.1. Уравнения вида $x^m y = 0$
**Теорема:** Общее решение при $x,y \in \mathcal{D}'$:
$$
y = \sum_{k=0}^{m-1} c_k \delta^{(k)}(x), \quad c_k \in \mathbb{R}
$$

**Примеры:**
- $xy = 0 \Rightarrow y = C\delta(x)$
- $x^2 y = 0 \Rightarrow y = C_0 \delta(x) + C_1 \delta'(x)$
- $(x-1)y = 0 \Rightarrow y = C\delta(x-1)$
- $x(x-1)y = 0 \Rightarrow y = C_1\delta(x) + C_2\delta(x-1)$

### 9.2. Уравнения с правой частью
**Пример:** $xy = 1 \Rightarrow y = \text{v.p.}\frac{1}{x} + C\delta(x)$

**Пример:** $x^2 y''' = 0 \Rightarrow y = c_0 \frac{x^2}{2}\theta(x) + c_1 x\theta(x) + c_2\frac{x^2}{2} + c_3 x + c_4$

---

## 10. Фундаментальное решение

### 10.1. Определение
$\mathscr{E} \in \mathcal{D}'$ — **фундаментальное решение** (функция влияния) линейного дифференциального оператора 
$$
L(D) = \sum_{|\alpha|=0}^{m} a_\alpha D^\alpha
$$
с постоянными коэффициентам $a_\alpha(x) = a_\alpha$, если в $\mathbb{R}^n$ выполняется:
$$
L(D)\,\mathscr{E} = \delta(x).
$$

### 10.2. Теорема Мальгранжа-Эренпрейса
Всякое уравнение $L(D)\mathscr{E} = \delta$ имеет решение в $\mathcal{D}'(\mathbb{R}^n)$.

### 10.3. Метод решения через ФР
Если $L(D)u = f$ и свёртка $\mathscr{E} * f$ существует, то:
$$
u = \mathscr{E} * f
$$

### 10.4. ФР для ОДУ с постоянными коэффициентами
*(Владимиров, 8.26)*

Для $L\left(\frac{d}{dx}\right) = \frac{d^n}{dx^n} + a_1(x)\frac{d^{x-1}}{dx^{n-1}} + \ldots + a_n(x), a_i \in C^{\infty}(R^1)$ решением уравнения $Lu = \delta$ является:
$$
u(x) = \theta(x)Z(x),
$$
где $Z(x) \in C^{m}(R^1)$ — решение задачи Коши:
$$
LZ = 0, \quad Z(0) = Z'(0) = \ldots = Z^{(n-2)}(0) = 0, \quad Z^{(n-1)}(0) = 1.
$$

**Пример:** $L = \frac{d}{dx}$: 
$$
\mathscr{E}(x) = \theta(x)
$$

### 10.5. ФР оператора Коши-Римана
$$
\frac{\partial}{\partial \bar{z}} = \frac{1}{2}\left(\frac{\partial}{\partial x} + i\frac{\partial}{\partial y}\right)
$$
$$
\mathscr{E}(z) = \frac{1}{\pi z} = \frac{1}{\pi(x+iy)}
$$

### 10.6. Метод Фурье для нахождения ФР
**Пример:** $L = \frac{d}{dx}$, $L\mathscr{E} = \delta$
$$
F[L\mathscr{E}] = 1 \Rightarrow -i\xi F[\mathscr{E}] = 1 \Rightarrow F[\mathscr{E}] = \frac{i}{\xi}
$$
$$
\mathscr{E} = F^{-1}\left[\pi\delta + i\,\text{v.p.}\frac{1}{\xi}\right] = \theta(x)
$$

---

## 11. Важные формулы и тождества

### 11.1. Основные тождества с $\delta$
- $\delta(ax) = \frac{1}{|a|}\delta(x)$
- $x^k \delta^{(m)}(x) = (-1)^k \frac{m!}{(m-k)!} \delta^{(m-k)}(x)$ при $m \geq k$
- $x^m \delta^{(m)}(x) = (-1)^m m!\,\delta(x)$

### 11.2. Производные v.p.
- $\left(\text{v.p.}\frac{1}{x}\right)' = -\text{v.p.}\frac{1}{x^2}$


### 11.3. Интегральные тождества
- $\langle \text{v.p.}\frac{1}{x}, \varphi \rangle = \text{v.p.}\int \frac{\varphi(x)}{x}\,dx = \lim_{\varepsilon \to 0} \int_{|x|>\varepsilon} \frac{\varphi(x)}{x}\,dx$
- $\langle \text{pf}\frac{1}{x^2+y^2}, \varphi \rangle = \int_{x^2+y^2<1} \frac{\varphi(x,y)-\varphi(0,0)}{x^2+y^2}\,dxdy + \int_{x^2+y^2>1} \frac{\varphi(x,y)}{x^2+y^2}\,dxdy$