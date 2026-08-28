
# 4. Доказательство того, что характеристическое решение удовлетворяет УРЧП

### 4.1 Утверждение

**Утверждение.** Функция $u(x) := Y(s(x), \sigma(x))$ удовлетворяет квазилинейному УРЧП $\sum_i b_i(x, u), u_{x_i} = f(x, u)$.

### 4.2 Шаг 1 — Начальное условие

Если $x \in \Sigma$, то $s(x) = 0$, поэтому:

$$u(x) = Y(0, \sigma(x)) = \bar{u}(\Phi(\sigma(x))) \quad \checkmark$$

### 4.3 Шаг 2 — Проверка УРЧП

Дифференцируем $u = Y(s(x), \sigma(x))$ по правилу сложной функции:

$$\frac{\partial u}{\partial x_i} = \frac{\partial Y}{\partial s}, \frac{\partial s}{\partial x_i} + \sum_{k=1}^{N-1} \frac{\partial Y}{\partial \sigma_k}, \frac{\partial \sigma_k}{\partial x_i}$$

Умножаем на $b_i$ и суммируем по $i$:

$$\sum_i b_i, u_{x_i} = \frac{\partial Y}{\partial s} \underbrace{\left(\sum_i b_i, \frac{\partial s}{\partial x_i}\right)}_{A} + \sum_k \frac{\partial Y}{\partial \sigma_k} \underbrace{\left(\sum_i b_i, \frac{\partial \sigma_k}{\partial x_i}\right)}_{B_k}$$

**Ключевые тождества: $A = 1$ и $B_k = 0$**, которые дают:

$$\sum_i b_i, u_{x_i} = \frac{\partial Y}{\partial s} \cdot 1 = \dot{Y} = f(X, Y) = f(x, u) \quad \checkmark$$

### 4.4 Доказательство ключевых тождеств

Отображение $(s, \sigma) \mapsto X(s, \sigma)$ и его обратное $x \mapsto (s(x), \sigma(x))$ при композиции дают тождество.

**Тождество $A = 1$.** Дифференцируем $s(X(s, \sigma)) = s$ по $s$:

$$\sum_i \frac{\partial s}{\partial x_i}\bigg|_{X(s,\sigma)} \cdot \dot{X}_i = 1$$

Так как $\dot{X}_i = b_i$ из характеристического ОДУ, получаем $\sum_i b_i, \frac{\partial s}{\partial x_i} = 1$.

**Тождество $B_k = 0$.** Дифференцируем $\sigma_k(X(s, \sigma)) = \sigma_k$ по $s$:

$$\sum_i \frac{\partial \sigma_k}{\partial x_i}\bigg|_{X(s,\sigma)} \cdot \dot{X}_i = 0$$

Снова используя $\dot{X}_i = b_i$: $\sum_i b_i, \frac{\partial \sigma_k}{\partial x_i} = 0$. $\quad\blacksquare$

---
