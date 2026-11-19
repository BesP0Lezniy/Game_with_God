---
layout: default
title: Главная
---

# **(РУС) Продолжения Евклида-Гёделя**

## *Глава 1. Теория Структур*
{: .#ch-1}

### **Раздел I. Искусственная артикуляция**
{: .accent #prt-I}

#### <span class="accent">— [Определение I.1]</span>
{: .courier #def-I-1}

Пусть $$\Sigma = \{1,2,3,4,5,6\}$$ — конечный алфавит сортов (цветов) в теории множеств Цермело-Франкеля (ZF). Элементы $$\Sigma$$ называются сортами.

#### <span class="accent">— [Определение I.2]</span>
{: .courier #def-I-2}

Пусть $\mathcal G = (\Sigma,\mathcal F)$ — полиадическая сигнатура, где $\mathcal F$ — множество из шести генераторов (1-ячеек). Каждый генератор имеет профиль сортов $$\alpha_i: i \to j_i \otimes k_i \otimes l_i$$, $$i, j_i, k_i, l_i \in \Sigma$$, где индексы $$j_i, k_i, l_i$$ зависят от $$i$$ согласно таблице:

$$
\mathcal F = \{\, 1 \xrightarrow{\alpha_1} 2\otimes 3\otimes 4,\quad 2 \xrightarrow{\alpha_2} 1\otimes 3\otimes 5,\quad 3 \xrightarrow{\alpha_3} 1\otimes 2\otimes 6,\quad 4 \xrightarrow{\alpha_4} 5\otimes 6\otimes 1,\quad 5 \xrightarrow{\alpha_5} 4\otimes 6\otimes 2,\quad 6 \xrightarrow{\alpha_6} 4\otimes 5\otimes 3 \, \}
$$

#### <span class="accent">— [Определение I.3]</span>
{: .courier #def-I-3}

Оператор искусственной инициализации $\mathcal I_{art}$ сопоставляет сигнатуре $\mathcal G$ свободный $\Sigma$-цветной PROP $$\mathbf C = \mathrm{FreePROP}_\Sigma(\mathcal G)$$, порождённый сигнатурой $\mathcal G$. Инициализация является исключительно синтаксической: 2-ячейки (соотношения) в [Разделе I](#prt-I) не задаются.

#### <span class="accent">— [Лемма I.1]</span>
{: .courier #lem-I-1}

Объекты (0-ячейки) $\mathbf C$ образуют свободный моноид $\Sigma^{*}$ над $\Sigma$. В частности, $2\otimes 3\otimes 4$ и $3\otimes 2\otimes 4$ — различные 0-ячейки.

***<span class="accent">Доказательство</span>***. По построению свободного цветного PROP объекты порождаются $\Sigma$ и моноидальным произведением $\otimes$ без соотношений. Следовательно, объекты — слова над $\Sigma$, а различные слова — различные объекты. $\square$

#### <span class="accent">— [Лемма I.2]</span>
{: .courier #lem-I-2}

Симметричная моноидальная структура $\mathbf C$ предоставляет канонические 1-ячейки симметрии $$\sigma_{i,j}: i \otimes j \to j \otimes i$$, посредством которых переставленные множители канонически изоморфны.

***<span class="accent">Доказательство</span>***. В свободном симметричном моноидальном PROP симметрии $\sigma_{i,j}$ входят в число образующих 1-ячеек (по определению симметричной моноидальной структуры). Они каноничны и не зависят от выбора. $\square$

#### <span class="accent">— [Замечание I.1]</span>
{: .courier #rem-I-1}

Порядок множителей в кодомене $\alpha_i$ не имеет инвариантного структурного статуса: любой морфизм, различающий порядок, сопряжён с соответствующей симметрией $\sigma$. Декартовы проекции на отдельные компоненты триплета не определены, поскольку объекты $\mathbf C$ — слова, а не кортежи.

#### <span class="accent">— [Теорема I.1]</span>
{: .courier #thm-I-1}

$$\mathbf C$$ является инициальным объектом в категории $\Sigma$-цветных PROP с цветосохраняющими морфизмами: для любого $\Sigma$-цветного PROP $\mathbf D$, снабжённого семейством генераторов $$\{\alpha_i'\}_{i\in\Sigma}$$ с профилями сортов $$\alpha_i': i \to j_i \otimes k_i \otimes l_i$$ (теми же, что у $\alpha_i$), существует единственный цветосохраняющий морфизм цветных PROP $$\mathbf C \to \mathbf D$$, $$\alpha_i \mapsto \alpha_i'$$.

***<span class="accent">Доказательство</span>***. По универсальному свойству свободного PROP: для любого отображения образующих 1-ячеек $$\alpha_i \mapsto \alpha_i'$$, сохраняющего профили сортов, существует единственное продолжение до морфизма цветных PROP. Единственность следует из того, что $\mathbf C$ порождён $\mathcal F$ как PROP; существование — из того, что $\mathbf D$ снабжён генераторами того же профиля. $\square$

#### <span class="accent">— [Следствие I.1]</span>
{: .courier #cor-I-1}

На шаге I никакая семантика не фиксирована: $\mathbf C$ задан чисто синтаксически, никакая категория моделей не выбрана, никакое семейство $\mathbf C$-алгебр не постулировано.

***<span class="accent">Доказательство</span>***. 2-ячейки не задаются [\[Определение I.3\]](#def-I-3); $\mathbf C$ универсален в категории PROP, но не в категории алгебр [\[Теорема I.1\]](#thm-I-1). Следовательно, семантика (модель, алгебра) не входит в определение $\mathbf C$. $\square$

---

#### <span class="accent">— [Интуитивное описание I]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

Мы начали с чистого синтаксиса: конечный алфавит $\Sigma$ и шесть генераторов $\alpha_i: i \to j_i\otimes k_i\otimes l_i$. Никакой семантики, никакой модели, никакой категории алгебр. Причина: если начать с семантики, она войдёт в определение $\mathbf C$, чего мы избегаем.

**2. <span class="accent">Какие шаги выполнили</span>?**

Построили свободный $\Sigma$-цветной PROP $$\mathbf{C} = \mathrm{FreePROP}_{\Sigma}(\mathcal{G})$$. Установили:

(а) Объекты $$\mathbf C$$ — слова над $\Sigma$ [\[Лемма I.1\]](#lem-I-1).

(б) Симметрии $\sigma\_{i,j}$ каноничны, порядок множителей не инвариантен [\[Лемма I.2\]](#lem-I-2), [\[Замечание I.1\]](#rem-I-1).

(в) $\mathbf{C}$ инициальный в категории $\Sigma$-цветных PROP [\[Теорема I.1\]](#thm-I-1).

(г) Семантика не фиксирована [\[Следствие I.1\]](#cor-I-1).

**3. <span class="accent">К чему пришли</span>?**

Получили чисто синтаксический объект $\mathbf C$, который:

(а) Полностью определён конечными данными $(\Sigma,\mathcal F)$.

(б) Универсален в категории PROP.

(в) Не содержит никакой семантики.

(г) Является инициальным — из него единственным образом отображается в любой PROP с теми же генераторами.

**4. <span class="accent">Что это значит сейчас</span>?**

$\mathbf C$ не содержит ни булевой алгебры, ни идеала, ни коалгебры, ни топологии, ни динамики. Сейчас $\mathbf C$ полон как свободный PROP.

---

### **Раздел II. Брунновость**
{: .accent #prt-II}


#### <span class="accent">— [Определение II.1]</span>
{: .courier #def-II-1}

Пусть $B\_{6} = \mathbb{F}\_{2}[x\_{1},\dots,x\_{6}]/\langle x\_{i}^{2} - x\_{i}\rangle\_{i=1}^{6}$ — булево кольцо (коммутативная идемпотентная $\mathbb{F}\_{2}$-алгебра с единицей). Элементы $B\_{6}$ — функции $\mathbb{F}\_{2}^{6} \to \mathbb{F}\_{2}$, то есть $B\_{6} \cong \mathbb{F}\_{2}^{64}$.

Формализм ZF не запрещает введение семантизации. Другие синтаксические базы и другие семантизации также не запрещены; введение $\mathbf C$ как свободного $\Sigma$-цветного PROP — одно из разрешённых описаний.

#### <span class="accent">— [Определение II.2]</span>
{: .courier #def-II-2}

Сортам $\Sigma$ сопоставляются координатные функции $x_1,\dots,x_6 \in B_6$. Генератору $\alpha_i: i \to j_i \otimes k_i \otimes l_i$ сопоставляется полиномиальное соотношение $x_i + x_{j_i}x_{k_i}x_{l_i} = 0$. Идеал ограничений:

$$
I = \langle x_1 + x_2x_3x_4,\; x_2 + x_1x_3x_5,\; x_3 + x_1x_2x_6,\; x_4 + x_5x_6x_1,\; x_5 + x_4x_6x_2,\; x_6 + x_4x_5x_3 \rangle \subset B_6.
$$

Выбор $B_6$ и этой семантизации ничем не вынуждается из $\mathbf{C}$. Семантика вводится здесь; $\mathbf{C}$ остаётся чисто синтаксическим. После выбора обязательны: $V(I) = \{\mathbf{0}, \mathbf{1}\}$, $I + \langle x_i\rangle = \mathfrak m$, $B_6/I \cong \mathbb{F}_2\times\mathbb{F}_2$.

#### <span class="accent">— [Определение II.3]</span>
{: .courier #def-II-3}

Определим $$T: \mathbb{F}_2^6 \to \mathbb{F}_2^6$$ покомпонентно: $$T(v)_i = v_{j_i}\,v_{k_i}\,v_{l_i}$$.

Тогда $\mathrm{Fix}(T) = \{v \in \mathbb{F}_2^6 : T(v) = v\} = V(I)$ — точное равенство.

#### <span class="accent">— [Замечание II.1]</span>
{: .courier #rem-II-1}

В кольце $\mathbb{F}_2[x_1,\dots,x_6]$ идеал $I$ не радикален: например, $x_1 + x_2 \in \sqrt{I} \setminus I$ (на $V(I) = \{\mathbf{0}, \mathbf{1}\}$ выполнено $x_1 + x_2 = 0$, но $x_1 + x_2 \notin I$). В булевом кольце $B_6$ всякий идеал радикален, поскольку $f^2 = f$ для любого $f \in B_6$; следовательно, $f^n \in I \Rightarrow f \in I$.

#### <span class="accent">— [Теорема II.1]</span>
{: .courier #thm-II-1}

Двухточечность многообразия $V(I) = \{\mathbf{0}, \mathbf{1}\}$.

***<span class="accent">Доказательство</span>***.

(1) $\mathbf{1} \in V(I)$: $1 = 1\cdot 1\cdot 1$ во всех шести уравнениях.

(2) Пусть $v \in V(I)$, $v \neq \mathbf{1}$. Покажем $v = \mathbf{0}$. Если существует $s$ с $v_s = 1$, то из $v_s = v_{j_s}v_{k_s}v_{l_s}$ следует $v_{j_s} = v_{k_s} = v_{l_s} = 1$. Индукцией вдоль путей в 3-гиперграфе $\mathcal{G}$ и по его сильной связности (проверяется прямой выпиской достижимости: $1 \to \{2,3,4\}$, $2 \to \{1,3,5\}$, $3 \to \{1,2,6\}$, $4 \to \{5,6,1\}$, $5 \to \{4,6,2\}$, $6 \to \{4,5,3\}$, откуда из любой вершины достижимы все) получаем $v = \mathbf{1}$, противоречие. Значит $v_i = 0$ для всех $i$, т.е. $v = \mathbf{0}$.

(3) $\mathbf{0} \in V(I)$: $0 = 0\cdot 0\cdot 0$. $\square$

#### <span class="accent">— [Замечание II.2]</span>
{: .courier #rem-II-2}

***<span class="accent">Доказательство</span>*** [\[Теоремы II.1\]](#thm-II-1) использует только сильную связность $\mathcal{G}$ и конъюнктивную форму уравнений. Самоссылки не исключаются. Для конкретной таблицы $\mathcal{F}$ самоссылок нет, но это частное комбинаторное свойство, не необходимое для теоремы.

#### <span class="accent">— [Следствие II.1]</span>
{: .courier #cor-II-1}

$$
I = \langle x_1 + x_6,\; x_2 + x_6,\; x_3 + x_6,\; x_4 + x_6,\; x_5 + x_6 \rangle.
$$

***<span class="accent">Доказательство</span>***.

(1) $B\_{6} \cong \mathbb{F}\_{2}^{64}$ (произведение копий $\mathbb{F}\_{2}$ по точкам $\mathbb{F}\_{2}^{6}$).

(2) Всякий идеал в $B\_{6}$ радикален [\[Замечание II.1\]](#rem-II-1), $V(I) = \{\mathbf{0}, \mathbf{1}\}$ [\[Теорема II.1\]](#thm-II-1).

(3) Многочлен $x\_{i} + x\_{6}$ обращается в нуль на обеих точках, по радикальности $I = I(V(I)) = \langle x\_{i} + x\_{6}\rangle\_{i=1}^{5}$.

(4) Само вычисление $I(V(I))$ в $B_6$ также корректно вследствие описанного свойства [\[Замечание II.1\]](#rem-II-1) $\square$

#### <span class="accent">— [Определение II.4]</span>
{: .courier}

Пусть $\mathcal{H}$ — ориентированный 3-гиперграф на конечном множестве $\Sigma$ с оператором $T\_{\mathcal{H}}(v)\_{i} = v\_{j\_{i}}v\_{k\_{i}}v\_{l\_{i}}$. $\mathcal{H}$ называется комбинаторной брунновой сетью, если:

(а) $\mathcal{H}$ сильно связен.

(б) Форма соотношений конъюнктивна: $x_i = x_{j_i}x_{k_i}x_{l_i}$.

(в) $\mathrm{Fix}(T_{\mathcal{H}}) = \{\mathbf{0}, \mathbf{1}\}$.

(г) Для любого $i \in \Sigma$: $\mathrm{Fix}(T_{\mathcal{H}}) \cap \{v_i = 0\} = \{\mathbf{0}\}$.

#### <span class="accent">— [Теорема II.2]</span>
{: .courier #thm-II-2}

Сигнатура $\mathcal{G}$ из [Раздела I](#prt-I) является комбинаторной брунновой сетью.

***<span class="accent">Доказательство</span>***.

(1) Сильная связность — проверена в доказательстве при прямой выписке достижимости [\[Теорема II.1\]](#thm-II-1).

(2) Конъюнктивная форма — задана по определению [\[Определение II.2\]](#def-II-2).

(3) $\mathrm{Fix}(T) = V(I) = \{\mathbf{0}, \mathbf{1}\}$ — [\[Теорема II.1\]](#thm-II-1), [\[Определение II.3\]](#def-II-3).

(4) Для любого $i \in \Sigma$: если $v \in V(I)$ и $v_i = 0$, то $v \neq \mathbf{1}$; по (3) $v = \mathbf{0}$. Значит $\mathrm{Fix}(T) \cap \{v_i = 0\} = \{\mathbf{0}\}$. $\square$

#### <span class="accent">— [Следствие II.2]</span>
{: .courier #cor-II-2}

Для любого $i \in \Sigma$:

$$
I + \langle x_i\rangle = \mathfrak{m} = \langle x_1,\dots,x_6\rangle, \qquad V(I + \langle x_i\rangle) = \{\mathbf{0}\}.
$$

***<span class="accent">Доказательство</span>***.

(1) $I = \langle x_j + x_6\rangle_{j=1}^5$ в $B_6$ [\[Следствие II.1\]](#cor-II-1).

(2) Если $i \neq 6$: из $x_i = 0$ и $x_i + x_6 \in I + \langle x_i\rangle$ следует $x_6 = 0$; тогда из $x_j + x_6 \in I + \langle x_i\rangle$ следует $x_j = 0$ для $j = 1,\dots,5$.

(3) Если $i = 6$: $x_6 = 0$, и $x_j + x_6 = x_j = 0$ для $j=1,\dots,5$.

(4) В обоих случаях $I + \langle x_i\rangle = \mathfrak{m}$. $\square$

#### <span class="accent">— [Следствие II.3]</span>
{: .courier #cor-II-3}

$$
B_6/I \cong \mathbb{F}_2 \times \mathbb{F}_2, \qquad B_6/(I + \langle x_i\rangle) \cong \mathbb{F}_2 \quad (i \in \Sigma).
$$

***<span class="accent">Доказательство</span>***.

(1) $V(I) = \{\mathbf{0}, \mathbf{1}\}$ и $B_6$ — произведение копий $\mathbb{F}_2$ по точкам.

(2) $B_6/(I + \langle x_i\rangle) \cong \mathbb{F}_2$ тоже верно [\[Следствие II.2\]](#cor-II-2). $\square$

#### <span class="accent">[Замечание II.3]</span>
{: .courier #rem-II-3}

В аффинной алгебраической геометрии многообразие $V(I^*)$ определяется как статическое множество общих нулей; итеративная процедура вычисления не входит в определение. Утверждение «коллапс симультанен» в настоящем разделе означает только это: $V(I + \langle x_i\rangle) = \{\mathbf{0}\}$ есть факт алгебраической геометрии, а не результат пошагового алгоритма. Никаких утверждений об «отсутствии алгоритмического шага» или «мгновенности» в смысле теории вычислений не делается.

---

#### <span class="accent">— [Интуитивное описание II]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

Начали с чисто синтаксического $\mathbf{C}$ ([Раздел I](#prt-I)), оно полно как свободный PROP, но $\mathbf{C}$ не содержит семантики: ни идемпотентности, ни идеала, ни многообразия. Формализм не запрещает задать вопрос «чему равно $V(I)$?» — это разрешает ввести семантизацию в принципе.

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Ввели булево кольцо $B_6$ и идеал $I$ (выбор $\mathcal{P}_{sem}$).

(б) Определили оператор $T$ с $\mathrm{Fix}(T) = V(I)$.

(в) Установили нерадикальность $I$ в $\mathbb{F}_2[x]$ и радикальность в $B_6$ [\[Замечание II.1\]](#rem-II-1).

(г) Доказали: $V(I) = \{\mathbf{0}, \mathbf{1}\}$ [\[Теорема II.1\]](#thm-II-1); $I = \langle x_i + x_6\rangle$ в $B_6$ [\[Следствие II.1\]](#cor-II-1); $\mathcal{G}$ — комбинаторная бруннова сеть [\[Теорема II.2\]](#thm-II-2); $I + \langle x_i\rangle = \mathfrak{m}$ [\[Следствие II.2\]](#cor-II-2); $B_6/I \cong \mathbb{F}_2\times\mathbb{F}_2$ [\[Следствие II.3\]](#cor-II-3).

**3. <span class="accent">К чему пришли</span>?**

Получили брунновость: $V(I) = \{\mathbf{0}, \mathbf{1}\}$ («всё или ничего», нет частичного), $I + \langle x_i\rangle = \mathfrak{m}$ (любой нуль стягивает всё), $B_6/I \cong \mathbb{F}_2\times\mathbb{F}_2$ (два атома). Это точная алгебраическая структура, не метафора.

**4. <span class="accent">Что это значит сейчас</span>?**

Брунновость — фундамент всей дальнейшей цепи. Она задаёт:

(а) Два полюса $\mathbf{0}, \mathbf{1}$.

(б) Запрет третьего.

(в) Коллапс при любом нуле.

Формализм не запрещает перейти к коалгебраическому развёртыванию ([Раздел III](#prt-III)): статика $B_6$ не даёт коалгебры, поэтому принципиально разрешено ввести копредел.

---

### **Раздел III. Рекурсия**
{: .accent #prt-III}

#### <span class="accent">— [Определение III.1]</span>
{: .courier #def-III-1}

Тензорный эндофунктор $F: \mathbf{BoolAlg} \to \mathbf{BoolAlg}$, $F(X) = X \otimes_{\mathbb{F}\_{2}} X \otimes_{\mathbb{F}\_{2}} X$. В $\mathbf{BoolAlg}$ тензор есть копроизведение; $F$ сохраняет фильтрованные копределы.

#### <span class="accent">— [Определение III.2]</span>
{: .courier #def-III-2}

Структурное отображение $\alpha: B\_{6} \to F(B\_{6}) = B\_{6}^{\otimes 3}$ — гомоморфизм $\mathbb{F}\_{2}$-алгебр, заданный на образующих $x\_{i} \mapsto x\_{j\_{i}} \otimes x\_{k\_{i}} \otimes x\_{l\_{i}}$.

Корректность: $\alpha(x\_{i}^{2}) = x\_{j\_{i}}^{2} \otimes x\_{k\_{i}}^{2} \otimes x\_{l\_{i}}^{2} = x\_{j\_{i}} \otimes x\_{k\_{i}} \otimes x\_{l\_{i}} = \alpha(x\_{i})$ в силу идемпотентности $x^{2} = x$ в $B\_{6}$. Значит, $\alpha$ продолжается до гомоморфизма на $B\_{6}$.

#### <span class="accent">— [Определение III.3]</span>
{: .courier #def-III-3}

Для $A \in \mathbf{BoolAlg}$ и идеала $J \subset A$: $J^{[n]} := \ker(A^{\otimes n} \twoheadrightarrow (A/J)^{\otimes n}) = \sum_{s=1}^{n} A^{\otimes(s-1)} \otimes J \otimes A^{\otimes(n-s)} \subset A^{\otimes n}$.

Канонический изоморфизм: $A^{\otimes n}/J^{[n]} \cong (A/J)^{\otimes n}$. В частности, $I^{[3]} = I \otimes B\_{6} \otimes B\_{6} + B\_{6} \otimes I \otimes B\_{6} + B\_{6} \otimes B\_{6} \otimes I$.

#### <span class="accent">— [Лемма III.1]</span>
{: .courier #lem-III-1}

$\alpha$ инъективно.

***<span class="accent">Доказательство</span>***.

(1) Достаточно сюръективности $\mathrm{Spec}(\alpha)$ на $\mathbb{F}\_{2}$-точках.

(2) Положим $T(v^{1},v^{2},v^{3})\_{i} = v^{1}\_{j\_{i}}v^{2}\_{k\_{i}}v^{3}\_{l\_{i}}$. Для $w \in \mathbb{F}\_{2}^{6}$: $S = \{i: w\_{i} = 1\}$; $v^{1}\_{j} = 1 \iff j \in \{j\_{i} : i \in S\}$, $v^{2}\_{k} = 1 \iff k \in \{k\_{i} : i \in S\}$, $v^{3}\_{l} = 1 \iff l \in \{l\_{i} : i \in S\}$.

(3) Тогда $T\_{i} = 1 \iff i \in S$ — по таблице $\mathcal{F}$: для каждого $i$ существует координата $c(i) \in \{j,k,l\}$, значение которой у $\alpha\_{i}$ не встречается у $\alpha\_{i'}$ при $i' \neq i$: $c(1)=j$ (значение 2), $c(2)=l$ (5), $c(3)=k$ (2), $c(4)=j$ (5), $c(5)=l$ (2), $c(6)=k$ (5).

(4) Если $i \notin S$, то $c(i)$-координата $\alpha\_{i}$ не входит в соответствующее множество (уникальность), значит соответствующая $v$-координата равна 0, и $T\_{i} = 0$. $\square$

#### <span class="accent">— [Замечание III.1]</span>
{: .courier #rem-III-3}

***<span class="accent">Доказательство</span>*** использует фиксированную таблицу $\mathcal{F}$ (свидетели). Замена таблицы может нарушить инъективность.

#### <span class="accent">— [Лемма III.2]</span>
{: .courier #lem-III-2}

$\alpha(I) \subset I^{[3]}$.

***<span class="accent">Доказательство</span>***.

(1) В $B\_{6}/I \cong \mathbb{F}\_{2} \times \mathbb{F}\_{2}$ — две точки $\mathbf{0}, \mathbf{1}$. В $(B\_{6}/I)^{\otimes 3}$ — 8 точек.

(2) Для $x \in I$ и $u = (u^{1},u^{2},u^{3}) \in \{(\mathbf{0},\mathbf{0},\mathbf{0}), \ldots, (\mathbf{1},\mathbf{1},\mathbf{1})\}$: если хотя бы один $u^{k} = \mathbf{0}$, то оба слагаемых $= 0$; если $u^{1}=u^{2}=u^{3}=\mathbf{1}$, то оба $=1$, сумма $1+1=0$ в $\mathbb{F}\_{2}$.

(3) Во всех 8 случаях $=0$, значит $\alpha(x\_{i} + x\_{j\_{i}}x\_{k\_{i}}x\_{l\_{i}}) \in \ker(\pi^{\otimes 3}) = I^{[3]}$. $\square$

#### <span class="accent">— [Определение III.4]</span>
{: .courier #def-III-4}

Итерационная цепь: $\mathcal{L}\_{0} = B\_{6}$, $\mathcal{L}\_{k+1} = F(\mathcal{L}\_{k})$, $\alpha\_{k} = F^{k}(\alpha): \mathcal{L}\_{k} \to \mathcal{L}\_{k+1}$. Идеалы: $I\_{0} = I \subset \mathcal{L}\_{0}$; $I\_{k+1} := \ker(\mathcal{L}\_{k+1} \twoheadrightarrow (B\_{6}/I)^{\otimes 3^{k+1}})$.

Канонические вложения копредела: $\iota\_{k}: \mathcal{L}\_{k} \to \mathbb{H}\_{core}$, согласованные с $\alpha\_{k}$.

#### <span class="accent">— [Лемма III.3]</span>
{: .courier #lem-III-3}

$I\_{k+1} = I\_{k}^{[3]}$ и $\alpha\_{k}(I\_{k}) \subset I\_{k+1}$.

***<span class="accent">Доказательство</span>***.

(1) $\mathcal{L}\_{k+1} = \mathcal{L}\_{k}^{\otimes 3}$ и $(B\_{6}/I)^{\otimes 3^{k+1}} = ((B\_{6}/I)^{\otimes 3^{k}})^{\otimes 3}$ [\[Определение III.3\]](#def-III-3), следовательно $I\_{k+1} = \ker(\mathcal{L}\_{k}^{\otimes 3} \twoheadrightarrow (\mathcal{L}\_{k}/I\_{k})^{\otimes 3}) = I\_{k}^{[3]}$.

(2) Индукция: $k=0$ [\[Лемма III.2\]](#lem-III-2); $k \Rightarrow k+1$: $\alpha\_{k+1}(I\_{k+1}) = \alpha\_{k}^{\otimes 3}(I\_{k}^{[3]}) = (\alpha\_{k}(I\_{k}))^{[3]} \subset I\_{k+1}^{[3]} = I\_{k+2}$ (использовано $\alpha\_{k+1} = \alpha\_{k}^{\otimes 3}$, что следует из $\alpha\_{k} = F^{k}(\alpha)$). $\square$

#### <span class="accent">— [Теорема III.1]</span>
{: .courier #thm-III-1}

В $\mathbf{BoolAlg}$ существуют:

(а) $\mathbb{H}\_{core} = \varinjlim\_{k} \mathcal{L}\_{k}$ с $F$-коалгебраической структурой $\omega\_{core}: \mathbb{H}\_{core} \to F(\mathbb{H}\_{core})$.

(б) Идеал $I\_{\infty} = \varinjlim\_{k} I\_{k} \subset \mathbb{H}\_{core}$, $\alpha\_{\infty}$-инвариантный: $\alpha\_{\infty}(I\_{\infty}) \subset I\_{\infty}^{[3]}$.

(в) Фактор-коалгебра $\mathbb{H}\_{brunn} = \mathbb{H}\_{core}/I\_{\infty}$ с $\omega\_{brunn}$.

***<span class="accent">Доказательство</span>***.

(1) Копредел существует (фильтрованная диаграмма, коконечность $\mathbf{BoolAlg}$). Копроизведение $\otimes\_{\mathbb{F}\_{2}}$ сохраняет копределы: $F(\mathbb{H}\_{core}) = \varinjlim F(\mathcal{L}\_{k}) = \varinjlim \mathcal{L}\_{k+1} \cong \mathbb{H}\_{core}$; канонический изоморфизм даёт $\omega\_{core}$.

(2) $I\_{\infty}$ — идеал (фильтрованный копредел идеалов). $\alpha\_{\infty}(I\_{\infty}) = \varinjlim \alpha\_{k}(I\_{k}) \subset \varinjlim I\_{k+1} = \varinjlim I\_{k}^{[3]} = (\varinjlim I\_{k})^{[3]} = I\_{\infty}^{[3]}$ (последнее равенство — сохранение копределов тензором: $I\_{k}^{[3]}$ есть сумма $I\_{k} \otimes \mathcal{L}\_{k} \otimes \mathcal{L}\_{k} + \ldots$, и копредел суммы есть сумма копределов).

(3) По (2) $\alpha\_{\infty}$ пропускается через $\mathbb{H}\_{core}/I\_{\infty}$, давая $\omega\_{brunn}$. $\square$

#### <span class="accent">— [Следствие III.1]</span>
{: .courier #cor-III-1}

$\mathbb{H}\_{brunn} \cong \varinjlim\_{k} F^{k}(B\_{6}/I)$.

***<span class="accent">Доказательство</span>***.

$I\_{k} = \ker(\mathcal{L}\_{k} \twoheadrightarrow (B\_{6}/I)^{\otimes 3^{k}})$ [\[Определение III.4\]](#def-III-4), значит $\mathcal{L}\_{k}/I\_{k} \cong (B\_{6}/I)^{\otimes 3^{k}}$. Тогда $\varinjlim (\mathcal{L}\_{k}/I\_{k}) \cong \varinjlim (B\_{6}/I)^{\otimes 3^{k}}$. $\square$

#### <span class="accent">— [Теорема III.2]</span>
{: .courier #thm-III-2}

$\vert \mathbb{H}\_{core}\vert = \vert \mathbb{H}\_{brunn}\vert = \aleph\_{0}$ в ZF.

***<span class="accent">Доказательство</span>***.

(1) $\vert B\_{6}\vert = 2^{6} = 64$, $\dim\_{\mathbb{F}\_{2}}(B\_{6}) = 6$; $\vert \mathcal{L}\_{k}\vert = 2^{6 \cdot 3^{k}}$. $\vert B\_{6}/I\vert = 4$ ($\dim\_{\mathbb{F}\_{2}}(B\_{6}/I) = 2$); $\vert F^{k}(B\_{6}/I)\vert = 2^{2^{3^{k}}}$ (так как $\dim\_{\mathbb{F}\_{2}}((B\_{6}/I)^{\otimes 3^{k}}) = 2^{3^{k}}$).

(2) Каждый слой конечен, явно упорядочен, инъекции $\alpha\_{k}$ сохраняют «старые» элементы. Нумерация: элемент из $\mathcal{L}\_{k}$ под номером $m$ получает номер $\sum\_{j \lt k}\vert \mathcal{L}\_{j}\vert + m$. Явная биекция с $\mathbb{N}$, без AC. $\square$

#### <span class="accent">— [Следствие III.2]</span>
{: .courier #cor-III-2}

Каноническая проекция $\pi\_{\infty}: \mathbb{H}\_{core} \twoheadrightarrow \mathbb{H}\_{brunn} = \mathbb{H}\_{core}/I\_{\infty}$ есть сюръективный морфизм $F$-коалгебр.

***<span class="accent">Доказательство</span>***. $\pi\_{\infty}$ — сюръекция по определению фактора. Коммутативность с коалгебраическими структурами: $\omega\_{brunn}\circ\pi\_{\infty} = (\pi\_{\infty}^{\otimes 3})\circ\omega\_{core}$ — следует из спуска $\alpha\_{\infty}$ на фактор [\[Теорема III.1\]](#thm-III-1). $\square$

#### <span class="accent">— [Замечание III.2]</span>
{: .courier #rem-III-2}

***<span class="accent">Доказательство</span>*** $\mathbb{H}\_{brunn}$ — фактор $\mathbb{H}\_{core}$, не подобъект: в $\mathbf{BoolAlg}$ у сюръекции нет канонического сечения.

#### <span class="accent">— [Следствие III.3]</span>
{: .courier #cor-III-3}

$\omega\_{core}\circ\iota\_{0} = F(\iota\_{0})\circ\alpha$ как морфизмы $B\_{6} \to \mathbb{H}\_{core}^{\otimes 3}$.

***<span class="accent">Доказательство</span>***. Тождество следует из определения $\omega\_{core} = \varinjlim \alpha\_{k}$ и согласованности $\iota\_{k+1}\circ\alpha\_{k} = \iota\_{k}$ (каноническое свойство копредела). $\square$

---

#### <span class="accent">— [Интуитивное описание III]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

Начали с $B\_{6}$ и идеала $I$ ([Раздел II](#prt-II)). $B\_{6}$ конечна; формализм не запрещает ввести копредел.

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Построили $\alpha: B\_{6} \to B\_{6}^{\otimes 3}$.

(б) Доказали: $\alpha$ инъективно ([\[Лемма III.1\]](#lem-III-1)); $\alpha(I) \subset I^{[3]}$ ([\[Лемма III.2\]](#lem-III-2)); $I\_{k+1} = I\_{k}^{[3]}$, $\alpha\_{k}(I\_{k}) \subset I\_{k+1}$ ([\[Лемма III.3\]](#lem-III-3)). А также счётность ([\[Теорема III.2\]](#thm-III-2)), проекцию ([\[Следствие III.2\]](#cor-III-2)), коммутативность с $\iota\_{0}$ ([\[Следствие III.3\]](#cor-III-3)).

(в) Ввели $\mathbb{H}\_{core}$, $I\_{\infty}$, $\mathbb{H}\_{brunn}$ ([\[Теорема III.1\]](#thm-III-1)).

**3. <span class="accent">К чему пришли</span>?**

$\mathbb{H}\_{core}$ — счётная $F$-коалгебра с $\omega\_{core}: \mathbb{H}\_{core} \to F(\mathbb{H}\_{core})$ (изоморфизм, так как $F$ сохраняет копределы). $\mathbb{H}\_{brunn}$ — фактор-коалгебра. Оба счётны.

**4. <span class="accent">Что это значит сейчас</span>?**

Получили бесконечный счётный остов с коалгебраической структурой.

---

### **Раздел IV. Счётная бесконечность**
{: .accent #prt-IV}

#### <span class="accent">— [Определение IV.1]</span>
{: .courier #def-IV-1}

Для $A \in \mathbf{BoolAlg}$: $\mathrm{Spec}(A) := \mathrm{Hom}_{\mathbf{BoolAlg}}(A, \mathbb{F}\_{2})$ с базой $\{U\_{a} := \{h : h(a) = 1\}\}\_{a \in A}$.

Обозначим $\partial\mathbb{H}\_{core} := \mathrm{Spec}(\mathbb{H}\_{core})$, $\partial\mathbb{H}\_{brunn} := \mathrm{Spec}(\mathbb{H}\_{brunn})$.

Формализм ZF не запрещает ввести $\mathrm{Spec}$.

#### <span class="accent">— [Лемма IV.1]</span>
{: .courier #lem-IV-1}

$\partial\mathbb{H}\_{core} \cong \varprojlim\_{k} \mathrm{Spec}(\mathcal{L}\_{k})$ канонически.

***<span class="accent">Доказательство</span>***.

Двойственность Стоуна переводит копределы в пределы. $\square$

#### <span class="accent">— [Лемма IV.2]</span>
{: .courier #lem-IV-2}

$\mathbb{H}\_{core}$ не имеет атомов.

***<span class="accent">Доказательство</span>***.

(1) Пусть $x \in \mathbb{H}\_{core}$, $x \neq 0$. Без ограничения $x = e\_{p}$ для атома $e\_{p} \in \mathcal{L}\_{k}$, $p \in \mathrm{Spec}(\mathcal{L}\_{k})$. Тогда $\alpha\_{k}(e\_{p}) = \sum\_{q \in (\alpha\_{k}^{\*})^{-1}(p)} e\_{q}$ в $\mathcal{L}\_{k+1}$.

(2) Пусть $p = (p\_{1},\dots,p\_{3^{k}})$, $p\_{t} \in \mathbb{F}\_{2}^{6}$. Тогда $\vert(\alpha\_{k}^{\*})^{-1}(p)\vert = \prod\_{t=1}^{3^{k}} \vert T^{-1}(p\_{t})\vert$, где $T: (\mathbb{F}\_{2}^{6})^{3} \to \mathbb{F}\_{2}^{6}$, $T(v^{1},v^{2},v^{3})\_{i} = v^{1}\_{j\_{i}}v^{2}\_{k\_{i}}v^{3}\_{l\_{i}}$.

(3) Конечная проверка: для $p\_{t} = \mathbf{1}$: $j\_{i}$ принимает значения $\{2,1,1,5,4,4\}$, уникальные $\{1,2,4,5\}$ фиксированы, свободны 2; $k\_{i}$: $\{3,3,2,6,6,5\}$, уникальные $\{2,3,5,6\}$, свободны 2; $l\_{i}$: $\{4,5,6,1,2,3\}$, все 6 фиксированы.

(4) Итого $\vert T^{-1}(\mathbf{1})\vert = 2^{2} \cdot 2^{2} \cdot 1 = 16$. Для остальных $p\_{t}$ перебор 64 случаев даёт $\vert T^{-1}(p\_{t})\vert \geq 16$. Следовательно, $\vert(\alpha\_{k}^{\*})^{-1}(p)\vert \geq 16^{3^{k}} \geq 2$, и $\alpha\_{k}(e\_{p})$ — сумма $\geq 2$ различных атомов, значит не атом. $\square$

#### <span class="accent">— [Следствие IV.1]</span>
{: .courier #cor-IV-1}

$\partial\mathbb{H}\_{core}$ не имеет изолированных точек.

***<span class="accent">Доказательство</span>***.

Изолированная точка $\partial\mathbb{H}\_{core}$ соответствует атому $\mathbb{H}\_{core}$ (двойственность Стоуна). Атомов нет [\[Лемма IV.2\]](#lem-IV-2). $\square$

#### <span class="accent">— [Лемма IV.3]</span>
{: .courier #lem-IV-3}

$\mathbb{H}\_{brunn}$ имеет ровно один атом — образ $e\_{\mathbf{1}}$, соответствующий точке $\mathbf{1}\_{\infty} \in \partial\mathbb{H}\_{brunn}$.

***<span class="accent">Доказательство</span>***.

(1) В $B\_{6}/I \cong \mathbb{F}\_{2} \times \mathbb{F}\_{2}$ — два атома $e\_{\mathbf{0}}, e\_{\mathbf{1}}$. Индуцированное $\alpha'$: $x \mapsto x^{1} x^{2} x^{3}$.

(2) На слое $k$: для $q \in \{0,1\}^{3^{k}}$ с $z(q)$ нулями, $\vert(\alpha\_{k}'^{\*})^{-1}(q)\vert = 7^{z(q)}$. При $q = \mathbf{1}$: $z(q) = 0$, один прообраз. При $q \neq \mathbf{1}$: $z(q) \geq 1$, $\geq 7$ прообразов.

(3) Индукцией: в каждом слое ровно один атом, выживающий при переходе — образ $e\_{\mathbf{1}}$. $\square$

#### <span class="accent">— [Следствие IV.2]</span>
{: .courier #cor-IV-2}

$\partial\mathbb{H}\_{brunn}$ имеет ровно одну изолированную точку — $\mathbf{1}\_{\infty}$.

***<span class="accent">Доказательство</span>***.

Изолированная точка $\leftrightarrow$ атом (двойственность Стоуна). Атом один [\[Лемма IV.3\]](#lem-IV-3). $\square$

#### <span class="accent">— [Теорема IV.1]</span>
{: .courier #thm-IV-1}

Следующие факты имеют место одновременно:

(а) $B\_{6}$ конечна, $\vert\mathrm{At}(B\_{6})\vert = 64$; точки $V(I) = \{\mathbf{0}, \mathbf{1}\}$ соответствуют двум атомам $B\_{6}/I$ — глобальное состояние реализуется внутри.

(б) $\mathbb{H}\_{core}$ безатомна; в $\mathbb{H}\_{core}$ нет элементов, кодирующих глобальные состояния бесконечной итерации.

(в) $\mathbb{H}\_{brunn}$ имеет ровно один атом ($\mathbf{1}\_{\infty}$); одно состояние кодируется внутри, остальные нет.

(г) Глобальные состояния $\mathbb{H}\_{core}$ (и всех, кроме $\mathbf{1}\_{\infty}$, состояний $\mathbb{H}\_{brunn}$) не реализуются элементами алгебр; переход к $\mathrm{Spec}$ даёт их.

***<span class="accent">Доказательство</span>***.

(1) $B\_{6} \cong \mathbb{F}\_{2}^{64}$.

(2) [\[Лемма IV.2\]](#lem-IV-2), [\[Лемма IV.3\]](#lem-IV-3).

(3) Двойственность Стоуна: точка $h \in \mathrm{Spec}(A)$ соответствует атому $A$ тогда и только тогда, когда $h$ изолирована. Нет атомов — нет точек, реализуемых элементами. $\square$

#### <span class="accent">— [Замечание IV.1]</span>
{: .courier #rem-IV-1}

$\mathrm{Spec}$ есть канонический дуал, определённый для любой булевой алгебры. Здесь он идентифицируется в момент, когда исходный объект обнаруживает дефицит атомов.

#### <span class="accent">— [Теорема IV.2]</span>
{: .courier #thm-IV-2}

$\partial\mathbb{H}\_{core}$ и $\partial\mathbb{H}\_{brunn}$ — компактные хаусдорфовы пространства.

***<span class="accent">Доказательство</span>***.

$\partial\mathbb{H}\_{core} \cong \varprojlim \mathrm{Spec}(\mathcal{L}\_{k})$ — замкнутое подмножество $\prod\_{k} \mathrm{Spec}(\mathcal{L}\_{k})$ (конечные дискретные). На произведении — метрика $d(u,v) = 2^{-\min\{k : u\_{k} \neq v\_{k}\}}$, полная и вполне ограниченная. Компактность метрического пространства — теорема ZF. Замкнутое подмножество компакта компактно. Аналогично для $\partial\mathbb{H}\_{brunn}$. $\square$

#### <span class="accent">— [Теорема IV.3]</span>
{: .courier #thm-IV-3}

$\vert\partial\mathbb{H}\_{core}\vert = \vert\partial\mathbb{H}\_{brunn}\vert = 2^{\aleph\_{0}}$.

***<span class="accent">Доказательство</span>***.

Для $\partial\mathbb{H}\_{core}$:

(1) Верхняя граница: $\partial\mathbb{H}\_{core} \subset \prod\_{k} \mathrm{Spec}(\mathcal{L}\_{k})$, $\vert\mathrm{Spec}(\mathcal{L}\_{k})\vert = 2^{6\cdot 3^{k}}$, значит $\vert\partial\mathbb{H}\_{core}\vert \leq \prod\_{k} 2^{6\cdot 3^{k}} = 2^{\sum\_{k} 6\cdot 3^{k}} = 2^{\aleph\_{0}}$.

(2) Нижняя граница: слои $\alpha\_{k}^{\*}$ имеют размер $\geq 16$ [\[Лемма IV.2\]](#lem-IV-2). Строим инъекцию $\{0,1\}^{\mathbb{N}} \hookrightarrow \partial\mathbb{H}\_{core}$: на каждом шаге из прообраза выбираем первый и второй элементы по лексикографическому порядку. Явная конструкция в ZF, Кантор-Бернштейн. $\square$

Для $\partial\mathbb{H}\_{brunn}$:

(1) Верхняя граница: $\vert\mathrm{Spec}(\mathcal{L}\_{k}^{brunn})\vert = 2^{2^{3^{k}}}$, значит $\vert\partial\mathbb{H}\_{brunn}\vert \leq 2^{\sum\_{k} 2^{3^{k}}} = 2^{\aleph\_{0}}$.

(2) Нижняя граница: замкнутое подмножество $Z \subset \partial\mathbb{H}\_{brunn}$ нитей с $u^{(0)} = \mathbf{0}$ и $u^{(k)}\_{3m} = 0$ для каждого $k \geq 1$, $m$: свободных координат на слое $k \geq 1$ — $2\cdot 3^{k-1}$, значит $Z \cong \{0,1\}^{\mathbb{N}}$, $\vert Z\vert = 2^{\aleph\_{0}}$, Кантор-Бернштейн. $\square$

#### <span class="accent">— [Следствие IV.3]</span>
{: .courier #cor-IV-3}

(а) $\partial\mathbb{H}\_{core}$ — совершенный компакт веса $\aleph\_{0}$ и мощности $2^{\aleph\_{0}}$.

(б) $\partial\mathbb{H}\_{brunn}$ — компакт веса $\aleph\_{0}$ и мощности $2^{\aleph\_{0}}$, имеющий ровно одну изолированную точку $\mathbf{1}\_{\infty}$.

***<span class="accent">Доказательство</span>***.

(1) Совершенность — [\[Следствие IV.1\]](#cor-IV-1); мощность — [\[Теорема IV.3\]](#thm-IV-3). Вес $\aleph\_{0}$: база $\{U\_{a} : a \in \mathbb{H}\_{core}\}$ имеет мощность $\vert\mathbb{H}\_{core}\vert = \aleph\_{0}$.

(2) Единственная изолированная точка — [\[Следствие IV.2\]](#cor-IV-2); вес и мощность — аналогично. $\square$

---

#### <span class="accent">— [Интуитивное описание IV]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

С $\mathbb{H}\_{core}$, $\mathbb{H}\_{brunn}$ ([Раздел III](#prt-III)). Они счётны. Формализм не запрещает ввести $\mathrm{Spec}$ — канонический дуал булевой алгебры.

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Определили $\mathrm{Spec}$.

(б) Доказали: тождество с обратным пределом [\[Лемма IV.1\]](#lem-IV-1); безатомность $\mathbb{H}\_{core}$ [\[Лемма IV.2\]](#lem-IV-2); совершенность [\[Следствие IV.1\]](#cor-IV-1); единственный атом $\mathbb{H}\_{brunn}$ [\[Лемма IV.3\]](#lem-IV-3); изолированная точка [\[Следствие IV.2\]](#cor-IV-2); переход к спектру [\[Теорема IV.1\]](#thm-IV-1); компактность [\[Теорема IV.2\]](#thm-IV-2); мощность $2^{\aleph\_{0}}$ [\[Теорема IV.3\]](#thm-IV-3); спектральная структура [\[Следствие IV.3\]](#cor-IV-3).

**3. <span class="accent">К чему пришли</span>?**

$\partial\mathbb{H}\_{core}$ — совершенный компакт веса $\aleph\_{0}$ и мощности $2^{\aleph\_{0}}$. $\partial\mathbb{H}\_{brunn}$ — компакт с одной изолированной точкой $\mathbf{1}\_{\infty}$ и совершенным $K\_{coll} = \partial\mathbb{H}\_{brunn} \setminus \{\mathbf{1}\_{\infty}\}$, мощность $2^{\aleph\_{0}}$. Исходная алгебра счётна ($\aleph\_{0}$), вес спектра счётен ($\aleph\_{0}$); мощность спектра континуальна.

**4. <span class="accent">Что это значит сейчас</span>?**

Получили спектр с весом $\aleph\_{0}$ (счётная база) и мощностью $2^{\aleph\_{0}}$.

---

### **Раздел V. Несчётная бесконечность**
{: .accent #prt-V}

#### <span class="accent">— [Определение V.1]</span>
{: .courier #def-V-1}

$\Phi\_{core} := \mathrm{Spec}(\omega\_{core}): (\partial\mathbb{H}\_{core})^{3} \xrightarrow{\sim} \partial\mathbb{H}\_{core}$; $\Phi\_{brunn} := \mathrm{Spec}(\omega\_{brunn}): (\partial\mathbb{H}\_{brunn})^{3} \xrightarrow{\sim} \partial\mathbb{H}\_{brunn}$.

#### <span class="accent">— Замечание V.1]</span>
{: .courier #rem-V-1}

$\omega\_{core}$, $\omega\_{brunn}$ индуцированы $\alpha\_{k}: \mathcal{L}\_{k} \to \mathcal{L}\_{k}^{\otimes 3}$ с фиксированным порядком трёх тензорных факторов, заданным $F(X) = X \otimes X \otimes X$. Симметрии [Раздела I](#prt-I) относятся к цветам (сортам), не к факторам $F$. Проекции ниже определены корректно.

#### <span class="accent">— [Определение V.2]</span>
{: .courier #def-V-2}

$\sigma\_{r} := p\_{r} \circ \Phi^{-1}: \partial\mathbb{H} \to \partial\mathbb{H}$, $r = 1,2,3$, где $p\_{r}$ — $r$-я координатная проекция, $\Phi \in \{\Phi\_{core}, \Phi\_{brunn}\}$.

#### <span class="accent">— [Лемма V.1]</span>
{: .courier #lem-V-1}

Каждое $\sigma\_{r}$ — непрерывная сюръекция; не инъекция: $\sigma\_{r}^{-1}(\eta) \cong (\partial\mathbb{H})^{2}$.

***<span class="accent">Доказательство</span>***.

$\Phi^{-1}$ — гомеоморфизм, $p\_{r}$ — непрерывная сюръекция. Неинъективность: $p\_{r}$ склеивает квадрат $(\partial\mathbb{H})^{2}$ в точку. $\square$

#### <span class="accent">— [Лемма V.2]</span>
{: .courier #lem-V-2}

(а) $\sigma\_{r}(\mathbf{1}\_{\infty}) = \mathbf{1}\_{\infty}$ для $r = 1,2,3$.

(б) $\sigma\_{r}(\mathbf{0}\_{\infty}) = \mathbf{0}\_{\infty}$ для $r = 1,2,3$.

***<span class="accent">Доказательство</span>***.

(1) $\Phi\_{brunn}(\mathbf{1},\mathbf{1},\mathbf{1}) = \mathbf{1}$.

(2) $\Phi\_{brunn}(\mathbf{0},\mathbf{0},\mathbf{0}) = \mathbf{0}$. $\square$

#### <span class="accent">— [Лемма V.3]</span>
{: .courier #lem-V-3}

(а) $\sigma\_{r}(K\_{coll}) = \partial\mathbb{H}\_{brunn}$ (в частности, $\mathbf{1}\_{\infty} \in \sigma\_{r}(K\_{coll})$).

(б) $\sigma\_{r}^{-1}(\mathbf{1}\_{\infty}) = \Phi\_{brunn}(\{(\eta\_{1}, \eta\_{2}, \eta\_{3}) \in (\partial\mathbb{H})^{3} : \eta\_{r} = \mathbf{1}\_{\infty}\})$ — $r$-я грань куба $(\partial\mathbb{H})^{3}$.

***<span class="accent">Доказательство</span>***.

(1) Для $\eta \in \partial\mathbb{H}\_{brunn}$ положим $\pi := \Phi\_{brunn}(\eta, \mathbf{0}\_{\infty}, \mathbf{0}\_{\infty})$. На слое 0: $\pi^{(0)} = \eta^{(0)} \cdot 0 \cdot 0 = 0 \neq 1$, значит $\pi \neq \mathbf{1}\_{\infty}$, т.е. $\pi \in K\_{coll}$; $\sigma\_{1}(\pi) = \eta$.

(2) Значит $\sigma\_{1}(K\_{coll}) = \partial\mathbb{H}\_{brunn}$. Аналогично для $r = 2, 3$: $\pi := \Phi\_{brunn}(\mathbf{0}\_{\infty}, \eta, \mathbf{0}\_{\infty})$ для $r=2$; $\pi := \Phi\_{brunn}(\mathbf{0}\_{\infty}, \mathbf{0}\_{\infty}, \eta)$ для $r=3$.

(3) По биективности $\Phi$: $\sigma\_{r}(\pi) = \mathbf{1}\_{\infty}$ $\iff$ $p\_{r}(\Phi^{-1}(\pi)) = \mathbf{1}\_{\infty}$ $\iff$ $r$-я координата $\Phi^{-1}(\pi)$ равна $\mathbf{1}\_{\infty}$. $\square$

#### <span class="accent">— [Следствие V.1]</span>
{: .courier #cor-V-1}

$\{\mathbf{1}\_{\infty}\}$ инвариантно вперёд, но не назад. $K\_{coll}$ не инвариантно ни вперёд ($\sigma\_{r}(K\_{coll}) = \partial\mathbb{H}\_{brunn}$), ни в смысле $\sigma\_{r}^{-1}$ ($\sigma\_{r}^{-1}(\mathbf{1}\_{\infty}) \cap K\_{coll} \neq \varnothing$).

***<span class="accent">Доказательство</span>***. Непосредственно [\[Лемма V.2\]](#lem-V-2) и [\[Лемма V.3\]](#lem-V-3). $\square$

#### <span class="accent">— [Теорема V.1]</span>
{: .courier #thm-V-1}

В ZF без AC: $\partial\mathbb{H}\_{core} \cong 2^{\omega}$; $K\_{coll} \cong 2^{\omega}$.

***<span class="accent">Доказательство</span>***.

Оба — непустые, компактные, метризуемые, нульмерные, совершенные (для $K\_{coll}$ — Лемма V.4 ниже). Характеризация Брауэра (нульмерный совершенный метризуемый компакт $\cong 2^{\omega}$) доказуема в ZF: метрика и счётная база заданы в [Разделе IV](#prt-IV). $\square$

#### <span class="accent">— [Лемма V.4]</span>
{: .courier #lem-V-4}

$K\_{coll}$ не имеет изолированных точек.

***<span class="accent">Доказательство</span>***.

(1) Пусть $\pi \in K\_{coll}$ изолирована в $K\_{coll}$. Тогда существует $V \subseteq \partial\mathbb{H}\_{brunn}$ открытое с $V \cap K\_{coll} = \{\pi\}$, значит $V \subseteq \{\pi, \mathbf{1}\_{\infty}\}$ (поскольку $\partial\mathbb{H}\_{brunn} = K\_{coll} \sqcup \{\mathbf{1}\_{\infty}\}$). Если $V = \{\pi\}$, то $\pi$ изолирована в $\partial\mathbb{H}\_{brunn}$ — противоречие с [\[Следствием IV.2\]](#cor-IV-2).

(2) Если $V = \{\pi, \mathbf{1}\_{\infty}\}$, то $\{\mathbf{1}\_{\infty}\}$ открыто (изолированная точка [\[Следствие IV.2\]](#cor-IV-2)), следовательно $\{\pi\} = V \setminus \{\mathbf{1}\_{\infty}\}$ открыто как разность открытых, значит $\pi$ изолирована в $\partial\mathbb{H}\_{brunn}$ — противоречие с [\[Следствие IV.2\]](#cor-IV-2). $\square$

#### <span class="accent">— [Теорема V.2]</span>
{: .courier #thm-V-2}

Имеет место топологическое разложение $\partial\mathbb{H}\_{brunn} = \{\mathbf{1}\_{\infty}\} \sqcup K\_{coll}$, где $\{\mathbf{1}\_{\infty}\}$ — clopen синглтон, $K\_{coll} \cong 2^{\omega}$. При этом:

(а) $\{\mathbf{1}\_{\infty}\}$ инвариантно вперёд: $\sigma\_{r}(\mathbf{1}\_{\infty}) = \mathbf{1}\_{\infty}$.

(б) $\sigma\_{r}^{-1}(\mathbf{1}\_{\infty})$ — континуальное множество, пересекающее $K\_{coll}$.

(в) $K\_{coll}$ не инвариантно; $\sigma\_{r}(K\_{coll}) = \partial\mathbb{H}\_{brunn}$.

(г) На уровне прямого гомеоморфизма: $\Phi\_{brunn}(K\_{coll}^{3}) \subsetneq K\_{coll}$.

***<span class="accent">Доказательство</span>***.

(1) Топологическое разложение — [Раздел IV](#prt-IV); для (а) — [\[Лемма V.2\]](#lem-V-2); для (б), (в) — [\[Лемма V.3\]](#lem-V-3).

(2) Если $a,b,c \in K\_{coll}$ (все $\neq \mathbf{1}\_{\infty}$), то каждый не содержит атом $e\_{\mathbf{1}}$ (иначе был бы главным ультрафильтром $=\mathbf{1}\_{\infty}$), значит $a^{(0)} = b^{(0)} = c^{(0)} = \mathbf{0}$, и $\Phi\_{brunn}(a,b,c)^{(0)} = 0 \cdot 0 \cdot 0 = 0$, т.е. $\Phi\_{brunn}(a,b,c) \neq \mathbf{1}\_{\infty}$, значит в $K\_{coll}$.

(3) Строгость: $\Phi\_{brunn}(\mathbf{1}\_{\infty}, \mathbf{1}\_{\infty}, \mathbf{0}\_{\infty}) \in K\_{coll}$ (так как на слое 0: $1 \cdot 1 \cdot 0 = 0$), но $(\mathbf{1}\_{\infty},\mathbf{1}\_{\infty},\mathbf{0}\_{\infty}) \notin K\_{coll}^{3}$. $\square$

---

#### <span class="accent">— [Интуитивное описание V]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

С $\partial\mathbb{H}\_{core}$, $\partial\mathbb{H}\_{brunn}$ ([Раздел IV](#prt-IV)). Они компактны, мощность $2^{\aleph\_{0}}$. Формализм не запрещает ввести динамику через $\mathrm{Spec}(\omega)$.

**2. <span class="accent">Какие шаги выполнили</span>?**

(1) Определили $\Phi\_{core}$, $\Phi\_{brunn}$, $\sigma\_{r}$.

(2) Доказали: сюръекции, не инъекции [\[Лемма V.1\]](#lem-V-1); неподвижные точки $\mathbf{1}\_{\infty}, \mathbf{0}\_{\infty}$ [\[Лемма V.2\]](#lem-V-2); неинвариантность $K\_{coll}$ [\[Лемма V.3\]](#lem-V-3); асимметрия [\[Следствие V.1\]](#cor-V-1); характеризация Брауэра [\[Теорема V.1\]](#thm-V-1); совершенность $K\_{coll}$ [\[Лемма V.4\]](#lem-V-4); разложение и динамическая асимметрия [\[Теорема V.2\]](#thm-V-2).

**3. <span class="accent">К чему пришли</span>?**

$\partial\mathbb{H}\_{core} \cong 2^{\omega}$, $\partial\mathbb{H}\_{brunn} = \{\mathbf{1}\_{\infty}\} \sqcup K\_{coll}$ с $K\_{coll} \cong 2^{\omega}$. Три сдвига $\sigma\_{r}$ — сюръекции, не инъекции. $\mathbf{1}\_{\infty}, \mathbf{0}\_{\infty}$ неподвижны. Динамическая асимметрия: $\{\mathbf{1}\_{\infty}\}$ инвариантно вперёд, но не назад; $\sigma\_{r}(K\_{coll}) = \partial\mathbb{H}\_{brunn}$.

**4. <span class="accent">Что это значит сейчас</span>?**

Несчётность из IV стала динамической: континуум нитей, континуум орбит.

---

### **Раздел VI. Фрактал**
{: .accent #prt-VI}

#### <span class="accent">— [Определение VI.1]</span>
{: .courier #def-VI-1}

Сигнатура $\mathcal{G} = (\Sigma, \mathcal{F})$ из [Раздела I](#prt-I) задаёт тернарную подстановку постоянной длины $\theta: \Sigma \to \Sigma^{3}$ по правилу $\theta(i) = j\_{i}k\_{i}l\_{i}$:

$$
\theta(1) = 234,\quad \theta(2) = 135,\quad \theta(3) = 126,\quad \theta(4) = 561,\quad \theta(5) = 462,\quad \theta(6) = 453.
$$

Матрица инцидентности $M \in \mathbb{N}^{6 \times 6}$: $M\_{ij} = 1$ при $j \in \{j\_{i}, k\_{i}, l\_{i}\}$, $0$ иначе. Сумма каждой строки и каждого столбца $M$ равна $3$ (каждый сорт входит в три триплета, каждый триплет содержит три сорта); значит $M$ примитивна ($M^{3} > 0$), $\lambda\_{PF}(M) = 3$, правый и левый векторы Перрона–Фробениуса равны $\mathbf{1} = (1,\dots,1)^{T}$.

#### <span class="accent">— [Замечание VI.1]</span>
{: .courier #rem-VI-1}

Два уровня необходимо различать.

(а) Типовой подстановочный подшифт $(X\_{\theta}, S)$: пространство последовательностей $X\_{\theta} \subseteq \Sigma^{\mathbb{N}}$, порождённое $\theta$, с односторонним сдвигом $S$. По теореме Мосье сложность $p(n)$ растёт линейно, откуда $h\_{top}(S\vert{}\_{X\_{\theta}}) = 0$; система строго эргодична с равномерными частотами $1/6$. Число $\log 3 = \log \lambda\_{PF}(M)$ характеризует скорость роста длины $\vert{}\theta^{k}(i)\vert{} = 3^{k}$, не энтропию.

(б) Спектральная динамика $(\partial\mathbb{H}, \sigma\_{r})$: пространство булевых оценок на координатной сетке. Мощность слоёв растёт сверхэкспоненциально ($2^{6\cdot 3^{k}}$ для $\partial\mathbb{H}\_{core}$, $2^{2^{3^{k}}}$ для $\partial\mathbb{H}\_{brunn}$).

#### <span class="accent">— [Лемма VI.1]</span>
{: .courier #lem-VI-1}

В $\mathbf{BoolAlg}$ канонический морфизм $\omega\_{core}: \mathbb{H}\_{core} \to F(\mathbb{H}\_{core})$ — строгий изоморфизм (аналогично $\omega\_{brunn}$), а $\Phi\_{core} = \mathrm{Spec}(\omega\_{core})$ — гомеоморфизм. Для любого $n \geq 1$ прообраз $\sigma\_{r}^{-n}(\mathcal{U}\_{0})$ базового clopen-разбиения уровня $0$ совпадает с разбиением $\mathcal{U}\_{n}$, индуцированным $r^{n}$-й координатной компонентой слоя $\mathcal{L}\_{n}$.

***<span class="accent">Доказательство</span>***.

Сдвинутая подцепь $\varinjlim\_{k \geq 1} \mathcal{L}\_{k}$ конфинальна исходной $\varinjlim\_{k \geq 0} \mathcal{L}\_{k} = \mathbb{H}\_{core}$; копредел по конфинальной подкатегории совпадает с копределом по исходной, откуда $\mathbb{H}\_{core} \cong \varinjlim\_{k \geq 1} \mathcal{L}\_{k} = \varinjlim\_{k \geq 0} F(\mathcal{L}\_{k})$. Так как $F(X) = X^{\otimes 3}$ сохраняет фильтрованные копределы [\[Определение III.1\]](#def-III-1)), канонический морфизм $\varinjlim F(\mathcal{L}\_{k}) \xrightarrow{\sim} F(\mathbb{H}\_{core})$ — изоморфизм; композиция даёт $\omega\_{core}$. На конечных слоях $\Phi^{-1}$ индуцируется каноническими биекциями $\mathrm{Spec}(\mathcal{L}\_{k+1}) = \mathrm{Spec}(\mathcal{L}\_{k}^{\otimes 3}) \xrightarrow{\sim} (\mathrm{Spec}(\mathcal{L}\_{k}))^{3}$, поэтому $n$-кратное применение $p\_{r} \circ \Phi^{-1}$ переводит ограничения уровня $0$ в ограничения на $r^{n}$-м множителе слоя $\mathcal{L}\_{n}$. $\square$

#### <span class="accent">— [Определение VI.2]</span>
{: .courier #def-VI-2}

На $\partial\mathbb{H} \in \{\partial\mathbb{H}\_{core}, \partial\mathbb{H}\_{brunn}\}$: экспоненциальная фильтрационная ультраметрика $d(\pi\_{1}, \pi\_{2}) := 2^{-k(\pi\_{1}, \pi\_{2})}$ при $\pi\_{1} \neq \pi\_{2}$, $d(\pi, \pi) := 0$, где $k(\pi\_{1}, \pi\_{2}) := \min\{k \in \mathbb{N} : \pi\_{1}^{(k)} \neq \pi\_{2}^{(k)}\}$; послойно-нормированная ультраметрика $d\_{norm}(\pi\_{1}, \pi\_{2}) := \vert\mathrm{Spec}(\mathcal{L}\_{k(\pi\_{1}, \pi\_{2})})\vert^{-1}$ при $\pi\_{1} \neq \pi\_{2}$, $d\_{norm}(\pi, \pi) := 0$. Обе совместимы с топологией Стоуна и заданы конструктивно в ZF.

#### <span class="accent">— [Теорема VI.1]</span>
{: .courier #thm-VI-1}

Для каждого $r \in \{1,2,3\}$: $h\_{top}(\sigma\_{r}\vert{}\_{\partial\mathbb{H}\_{core}}) = h\_{top}(\sigma\_{r}\vert{}\_{\partial\mathbb{H}\_{brunn}}) = +\infty$.

***<span class="accent">Доказательство</span>***.

Пусть $\mathcal{U}\_{0}$ — конечное clopen-разбиение уровня $0$. По [Лемме VI.1](#lem-VI-1) измельчение $\mathcal{U}\_{0} \vee \sigma\_{r}^{-1}\mathcal{U}\_{0} \vee \cdots \vee \sigma\_{r}^{-(n-1)}\mathcal{U}\_{0}$ разделяет все компоненты слоя $\mathcal{L}\_{n-1}$. Для $\partial\mathbb{H}\_{core}$ число непустых элементов измельчения $\geq \vert\mathrm{Spec}(\mathcal{L}\_{n-1})\vert = 2^{6 \cdot 3^{n-1}}$, откуда $h\_{top}(\sigma\_{r}\vert{}\_{\partial\mathbb{H}\_{core}}) \geq \lim\_{n \to \infty} \frac{1}{n}\log(2^{6\cdot 3^{n-1}}) = +\infty$. Аналогично для $\partial\mathbb{H}\_{brunn}$: $\vert\mathrm{Spec}(\mathcal{L}\_{n-1}^{brunn})\vert = 2^{2^{3^{n-1}}}$, и $\lim\_{n \to \infty} \frac{2^{3^{n-1}}\log 2}{n} = +\infty$. $\square$

#### <span class="accent">— [Теорема VI.2]</span>
{: .courier #thm-VI-2}

В ультраметрике $d = 2^{-k}$: $\dim\_{H}(\partial\mathbb{H}\_{core}, d) = \dim\_{H}(K\_{coll}, d) = +\infty$. В $d\_{norm}$: $\dim\_{H}(\partial\mathbb{H}\_{core}, d\_{norm}) = \dim\_{H}(K\_{coll}, d\_{norm}) = 1$.

***<span class="accent">Доказательство</span>***.

При $d = 2^{-k}$: $N\_{k} = \vert\mathrm{Spec}(\mathcal{L}\_{k})\vert = 2^{6\cdot 3^{k}}$, $\varepsilon\_{k} = 2^{-k}$, откуда $\dim\_{H}(\partial\mathbb{H}\_{core}, d) = \lim\_{k} \frac{6\cdot 3^{k}\log 2}{k\log 2} = +\infty$. Для $K\_{coll}$: $N\_{k} = 2^{2^{3^{k}}} - 1$, $\dim\_{H} = +\infty$. При $d\_{norm}$: $\varepsilon\_{k} = N\_{k}^{-1}$, $\dim\_{H} = \lim\_{k} \frac{\log N\_{k}}{\log N\_{k}} = 1$. $\square$

#### <span class="accent">— [Теорема VI.3]</span>
{: .courier #thm-VI-3}

(а) $\partial\mathbb{H}\_{core} = V\_{0} \sqcup V\_{+}$, где $V\_{0} := \{\pi : \pi^{(0)} = \mathbf{0}\}$, $V\_{+} := \{\pi : \pi^{(0)} \neq \mathbf{0}\}$ — непустые clopen.

(б) $V\_{+}$ инвариантно вперёд относительно всех трёх сдвигов ($\sigma\_{r}(V\_{+}) \subseteq V\_{+}$), причём для $r \in \{1, 2\}$ включение строгое, а для $r = 3$ — равенство ($\sigma\_{3}(V\_{+}) = V\_{+}$). $V\_{0}$ отображается на всё пространство: $\sigma\_{r}(V\_{0}) = \partial\mathbb{H}\_{core}$.

(в) Ни $(\partial\mathbb{H}\_{core}, \sigma\_{r})$, ни $(\partial\mathbb{H}\_{brunn}, \sigma\_{r})$ не являются топологически транзитивными и не обладают свойством топологического перемешивания.

***<span class="accent">Доказательство</span>***.

(1) Очевидно из дискретности слоя $0$.

(2) Если $\pi \in V\_{+}$, то $T(\pi\_{1}^{(0)}, \pi\_{2}^{(0)}, \pi\_{3}^{(0)}) = \pi^{(0)} \neq \mathbf{0}$, откуда $\pi\_{r}^{(0)} \neq \mathbf{0}$ для всех $r$, т.е. $\sigma\_{r}(\pi) \in V\_{+}$. Для $r=1$ множество $\{j\_{i}\} = \{1,2,4,5\}$ не содержит $6$; если $\eta \in V\_{+}$ с $\eta^{(0)} = e\_{6}$, то $T(e\_{6}, v^{2}, v^{3}) = \mathbf{0}$ для любых $v^{2}, v^{3}$ (так как $(e\_{6})\_{j\_{i}} = 0$), значит $\sigma\_{1}^{-1}(\eta) \subseteq V\_{0}$, т.е. $\eta \notin \sigma\_{1}(V\_{+})$ — строгое включение. Для $r=2$: $\{k\_{i}\} = \{2,3,5,6\}$ не содержит $1$; если $\eta^{(0)} = e\_{1}$, то $T(v^{1}, e\_{1}, v^{3}) = \mathbf{0}$, значит $\eta \notin \sigma\_{2}(V\_{+})$ — строгое включение. Для $r=3$: $i \mapsto l\_{i}$ — биекция $\{4,5,6,1,2,3\}$; для любого $\eta \in V\_{+}$ точка $\pi := \Phi\_{core}(\mathbf{1}\_{\infty}, \mathbf{1}\_{\infty}, \eta)$ имеет $\pi^{(0)}\_{i} = \eta^{(0)}\_{l\_{i}}$, и так как $l$ — биекция и $\eta^{(0)} \neq \mathbf{0}$, $\pi^{(0)} \neq \mathbf{0}$, т.е. $\pi \in V\_{+}$, и $\sigma\_{3}(\pi) = \eta$ — равенство. Для $V\_{0}$: при $\pi = \Phi\_{core}(\eta, \mathbf{0}\_{\infty}, \mathbf{0}\_{\infty})$ имеем $\sigma\_{1}(\pi) = \eta$ (аналогично для $r=2,3$).

(3) В силу $\sigma\_{r}^{n}(V\_{+}) \subseteq V\_{+}$ и $V\_{0} \cap V\_{+} = \varnothing$ имеем $V\_{+} \cap \sigma\_{r}^{-n}(V\_{0}) = \varnothing$ для всех $n \geq 0$; для $\partial\mathbb{H}\_{brunn}$ — $\{\mathbf{1}\_{\infty}\} \cap \sigma\_{r}^{-n}(K\_{coll}) = \varnothing$ [\[Теорема V.2\]](#thm-V-2)). $\square$

#### <span class="accent">— [Замечание VI.2]</span>
{: .courier #rem-VI-2}

Динамическая асимметрия $\partial\mathbb{H}\_{core} = V\_{0} \sqcup V\_{+}$ структурно аналогична разложению $\partial\mathbb{H}\_{brunn} = \{\mathbf{1}\_{\infty}\} \sqcup K\_{coll}$, но не тождественна: в $\partial\mathbb{H}\_{brunn}$ инвариантное вперёд ядро $\{\mathbf{1}\_{\infty}\}$ — одна изолированная точка, тогда как в $\partial\mathbb{H}\_{core}$ ядро $V\_{+}$ — несчётное clopen, строго вложенное в себя под действием $\sigma\_{1}, \sigma\_{2}$.

#### <span class="accent">— [Лемма VI.2]</span>
{: .courier #lem-VI-2}

(а) В $\partial\mathbb{H}\_{brunn}$ множество общих неподвижных точек $\sigma\_{1}, \sigma\_{2}, \sigma\_{3}$ плотно.

(б) В $\partial\mathbb{H}\_{core}$ точки $\mathbf{0}\_{\infty} \in V\_{0}$, $\mathbf{1}\_{\infty} \in V\_{+}$ — общие неподвижные точки всех $\sigma\_{r}$, но множество неподвижных не плотно.

***<span class="accent">Доказательство</span>***.

(1) Любое непустое базовое clopen $U \subseteq \partial\mathbb{H}\_{brunn}$ задаётся фиксацией $u^{(k)} \in \{0,1\}^{3^{k}}$ на уровне $k$. В силу идемпотентности $a \cdot a \cdot a = a^{3} = a$ в $\mathbb{F}\_{2}$, тройка $(u^{(k)}, u^{(k)}, u^{(k)})$ проектируется в $u^{(k)}$ при $(\alpha\_{k}')^{\*}$. Рекурсивно для всех $m \geq k$ получаем $\pi \in U$, для которой $\Phi\_{brunn}^{-1}(\pi) = (\pi, \pi, \pi)$, откуда $\sigma\_{r}(\pi) = p\_{r}(\Phi^{-1}(\pi)) = p\_{r}(\pi,\pi,\pi) = \pi$ для всех $r$.

(2) Для $\mathbf{0}\_{\infty}, \mathbf{1}\_{\infty}$ неподвижность следует из $T(\mathbf{0}, \mathbf{0}, \mathbf{0}) = \mathbf{0}$, $T(\mathbf{1}, \mathbf{1}, \mathbf{1}) = \mathbf{1}$. Clopen $\{\pi \in \partial\mathbb{H}\_{core} : \pi^{(0)} = e\_{1}\}$ не содержит неподвижных точек $\sigma\_{1}$: если $\sigma\_{1}(\pi) = \pi$ и $\pi^{(0)} = e\_{1}$, то $\pi\_{1}^{(0)} = e\_{1}$ (так как $\sigma\_{1}(\pi)^{(0)} = p\_{1}(\Phi^{-1}(\pi))^{(0)} = \pi\_{1}^{(0)}$), и $T(e\_{1}, \pi\_{2}^{(0)}, \pi\_{3}^{(0)}) = \pi^{(0)} = e\_{1}$; но $T(e\_{1}, v^{2}, v^{3})\_{1} = (e\_{1})\_{j\_{1}} \cdot (v^{2})\_{k\_{1}} \cdot (v^{3})\_{l\_{1}} = (e\_{1})\_{2} \cdot \ldots = 0 \neq 1 = (e\_{1})\_{1}$ — противоречие. Значит $\pi\_{1}^{(0)} \neq e\_{1}$, т.е. $\sigma\_{1}(\pi)^{(0)} \neq \pi^{(0)}$ — не неподвижна. $\square$

#### <span class="accent">— [Замечание VI.3]</span>
{: .courier #rem-VI-3}

Границы [Раздела VI](#prt-VI):

(а) Классификация периодических орбит произвольных периодов $p \geq 2$ в $\partial\mathbb{H}\_{core}$ не проводится.

(б) Инвариантная мера на $\partial\mathbb{H}$, согласованная с проекциями $\alpha\_{k}^{\*}$, не строится (равномерная мера не согласована, так как слои $\alpha\_{k}^{\*}$ непостоянны).

(в) Аттракторные свойства в смысле сходимости орбит не устанавливаются.

---

#### <span class="accent">— [Интуитивное описание VI]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

С $\partial\mathbb{H}\_{core}$, $\partial\mathbb{H}\_{brunn}$ с динамикой $\sigma\_{r}$ ([Раздел V](#prt-V)). Формализм не запрещает ввести метрику, энтропию, матрицу подстановки.

**2. <span class="accent">Какие шаги выполнили</span>?**

(1) Ввели подстановку $\theta$ и матрицу $M$ [\[Определение VI.1\]](#def-VI-1); разделили уровни (типовая сетка vs. спектр) [\[Замечание VI.0\]](#rem-VI-0); доказали изоморфизм $\omega\_{core}$ и сдвиг уровней [\[Лемма VI.1\]](#lem-VI-1); определили ультраметрики [\[Определение VI.2\]](#def-VI-2);

(2) доказали $h\_{top}(\sigma\_{r}) = +\infty$ [\[Теорема VI.1\]](#thm-VI-1); вычислили $\dim\_{H}$ [\[Теорема VI.2\]](#thm-VI-2); доказали no-mixing и расщепление $V\_{0} \sqcup V\_{+}$ [\[Теорема VI.3\]](#thm-VI-3); плотность/неплотность неподвижных [\[Лемма VI.2\]](#lem-VI-2).

**3. <span class="accent">К чему пришли</span>?**

$h\_{top}(\sigma\_{r}) = +\infty$ на обоих пространствах; $\dim\_{H} = +\infty$ при $d = 2^{-k}$, $\dim\_{H} = 1$ при $d\_{norm}$; $\partial\mathbb{H}\_{core} = V\_{0} \sqcup V\_{+}$ с $V\_{+}$ инвариантным вперёд (строго для $r=1,2$; сюръекция для $r=3$); $\sigma\_{r}(V\_{0}) = \partial\mathbb{H}\_{core}$; no-mixing; неподвижные точки плотны в $\partial\mathbb{H}\_{brunn}$, не плотны в $\partial\mathbb{H}\_{core}$.

**4. <span class="accent">Что это значит сейчас</span>?**

Получили динамическую структуру на контуральных спектрах: бесконечная энтропия, бесконечная размерность (при $d=2^{-k}$), инвариантное расщепление с асимметрией.

---
