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

Пусть $\Sigma = \{1,2,3,4,5,6\}$ — конечный алфавит сортов в ZF.

#### <span class="accent">— [Определение I.2]</span>
{: .courier #def-I-2}

Пусть $\mathcal{G} = (\Sigma,\mathcal{F})$ — полиадическая сигнатура, где $\mathcal{F}$ — множество из шести генераторов (1-ячеек). Каждый генератор имеет профиль сортов $\alpha\_{i}: i \to j\_{i} \otimes k\_{i} \otimes l\_{i}$, $i, j\_{i}, k\_{i}, l\_{i} \in \Sigma$, где индексы $j\_{i}, k\_{i}, l\_{i}$ зависят от $i$ согласно таблице:

$$
\mathcal{F} = \{\, 1 \xrightarrow{\alpha_{1}} 2\otimes 3\otimes 4,\quad 2 \xrightarrow{\alpha_{2}} 1\otimes 3\otimes 5,\quad 3 \xrightarrow{\alpha_{3}} 1\otimes 2\otimes 6,\quad 4 \xrightarrow{\alpha_{4}} 5\otimes 6\otimes 1,\quad 5 \xrightarrow{\alpha_{5}} 4\otimes 6\otimes 2,\quad 6 \xrightarrow{\alpha_{6}} 4\otimes 5\otimes 3 \,\}
$$

#### <span class="accent">— [Определение I.3]</span>
{: .courier #def-I-3}

Оператор искусственной инициализации $\mathcal{I}\_{art}$ сопоставляет сигнатуре $\mathcal{G}$ свободный $\Sigma$-цветной PROP $\mathbf{C} = \mathrm{FreePROP}\_{\Sigma}(\mathcal{G})$, порождённый сигнатурой $\mathcal{G}$. Инициализация является исключительно синтаксической: соотношения (равенства морфизмов) на шаге I не задаются.

#### <span class="accent">— [Лемма I.1]</span>
{: .courier #lem-I-1}

Объекты (0-ячейки) $\mathbf{C}$ образуют свободный моноид $\Sigma^{\*}$ над $\Sigma$. В частности, $2\otimes 3\otimes 4$ и $3\otimes 2\otimes 4$ — различные 0-ячейки.

***<span class="accent">Доказательство</span>***.

По построению свободного цветного PROP объекты порождаются $\Sigma$ и моноидальным произведением $\otimes$ без соотношений. Следовательно, объекты — слова над $\Sigma$, а различные слова — различные объекты. $\square$

#### <span class="accent">— [Лемма I.2]</span>
{: .courier #lem-I-2}

Симметричная моноидальная структура $\mathbf{C}$ предоставляет канонические 1-ячейки симметрии $\sigma\_{i,j}: i \otimes j \to j \otimes i$, посредством которых переставленные множители канонически изоморфны.

***<span class="accent">Доказательство</span>***.

В свободном симметричном моноидальном PROP симметрии $\sigma\_{i,j}$ входят в число образующих 1-ячеек (по определению симметричной моноидальной структуры). Они каноничны и не зависят от выбора. $\square$

#### <span class="accent">— [Замечание I.1]</span>
{: .courier #rem-I-1}

Конкретный порядок множителей в кодомене $\alpha\_{i}$ — часть выбранной презентации $\mathcal{F}$. Симметрии $\sigma$ дают канонические изоморфизмы между разными порядками, но $\sigma \circ \alpha\_{i} \neq \alpha\_{i}$: перестановка меняет сам морфизм. Разные порядки дают канонически изоморфные PROP, но не равные морфизмы. Порядок — часть выбора презентации, не канонический инвариант.

#### <span class="accent">— [Замечание I.2]</span>
{: .courier #rem-I-2}

Граф инцидентности сигнатуры $\mathcal{F}$ (рёбра $i$–$j$ при $j \in \{j\_{i}, k\_{i}, l\_{i}\}$) — треугольная призма: два треугольника $\{1,2,3\}$ и $\{4,5,6\}$, три перекладины $(1,4)$, $(2,5)$, $(3,6)$.

***<span class="accent">Доказательство</span>***.

Прямая выписка: внутри $\{1,2,3\}$ все три ребра присутствуют ($1\to 2,3$; $2\to 1,3$; $3\to 1,2$); внутри $\{4,5,6\}$ все три ребра присутствуют ($4\to 5,6$; $5\to 4,6$; $6\to 4,5$); между основаниями — только $(1,4), (2,5), (3,6)$. $\square$

#### <span class="accent">— [Теорема I.1]</span>
{: .courier #thm-I-1}

$\mathbf{C}$ является инициальным объектом в категории $\mathcal{G}$-размеченных $\Sigma$-цветных PROP с морфизмами, сохраняющими разметку: для любого $\mathcal{G}$-размеченного $\Sigma$-цветного PROP $\mathbf{D}$ (то есть $\mathbf{D}$ с фиксированным семейством генераторов $\{\alpha\_{i}'\}\_{i \in \Sigma}$ того же профиля, что у $\alpha\_{i}$) существует единственный цветосохраняющий морфизм $\mathbf{C} \to \mathbf{D}$, отправляющий $\alpha\_{i} \mapsto \alpha\_{i}'$.

***<span class="accent">Доказательство</span>***.

По универсальному свойству свободного PROP: для любого отображения образующих 1-ячеек $\alpha\_{i} \mapsto \alpha\_{i}'$, сохраняющего профили сортов, существует единственное продолжение до морфизма цветных PROP. Единственность следует из того, что $\mathbf{C}$ порождён $\mathcal{F}$ как PROP; существование — из того, что $\mathbf{D}$ снабжён разметкой (генераторами того же профиля). $\square$

#### <span class="accent">— [Следствие I.1]</span>
{: .courier #cor-I-1}

$\mathbf{C}$ — свободный синтаксический PROP. Его модели в произвольной симметричной моноидальной категории $\mathbf{V}$ — симметричные моноидальные функторы $\mathbf{C} \to \mathbf{V}$. На данном этапе ни $\mathbf{V}$, ни конкретный функтор не зафиксированы.

***<span class="accent">Доказательство</span>***.

Соотношения не задаются [\[Определение I.3\]](#def-I-3); $\mathbf{C}$ инициальный в категории $\mathcal{G}$-размеченных PROP [\[Теорема I.1\]](#thm-I-1), но универсальное свойство не фиксирует целевую категорию $\mathbf{V}$. Следовательно, ни модель $\mathbf{C} \to \mathbf{V}$, ни $\mathbf{V}$ не входят в определение $\mathbf{C}$. $\square$

---

#### <span class="accent">— [Интуитивное описание I]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

Начали с чистого синтаксиса: конечный алфавит $\Sigma$ и шесть генераторов $\alpha\_{i}: i \to j\_{i}\otimes k\_{i}\otimes l\_{i}$. Никакой семантики, никакой модели, никакой категории алгебр. Причина: если начать с семантики, она войдёт в определение $\mathbf{C}$, чего мы избегаем. Формализм не запрещает ввести семантику позже.

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Построили свободный $\Sigma$-цветной PROP $\mathbf{C} = \mathrm{FreePROP}\_{\Sigma}(\mathcal{G})$.

(б) Установили: объекты $\mathbf{C}$ — слова над $\Sigma$ [\[Лемма I.1\]](#lem-I-1); симметрии $\sigma\_{i,j}$ каноничны, порядок множителей — часть презентации [\[Лемма I.2\]](#lem-I-2), [\[Замечание I.1\]](#rem-I-1); $\mathbf{C}$ инициальный в категории $\mathcal{G}$-размеченных $\Sigma$-цветных PROP [\[Теорема I.1\]](#thm-I-1); модели $\mathbf{C}$ в произвольной $\mathbf{V}$ — симметричные моноидальные функторы, ни $\mathbf{V}$, ни функтор не зафиксированы [\[Следствие I.1\]](#cor-I-1).

**3. <span class="accent">К чему пришли</span>?**

Получили чисто синтаксический объект $\mathbf{C}$, который:

(а) Определён конечными данными $(\Sigma,\mathcal{F})$.

(б) Инициалиен в категории $\mathcal{G}$-размеченных PROP.

(в) Не содержит семантики.

(г) Имеет модели в любой SMC $\mathbf{V}$, но конкретная модель не зафиксирована.

**4. <span class="accent">Что это значит сейчас</span>?**

$\mathbf{C}$ не содержит ни булевой алгебры, ни идеала, ни коалгебры, ни топологии, ни динамики. Сейчас $\mathbf{C}$ полон как свободный PROP.

---

### **Раздел II. Брунновость**
{: .accent #prt-II}

#### <span class="accent">— [Определение II.1]</span>
{: .courier #def-II-1}

Семантический функтор $\mathrm{Sem}: \mathbf{C} \to \mathbf{BoolAlg}$ — симметричный моноидальный функтор из свободного $\Sigma$-цветного PROP $\mathbf{C}$ ([Раздел I](#prt-I)) в категорию $\mathbf{BoolAlg}$ коммутативных идемпотентных $\mathbb{F}\_{2}$-алгебр с единицей (тензор $\otimes\_{\mathbb{F}\_{2}}$ — копроизведение в $\mathbf{BoolAlg}$):

(а) На объектах: $\mathrm{Sem}(i) = \mathbb{F}\_{2}[x\_{i}]/(x\_{i}^{2} - x\_{i})$ для $i \in \Sigma$; $\mathrm{Sem}(i\_{1} \otimes \dots \otimes i\_{n}) = \mathrm{Sem}(i\_{1}) \otimes\_{\mathbb{F}\_{2}} \dots \otimes\_{\mathbb{F}\_{2}} \mathrm{Sem}(i\_{n})$;

(б) На морфизмах: $\mathrm{Sem}(\alpha\_{i}): \mathrm{Sem}(i) \to \mathrm{Sem}(j\_{i}) \otimes \mathrm{Sem}(k\_{i}) \otimes \mathrm{Sem}(l\_{i})$ — гомоморфизм $\mathbb{F}\_{2}$-алгебр, заданный $x\_{i} \mapsto x\_{j\_{i}} \otimes x\_{k\_{i}} \otimes x\_{l\_{i}}$.

Корректность: $\mathrm{Sem}(i)$ — свободная $\mathbb{F}\_{2}$-алгебра на одной образующей $x\_{i}$ с $x\_{i}^{2} = x\_{i}$; гомоморфизм из свободной алгебры однозначно определяется значением на образующей.

#### <span class="accent">— [Определение II.2]</span>
{: .courier #def-II-2}

Булево кольцо $B\_{6} := \mathrm{Sem}(1 \otimes 2 \otimes 3 \otimes 4 \otimes 5 \otimes 6) = \mathbb{F}\_{2}[x\_{1},\dots,x\_{6}]/\langle x\_{i}^{2} - x\_{i}\rangle\_{i=1}^{6}$.

Элементы $B\_{6}$ — функции $\mathbb{F}\_{2}^{6} \to \mathbb{F}\_{2}$, то есть $B\_{6} \cong \mathbb{F}\_{2}^{64}$.

#### <span class="accent">— [Определение II.3]</span>
{: .courier #def-II-3}

Идеал ограничений $I \subset B\_{6}$ — идеал, порождённый разностями $\mathrm{Sem}(\alpha\_{i})(x\_{i}) - x\_{i}$ для $i \in \Sigma$ (где $x\_{i}$ в $B\_{6}$ — образующая $i$-го тензорного множителя):

$$
I = \langle x_{1} + x_{2}x_{3}x_{4},\; x_{2} + x_{1}x_{3}x_{5},\; x_{3} + x_{1}x_{2}x_{6},\; x_{4} + x_{5}x_{6}x_{1},\; x_{5} + x_{4}x_{6}x_{2},\; x_{6} + x_{4}x_{5}x_{3} \rangle \subset B_{6}
$$

#### <span class="accent">— [Определение II.4]</span>
{: .courier #def-II-4}

Оператор состояния $T: \mathbb{F}\_{2}^{6} \to \mathbb{F}\_{2}^{6}$, $T(v)\_{i} = v\_{j\_{i}}v\_{k\_{i}}v\_{l\_{i}}$. Тогда $\mathrm{Fix}(T) = \{v \in \mathbb{F}\_{2}^{6} : T(v) = v\} = V(I)$ — точное равенство.

#### <span class="accent">— [Замечание II.1]</span>
{: .courier #rem-II-1}

В кольце $\mathbb{F}\_{2}[x\_{1},\dots,x\_{6}]$ идеал $I$ не радикален: например, $x\_{1} + x\_{2} \in \sqrt{I} \setminus I$ (на $V(I) = \{\mathbf{0}, \mathbf{1}\}$ выполнено $x\_{1} + x\_{2} = 0$, но $x\_{1} + x\_{2} \notin I$). В булевом кольце $B\_{6}$ всякий идеал радикален, поскольку $f^{2} = f$ для любого $f \in B\_{6}$; следовательно, $f^{n} \in I \Rightarrow f \in I$.

#### <span class="accent">— [Теорема II.1]</span>
{: .courier #thm-II-1}

$V(I) = \{\mathbf{0}, \mathbf{1}\}$.

***<span class="accent">Доказательство</span>***.

(1) $\mathbf{1} \in V(I)$: $1 = 1\cdot 1\cdot 1$ во всех шести уравнениях.

(2) Пусть $v \in V(I)$, $v \neq \mathbf{1}$. Покажем $v = \mathbf{0}$. Если существует $s$ с $v\_{s} = 1$, то из $v\_{s} = v\_{j\_{s}}v\_{k\_{s}}v\_{l\_{s}}$ следует $v\_{j\_{s}} = v\_{k\_{s}} = v\_{l\_{s}} = 1$. Индукцией вдоль путей в 3-гиперграфе $\mathcal{G}$ и по его сильной связности (проверяется прямой выпиской достижимости: $1 \to \{2,3,4\}$, $2 \to \{1,3,5\}$, $3 \to \{1,2,6\}$, $4 \to \{5,6,1\}$, $5 \to \{4,6,2\}$, $6 \to \{4,5,3\}$, откуда из любой вершины достижимы все) получаем $v = \mathbf{1}$, противоречие. Значит $v\_{i} = 0$ для всех $i$, т.е. $v = \mathbf{0}$.

(3) $\mathbf{0} \in V(I)$: $0 = 0\cdot 0\cdot 0$. $\square$

#### <span class="accent">— [Замечание II.2]</span>
{: .courier #rem-II-2}

Доказательство [Теоремы II.1](#thm-II-1) использует только сильную связность $\mathcal{G}$ и конъюнктивную форму уравнений. Самоссылки не исключаются. Для конкретной таблицы $\mathcal{F}$ самоссылок нет, но это частное комбинаторное свойство, не необходимое для теоремы.

#### <span class="accent">— [Следствие II.1]</span>
{: .courier #cor-II-1}

В $B\_{6}$:

$$
I = \langle x_{1} + x_{6},\; x_{2} + x_{6},\; x_{3} + x_{6},\; x_{4} + x_{6},\; x_{5} + x_{6} \rangle
$$

***<span class="accent">Доказательство</span>***.

(1) $B\_{6} \cong \mathbb{F}\_{2}^{64}$ (произведение копий $\mathbb{F}\_{2}$ по точкам $\mathbb{F}\_{2}^{6}$).

(2) Всякий идеал в $B\_{6}$ радикален [\[Замечание II.1\]](#rem-II-1); $V(I) = \{\mathbf{0}, \mathbf{1}\}$ [\[Теорема II.1\]](#thm-II-1).

(3) Многочлен $x\_{i} + x\_{6}$ обращается в нуль на обеих точках, по радикальности $I = I(V(I)) = \langle x\_{i} + x\_{6}\rangle\_{i=1}^{5}$. $\square$

#### <span class="accent">— [Определение II.5]</span>
{: .courier #def-II-5}

Комбинаторная 3-сеть — ориентированный 3-гиперграф $\mathcal{H}$ на конечном множестве $\Sigma$ с оператором $T\_{\mathcal{H}}(v)\_{i} = v\_{j\_{i}}v\_{k\_{i}}v\_{l\_{i}}$, удовлетворяющий:

(а) $\mathcal{H}$ сильно связен.

(б) Форма соотношений конъюнктивна: $x\_{i} = x\_{j\_{i}}x\_{k\_{i}}x\_{l\_{i}}$.

Бруннова 3-сеть — комбинаторная 3-сеть, для которой $\mathrm{Fix}(T\_{\mathcal{H}}) = \{\mathbf{0}, \mathbf{1}\}$.

#### <span class="accent">— [Теорема II.2]</span>
{: .courier #thm-II-2}

Сигнатура $\mathcal{G}$ из [Раздела I](#prt-I) является брунновой 3-сетью.

***<span class="accent">Доказательство</span>***.

(1) Сильная связность [\[Теорема II.1\]](#thm-II-1).

(2) Конъюнктивная форма — по построению [\[Определение II.2\]](#def-II-2). (3) $\mathrm{Fix}(T) = \{\mathbf{0}, \mathbf{1}\}$ — [\[Теорема II.1\]](#thm-II-1). $\square$

#### <span class="accent">— [Следствие II.2]</span>
{: .courier #cor-II-2}

Для любого $i \in \Sigma$:

$$
I + \langle x_{i}\rangle = \mathfrak{m} = \langle x_{1},\dots,x_{6}\rangle, \qquad V(I + \langle x_{i}\rangle) = \{\mathbf{0}\}
$$

***<span class="accent">Доказательство</span>***.

(1) $I = \langle x\_{j} + x\_{6}\rangle\_{j=1}^{5}$ в $B\_{6}$ [\[Следствие II.1\]](#cor-II-1).

(2) Если $i \neq 6$: из $x\_{i} = 0$ и $x\_{i} + x\_{6} \in I + \langle x\_{i}\rangle$ следует $x\_{6} = 0$; тогда из $x\_{j} + x\_{6} \in I + \langle x\_{i}\rangle$ следует $x\_{j} = 0$ для $j = 1,\dots,5$.

(3) Если $i = 6$: $x\_{6} = 0$, и $x\_{j} + x\_{6} = x\_{j} = 0$ для $j=1,\dots,5$. (4) В обоих случаях $I + \langle x\_{i}\rangle = \mathfrak{m}$. $\square$

#### <span class="accent">— [Следствие II.3]</span>
{: .courier #cor-II-3}

$$
B_{6}/I \cong \mathbb{F}_{2} \times \mathbb{F}_{2}, \qquad B_{6}/(I + \langle x_{i}\rangle) \cong \mathbb{F}_{2} \quad (i \in \Sigma)
$$

***<span class="accent">Доказательство</span>***.

$V(I) = \{\mathbf{0}, \mathbf{1}\}$ и $B\_{6}$ — произведение копий $\mathbb{F}\_{2}$ по точкам. (2) $B\_{6}/(I + \langle x\_{i}\rangle) \cong \mathbb{F}\_{2}$ [\[Следствие II.2\]](#cor-II-2). $\square$

#### <span class="accent">— [Замечание II.3]</span>
{: .courier #rem-II-3}

Многообразие $V(I + \langle x\_{i}\rangle) = \{\mathbf{0}\}$ — статическое множество общих нулей в смысле алгебраической геометрии, не результат пошагового вычисления.

---

#### <span class="accent">— [Интуитивное описание II]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

Начали с чисто синтаксического $\mathbf{C}$ ([Раздел I](#prt-I)). $\mathbf{C}$ полон как свободный PROP — дефекта нет. Но $\mathbf{C}$ не содержит семантики: ни идемпотентности, ни идеала, ни многообразия. Формализм не запрещает ввести семантизацию — это делается функтором $\mathrm{Sem}$ [\[Определение II.1\]](#def-II-1).

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Задали функтор $\mathrm{Sem}: \mathbf{C} \to \mathbf{BoolAlg}$ [\[Определение II.1\]](#def-II-1).

(б) Определили $B\_{6} = \mathrm{Sem}(1 \otimes \dots \otimes 6)$ [\[Определение II.2\]](#def-II-2) и идеал $I$ [\[Определение II.3\]](#def-II-3); определили $T$ с $\mathrm{Fix}(T) = V(I)$ [\[Определение II.4\]](#def-II-4); установили нерадикальность $I$ в $\mathbb{F}\_{2}[x]$ и радикальность в $B\_{6}$ [\[Замечание II.1\]](#rem-II-1); доказали $V(I) = \{\mathbf{0}, \mathbf{1}\}$ [\[Теорема II.1\]](#thm-II-1).

(в) Вывели $I = \langle x\_{i} + x\_{6}\rangle$ [\[Следствие II.1\]](#cor-II-1); установили брунновость $\mathcal{G}$ [\[Теорема II.2\]](#thm-II-2); коллапс $I + \langle x\_{i}\rangle = \mathfrak{m}$ [\[Следствие II.2\]](#cor-II-2); фактор $B\_{6}/I \cong \mathbb{F}\_{2}\times\mathbb{F}\_{2}$ [\[Следствие II.3\]](#cor-II-3).

**3. <span class="accent">К чему пришли</span>?**

Получили брунновость: $V(I) = \{\mathbf{0}, \mathbf{1}\}$ («всё или ничего»), $I + \langle x\_{i}\rangle = \mathfrak{m}$ (любой нуль стягивает всё), $B\_{6}/I \cong \mathbb{F}\_{2}\times\mathbb{F}\_{2}$ (два атома). Это точная алгебраическая структура.

**4. <span class="accent">Что это значит сейчас</span>?**

Брунновость — фундамент всей дальнейшей цепи: два полюса $\mathbf{0}, \mathbf{1}$, запрет третьего, коллапс при любом нуле. Статика $B\_{6}$ не даёт коалгебры, вводится копредел.

---

### **Раздел III. Рекурсия**
{: .accent #prt-III}

#### <span class="accent">— [Определение III.1]</span>
{: .courier #def-III-1}

Тензорный эндофунктор $F: \mathbf{BoolAlg} \to \mathbf{BoolAlg}$, $F(X) = X \otimes\_{\mathbb{F}\_{2}} X \otimes\_{\mathbb{F}\_{2}} X$. В $\mathbf{BoolAlg}$ тензор есть копроизведение; $F$ сохраняет фильтрованные копределы.

#### <span class="accent">— [Определение III.2]</span>
{: .courier #def-III-2}

Структурное отображение $\alpha: B\_{6} \to F(B\_{6}) = B\_{6}^{\otimes 3}$ — гомоморфизм $\mathbb{F}\_{2}$-алгебр, заданный на образующих $x\_{i} \mapsto x\_{j\_{i}} \otimes x\_{k\_{i}} \otimes x\_{l\_{i}}$.

Корректность: $\alpha(x\_{i}^{2}) = x\_{j\_{i}}^{2} \otimes x\_{k\_{i}}^{2} \otimes x\_{l\_{i}}^{2} = x\_{j\_{i}} \otimes x\_{k\_{i}} \otimes x\_{l\_{i}} = \alpha(x\_{i})$ в силу идемпотентности $x^{2} = x$ в $B\_{6}$; $\alpha$ продолжается до гомоморфизма на $B\_{6}$.

#### <span class="accent">— [Определение III.3]</span>
{: .courier #def-III-3}

Для $A \in \mathbf{BoolAlg}$ и идеала $J \subset A$:

$$
J^{[n]} := \ker(A^{\otimes n} \twoheadrightarrow (A/J)^{\otimes n}) = \sum_{s=1}^{n} A^{\otimes(s-1)} \otimes J \otimes A^{\otimes(n-s)} \subset A^{\otimes n}.
$$

Канонический изоморфизм $A^{\otimes n}/J^{[n]} \cong (A/J)^{\otimes n}$. В частности, $I^{[3]} = I \otimes B\_{6} \otimes B\_{6} + B\_{6} \otimes I \otimes B\_{6} + B\_{6} \otimes B\_{6} \otimes I$.

#### <span class="accent">— [Лемма III.1]</span>
{: .courier #lem-III-1}

$\alpha$ инъективно.

***<span class="accent">Доказательство</span>***.

Кольцо $B\_{6} \cong \mathbb{F}\_{2}^{64}$ — конечное булево (редуцированное, без нильпотентов); элемент $B\_{6}$ однозначно определяется значениями на $\mathbb{F}\_{2}$-точках $\mathrm{Spec}(B\_{6}) = \mathbb{F}\_{2}^{6}$. Следовательно, $\alpha$ инъективно тогда и только тогда, когда $\mathrm{Spec}(\alpha): (\mathbb{F}\_{2}^{6})^{3} \to \mathbb{F}\_{2}^{6}$ сюръективно.

Положим $T(v^{1}, v^{2}, v^{3})\_{i} = v^{1}\_{j\_{i}} v^{2}\_{k\_{i}} v^{3}\_{l\_{i}}$. Для $w \in \mathbb{F}\_{2}^{6}$ с носителем $S = \{i : w\_{i} = 1\}$ зададим: $v^{1}\_{j} = 1 \iff j \in \{j\_{i} : i \in S\}$, $v^{2}\_{k} = 1 \iff k \in \{k\_{i} : i \in S\}$, $v^{3}\_{l} = 1 \iff l \in \{l\_{i} : i \in S\}$.

Проверим $T\_{i} = 1 \iff i \in S$.

($\Rightarrow$) Пусть $i \in S$. По определению $j\_{i} \in \{j\_{i'} : i' \in S\}$ (при $i' = i$), значит $v^{1}\_{j\_{i}} = 1$; аналогично $v^{2}\_{k\_{i}} = 1$, $v^{3}\_{l\_{i}} = 1$. Следовательно $T\_{i} = 1$.

($\Leftarrow$) Пусть $i \notin S$. По таблице $\mathcal{F}$ для каждого $i$ существует координата $c(i) \in \{j, k, l\}$, значение которой у $\alpha\_{i}$ не встречается у $\alpha\_{i'}$ при $i' \neq i$: $c(1) = j$ (значение 2), $c(2) = l$ (5), $c(3) = k$ (2), $c(4) = j$ (5), $c(5) = l$ (2), $c(6) = k$ (5). Так как $i \notin S$, координата $c(i)$ не входит в соответствующее множество (уникальность), значит соответствующая $v$-компонента равна $0$, и $T\_{i} = 0$. $\square$

#### <span class="accent">— [Замечание III.1]</span>
{: .courier #rem-III-1}

***<span class="accent">Доказательство</span>*** использует фиксированную таблицу $\mathcal{F}$ (свидетели). Замена таблицы может нарушить инъективность.

#### <span class="accent">— [Лемма III.2]</span>
{: .courier #lem-III-2}

$\alpha(I) \subset I^{[3]}$.

***<span class="accent">Доказательство</span>***.

В $B\_{6}/I \cong \mathbb{F}\_{2} \times \mathbb{F}\_{2}$ — две точки $\mathbf{0}, \mathbf{1}$; в $(B\_{6}/I)^{\otimes 3}$ — 8 точек. Для $x \in I$ и $u = (u^{1}, u^{2}, u^{3}) \in \{(\mathbf{0},\mathbf{0},\mathbf{0}), \ldots, (\mathbf{1},\mathbf{1},\mathbf{1})\}$: если хотя бы один $u^{k} = \mathbf{0}$, то оба слагаемых $= 0$; если $u^{1} = u^{2} = u^{3} = \mathbf{1}$, то оба $= 1$, сумма $1 + 1 = 0$ в $\mathbb{F}\_{2}$. Во всех 8 случаях $= 0$, значит $\alpha(x\_{i} + x\_{j\_{i}}x\_{k\_{i}}x\_{l\_{i}}) \in \ker(\pi^{\otimes 3}) = I^{[3]}$. $\square$

#### <span class="accent">— [Определение III.4]</span>
{: .courier #def-III-4}

Итерационная цепь: $\mathcal{L}\_{0} = B\_{6}$, $\mathcal{L}\_{k+1} = F(\mathcal{L}\_{k})$, $\alpha\_{k} = F^{k}(\alpha): \mathcal{L}\_{k} \to \mathcal{L}\_{k+1}$. Идеалы: $I\_{0} = I \subset \mathcal{L}\_{0}$; $I\_{k+1} := \ker(\mathcal{L}\_{k+1} \twoheadrightarrow (B\_{6}/I)^{\otimes 3^{k+1}})$. Канонические вложения копредела: $\iota\_{k}: \mathcal{L}\_{k} \to \mathbb{H}\_{core}$, согласованные с $\alpha\_{k}$ ($\iota\_{k+1} \circ \alpha\_{k} = \iota\_{k}$).

#### <span class="accent">— [Лемма III.3]</span>
{: .courier #lem-III-3}

$I\_{k+1} = I\_{k}^{[3]}$ и $\alpha\_{k}(I\_{k}) \subset I\_{k+1}$.

***<span class="accent">Доказательство</span>***.

$\mathcal{L}\_{k+1} = \mathcal{L}\_{k}^{\otimes 3}$ и $(B\_{6}/I)^{\otimes 3^{k+1}} = ((B\_{6}/I)^{\otimes 3^{k}})^{\otimes 3}$ [\[Определение III.4\]](#def-III-4), следовательно $I\_{k+1} = \ker(\mathcal{L}\_{k}^{\otimes 3} \twoheadrightarrow (\mathcal{L}\_{k}/I\_{k})^{\otimes 3}) = I\_{k}^{[3]}$. Индукция: $k = 0$ — [\[Лемма III.2\]](#lem-III-2); $k \Rightarrow k+1$: $\alpha\_{k+1}(I\_{k+1}) = \alpha\_{k}^{\otimes 3}(I\_{k}^{[3]}) = (\alpha\_{k}(I\_{k}))^{[3]} \subset I\_{k+1}^{[3]} = I\_{k+2}$; использовано $\alpha\_{k+1} = \alpha\_{k}^{\otimes 3}$, что следует из $\alpha\_{k} = F^{k}(\alpha)$. $\square$

#### <span class="accent">— [Теорема III.1]</span>
{: .courier #thm-III-1}

В $\mathbf{BoolAlg}$ существуют:

(а) $\mathbb{H}\_{core} = \varinjlim\_{k} \mathcal{L}\_{k}$ с $F$-коалгебраической структурой $\omega\_{core}: \mathbb{H}\_{core} \to F(\mathbb{H}\_{core})$.

(б) Идеал $I\_{\infty} = \varinjlim\_{k} I\_{k} \subset \mathbb{H}\_{core}$, $\alpha\_{\infty}$-инвариантный: $\alpha\_{\infty}(I\_{\infty}) \subset I\_{\infty}^{[3]}$.

(в) Фактор-коалгебра $\mathbb{H}\_{brunn} = \mathbb{H}\_{core}/I\_{\infty}$ с $\omega\_{brunn}$.

***<span class="accent">Доказательство</span>***.

(1) Копредел существует: $\mathbf{BoolAlg}$ кополна (многообразие универсальной алгебры, замкнутое относительно всех малых копределов). $\otimes\_{\mathbb{F}\_{2}}$ — копроизведение в $\mathbf{BoolAlg}$, сохраняет копределы: $F(\mathbb{H}\_{core}) = \varinjlim F(\mathcal{L}\_{k}) = \varinjlim \mathcal{L}\_{k+1} \cong \mathbb{H}\_{core}$; канонический изоморфизм даёт $\omega\_{core}$.

(2) $I\_{\infty}$ — идеал (фильтрованный копредел идеалов). $\alpha\_{\infty}(I\_{\infty}) = \varinjlim \alpha\_{k}(I\_{k}) \subset \varinjlim I\_{k+1} = \varinjlim I\_{k}^{[3]} = (\varinjlim I\_{k})^{[3]} = I\_{\infty}^{[3]}$ (последнее — сохранение копределов тензором: $I\_{k}^{[3]}$ есть сумма $I\_{k} \otimes \mathcal{L}\_{k} \otimes \mathcal{L}\_{k} + \ldots$, копредел суммы — сумма копределов).

(3) По (2) $\alpha\_{\infty}$ пропускается через $\mathbb{H}\_{core}/I\_{\infty}$, давая $\omega\_{brunn}$. $\square$

#### <span class="accent">— [Следствие III.1]</span>
{: .courier #cor-III-1}

$\mathbb{H}\_{brunn} \cong \varinjlim\_{k} F^{k}(B\_{6}/I)$.

***<span class="accent">Доказательство</span>***.

$\alpha$ индуцирует $\bar\alpha: B\_{6}/I \to (B\_{6}/I)^{\otimes 3}$ ([\[Лемма III.2\]](#lem-III-2)), $\bar\alpha(x) = x^{1} x^{2} x^{3}$. Положим $\bar\alpha\_{k} := F^{k}(\bar\alpha): (B\_{6}/I)^{\otimes 3^{k}} \to (B\_{6}/I)^{\otimes 3^{k+1}}$; это переходные морфизмы цепи $((B\_{6}/I)^{\otimes 3^{k}}, \bar\alpha\_{k})\_{k \geq 0}$.

Инъективность $\bar\alpha$: $\mathrm{Spec}(\bar\alpha): \{0,1\}^{3} \to \{0,1\}$, $(u^{1}, u^{2}, u^{3}) \mapsto u^{1} u^{2} u^{3}$, сюръективно ($(0,0,0) \mapsto 0$, $(1,1,1) \mapsto 1$); по булевости $B\_{6}/I \cong \mathbb{F}\_{2} \times \mathbb{F}\_{2}$ (элемент определяется значениями на $\mathbb{F}\_{2}$-точках) $\bar\alpha$ инъективно. Функтор $F$ сохраняет инъективность (в $\mathbf{BoolAlg}$ мономорфизмы суть инъекции; тензор — копроизведение, сохраняет мономорфизмы). Значит, все $\bar\alpha\_{k}$ инъективны.

$I\_{k} = \ker(\mathcal{L}\_{k} \twoheadrightarrow (B\_{6}/I)^{\otimes 3^{k}})$ [\[Определение III.4\]](#def-III-4), значит $\mathcal{L}\_{k}/I\_{k} \cong (B\_{6}/I)^{\otimes 3^{k}}$, и $\varinjlim (\mathcal{L}\_{k}/I\_{k}) \cong \varinjlim (B\_{6}/I)^{\otimes 3^{k}}$. $\square$

#### <span class="accent">— [Теорема III.2]</span>
{: .courier #thm-III-2}

$\vert\mathbb{H}\_{core}\vert = \vert\mathbb{H}\_{brunn}\vert = \aleph\_{0}$ в ZF.

***<span class="accent">Доказательство</span>***.

(1) Размерности и мощности: $\dim\_{\mathbb{F}\_{2}}(B\_{6}) = 64$ (базис — мономы $\prod\_{i \in S} x\_{i}$, $S \subseteq \{1,\ldots,6\}$), $\vert B\_{6}\vert = 2^{64}$; $\dim\_{\mathbb{F}\_{2}}(\mathcal{L}\_{k}) = 64^{3^{k}} = 2^{6 \cdot 3^{k}}$, $\vert\mathcal{L}\_{k}\vert = 2^{2^{6 \cdot 3^{k}}}$. $\dim\_{\mathbb{F}\_{2}}(B\_{6}/I) = 2$, $\vert B\_{6}/I\vert = 4$; $\dim\_{\mathbb{F}\_{2}}((B\_{6}/I)^{\otimes 3^{k}}) = 2^{3^{k}}$, $\vert F^{k}(B\_{6}/I)\vert = 2^{2^{3^{k}}}$.

(2) Счётность $\mathbb{H}\_{core}$: каждый слой $\mathcal{L}\_{k}$ конечен; $\mathbb{H}\_{core} = \bigcup\_{k} \iota\_{k}(\mathcal{L}\_{k})$ — счётное объединение конечных множеств вдоль возрастающей цепи (инъекции $\alpha\_{k}$). Явная нумерация: элемент из $\mathcal{L}\_{k}$ под номером $m$ получает номер $\sum\_{j < k} \vert\mathcal{L}\_{j}\vert + m$; биекция с $\mathbb{N}$ без AC.

(3) Счётность $\mathbb{H}\_{brunn}$: существует сюръекция $\pi\_{\infty}: \mathbb{H}\_{core} \twoheadrightarrow \mathbb{H}\_{brunn}$ ([\[Следствие III.2\]](#cor-III-2)); образ счётного множества при сюръекции счётен в ZF (каждому элементу образа сопоставляем наименьший прообраз в $\mathbb{N}$).

(4) Невырожденность $\mathbb{H}\_{brunn}$: все $\bar\alpha\_{k}$ инъективны [\[Следствие III.1\]](#cor-III-1), значит $I\_{\infty} \neq \mathbb{H}\_{core}$ и $\mathbb{H}\_{brunn} \neq \mathbb{F}\_{2}$: это бесконечная безатомная булева алгебра. $\square$

#### <span class="accent">— [Следствие III.2]</span>
{: .courier #cor-III-2}

Каноническая проекция $\pi\_{\infty}: \mathbb{H}\_{core} \twoheadrightarrow \mathbb{H}\_{brunn} = \mathbb{H}\_{core}/I\_{\infty}$ — сюръективный морфизм $F$-коалгебр.

***<span class="accent">Доказательство</span>***.

$\pi\_{\infty}$ — сюръекция по определению фактора. Коммутативность с коалгебраическими структурами: $\omega\_{brunn} \circ \pi\_{\infty} = (\pi\_{\infty}^{\otimes 3}) \circ \omega\_{core}$ — следует из спуска $\alpha\_{\infty}$ на фактор [\[Теорема III.1\]](#thm-III-1). $\square$

#### <span class="accent">— [Замечание III.2]</span>
{: .courier #rem-III-2}

$\mathbb{H}\_{brunn}$ — фактор $\mathbb{H}\_{core}$, не подобъект: в $\mathbf{BoolAlg}$ у сюръекции нет канонического сечения.

#### <span class="accent">— [Следствие III.3]</span>
{: .courier #cor-III-3}

$\omega\_{core} \circ \iota\_{0} = F(\iota\_{0}) \circ \alpha$ как морфизмы $B\_{6} \to \mathbb{H}\_{core}^{\otimes 3}$.

***<span class="accent">Доказательство</span>***.

Тождество следует из определения $\omega\_{core} = \varinjlim \alpha\_{k}$ и согласованности $\iota\_{k+1} \circ \alpha\_{k} = \iota\_{k}$ (каноническое свойство копредела). $\square$

---

#### <span class="accent">— [Интуитивное описание III]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

С $B\_{6}$ и идеала $I$ ([Раздел II](#prt-II)). $B\_{6}$ конечна; формализм не запрещает ввести копредел.

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Построили $\alpha: B\_{6} \to B\_{6}^{\otimes 3}$ [\[Определение III.2\]](#def-III-2). Ввели $\mathbb{H}\_{core}$, $I\_{\infty}$, $\mathbb{H}\_{brunn}$ [\[Теорема III.1\]](#thm-III-1); индуцировали $\bar\alpha\_{k}$ и установили их инъективность [\[Следствие III.1\]](#cor-III-1).

(б) Доказали: $\alpha$ инъективно [\[Лемма III.1\]](#lem-III-1); $\alpha(I) \subset I^{[3]}$ [\[Лемма III.2\]](#lem-III-2); $I\_{k+1} = I\_{k}^{[3]}$, $\alpha\_{k}(I\_{k}) \subset I\_{k+1}$ [\[Лемма III.3\]](#lem-III-3); счётность $\mathbb{H}\_{core}$ (объединение) и $\mathbb{H}\_{brunn}$ (фактор), невырожденность [\[Теорема III.2\]](#thm-III-2); проекцию [\[Следствие III.2\]](#cor-III-2); коммутативность с $\iota\_{0}$ [\[Следствие III.3\]](#cor-III-3).

**3. <span class="accent">К чему пришли</span>?**

$\mathbb{H}\_{core}$ — счётная $F$-коалгебра с $\omega\_{core}: \mathbb{H}\_{core} \to F(\mathbb{H}\_{core})$ (изоморфизм, так как $F$ сохраняет копределы). $\mathbb{H}\_{brunn} = \mathbb{H}\_{core}/I\_{\infty}$ — счётная невырожденная фактор-коалгебра. Оба счётны ($\aleph\_{0}$).

**4. <span class="accent">Что это значит сейчас</span>?**

Получили бесконечный счётный остов с коалгебраической структурой.

---

### **Раздел IV. Счётная бесконечность**
{: .accent #prt-IV}

#### <span class="accent">— [Определение IV.1]</span>
{: .courier #def-IV-1}

Для $A \in \mathbf{BoolAlg}$: $\mathrm{Spec}(A) := \mathrm{Hom}_{\mathbf{BoolAlg}}(A, \mathbb{F}\_{2})$ с базой $\{U\_{a} := \{h : h(a) = 1\}\}\_{a \in A}$.

Обозначим $\partial\mathbb{H}\_{core} := \mathrm{Spec}(\mathbb{H}\_{core})$, $\partial\mathbb{H}\_{brunn} := \mathrm{Spec}(\mathbb{H}\_{brunn})$.

#### <span class="accent">— [Замечание IV.1]</span>
{: .courier #rem-IV-1}

Для счётной булевой алгебры ($\vert A\vert \le \aleph_{0}$) двойственность Стоуна — биекция $\mathrm{Atom}(A) \leftrightarrow \mathrm{Isol}(\mathrm{Spec}(A))$, тождество $\mathrm{Spec}(\varinjlim A_{k}) \cong \varprojlim \mathrm{Spec}(A_{k})$, компактность $\mathrm{Spec}(A)$ — доказуема в ZF без AC: ультрафильтр на счётной алгебре строится явной рекурсией по перенумерации; для обратных пределов конечных дискретных пространств — как замкнутое подмножество счётного произведения конечных метризуемых компактов. Полная теорема Стоуна для произвольных булевых алгебр требует BPI; здесь она не используется.

#### <span class="accent">— [Лемма IV.1]</span>
{: .courier #lem-IV-1}

$\partial\mathbb{H}\_{core} \cong \varprojlim\_{k} \mathrm{Spec}(\mathcal{L}\_{k})$ канонически.

***<span class="accent">Доказательство</span>***.

$\mathbb{H}\_{core} = \varinjlim \mathcal{L}\_{k}$ — счётный копредел; двойственность Стоуна для счётных алгебр в ZF переводит копределы в пределы [\[Замечание IV.1\]](#rem-IV-1). $\square$

#### <span class="accent">— [Лемма IV.2]</span>
{: .courier #lem-IV-2}

$\mathbb{H}\_{core}$ не имеет атомов.

***<span class="accent">Доказательство</span>***.

(1) Пусть $x \in \mathbb{H}\_{core}$, $x \neq 0$. Без ограничения $x = e\_{p}$ для атома $e\_{p} \in \mathcal{L}\_{k}$, $p \in \mathrm{Spec}(\mathcal{L}\_{k})$. Тогда $\alpha\_{k}(e\_{p}) = \sum\_{q \in (\alpha\_{k}^{\*})^{-1}(p)} e\_{q}$ в $\mathcal{L}\_{k+1}$.

(2) Пусть $p = (p\_{1},\dots,p\_{3^{k}})$, $p\_{t} \in \mathbb{F}\_{2}^{6}$; тогда $\vert(\alpha\_{k}^{\*})^{-1}(p)\vert = \prod\_{t=1}^{3^{k}} \vert T^{-1}(p\_{t})\vert$.

(3) Оценка $\vert T^{-1}(p\_{t})\vert \ge 16$ для любого $p\_{t} \in \mathbb{F}\_{2}^{6}$: по таблице $\mathcal{F}$ индексы $j\_{i}$ принимают значения из $\{1,2,4,5\}$, индексы $k\_{i}$ — из $\{2,3,5,6\}$; следовательно, координаты $v^{1}\_{3}, v^{1}\_{6}, v^{2}\_{1}, v^{2}\_{4}$ не входят ни в одно из уравнений $T(v^{1}, v^{2}, v^{3}) = p\_{t}$.

(4) Множество $T^{-1}(p\_{t})$ непусто; изменение этих четырёх координат произвольно даёт $2^{4} = 16$ различных элементов $T^{-1}(p\_{t})$ [\[Лемма III.1\]](#lem-III-1). Значит, $\vert(\alpha\_{k}^{\*})^{-1}(p)\vert \ge 16^{3^{k}} \ge 2$: $\alpha\_{k}(e\_{p})$ — сумма $\ge 2$ различных атомов, не атом. $\square$

#### <span class="accent">— [Следствие IV.1]</span>
{: .courier #cor-IV-1}

$\partial\mathbb{H}\_{core}$ не имеет изолированных точек.

***<span class="accent">Доказательство</span>***.

Изолированная точка $\partial\mathbb{H}\_{core}$ соответствует атому $\mathbb{H}\_{core}$ [\[Замечание IV.1\]](#rem-IV-1) для счётной алгебры в ZF. Атомов нет [\[Лемма IV.2\]](#lem-IV-2). $\square$

#### <span class="accent">— [Лемма IV.3]</span>
{: .courier #lem-IV-3}

$\mathbb{H}\_{brunn}$ имеет ровно один атом — образ $e\_{\mathbf{1}}$, соответствующий точке $\mathbf{1}\_{\infty} \in \partial\mathbb{H}\_{brunn}$.

***<span class="accent">Доказательство</span>***.

(1) В $B\_{6}/I \cong \mathbb{F}\_{2} \times \mathbb{F}\_{2}$ — два атома $e\_{\mathbf{0}}, e\_{\mathbf{1}}$. Индуцированное $\bar\alpha: B\_{6}/I \to (B\_{6}/I)^{\otimes 3}$, $x \mapsto x^{1} x^{2} x^{3}$. На слое $k$: для $q \in \{0,1\}^{3^{k}}$ с $z(q)$ нулями, $\vert(\bar\alpha\_{k}^{\*})^{-1}(q)\vert = 7^{z(q)}$ (при $q = \mathbf{1}$: $z(q) = 0$, один прообраз $(1,1,1)$; при $q \neq \mathbf{1}$: $z(q) \ge 1$, $\ge 7$ прообразов — все тройки, кроме $(1,1,1)$).

(2) Индукцией: в каждом слое ровно один атом, выживающий при переходе — образ $e\_{\mathbf{1}}$. $\square$

#### <span class="accent">— [Следствие IV.2]</span>
{: .courier #cor-IV-2}

$\partial\mathbb{H}\_{brunn}$ имеет ровно одну изолированную точку — $\mathbf{1}\_{\infty}$.

***<span class="accent">Доказательство</span>***.

Изолированная точка $\leftrightarrow$ атом [\[Замечание IV.1\]](#rem-IV-1). Атом один [\[Лемма IV.3\]](#lem-IV-3). $\square$

#### <span class="accent">— [Теорема IV.1]</span>
{: .courier #thm-IV-1}

Следующие факты имеют место одновременно:

(а) $B\_{6}$ конечна, $\vert\mathrm{At}(B\_{6})\vert = 64$; точки $V(I) = \{\mathbf{0}, \mathbf{1}\}$ соответствуют двум атомам $B\_{6}/I$ — глобальное состояние реализуется внутри.

(б) $\mathbb{H}\_{core}$ безатомна; в $\mathbb{H}\_{core}$ нет элементов, кодирующих глобальные состояния бесконечной итерации.

(в) $\mathbb{H}\_{brunn}$ имеет ровно один атом ($\mathbf{1}\_{\infty}$); одно состояние кодируется внутри, остальные нет.

(г) Глобальные состояния $\mathbb{H}\_{core}$ (и всех, кроме $\mathbf{1}\_{\infty}$, состояний $\mathbb{H}\_{brunn}$) не реализуются элементами алгебр; переход к $\mathrm{Spec}$ даёт их.

***<span class="accent">Доказательство</span>***.

(1) Для (а): $B\_{6} \cong \mathbb{F}\_{2}^{64}$; для (б): [\[Лемма IV.2\]](#lem-IV-2); для (в): [\[Лемма IV.3\]](#lem-IV-3).

(2) Для счётных алгебр в ZF: точка $h \in \mathrm{Spec}(A)$ соответствует атому $A$ тогда и только тогда, когда $h$ изолирована [Замечание IV.1](#rem-IV-1). Нет атомов — нет точек, реализуемых элементами. $\square$

#### <span class="accent">— [Замечание IV.2]</span>
{: .courier #rem-IV-2}

$\mathrm{Spec}$ — канонический дуал, определённый для любой булевой алгебры. Здесь он идентифицируется в момент, когда исходный объект обнаруживает дефицит атомов.

#### <span class="accent">— [Теорема IV.2]</span>
{: .courier #thm-IV-2}

$\partial\mathbb{H}\_{core}$ и $\partial\mathbb{H}\_{brunn}$ — компактные хаусдорфовы пространства.

***<span class="accent">Доказательство</span>***.

$\partial\mathbb{H}\_{core} \cong \varprojlim \mathrm{Spec}(\mathcal{L}\_{k})$ — замкнутое подмножество $\prod\_{k} \mathrm{Spec}(\mathcal{L}\_{k})$ (конечные дискретные). На произведении — метрика $d(u,v) = 2^{-\min\{k : u\_{k} \neq v\_{k}\}}$, полная и вполне ограниченная; компактность метрического пространства — теорема ZF. Замкнутое подмножество компакта компактно. Аналогично для $\partial\mathbb{H}\_{brunn}$. $\square$

#### <span class="accent">— [Теорема IV.3]</span>
{: .courier #thm-IV-3}

$\vert\partial\mathbb{H}\_{core}\vert = \vert\partial\mathbb{H}\_{brunn}\vert = 2^{\aleph\_{0}}$.

***<span class="accent">Доказательство</span>***.

Для $\partial\mathbb{H}\_{core}$:

(1) Верхняя граница: $\vert\mathrm{Spec}(\mathcal{L}\_{k})\vert = \dim\_{\mathbb{F}\_{2}}(\mathcal{L}\_{k}) = 2^{6\cdot 3^{k}}$; значит $\vert\partial\mathbb{H}\_{core}\vert \le \prod\_{k} 2^{6\cdot 3^{k}} = 2^{\sum\_{k} 6\cdot 3^{k}} = 2^{\aleph\_{0}}$.

(2) Нижняя граница: слои $\alpha\_{k}^{\*}$ имеют размер $\ge 16$ [\[Лемма IV.2\]](#lem-IV-2); строим инъекцию $\{0,1\}^{\mathbb{N}} \hookrightarrow \partial\mathbb{H}\_{core}$, выбирая в каждом прообразе первый и второй элементы по лексикографическому порядку. Явная конструкция в ZF без AC, Кантор-Бернштейн. $\square$

Для $\partial\mathbb{H}\_{brunn}$:

(1) Верхняя граница: $\vert\mathrm{Spec}(\mathcal{L}\_{k}^{brunn})\vert = \dim\_{\mathbb{F}\_{2}}((B\_{6}/I)^{\otimes 3^{k}}) = 2^{3^{k}}$; значит $\vert\partial\mathbb{H}\_{brunn}\vert \le \prod\_{k} 2^{3^{k}} = 2^{\sum\_{k} 3^{k}} = 2^{\aleph\_{0}}$.

(2) Нижняя граница: для каждой $\varepsilon = (\varepsilon\_{0}, \varepsilon\_{1}, \ldots) \in \{0,1\}^{\mathbb{N}}$ индуктивно строим нить $\pi = (u^{(0)}, u^{(1)}, \ldots) \in \partial\mathbb{H}\_{brunn}$: $u^{(0)} = 0$; при переходе $k \to k+1$ пусть $m\_{k} \in \{1, \ldots, 3^{k}\}$ — наименьший индекс с $u^{(k)}\_{m\_{k}} = 0$ (существует: $u^{(0)} = 0$, и индуктивно в позиции $m\_{k}$ сохраняется ноль); для $m \neq m\_{k}$ полагаем тройку равной $(0,0,0)$ если $u^{(k)}\_{m} = 0$, и $(1,1,1)$ если $u^{(k)}\_{m} = 1$; для $m = m\_{k}$ полагаем $(0,0,0)$ если $\varepsilon\_{k} = 0$, и $(1,0,0)$ если $\varepsilon\_{k} = 1$.

(3) Обе тройки дают произведение $0 = u^{(k)}\_{m\_{k}}$; для $m \neq m\_{k}$ произведение тройки равно $u^{(k)}\_{m}$; нить когерентна. Отображение $\varepsilon \mapsto \pi$ инъективно: если $\varepsilon\_{k} \neq \varepsilon'\_{k}$ при наименьшем таком $k$, то $u^{(k)} = u'^{(k)}$ (по индукции), значит $m\_{k} = m'\_{k}$, и $u^{(k+1)} \neq u'^{(k+1)}$ в позиции $3m\_{k}-2$. Явная рекурсия в ZF без AC, Кантор-Бернштейн. $\square$

#### <span class="accent">— [Следствие IV.3]</span>
{: .courier #cor-IV-3}

(а) $\partial\mathbb{H}\_{core}$ — совершенный компакт веса $\aleph\_{0}$ и мощности $2^{\aleph\_{0}}$.

(б) $\partial\mathbb{H}\_{brunn}$ — компакт веса $\aleph\_{0}$ и мощности $2^{\aleph\_{0}}$, имеющий ровно одну изолированную точку $\mathbf{1}\_{\infty}$.

***<span class="accent">Доказательство</span>***.

(1) Совершенность — [\[Следствие IV.1\]](#cor-IV-1); вес $\aleph\_{0}$ — база $\{U\_{a}: a \in \mathbb{H}\_{core}\}$, $\vert\mathbb{H}\_{core}\vert = \aleph\_{0}$; мощность — [\[Теорема IV.3\]](#thm-IV-3).

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

$\Phi\_{core}: (\partial\mathbb{H}\_{core})^{3} \to \partial\mathbb{H}\_{core}$ — морфизм в $\mathbf{Stone}$, равный композиции $\mathrm{Spec}(\omega\_{core}): \mathrm{Spec}(\mathbb{H}\_{core}^{\otimes 3}) \to \partial\mathbb{H}\_{core}$ с каноническим гомеоморфизмом $\mathrm{Spec}(\mathbb{H}\_{core}^{\otimes 3}) \cong (\partial\mathbb{H}\_{core})^{3}$ (универсальное свойство копроизведения в $\mathbf{BoolAlg}$).

Аналогично $\Phi\_{brunn}: (\partial\mathbb{H}\_{brunn})^{3} \to \partial\mathbb{H}\_{brunn}$.

#### <span class="accent">— [Замечание V.1]</span>
{: .courier #rem-V-1}

$\omega\_{core}$, $\omega\_{brunn}$ индуцированы $\alpha\_{k}: \mathcal{L}\_{k} \to \mathcal{L}\_{k}^{\otimes 3}$ с фиксированным порядком тензорных факторов ($F(X) = X^{\otimes 3}$). Симметрии из [Раздела I](#prt-I) относятся к цветам, не к факторам $F$. Проекции ниже определены корректно.

#### <span class="accent">— [Лемма V.1]</span>
{: .courier #lem-V-1}

$\omega\_{core}: \mathbb{H}\_{core} \to F(\mathbb{H}\_{core})$ и $\omega\_{brunn}: \mathbb{H}\_{brunn} \to F(\mathbb{H}\_{brunn})$ — изоморфизмы в $\mathbf{BoolAlg}$. Следовательно, $\Phi\_{core}$ и $\Phi\_{brunn}$ — гомеоморфизмы.

***<span class="accent">Доказательство</span>***.

(1) $\omega\_{core}$ — изоморфизм [\[Теорема III.1\]](#thm-III-1): $F(\mathbb{H}\_{core}) = \varinjlim F(\mathcal{L}\_{k}) = \varinjlim \mathcal{L}\_{k+1} \cong \mathbb{H}\_{core}$.

(2) $\omega\_{brunn}$: $\mathbb{H}\_{brunn} \cong \varinjlim\_{k} (B\_{6}/I)^{\otimes 3^{k}}$ [\[Следствие III.1\]](#cor-III-1); $F(\mathbb{H}\_{brunn}) \cong \varinjlim\_{k} (B\_{6}/I)^{\otimes 3^{k+1}}$ — тот же предел со сдвигом индекса; $\omega\_{brunn}$ индуцирован $\omega\_{core}$ через $I\_{\infty}$-инвариантность [\[Теорема III.1\]](#thm-III-1), значит изоморфизм.

(3) $\mathrm{Spec}$ переводит изоморфизм алгебр в гомеоморфизм пространств.

(4) $\mathrm{Spec}(A^{\otimes 3}) \cong (\mathrm{Spec}(A))^{3}$ — гомеоморфизм по двойственности Стоуна для счётных алгебр [\[Замечание IV.1\]](#rem-IV-1). Композиция гомеоморфизмов — гомеоморфизм. $\square$

#### <span class="accent">— [Определение V.2]</span>
{: .courier #def-V-2}

$\sigma\_{r} := p\_{r} \circ \Phi^{-1}: \partial\mathbb{H} \to \partial\mathbb{H}$, $r = 1,2,3$, где $p\_{r}$ — $r$-я координатная проекция, $\Phi \in \{\Phi\_{core}, \Phi\_{brunn}\}$.

#### <span class="accent">— [Лемма V.2]</span>
{: .courier #lem-V-2}

Каждое $\sigma\_{r}$ — непрерывная сюръекция; не инъекция: $\sigma\_{r}^{-1}(\eta) \cong (\partial\mathbb{H})^{2}$.

***<span class="accent">Доказательство</span>***.

$\Phi^{-1}$ — гомеоморфизм [\[Лемма V.1\]](#lem-V-1)), $p\_{r}$ — непрерывная сюръекция; композиция — непрерывная сюръекция. Неинъективность: $p\_{r}$ склеивает квадрат $(\partial\mathbb{H})^{2}$ в точку. $\square$

#### <span class="accent">— [Определение V.3]</span>
{: .courier #def-V-3}

$\mathbf{0}\_{\infty} \in \partial\mathbb{H}\_{brunn}$ — нить с $u^{(k)} = \mathbf{0}$ для всех $k \geq 0$ (корректность: $\bar\alpha^{\*}(\mathbf{0},\mathbf{0},\mathbf{0}) = 0 \cdot 0 \cdot 0 = 0$).

$K\_{coll} := \partial\mathbb{H}\_{brunn} \setminus \{\mathbf{1}\_{\infty}\} = \{\pi \in \partial\mathbb{H}\_{brunn} : \pi^{(0)} = \mathbf{0}\}$.

Корректность: $\mathbf{1}\_{\infty}$ — единственный атом $\mathbb{H}\_{brunn}$ [\[Лемма IV.3\]](#lem-IV-3), а значит единственная точка с $\pi^{(0)} = \mathbf{1}$ (остальные точки удовлетворяют $\pi(e\_{\mathbf{1}}) = 0$, т.е. $\pi^{(0)} = \mathbf{0}$). $K\_{coll} = U\_{1+e\_{\mathbf{1}}}$ — clopen (дополнение к открытому $\{\mathbf{1}\_{\infty}\}$), замкнуто, компактно.

#### <span class="accent">— [Лемма V.3]</span>
{: .courier #lem-V-3}

(а) $\sigma\_{r}(\mathbf{1}\_{\infty}) = \mathbf{1}\_{\infty}$ для $r = 1,2,3$.

(б) $\sigma\_{r}(\mathbf{0}\_{\infty}) = \mathbf{0}\_{\infty}$ для $r = 1,2,3$.

***<span class="accent">Доказательство</span>***.

(1) $\Phi\_{brunn}(\mathbf{1},\mathbf{1},\mathbf{1}) = \mathbf{1}$.

(2) $\Phi\_{brunn}(\mathbf{0},\mathbf{0},\mathbf{0}) = \mathbf{0}$. $\square$

#### <span class="accent">— [Лемма V.4]</span>
{: .courier #lem-V-4}

(а) $\sigma\_{r}^{-1}(\mathbf{1}\_{\infty}) = \Phi\_{brunn}(\{(\eta\_{1}, \eta\_{2}, \eta\_{3}) \in (\partial\mathbb{H})^{3} : \eta\_{r} = \mathbf{1}\_{\infty}\})$ — $r$-я грань куба, гомеоморфна $(\partial\mathbb{H})^{2}$, мощность $(2^{\aleph\_{0}})^{2} = 2^{\aleph\_{0}}$, пересекает $K\_{coll}$.

(б) $\sigma\_{r}(K\_{coll}) = \partial\mathbb{H}\_{brunn}$ (в частности, $\mathbf{1}\_{\infty} \in \sigma\_{r}(K\_{coll})$).

***<span class="accent">Доказательство</span>***.

(1) По биективности $\Phi$: $\sigma\_{r}(\pi) = \mathbf{1}\_{\infty} \iff p\_{r}(\Phi^{-1}(\pi)) = \mathbf{1}\_{\infty} \iff$ $r$-я координата $\Phi^{-1}(\pi)$ равна $\mathbf{1}\_{\infty}$. Мощность: $(\partial\mathbb{H})^{2}$ — произведение двух компактов мощности $2^{\aleph\_{0}}$ [\[Теорема IV.3\]](#thm-IV-3)), значит $(2^{\aleph\_{0}})^{2} = 2^{\aleph\_{0}}$. Пересечение с $K\_{coll}$: точка $\Phi\_{brunn}(\mathbf{1}\_{\infty}, \mathbf{0}\_{\infty}, \mathbf{0}\_{\infty})$ при $r = 1$ лежит в прообразе (первая координата $\mathbf{1}\_{\infty}$) и в $K\_{coll}$ (на слое 0: $1 \cdot 0 \cdot 0 = 0$).

(2) Для $\eta \in \partial\mathbb{H}\_{brunn}$ положим $\pi := \Phi\_{brunn}(\eta, \mathbf{0}\_{\infty}, \mathbf{0}\_{\infty})$. На слое 0: $\pi^{(0)} = \eta^{(0)} \cdot 0 \cdot 0 = 0$, значит $\pi \in K\_{coll}$; $\sigma\_{1}(\pi) = \eta$. Значит $\sigma\_{1}(K\_{coll}) = \partial\mathbb{H}\_{brunn}$; аналогично для $r = 2,3$. $\square$

#### <span class="accent">— [Следствие V.1]</span>
{: .courier #cor-V-1}

$\{\mathbf{1}\_{\infty}\}$ инвариантно вперёд, но не назад. $K\_{coll}$ не инвариантно ни вперёд ($\sigma\_{r}(K\_{coll}) = \partial\mathbb{H}\_{brunn}$), ни в смысле $\sigma\_{r}^{-1}$ ($\sigma\_{r}^{-1}(\mathbf{1}\_{\infty}) \cap K\_{coll} \neq \varnothing$).

***<span class="accent">Доказательство</span>***.

Непосредственно [\[Лемма V.3\]](#lem-V-3) и [\[Лемма V.4\]](#lem-V-4). $\square$

#### <span class="accent">— [Теорема V.1]</span>
{: .courier #thm-V-1}

В ZF без AC: $\partial\mathbb{H}\_{core} \cong 2^{\omega}$; $K\_{coll} \cong 2^{\omega}$.

***<span class="accent">Доказательство</span>***.

(1) Компактность — [\[Теорема IV.2\]](#thm-IV-2).

(2) Метризуемость: метрика $d(\pi\_{1}, \pi\_{2}) = 2^{-k(\pi\_{1}, \pi\_{2})}$ ([Раздел IV](#prt-IV)) задаёт топологию, совпадающую со стоуновской: база шаров $d$-метрики совпадает с базой clopen-цилиндров $U\_{a}$.

(3) Нульмерность: база $\{U\_{a}\}$ состоит из clopen; $U\_{a}^{c} = \{h : h(a) = 0\} = \{h : h(1+a) = 1\} = U\_{1+a}$.

(4) Совершенность: $\partial\mathbb{H}\_{core}$ — [\[Следствие IV.1\]](#cor-IV-1); $K\_{coll}$ — [\[Лемма V.5\]](#lem-V-5) ниже.

(5) Непустота: $\mathbf{0}\_{\infty} \in K\_{coll}$.

(6) Счётная база $\{U\_{a} : a \in \mathbb{H}\}$ явно перенумерована [\[Теорема III.2\]](#thm-III-2), $\vert\mathbb{H}\vert = \aleph\_{0}$. Характеризация Брауэра: гомеоморфизм на $2^{\omega}$ строится индуктивно; на каждом шаге выбирается в перенумерованной базе наименьшее по номеру clopen-подмножество, измельчающее текущее разбиение. Выбор детерминирован перенумерацией — AC не используется. $\square$

#### <span class="accent">— [Лемма V.5]</span>
{: .courier #lem-V-5}

$K\_{coll}$ не имеет изолированных точек.

***<span class="accent">Доказательство</span>***.

(1) Пусть $\pi \in K\_{coll}$ изолирована в $K\_{coll}$. Тогда существует $V \subseteq \partial\mathbb{H}\_{brunn}$ открытое с $V \cap K\_{coll} = \{\pi\}$, значит $V \subseteq \{\pi, \mathbf{1}\_{\infty}\}$ (поскольку $\partial\mathbb{H}\_{brunn} = K\_{coll} \sqcup \{\mathbf{1}\_{\infty}\}$). Если $V = \{\pi\}$, то $\pi$ изолирована в $\partial\mathbb{H}\_{brunn}$ — противоречие: [\[Следствие IV.2\]](#cor-IV-2).

(2) Если $V = \{\pi, \mathbf{1}\_{\infty}\}$, то $\{\mathbf{1}\_{\infty}\}$ открыто [\[Следствие IV.2\]](#cor-IV-2)), следовательно $\{\pi\} = V \setminus \{\mathbf{1}\_{\infty}\}$ открыто как разность открытых, значит $\pi$ изолирована в $\partial\mathbb{H}\_{brunn}$ — противоречие: [\[Следствие IV.2\]](#cor-IV-2). $\square$

#### <span class="accent">— [Теорема V.2]</span>
{: .courier #thm-V-2}

Имеет место топологическое разложение $\partial\mathbb{H}\_{brunn} = \{\mathbf{1}\_{\infty}\} \sqcup K\_{coll}$, где $\{\mathbf{1}\_{\infty}\}$ — clopen синглтон, $K\_{coll} \cong 2^{\omega}$ [\[Теорема V.1\]](#thm-V-1) и [\[Лемма V.5\]](#lem-V-5)). При этом:

(а) $\{\mathbf{1}\_{\infty}\}$ инвариантно вперёд: $\sigma\_{r}(\mathbf{1}\_{\infty}) = \mathbf{1}\_{\infty}$.

(б) $\sigma\_{r}^{-1}(\mathbf{1}\_{\infty})$ гомеоморфно $(\partial\mathbb{H})^{2}$, мощность $(2^{\aleph\_{0}})^{2} = 2^{\aleph\_{0}}$, пересекает $K\_{coll}$ [\[Лемма V.4\]](#lem-V-4).

(в) $K\_{coll}$ не инвариантно; $\sigma\_{r}(K\_{coll}) = \partial\mathbb{H}\_{brunn}$ [\[Лемма V.4\]](#lem-V-4).

(г) На уровне прямого гомеоморфизма: $\Phi\_{brunn}(K\_{coll}^{3}) \subsetneq K\_{coll}$.

***<span class="accent">Доказательство</span>***.

(1) Для (а): [\[Лемма V.3\]](#lem-V-3); для (б): [\[Лемма V.4\]](#lem-V-4)(а); для (в): [\[Лемма V.4\]](#lem-V-4)(б).

(2) Пусть $a, b, c \in K\_{coll}$; $a^{(0)} = b^{(0)} = c^{(0)} = \mathbf{0}$  [\[Определение V.3\]](#def-V-3), значит $\Phi\_{brunn}(a,b,c)^{(0)} = 0 \cdot 0 \cdot 0 = 0$, т.е. $\Phi\_{brunn}(a,b,c) \in K\_{coll}$ — включение.

Корректность: $\Phi\_{brunn}(\mathbf{1}\_{\infty}, \mathbf{1}\_{\infty}, \mathbf{0}\_{\infty}) \in K\_{coll}$ (на слое 0: $1 \cdot 1 \cdot 0 = 0$), но $(\mathbf{1}\_{\infty}, \mathbf{1}\_{\infty}, \mathbf{0}\_{\infty}) \notin K\_{coll}^{3}$. $\square$

---

#### <span class="accent">— [Интуитивное описание V]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

С $\partial\mathbb{H}\_{core}$, $\partial\mathbb{H}\_{brunn}$ ([Раздел IV](#prt-IV)). Они компактны, мощность $2^{\aleph\_{0}}$. Формализм не запрещает ввести динамику через $\mathrm{Spec}(\omega)$.

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Определили $\Phi\_{core}$, $\Phi\_{brunn}$ [\[Определение V.1\]](#def-V-1) и доказали, что это гомеоморфизмы [\[Лемма V.1\]](#lem-V-1); определили $\sigma\_{r}$ [\[Определение V.2\]](#def-V-2) и доказали, что это непрерывные сюръекции, не инъекции [\[Лемма V.2\]](#lem-V-2); доказали характеризацию Брауэра [\[Теорема V.1\]](#thm-V-1); совершенность $K\_{coll}$ [\[Лемма V.5\]](#lem-V-5); разложение и динамическую асимметрию [\[Теорема V.2\]](#thm-V-2).

(б) Определили $\mathbf{0}\_{\infty}$ и $K\_{coll}$ [\[Определение V.3\]](#def-V-3); установили неподвижные точки $\mathbf{1}\_{\infty}, \mathbf{0}\_{\infty}$ [\[Лемма V.3\]](#lem-V-3); вычислили $\sigma\_{r}^{-1}(\mathbf{1}\_{\infty})$ и $\sigma\_{r}(K\_{coll})$ [\[Лемма V.4\]](#lem-V-4); вывели асимметрию [\[Следствие V.1\]](#cor-V-1)

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

Матрица инцидентности $M \in \mathbb{N}^{6 \times 6}$: $M\_{ij} = 1$ при $j \in \{j\_{i}, k\_{i}, l\_{i}\}$, $0$ иначе. Сумма каждой строки и каждого столбца $M$ равна $3$ (каждый сорт входит в три триплета, каждый триплет содержит три сорта); значит $M$ примитивна ($M^{3} > 0$; индекс примитивности 3: например, $(M^{2})\_{14} = 0$, так как $N(1) = \{2,3,4\}$ и $N(4) = \{5,6,1\}$ не пересекаются, а $(M^{3})\_{14} = 7 > 0$), $\lambda\_{PF}(M) = 3$, правый и левый векторы Перрона–Фробениуса равны $\mathbf{1} = (1,\dots,1)^{T}$.

#### <span class="accent">— [Замечание VI.1]</span>
{: .courier #rem-VI-1}

Два уровня необходимо различать.

(а) Типовой подстановочный подшифт $(X\_{\theta}, S)$: пространство последовательностей $X\_{\theta} \subseteq \Sigma^{\mathbb{N}}$, порождённое $\theta$, с односторонним сдвигом $S$. По теореме Мосье сложность $p(n)$ растёт линейно, откуда $h\_{top}(S\vert\_{X\_{\theta}}) = 0$; система строго эргодична с равномерными частотами $1/6$. Число $\log 3 = \log \lambda\_{PF}(M)$ характеризует скорость роста длины $\vert\theta^{k}(i)\vert = 3^{k}$, а не энтропию.

(б) Спектральная динамика $(\partial\mathbb{H}, \sigma\_{r})$: пространство булевых оценок на координатной сетке. Мощность слоёв растёт сверхэкспоненциально ($2^{6\cdot 3^{k}}$ для $\partial\mathbb{H}\_{core}$, $2^{3^{k}}$ для $\partial\mathbb{H}\_{brunn}$).

#### <span class="accent">— [Определение VI.2]</span>
{: .courier #def-VI-2}

Нить $\mathbf{0}\_{\infty} \in \partial\mathbb{H}\_{core}$ — постоянная нить с $u^{(k)} = \mathbf{0}$ для всех $k \geq 0$ (корректность: $T(\mathbf{0},\mathbf{0},\mathbf{0}) = \mathbf{0}$ покомпонентно). Нить $\mathbf{1}\_{\infty} \in \partial\mathbb{H}\_{core}$ — постоянная нить с $u^{(k)} = \mathbf{1}$ для всех $k \geq 0$ (корректность: $T(\mathbf{1},\mathbf{1},\mathbf{1}) = \mathbf{1}$ покомпонентно).

#### <span class="accent">— [Лемма VI.1]</span>
{: .courier #lem-VI-1}

$\Phi\_{core}$ и $\Phi\_{brunn}$ — гомеоморфизмы [\[Лемма V.1\]](#lem-V-1). Для любого $n \geq 1$ и любого $r \in \{1,2,3\}$ прообраз $\sigma\_{r}^{-n}(\mathcal{U}\_{0})$ базового clopen-разбиения уровня 0 совпадает с разбиением $\mathcal{U}\_{n}$, индуцированным компонентой с мультииндексом $(r, r, \ldots, r) \in \{1,2,3\}^{n}$ слоя $\mathcal{L}\_{n}$.

***<span class="accent">Доказательство</span>***.

На конечных слоях $\Phi^{-1}$ индуцируется каноническими биекциями $\mathrm{Spec}(\mathcal{L}\_{k+1}) = \mathrm{Spec}(\mathcal{L}\_{k}^{\otimes 3}) \cong (\mathrm{Spec}(\mathcal{L}\_{k}))^{3}$, поэтому $n$-кратное применение $p\_{r} \circ \Phi^{-1}$ переводит ограничения уровня 0 в ограничения на компоненте с мультииндексом $(r, \ldots, r)$ слоя $\mathcal{L}\_{n}$. $\square$

#### <span class="accent">— [Определение VI.3]</span>
{: .courier #def-VI-3}

На $\partial\mathbb{H} \in \{\partial\mathbb{H}\_{core}, \partial\mathbb{H}\_{brunn}\}$: экспоненциальная фильтрационная ультраметрика $d(\pi\_{1}, \pi\_{2}) := 2^{-k(\pi\_{1}, \pi\_{2})}$ при $\pi\_{1} \neq \pi\_{2}$, $d(\pi, \pi) := 0$, где $k(\pi\_{1}, \pi\_{2}) := \min\{k \in \mathbb{N} : \pi\_{1}^{(k)} \neq \pi\_{2}^{(k)}\}$; послойно-нормированная ультраметрика $d\_{norm}(\pi\_{1}, \pi\_{2}) := \vert\mathrm{Spec}(\mathcal{L}\_{k(\pi\_{1}, \pi\_{2})})\vert^{-1}$ при $\pi\_{1} \neq \pi\_{2}$, $d\_{norm}(\pi, \pi) := 0$. Обе совместимы с топологией Стоуна и заданы конструктивно в ZF.

#### <span class="accent">— [Теорема VI.1]</span>
{: .courier #thm-VI-1}

Для каждого $r \in \{1,2,3\}$: $h\_{top}(\sigma\_{r}\vert\_{\partial\mathbb{H}\_{core}}) = h\_{top}(\sigma\_{r}\vert\_{\partial\mathbb{H}\_{brunn}}) = +\infty$.

***<span class="accent">Доказательство</span>***.

(1) Пусть $\mathcal{U}\_{0}$ — конечное clopen-разбиение уровня 0. Измельчение $\mathcal{U}\_{0} \vee \sigma\_{r}^{-1}\mathcal{U}\_{0} \vee \cdots \vee \sigma\_{r}^{-(n-1)}\mathcal{U}\_{0}$ разделяет все компоненты слоя $\mathcal{L}\_{n-1}$ [\[Лемма VI.1\]](#lem-VI-1).

(2) Для $\partial\mathbb{H}\_{core}$ число непустых элементов измельчения $\geq \vert\mathrm{Spec}(\mathcal{L}\_{n-1})\vert = 2^{6 \cdot 3^{n-1}}$, откуда $h\_{top}(\sigma\_{r}\vert\_{\partial\mathbb{H}\_{core}}) \geq \lim\_{n \to \infty} \frac{1}{n}\log(2^{6\cdot 3^{n-1}}) = +\infty$. Аналогично для $\partial\mathbb{H}\_{brunn}$: $\vert\mathrm{Spec}(\mathcal{L}\_{n-1}^{brunn})\vert = 2^{3^{n-1}}$, и $\lim\_{n \to \infty} \frac{3^{n-1}\log 2}{n} = +\infty$. $\square$

#### <span class="accent">— [Теорема VI.2]</span>
{: .courier #thm-VI-2}

В ультраметрике $d = 2^{-k}$: $\dim\_{H}(\partial\mathbb{H}\_{core}, d) = \dim\_{H}(K\_{coll}, d) = +\infty$. В $d\_{norm}$: $\dim\_{H}(\partial\mathbb{H}\_{core}, d\_{norm}) = \dim\_{H}(K\_{coll}, d\_{norm}) = 1$.

***<span class="accent">Доказательство</span>***.

(1) При $d = 2^{-k}$: $N\_{k}(\partial\mathbb{H}\_{core}) = \vert\mathrm{Spec}(\mathcal{L}\_{k})\vert = 2^{6\cdot 3^{k}}$, $\varepsilon\_{k} = 2^{-k}$, откуда $\underline{\dim}\_{B}(\partial\mathbb{H}\_{core}, d) = \lim\_{k} \frac{6\cdot 3^{k}\log 2}{k\log 2} = +\infty$; для $K\_{coll}$: $N\_{k}(K\_{coll}) = 2^{3^{k}} - 1$, $\underline{\dim}\_{B} = +\infty$. Так как $\dim\_{H} \leq \underline{\dim}\_{B}$, получаем $\dim\_{H} \leq +\infty$; нижняя оценка $\dim\_{H} \geq +\infty$ — по лемме Фростмана (масс-распределение ниже), $\dim\_{H} = +\infty$.

(2) При $d\_{norm}$: цилиндры уровня $k$ имеют диаметр ровно $\vert\mathrm{Spec}(\mathcal{L}\_{k})\vert^{-1}$; их число $N\_{k} = \vert\mathrm{Spec}(\mathcal{L}\_{k})\vert$, откуда $\underline{\dim}\_{B} = \lim\_{k} \frac{\log N\_{k}}{\log N\_{k}} = 1$. Верхняя оценка $\dim\_{H} \leq \dim\_{B} = 1$. Нижняя оценка ($\dim\_{H} \geq 1$): зададим вероятностную меру $\mu$ на цилиндрах уровня $k$ равенством $\mu(C\_{k}(u)) := 1/N\_{k}$ (равномерное распределение).

(3) Для любого шара $B$ уровня $k$ (clopen-цилиндр): $\mu(B) = 1/N\_{k} = \mathrm{diam}\_{norm}(B)^{1}$, то есть $\mu(B) \leq \mathrm{diam}(B)^{1}$. По лемме Фростмана (mass distribution principle) $\mathcal{H}^{1}(X) \geq 1 > 0$, значит $\dim\_{H}(X) \geq 1$. Для $K\_{coll}$: $\mu(C\_{k}(u)) := 1/(2^{3^{k}} - 1)$ (равномерно на $K\_{coll}$); для шара $B$ уровня $k$ имеем $\mu(B) \leq 2 \cdot (2^{3^{k}})^{-1} = 2\cdot \mathrm{diam}(B)$, откуда $\mathcal{H}^{1}(K\_{coll}) \geq 1/2 > 0$, значит $\dim\_{H}(K\_{coll}) \geq 1$. В итоге $\dim\_{H}(\cdot, d\_{norm}) = 1$. Мера $\mu$ счётно-аддитивна в ZF: цилиндры clopen, компактность даёт конечное подпокрытие для любого счётного открытого покрытия. $\square$

#### <span class="accent">— [Замечание VI.2]</span>
{: .courier #rem-VI-2}

При $d = 2^{-k}$ нижняя оценка $\dim\_{H} = +\infty$ через лемму Фростмана тривиальна ($\dim\_{B} = +\infty$ уже даёт $+\infty$ как верхнюю границу для любой меры, но у нас $\dim\_{H} = \dim\_{B} = +\infty$ по нижней оценке выше: любая мера даёт $\dim\_{H} \leq +\infty$, и $\dim\_{H} \geq +\infty$ следует из $N\_{k} \geq 2^{3^{k}}$ и масс-распределения с $\mu(B) \leq 2^{-3^{k}t}$ для любого $t > 0$).

#### <span class="accent">— [Теорема VI.3]</span>
{: .courier #thm-VI-3}

(а) $\partial\mathbb{H}\_{core} = V\_{0} \sqcup V\_{+}$, где $V\_{0} := \{\pi : \pi^{(0)} = \mathbf{0}\}$, $V\_{+} := \{\pi : \pi^{(0)} \neq \mathbf{0}\}$ — непустые clopen.

(б) $V\_{+}$ инвариантно вперёд относительно всех трёх сдвигов ($\sigma\_{r}(V\_{+}) \subseteq V\_{+}$), причём для $r \in \{1, 2\}$ включение строгое, а для $r = 3$ — равенство ($\sigma\_{3}(V\_{+}) = V\_{+}$). $V\_{0}$ отображается на всё пространство: $\sigma\_{r}(V\_{0}) = \partial\mathbb{H}\_{core}$.

(в) Ни $(\partial\mathbb{H}\_{core}, \sigma\_{r})$, ни $(\partial\mathbb{H}\_{brunn}, \sigma\_{r})$ не являются топологически транзитивными и не обладают свойством топологического перемешивания.

***<span class="accent">Доказательство</span>***.

(1) Из дискретности слоя 0 (а) — очевидно.

(2) Если $\pi \in V\_{+}$, то $T(\pi\_{1}^{(0)}, \pi\_{2}^{(0)}, \pi\_{3}^{(0)}) = \pi^{(0)} \neq \mathbf{0}$, откуда $\pi\_{r}^{(0)} \neq \mathbf{0}$ для всех $r$, т.е. $\sigma\_{r}(\pi) \in V\_{+}$. Для $r=1$ множество $\{j\_{i}\} = \{1,2,4,5\}$ не содержит $6$; если $\eta \in V\_{+}$ с $\eta^{(0)} = e\_{6}$, то $T(e\_{6}, v^{2}, v^{3}) = \mathbf{0}$ для любых $v^{2}, v^{3}$ (так как $(e\_{6})\_{j\_{i}} = 0$), значит $\sigma\_{1}^{-1}(\eta) \subseteq V\_{0}$, т.е. $\eta \notin \sigma\_{1}(V\_{+})$ — строгое включение.

(3) Для $r=2$: $\{k\_{i}\} = \{2,3,5,6\}$ не содержит $1$; если $\eta^{(0)} = e\_{1}$, то $T(v^{1}, e\_{1}, v^{3}) = \mathbf{0}$, значит $\eta \notin \sigma\_{2}(V\_{+})$ — строгое включение. Для $r=3$: $i \mapsto l\_{i}$ — биекция $\{4,5,6,1,2,3\}$; для любого $\eta \in V\_{+}$ точка $\pi := \Phi\_{core}(\mathbf{1}\_{\infty}, \mathbf{1}\_{\infty}, \eta)$ (где $\mathbf{1}\_{\infty} \in \partial\mathbb{H}\_{core}$ — [\[Определение VI.2\]](#def-VI-2)) имеет $\pi^{(0)}\_{i} = T(\mathbf{1}, \mathbf{1}, \eta^{(0)})\_{i} = 1 \cdot 1 \cdot \eta^{(0)}\_{l\_{i}} = \eta^{(0)}\_{l\_{i}}$; так как $l$ — биекция и $\eta^{(0)} \neq \mathbf{0}$, $\pi^{(0)} \neq \mathbf{0}$, т.е. $\pi \in V\_{+}$, и $\sigma\_{3}(\pi) = \eta$ — равенство. Для $V\_{0}$: при $\pi = \Phi\_{core}(\eta, \mathbf{0}\_{\infty}, \mathbf{0}\_{\infty})$ имеем $\sigma\_{1}(\pi) = \eta$ (аналогично для $r=2,3$).

(4) В силу $\sigma\_{r}^{n}(V\_{+}) \subseteq V\_{+}$ и $V\_{0} \cap V\_{+} = \varnothing$ имеем $V\_{+} \cap \sigma\_{r}^{-n}(V\_{0}) = \varnothing$ для всех $n \geq 0$; для $\partial\mathbb{H}\_{brunn}$ — $\{\mathbf{1}\_{\infty}\} \cap \sigma\_{r}^{-n}(K\_{coll}) = \varnothing$ [\[Теорема V.2\]](#thm-V-2). $\square$

#### <span class="accent">— [Замечание VI.3]</span>
{: .courier #rem-VI-3}

Динамическая асимметрия $\partial\mathbb{H}\_{core} = V\_{0} \sqcup V\_{+}$ структурно аналогична разложению $\partial\mathbb{H}\_{brunn} = \{\mathbf{1}\_{\infty}\} \sqcup K\_{coll}$, но не тождественна: в $\partial\mathbb{H}\_{brunn}$ инвариантное вперёд ядро $\{\mathbf{1}\_{\infty}\}$ — одна изолированная точка, тогда как в $\partial\mathbb{H}\_{core}$ ядро $V\_{+}$ — несчётное clopen, строго вложенное в себя под действием $\sigma\_{1}, \sigma\_{2}$.

#### <span class="accent">— [Лемма VI.2]</span>
{: .courier #lem-VI-2}

(а) В $\partial\mathbb{H}\_{brunn}$ множество общих неподвижных точек $\sigma\_{1}, \sigma\_{2}, \sigma\_{3}$ плотно.

(б) В $\partial\mathbb{H}\_{core}$ точки $\mathbf{0}\_{\infty} \in V\_{0}$, $\mathbf{1}\_{\infty} \in V\_{+}$ — общие неподвижные точки всех $\sigma\_{r}$, но множество неподвижных не плотно.

***<span class="accent">Доказательство</span>***.

(1) Любое непустое базовое clopen $U \subseteq \partial\mathbb{H}\_{brunn}$ задаётся фиксацией $u^{(k)} \in \{0,1\}^{3^{k}}$ на уровне $k$. В силу идемпотентности $a \cdot a \cdot a = a^{3} = a$ в $\mathbb{F}\_{2}$, тройка $(u^{(k)}, u^{(k)}, u^{(k)})$ проектируется в $u^{(k)}$ при $(\alpha\_{k}')^{*}$. Рекурсивно для всех $m \geq k$ получаем $\pi \in U$, для которой $\Phi\_{brunn}^{-1}(\pi) = (\pi, \pi, \pi)$, откуда $\sigma\_{r}(\pi) = p\_{r}(\Phi^{-1}(\pi)) = p\_{r}(\pi,\pi,\pi) = \pi$ для всех $r$.

(2) Для $\mathbf{0}\_{\infty}, \mathbf{1}\_{\infty}$ неподвижность следует из $T(\mathbf{0}, \mathbf{0}, \mathbf{0}) = \mathbf{0}$, $T(\mathbf{1}, \mathbf{1}, \mathbf{1}) = \mathbf{1}$. Clopen $\{\pi \in \partial\mathbb{H}\_{core} : \pi^{(0)} = e\_{1}\}$ не содержит неподвижных точек $\sigma\_{1}$: если $\sigma\_{1}(\pi) = \pi$ и $\pi^{(0)} = e\_{1}$, то $\pi\_{1}^{(0)} = e\_{1}$ (так как $\sigma\_{1}(\pi)^{(0)} = p\_{1}(\Phi^{-1}(\pi))^{(0)} = \pi\_{1}^{(0)}$), и $T(e\_{1}, \pi\_{2}^{(0)}, \pi\_{3}^{(0)}) = \pi^{(0)} = e\_{1}$; но $T(e\_{1}, v^{2}, v^{3})\_{1} = (e\_{1})\_{j\_{1}} \cdot (v^{2})\_{k\_{1}} \cdot (v^{3})\_{l\_{1}} = (e\_{1})\_{2} \cdot \ldots = 0 \neq 1 = (e\_{1})\_{1}$ — противоречие. Значит $\pi\_{1}^{(0)} \neq e\_{1}$, т.е. $\sigma\_{1}(\pi)^{(0)} \neq \pi^{(0)}$ — не неподвижна. $\square$

#### <span class="accent">— [Замечание VI.4]</span>
{: .courier #rem-VI-4}

Границы Раздела VI:

(а) Классификация периодических орбит произвольных периодов $p \geq 2$ в $\partial\mathbb{H}\_{core}$ не проводится.

(б) Проективно согласованная равномерная послойная мера (равный вес $1/\vert\mathrm{Spec}(\mathcal{L}\_{k})\vert$ всем точкам слоя $k$) не образует проективной системы при $\alpha\_{k}^{\ast}$, поскольку мощности слоёв $(\alpha\_{k}^{\ast})^{-1}(p)$ непостоянны ($7^{z(q)}$ для $\partial\mathbb{H}\_{brunn}$, зависимость от $p\_{t}$ для $\partial\mathbb{H}\_{core}$); тривиальные $\sigma\_{r}$-инвариантные меры Дирака в точках $\mathbf{0}\_{\infty}$, $\mathbf{1}\_{\infty}$ существуют; построение неатомарных эргодических $\sigma\_{r}$-инвариантных мер остаётся за рамками и не является необходимым для Раздела VI.

(в) Аттракторные свойства в смысле сходимости орбит не устанавливаются.

---

#### <span class="accent">— [Интуитивное описание VI]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

С $\partial\mathbb{H}\_{core}$, $\partial\mathbb{H}\_{brunn}$ с динамикой $\sigma\_{r}$ ([Раздел V](#prt-V)). Формализм не запрещает ввести метрику, энтропию, матрицу подстановки.

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Ввели подстановку $\theta$ и матрицу $M$ [\[Определение VI.1\]](#def-VI-1); разделили уровни (типовая сетка vs спектр) [\[Замечание VI.1\]](#rem-VI-1); определили $\mathbf{0}\_{\infty}, \mathbf{1}\_{\infty} \in \partial\mathbb{H}\_{core}$ [\[Определение VI.2\]](#def-VI-2) и ультраметрики [\[Определение VI.3\]](#def-VI-3).

(б) Доказали сдвиг уровней [\[Лемма VI.1\]](#lem-VI-1); $h\_{top}(\sigma\_{r}) = +\infty$ [\[Теорема VI.1\]](#thm-VI-1); no-mixing и расщепление $V\_{0} \sqcup V\_{+}$ [\[Теорема VI.3\]](#thm-VI-3); вычислили $\dim\_{H}$ через $\dim\_{B}$ и лемму Фростмана [\[Теорема VI.2\]](#thm-VI-2); плотность/неплотность неподвижных [\[Лемма VI.2\]](#lem-VI-2).

**3. <span class="accent">К чему пришли</span>?**

$h\_{top}(\sigma\_{r}) = +\infty$ на обоих пространствах; $\dim\_{H} = +\infty$ при $d = 2^{-k}$, $\dim\_{H} = 1$ при $d\_{norm}$ (через $\dim\_{B}$ и лемму Фростмана); $\partial\mathbb{H}\_{core} = V\_{0} \sqcup V\_{+}$ с $V\_{+}$ инвариантным вперёд (строго для $r=1,2$; сюръекция для $r=3$); $\sigma\_{r}(V\_{0}) = \partial\mathbb{H}\_{core}$; no-mixing; неподвижные точки плотны в $\partial\mathbb{H}\_{brunn}$, не плотны в $\partial\mathbb{H}\_{core}$.

**4. <span class="accent">Что это значит сейчас</span>?**

Получили динамическую структуру на континуальных спектрах: бесконечная энтропия, бесконечная размерность (при $d=2^{-k}$), инвариантное расщепление с асимметрией.

---

### **Раздел VII. Противоречие**
{: .accent #prt-VII}

#### <span class="accent">— [Определение VII.1]</span>
{: .courier #def-VII-1}

Шесть рамок:

(а) $\mathcal{R}\_{1} = \mathbf{PROP}\_{\Sigma}$: свободные $\Sigma$-цветные PROP ([Раздел I](#prt-I)).

(б) $\mathcal{R}\_{2} = \mathbf{BoolAlg}$: коммутативные идемпотентные $\mathbb{F}\_{2}$-алгебры с единицей ([Раздел II](#prt-II)).

(в) $\mathcal{R}\_{3} = \mathbf{Coalg}\_{F}(\mathbf{BoolAlg})$: $F$-коалгебры в $\mathbf{BoolAlg}$ ([Раздел III](#prt-III)).

(г) $\mathcal{R}\_{4} = \mathbf{Stone}$: компактные хаусдорфовы нульмерные пространства ([Раздел IV](#prt-IV)).

(д) $\mathcal{R}\_{5} = \mathbf{Dyn}(\mathbf{Stone})$: пары $(X, (\sigma\_{1}, \sigma\_{2}, \sigma\_{3}))$ с непрерывными $\sigma\_{r}: X \to X$ ([Раздел V](#prt-V)).

(е) $\mathcal{R}\_{6} = \mathbf{UMetDyn}$: $(X, (\sigma\_{1}, \sigma\_{2}, \sigma\_{3}), d)$ с ультраметрикой $d$, согласованной с топологией ([Раздел VI](#prt-VI)).

#### <span class="accent">— [Определение VII.2]</span>
{: .courier #def-VII-2}

Смена рамки $\mathcal{R}\_{i} \to \mathcal{R}\_{i+1}$ — функтор между соседними рамками (направление указано в таблице [\[Теорема VII.1\]](#thm-VII-1)), который не отражает изоморфизмы: существуют объекты $A, A' \in \mathcal{R}\_{i+1}$ с $A \not\cong A'$, но $F(A) \cong F(A')$ в $\mathcal{R}\_{i}$.

Инвариант $I$ уровня $\mathcal{R}\_{i+1}$ невыразим в $\mathcal{R}\_{i}$, если $I(A) \neq I(A')$ для таких $A, A'$.

#### <span class="accent">— [Теорема VII.1]</span>
{: .courier #thm-VII-1}

Конструкция Разделов I–VI реализуется как зигзаг из пяти функторов между шестью рамками. Каждый функтор не отражает изоморфизмы (примеры в таблице). Ни один из пяти функторов не запрещён в ZF; ни один не вынуждается внутренней дедукцией предыдущей рамки.

| Смена | Переход | Функтор | Пример склейки | Инвариант, невыразимый в $\mathcal{R}\_{i}$ |
|---|---|---|---|---|
| 1 | $\mathcal{R}\_{1} \to \mathcal{R}\_{2}$ (I → II) | $\mathrm{Sem}: \mathbf{PROP}\_{\Sigma} \to \mathbf{BoolAlg}$ (ковариантный) | $\mathcal{G}\_{1}$ с $\alpha^{(1)}\_{1}: 1 \to 2\otimes 2\otimes 4$ и $\mathcal{G}\_{2}$ с $\alpha^{(2)}\_{1}: 1 \to 2\otimes 4\otimes 4$: в $B\_{6}$ оба дают $x\_{2}x\_{4}$ (по идемпотентности $x^{2} = x$), но мультимножества $\{2,2,4\} \neq \{2,4,4\}$ не эквивалентны никакой симметрией, значит $\mathbf{C}(\mathcal{G}\_{1}) \not\cong \mathbf{C}(\mathcal{G}\_{2})$ в $\mathbf{PROP}\_{\Sigma}$ | Булева структура (аксиома $x\_{i}^{2} = x\_{i}$); свойства объекта: $V(I) = \{\mathbf{0}, \mathbf{1}\}$, $I + \langle x\_{i}\rangle = \mathfrak{m}$ |
| 2 | $\mathcal{R}\_{2} \to \mathcal{R}\_{3}$ (II → III) | $U\_{2}: \mathbf{Coalg}\_{F}(\mathbf{BoolAlg}) \to \mathbf{BoolAlg}$, $(H, \omega) \mapsto H$ (забывающий) | $(B\_{6}, \alpha)$ с $\alpha$ [\[Определение III.2\]](#def-III-2) (инъективно, [\[Лемма III.1\]](#lem-III-1)) и $(B\_{6}, \alpha\_{\mathrm{triv}})$ с $\alpha\_{\mathrm{triv}}(x\_{i}) = x\_{1} \otimes x\_{1} \otimes x\_{1}$ (не инъективно: $\alpha\_{\mathrm{triv}}(x\_{1} + x\_{2}) = 0$); инъективность $\omega$ — инвариант изоморфизма коалгебр, значит $(B\_{6}, \alpha) \not\cong (B\_{6}, \alpha\_{\mathrm{triv}})$ | Копредел $\mathbb{H}\_{core}$, изоморфизм $\mathbb{H} \cong \mathbb{H}^{\otimes 3}$ |
| 3 | $\mathcal{R}\_{3} \to \mathcal{R}\_{4}$ (III → IV) | $\mathrm{Spec}: \mathbf{Coalg}\_{F}(\mathbf{BoolAlg}) \to \mathbf{Stone}$ (ковариантный на объектах, контравариантный на морфизмах) | $(H, \omega\_{\mathrm{core}})$ и $(H, \omega\_{\mathrm{deg}})$ на $H \cong \mathrm{FreeBool}(\aleph\_{0})$, где $\omega\_{\mathrm{deg}}(a) = \varepsilon(a) \cdot (1 \otimes 1 \otimes 1)$ для $\varepsilon \in \mathrm{Spec}(H)$; $\omega\_{\mathrm{deg}}$ не инъективно ($\ker\varepsilon \neq \{0\}$), значит $(H, \omega\_{\mathrm{core}}) \not\cong (H, \omega\_{\mathrm{deg}})$ | Глобальные оценки, $\partial\mathbb{H}\_{core}$; единственный атом $e\_{\mathbf{1}}$ в $\mathbb{H}\_{brunn}$ и соответствующая изолированная точка $\mathbf{1}\_{\infty}$ в $\partial\mathbb{H}\_{brunn}$ |
| 4 | $\mathcal{R}\_{4} \to \mathcal{R}\_{5}$ (IV → V) | $U\_{4}: \mathbf{Dyn}(\mathbf{Stone}) \to \mathbf{Stone}$, $(X, \sigma\_{r}) \mapsto X$ (забывающий) | $(2^{\omega}, \mathrm{id})$ и $(2^{\omega}, \sigma\_{r})$: $U\_{4}$ одинаково, но $h\_{top}(\mathrm{id}) = 0 \neq +\infty = h\_{top}(\sigma\_{r})$, значит динамики неизоморфны | Необратимые сюръекции $\sigma\_{r}$, достижимость $\mathbf{1}\_{\infty}$; топологическая энтропия $h\_{top}(\sigma\_{r}) = +\infty$ |
| 5 | $\mathcal{R}\_{5} \to \mathcal{R}\_{6}$ (V → VI) | $U\_{5}: \mathbf{UMetDyn} \to \mathbf{Dyn}(\mathbf{Stone})$, $(X, \sigma\_{r}, d) \mapsto (X, \sigma\_{r})$ (забывающий) | $(\partial\mathbb{H}\_{core}, \sigma\_{r}, d)$ и $(\partial\mathbb{H}\_{core}, \sigma\_{r}, d\_{norm})$: $U\_{5}$ одинаково, $\dim\_{H} = +\infty$ vs $1$ | $\dim\_{H} = +\infty$ (при $d = 2^{-k}$), $\dim\_{H} = 1$ (при $d\_{norm}$) |

***<span class="accent">Доказательство</span>***.

Для каждой смены — предъявлен функтор и пара неизоморфных объектов $\mathcal{R}\_{i+1}$ с изоморфными образами в $\mathcal{R}\_{i}$.

(1) $\mathrm{Sem}$: в $B\_{6}$ выполнено $x^{2} = x$, значит $\mathrm{Sem}(\alpha^{(1)}\_{1})(x\_{1}) = x\_{2} \cdot x\_{2} \cdot x\_{4} = x\_{2}x\_{4} = x\_{2} \cdot x\_{4} \cdot x\_{4} = \mathrm{Sem}(\alpha^{(2)}\_{1})(x\_{1})$; тем самым $\mathrm{Sem}(\mathcal{G}\_{1}) = \mathrm{Sem}(\mathcal{G}\_{2})$. В $\mathbf{C}(\mathcal{G}\_{1})$ генератор $\alpha^{(1)}\_{1}$ имеет кодомен-слово $2 \otimes 2 \otimes 4$; в $\mathbf{C}(\mathcal{G}\_{2})$ — слово $2 \otimes 4 \otimes 4$; симметрии $\sigma$ переставляют множители, но не меняют кратностей; мультимножества $\{2,2,4\} \neq \{2,4,4\}$, значит слова неизоморфны в $\mathbf{PROP}\_{\Sigma}$, значит $\mathbf{C}(\mathcal{G}\_{1}) \not\cong \mathbf{C}(\mathcal{G}\_{2})$.

(2) $U\_{2}$: $(B\_{6}, \alpha) \not\cong (B\_{6}, \alpha\_{\mathrm{triv}})$, так как $\alpha$ инъективно [\[Лемма III.1\]](#lem-III-1)), а $\alpha\_{\mathrm{triv}}$ — нет; инъективность структурного морфизма сохраняется при изоморфизме коалгебр. При этом $U\_{2}(B\_{6}, \alpha) = B\_{6} = U\_{2}(B\_{6}, \alpha\_{\mathrm{triv}})$.

(3) $\mathrm{Spec}$: для счётной $H \cong \mathrm{FreeBool}(\aleph\_{0})$ все коалгебры дают $\mathrm{Spec}(H) \cong 2^{\omega}$ [\[Замечание IV.1\]](#rem-IV-1); $\omega\_{\mathrm{deg}}(a) = \varepsilon(a) \cdot (1\otimes 1\otimes 1)$ — гомоморфизм булевых алгебр с $\ker\varepsilon \neq \{0\}$, не инъективен; $\omega\_{\mathrm{core}}$ инъективен [\[Теорема III.1\]](#thm-III-1)); значит $(H, \omega\_{\mathrm{core}}) \not\cong (H, \omega\_{\mathrm{deg}})$, но $\mathrm{Spec}(H)$ в обоих случаях гомеоморфен $2^{\omega}$.

(4) $U\_{4}$: $\mathrm{id}$ на $2^{\omega}$ имеет $h\_{top} = 0$; сдвиги $\sigma\_{r}$ — $h\_{top} = +\infty$ ([\[Теорема VI.1\]](#thm-VI-1), топологический инвариант, метрика не используется); значит $(2^{\omega}, \mathrm{id}) \not\cong (2^{\omega}, \sigma\_{r})$, но $U\_{4}$ стирает сдвиги, давая один и тот же объект $2^{\omega}$ в $\mathbf{Stone}$.

(5) $U\_{5}$: $(\partial\mathbb{H}\_{core}, \sigma\_{r}, d)$ и $(\partial\mathbb{H}\_{core}, \sigma\_{r}, d\_{norm})$ [\[Теорема VI.2\]](#thm-VI-2) имеют разные $\dim\_{H}$ ($+\infty$ vs $1$), значит неизоморфны в $\mathbf{UMetDyn}$; но $U\_{5}$ стирает $d$, давая один и тот же $(\partial\mathbb{H}\_{core}, \sigma\_{r})$. $\square$

#### <span class="accent">— [Теорема VII.1]</span>
{: .courier #rem-VII-1}

$h\_{top}$ — инвариант рамки $\mathcal{R}\_{5}$ (топологическая динамика), не $\mathcal{R}\_{6}$: в $\mathbf{Dyn}(\mathbf{Stone})$ уже $h\_{top}(\sigma\_{r}) = +\infty$ ([\[Теорема VI.1\]](#thm-VI-1) не использует метрику). Метрика $d$ в $\mathcal{R}\_{6}$ добавляет только $\dim\_{H}$ (метрический инвариант), зависящий от выбора $d$: $+\infty$ при $d = 2^{-k}$, $1$ при $d\_{norm}$.

#### <span class="accent">— [Теорема VII.2]</span>
{: .courier #thm-VII-2}

Ни одна из шести рамок $\mathcal{R}\_{1}, \dots, \mathcal{R}\_{6}$ не покрывает цепь I–VI целиком: ни один из пяти функторов зигзага

$$
\mathcal{R}_{1} \xrightarrow{\ \mathrm{Sem}\ } \mathcal{R}_{2} \xleftarrow{\ U_{2}\ } \mathcal{R}_{3} \xrightarrow{\ \mathrm{Spec}\ } \mathcal{R}_{4} \xleftarrow{\ U_{4}\ } \mathcal{R}_{5} \xleftarrow{\ U_{5}\ } \mathcal{R}_{6}
$$

не является эквивалентностью категорий; $\mathcal{R}\_{6}$ не покрывает $\mathcal{R}\_{1}$–$\mathcal{R}\_{3}$ (в $\mathcal{R}\_{6}$ нет ни синтаксиса $\mathbf{PROP}\_{\Sigma}$, ни алгебраических операций $\mathbf{BoolAlg}$, ни коалгебраической структуры $\omega$).

***<span class="accent">Доказательство</span>***.

Каждый функтор зигзага не отражает изоморфизмы [\[Теорема VII.1\]](#thm-VII-1), значит не является эквивалентностью. Каждая рамка $\mathcal{R}\_{1}$–$\mathcal{R}\_{6}$ теряет при переходе к соседней хотя бы один инвариант. Композиция функторов зигзага не определена (направления стрелок несовместимы); цепь I–VI существует как путь по зигзагу, а не как один функтор. $\square$

#### <span class="accent">— [Следствие VII.1]</span>
{: .courier #cor-VII-1}

Траектория по зигзагу $\mathcal{R}\_{1} \to \dots \to \mathcal{R}\_{6}$ связывает все внутренние уровни конструкции I–VI, оставляя неразрешённым единственное открытое звено: статус выбора исходной сигнатуры $\mathcal{G} = (\Sigma, \mathcal{F})$ в Разделе I (искусственная артикуляция). Выбор $\mathcal{G}$ лежит в основе $\mathcal{R}\_{1}$ и не обосновывается ни одной из рамок $\mathcal{R}\_{1}$–$\mathcal{R}\_{6}$; в рамках I–VI этот выбор не обосновывается.

***<span class="accent">Доказательство</span>***.

Ни одна рамка не покрывает цепь [\[Теорема VII.2\]](#thm-VII-2). Выбор $\mathcal{G} = (\Sigma, \mathcal{F})$ определяет $\mathbf{C}$ и тем самым $\mathcal{R}\_{1}$; его обоснование не входит ни в одну из рамок $\mathcal{R}\_{1}$–$\mathcal{R}\_{6}$. $\square$

#### <span class="accent">— [Замечание VII.2]</span>
{: .courier #rem-VII-2}

Раздел VII не утверждает логического противоречия вида $A \wedge \neg A$ (метатеория ZF остаётся непротиворечивой) и не утверждает замыкание цепи. Его предмет:

(а) Зигзаг из пяти функторов, не отражающих изоморфизмы.

(б) Невозможность удержания всей структуры внутри одной классической рамки.

(в) Открытое звено — выбор $\mathcal{G}$ (искусственная артикуляция, Раздел I), не обоснованный в I–VI.

---

#### <span class="accent">— [Интуитивное описание VII]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

С цепи I–VI. Формализм не запрещает взять всю цепь как единый объект и рассмотреть её структуру.

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Определили рамки $\mathcal{R}\_{1}$–$\mathcal{R}\_{6}$ [\[Определение VII.1\]](#def-VII-1) и смены рамок как функторы, не отражающие изоморфизмы [\[Определение VII.2\]](#def-VII-2).

(б) Доказали: зигзаг из пяти функторов с явными примерами склейки [\[Теорема VII.1\]](#thm-VII-1); ни одна рамка не покрывает цепь [\[Теорема VII.2\]](#thm-VII-2); открытое звено — выбор $\mathcal{G}$ (искусственная артикуляция) [\[Следствие VII.1\]](#cor-VII-1).

**3. <span class="accent">К чему пришли</span>?**

Цепь I–VI реализуется как зигзаг пяти функторов $\mathrm{Sem}$, $U\_{2}$, $\mathrm{Spec}$, $U\_{4}$, $U\_{5}$, каждый не отражает изоморфизмы. Ни одна рамка не покрывает цепь. Открытое звено — выбор $\mathcal{G}$.

**4. <span class="accent">Что это значит сейчас</span>?**

Получили точную картину цепи I–VI как зигзага функторов с открытым звеном.

---

### **Раздел VIII. Естественная артикуляция**
{: .accent #prt-VIII}

Всё дальнейшее ведётся в ZF без AC.

#### <span class="accent">— [Определение VIII.1]</span>
{: .courier #def-VIII-1}

Класс допустимых презентаций $\mathfrak{P}\_{6}$ — все 6-сортовые тернарные сигнатуры $\mathcal{G} = (\Sigma, \mathcal{F})$ ($\vert\Sigma\vert = 6$, $\mathcal{F} = \{\alpha\_{i}: i \to j\_{i} \otimes k\_{i} \otimes l\_{i}\}\_{i \in \Sigma}$), удовлетворяющие:

(а) Отсутствие самоссылок и различие множителей в каждом триплете.

(б) Сильная связность и примитивность матрицы инцидентности $M$ ($M^{3} > 0$).

(в) Наличие уникальных свидетелей координат, обеспечивающих инъективность $\alpha\_{0}: B\_{6} \hookrightarrow B\_{6}^{\otimes 3}$.

Для $\mathcal{G} \in \mathfrak{P}\_{6}$ через $\mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F}) \leq S\_{6}$ обозначим группу перестановок, сохраняющих упорядоченные тройки $(j\_{i}, k\_{i}, l\_{i})$.

#### <span class="accent">— [Замечание VIII.1]</span>
{: .courier #rem-VIII-1}

Параметры $(6, 3)$ — число сортов и арность — зафиксированы в определении $\mathfrak{P}\_{6}$ как выбор, а не выведены из более общих принципов. Вопрос о минимальности пары $(6, 3)$ (существуют ли сильно связные конъюнктивные сети с меньшим числом сортов или арности 2, допускающие одновременно свидетелей инъективности и нетривиальную динамическую асимметрию) в настоящем разделе не ставится и не решается. Внутри фиксированного класса $\mathfrak{P}\_{6}$ устанавливается единственность $\mathcal{F}$ с точностью до $\mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F})$ [\[Теорема VIII.2\]](#thm-VIII-2)).

#### <span class="accent">— [Теорема VIII.1]</span>
{: .courier #thm-VIII-1}

В $\mathbf{BoolAlg}$ счётная безатомная булева алгебра $\mathrm{FreeBool}(\aleph\_{0})$ (любой объект, изоморфный $\mathbb{H}\_{core}(\mathcal{G})$) не определяет канонического коалгебраического эндоморфизма $\omega: \mathrm{FreeBool}(\aleph\_{0}) \to F(\mathrm{FreeBool}(\aleph\_{0}))$, порождающего структуру I–VI:

(1) любые две $\mathcal{G}, \mathcal{G}' \in \mathfrak{P}\_{6}$ дают $\mathbb{H}\_{core}(\mathcal{G}) \cong \mathbb{H}\_{core}(\mathcal{G}') \cong \mathrm{FreeBool}(\aleph\_{0})$;

(2) на $\mathrm{FreeBool}(\aleph\_{0})$ существуют коалгебраические структуры, не изоморфные ни одной $(\mathbb{H}\_{core}(\mathcal{G}), \omega\_{core}(\mathcal{G}))$;

(3) без выбора $\mathcal{G} \in \mathfrak{P}\_{6}$ коалгебраическая динамика I–VI не определена.

***<span class="accent">Доказательство</span>***.

(1) [\[Теорема III.2\]](#thm-III-2), [\[Лемма IV.2\]](#lem-IV-2) + теорема Кантора: все счётные безатомные булевы алгебры изоморфны $\mathrm{FreeBool}(\aleph\_{0})$.

(2) Зафиксируем $\varepsilon \in \mathrm{Spec}(H)$ для $H = \mathrm{FreeBool}(\aleph\_{0})$; определим $\omega\_{\mathrm{deg}}: H \to H^{\otimes 3}$ правилом $\omega\_{\mathrm{deg}}(a) = \varepsilon(a) \cdot (1 \otimes 1 \otimes 1)$. Гомоморфизм булевых алгебр: $\omega\_{\mathrm{deg}}(a \wedge b) = \varepsilon(a \wedge b)(1\otimes 1\otimes 1) = \varepsilon(a)\varepsilon(b)(1\otimes 1\otimes 1) = \omega\_{\mathrm{deg}}(a)\omega\_{\mathrm{deg}}(b)$; $\omega\_{\mathrm{deg}}(1) = 1$; $\omega\_{\mathrm{deg}}(a \vee b) = \omega\_{\mathrm{deg}}(a) + \omega\_{\mathrm{deg}}(b) + \omega\_{\mathrm{deg}}(a \wedge b)$. Не инъективен: $\ker\varepsilon \neq \{0\}$ (ядро характера в безатомной алгебре бесконечно), $\omega\_{\mathrm{deg}}(\ker\varepsilon) = 0$. При этом $\omega\_{core}(\mathcal{G})$ инъективен [\[Лемма III.1\]](#lem-III-1)); инъективность — инвариант изоморфизма коалгебр. Значит $(H, \omega\_{\mathrm{deg}}) \not\cong (\mathbb{H}\_{core}(\mathcal{G}), \omega\_{core}(\mathcal{G}))$.

(3) Из (1) и (2): $\mathrm{FreeBool}(\aleph\_{0})$ не выделяет $\omega\_{core}(\mathcal{G})$ без $\mathcal{G} \in \mathfrak{P}\_{6}$. $\square$

#### <span class="accent">— [Лемма VIII.1]</span>
{: .courier #lem-VIII-1}

Для любой $\mathcal{G} \in \mathfrak{P}\_{6}$:

(а) в $(\mathbb{H}\_{core}(\mathcal{G}), \omega\_{core}(\mathcal{G}))$ подкоалгебра $\iota\_{0}(B\_{6})$ — единственная минимальная нетривиальная конечная подкоалгебра;

(б) $\mathrm{Aut}(\mathbb{H}\_{core}(\mathcal{G}), \omega\_{core}(\mathcal{G})) \cong \mathrm{Aut}(B\_{6}, \alpha\_{0}) \cong \mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F})$.

***<span class="accent">Доказательство</span>***.

(1) Пусть $C \subset \mathbb{H}\_{core}$ — конечная подкоалгебра, $C \neq \mathbb{F}\_{2}$. Тогда $C \subseteq \iota\_{m}(\mathcal{L}\_{m})$ при некотором $m \geq 0$, и двойственно $C$ задаётся конгруэнцией $\approx$ на $(\mathbb{F}\_{2}^{6})^{3^{m}}$, согласованной с $T^{\times 3^{m}}$. Изоляция произвольной различающейся координаты $t\_{0} \in \{1, \ldots, 3^{m}\}$ нулевыми масками на $t \neq t\_{0}$ (в силу $T(x, \mathbf{0}, \mathbf{0}) = \mathbf{0}$) и сильная связность в $t\_{0}$-м блоке влекут распад $\approx$ в прямое произведение $\approx\_{1} \times \cdots \times \approx\_{3^{m}}$, где каждая $\approx\_{t}$ либо тривиальна, либо полна (отсутствие собственных нетривиальных конгруэнций на $\mathbb{F}\_{2}^{6}$). Инвариантность относительно $\alpha\_{m}$ даёт $C = \mathcal{L}\_{m}$.

(2) Проверим, что $\iota\_{0}(B\_{6})$ — подкоалгебра: $\omega\_{core}(\iota\_{0}(x)) = \iota\_{1}(\alpha\_{0}(x))$ [\[Следствие III.3\]](#cor-III-3), $\alpha\_{0}(x) \in \mathcal{L}\_{1} = B\_{6}^{\otimes 3}$, значит $\iota\_{1}(\alpha\_{0}(x)) \in \iota\_{1}(\mathcal{L}\_{1}) = \iota\_{0}(B\_{6})^{\otimes 3}$ (в $\mathbb{H}\_{core}$). При $m \geq 1$: $\iota\_{0}(B\_{6}) = \iota\_{m}(\alpha\_{m-1} \circ \cdots \circ \alpha\_{0}(B\_{6})) \subsetneq \iota\_{m}(\mathcal{L}\_{m})$ (размерности $64 < 2^{6\cdot 3^{m}}$). Значит $C = \mathcal{L}\_{m}$ при $m \geq 1$ не минимальна (содержит строго меньшую $\iota\_{0}(B\_{6})$). Следовательно $m = 0$ и $C = \iota\_{0}(B\_{6})$.

(3) В силу единственности $\iota\_{0}(B\_{6})$ любой автоморфизм $\Psi$ пары сохраняет $\iota\_{0}(B\_{6})$, значит однозначно определяется ограничением $\varphi$ на $\mathrm{Spec}(B\_{6}) = \mathbb{F}\_{2}^{6}$.

Шаг 1: $\varphi(\mathbf{0}) = \mathbf{0}$, $\varphi(\mathbf{1}) = \mathbf{1}$. Из $V(I) = \{\mathbf{0}, \mathbf{1}\}$ и $T(\varphi(\mathbf{0}), \varphi(\mathbf{0}), \varphi(\mathbf{0})) = \varphi(\mathbf{0})$: $\varphi(\mathbf{0}) \in V(I)$. Если $\varphi(\mathbf{0}) = \mathbf{1}$, то для $v^{2}$ с $\varphi(v^{2}) = \mathbf{0}$ (сюръективность) $\mathbf{1} = \varphi(\mathbf{0}) = \varphi(T(\mathbf{0}, v^{2}, \mathbf{1})) = T(\mathbf{1}, \mathbf{0}, \varphi(\mathbf{1})) = \mathbf{0}$ — противоречие.

Шаг 2: $\varphi$ коммутирует с $P\_{1}, P\_{2}, P\_{3}$, где $(P\_{1}u)\_{i} = u\_{j\_{i}}$, $(P\_{2}u)\_{i} = u\_{k\_{i}}$, $(P\_{3}u)\_{i} = u\_{l\_{i}}$. Подстановка констант $\mathbf{1}$ на две из трёх позиций в $\varphi(T(v^{1}, v^{2}, v^{3})) = T(\varphi v^{1}, \varphi v^{2}, \varphi v^{3})$ даёт $\varphi(P\_{r} u) = P\_{r}\varphi(u)$ для $r = 1,2,3$.

Шаг 3: сильная связность $\mathcal{G}$ влечёт $\bigcup\_{i}\{j\_{i}\} \cup \bigcup\_{i}\{k\_{i}\} \cup \bigcup\_{i}\{l\_{i}\} = \Sigma$: если вершина $m$ не входит ни в один кодомен, у неё нет входящих рёбер, значит она недостижима, что противоречит сильной связности.

Шаг 4: сохраняется порядок $x \le y$ (покомпонентно в $\mathbb{F}\_{2}^{6}$). Эквивалентность: $x \le y \iff \forall r \in \{1,2,3\}: P\_{r}(x) \le P\_{r}(y)$ (покомпонентно). (⇒) очевидно. (⇐) если $x \not\le y$, существует $m$ с $x\_{m} = 1$, $y\_{m} = 0$; по шагу 3 $m \in \{j\_{i}, k\_{i}, l\_{i}\}$ для некоторого $i$ и некоторого $r$; тогда $(P\_{r}x)\_{i} = x\_{m} = 1 > 0 = y\_{m} = (P\_{r}y)\_{i}$ — нарушение. Из $\varphi(\mathbf{0}) = \mathbf{0}$ и коммутирования с $P\_{r}$: $\varphi(x) \le \varphi(y) \iff x \le y$. Значит $\varphi$ — автоморфизм порядка, т.е. автоморфизм булевой решётки $\mathbb{F}\_{2}^{6}$; переставляет атомы: $\varphi(e\_{m}) = e\_{\pi(m)}$ для $\pi \in S\_{6}$.

Шаг 5: сплетение $\varphi(T(v^{1}, v^{2}, v^{3})) = T(\varphi v^{1}, \varphi v^{2}, \varphi v^{3})$ влечёт $\pi(j\_{i}) = j\_{\pi(i)}$, $\pi(k\_{i}) = k\_{\pi(i)}$, $\pi(l\_{i}) = l\_{\pi(i)}$, т.е. $\pi \in \mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F})$. $\square$

#### <span class="accent">— [Теорема VIII.2]</span>
{: .courier #thm-VIII-2}

(а) $\mathcal{G}, \mathcal{G}' \in \mathfrak{P}\_{6}$ дают изоморфные коалгебры $(\mathbb{H}\_{core}(\mathcal{G}), \omega\_{core}(\mathcal{G})) \cong (\mathbb{H}\_{core}(\mathcal{G}'), \omega\_{core}(\mathcal{G}'))$ $\iff$ $\mathcal{G}' = \pi(\mathcal{G})$ для $\pi \in \mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F})$.

(б) Класс $\mathfrak{P}\_{6}$ не сводится к единственному типу симметрии: для $\mathcal{F}$ из [Раздела I](#prt-I) $\mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F}) = \{\mathrm{id}, P\_{3}\} \cong \mathbb{Z}\_{2}$, $P\_{3} = (1\,4)(2\,5)(3\,6)$; для $\mathcal{F}'$ ($1 \to 2\otimes 3\otimes 4$, $2 \to 1\otimes 3\otimes 5$, $3 \to 1\otimes 2\otimes 6$, $4 \to 1\otimes 2\otimes 3$, $5 \to 1\otimes 3\otimes 2$, $6 \to 4\otimes 5\otimes 1$) $\mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F}') = \{\mathrm{id}\}$.

***<span class="accent">Доказательство</span>***.

(1) Изоморфизм коалгебр переводит единственную минимальную подкоалгебру $\iota\_{0}(B\_{6})$ в $\iota\_{0}'(B\_{6}')$ [\[Лемма VIII.1\]](#lem-VIII-1) а), откуда $\mathcal{F}' = \pi(\mathcal{F})$ для $\pi \in \mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F})$ [\[Лемма VIII.1\]](#lem-VIII-1) б).

(2) Для $\mathcal{F}$ перебор по инвариантным парам $P\_{3}$ и уникальным свидетелям $j\_{1} = 2$, $j\_{4} = 5$, $k\_{3} = 2$, $k\_{6} = 5$ оставляет $\{\mathrm{id}, P\_{3}\}$. Для $\mathcal{F}'$: (i) отсутствие самоссылок и различие множителей — прямая проверка по каждой строке; (ii) сильная связность: из $1$ достижимы $\{2,3,4\}$, из них — $\{1,2,3,4,5,6\}$ (например, $4 \to 1, 2, 3$; $3 \to 6$; $2 \to 5$), значит все; (iii) свидетели: $l' = (4, 5, 6, 3, 2, 1)$ — все 6 значений различны, значит инъективность $\alpha\_{0}'$; (iv) примитивность $M'^{3} > 0$: из $1$ за 1 шаг $\{2,3,4\}$, за 2 — $\{1,2,3,5,6\}$, за 3 — все $6$; из $6$ за 1 — $\{1,4,5\}$, за 2 — $\{1,2,3,4\}$, за 3 — все $6$; аналогично для остальных (симметрия конструкции). Коммутирование с $j' = (2,1,1,1,1,4)$ и $k' = (3,3,2,2,3,5)$ фиксирует все 6 элементов, оставляя $\{\mathrm{id}\}$. $\square$

#### <span class="accent">— [Теорема VIII.3]</span>
{: .courier #thm-VIII-3}

(а) Система I–VII допускает неизоморфные коалгебраические реализации ($\mathbb{Z}\_{2}$ для $\mathcal{F}$, $\{\mathrm{id}\}$ для $\mathcal{F}'$); ни одна не выделена внутренними средствами I–VII.

(б) При $\mathcal{F}$ регенерация из $(\mathbb{H}\_{core}, \omega\_{core})$ оставляет $\mathbb{Z}\_{2}$-неоднозначность двух представителей ($\mathcal{G}$ и $P\_{3}(\mathcal{G})$).

(в) Факторизация по орбитам симметрий или идеалам даёт профиль $(\mathbb{Z}\_{2}, \{\mathrm{id}\}, \{\mathrm{id}\})$: на $B\_{6}$ — $\mathbb{Z}\_{2} = \langle P\_{3}\rangle$; на $B\_{3} = B\_{6}/J\_{\mathrm{sym}}$ ($J\_{\mathrm{sym}} = \langle x\_{1}+x\_{4}, x\_{2}+x\_{5}, x\_{3}+x\_{6}\rangle$) — $\{\mathrm{id}\}$; на $B\_{6}/I \cong \mathbb{F}\_{2} \times \mathbb{F}\_{2}$ — $\{\mathrm{id}\}$. Снятие биполярности ($\mathbb{F}\_{2} \times \mathbb{F}\_{2} \twoheadrightarrow \mathbb{F}\_{2}$) уничтожает многообразие $V(I) = \{\mathbf{0}, \mathbf{1}\}$.

***<span class="accent">Доказательство</span>***.

(1) Обе презентации удовлетворяют условиям $\mathfrak{P}\_{6}$ и [\[Теорема VIII.2\]](#thm-VIII-2).

(2) Прямое следствие [\[Лемма VIII.1\]](#lem-VIII-1).

(3) Уровень $B\_{3}$. Идеал $J\_{\mathrm{sym}}$ — коидеал: $\alpha\_{0}(x\_{1} + x\_{4}) = x\_{2}\otimes x\_{3}\otimes x\_{4} + x\_{5}\otimes x\_{6}\otimes x\_{1}$; в $B\_{3}^{\otimes 3}$ (где $x\_{1} = x\_{4} = a$, $x\_{2} = x\_{5} = b$, $x\_{3} = x\_{6} = c$) это $b\otimes c\otimes a + b\otimes c\otimes a = 0$, значит $\alpha\_{0}(x\_{1}+x\_{4}) \in J\_{\mathrm{sym}}^{[3]}$; аналогично $\alpha\_{0}(x\_{2}+x\_{5}) = a\otimes c\otimes b + a\otimes c\otimes b = 0$ и $\alpha\_{0}(x\_{3}+x\_{6}) = a\otimes b\otimes c + a\otimes b\otimes c = 0$. Индуцированное $\alpha\_{\mathrm{sym}}: B\_{3} \to B\_{3}^{\otimes 3}$: $\alpha\_{\mathrm{sym}}(1') = 2'\otimes 3'\otimes 1'$, $\alpha\_{\mathrm{sym}}(2') = 1'\otimes 3'\otimes 2'$, $\alpha\_{\mathrm{sym}}(3') = 1'\otimes 2'\otimes 3'$ (где $1' = \{1,4\}$, $2' = \{2,5\}$, $3' = \{3,6\}$). Автоморфизмы: $(1'\,2')^{\otimes 3}(1'\otimes 2'\otimes 3') = 2'\otimes 1'\otimes 3' \neq \alpha\_{\mathrm{sym}}(3') = 1'\otimes 2'\otimes 3'$; $(1'\,3')$, $(2'\,3')$ аналогично; 3-циклы $(1'\,2'\,3')$ дают $(1'\,2'\,3')^{\otimes 3}(2'\otimes 3'\otimes 1') = 3'\otimes 1'\otimes 2' \neq \alpha\_{\mathrm{sym}}(2') = 1'\otimes 3'\otimes 2'$; аналогично $(1'\,3'\,2')$. Единственный — $\{\mathrm{id}\}$.

(4) Уровень $B\_{6}/I$. Атомы $B\_{6}/I$ обозначим $e\_{\mathbf{0}}, e\_{\mathbf{1}}$ (индикаторы точек $\mathbf{0}, \mathbf{1}$). $\bar\alpha\_{0}(e\_{\mathbf{1}}) = e\_{\mathbf{1}} \otimes e\_{\mathbf{1}} \otimes e\_{\mathbf{1}}$ (моном), $\bar\alpha\_{0}(e\_{\mathbf{0}}) = 1 - e\_{\mathbf{1}} \otimes e\_{\mathbf{1}} \otimes e\_{\mathbf{1}}$ (сумма 7 атомов). Инверсия $\tau: e\_{\mathbf{0}} \leftrightarrow e\_{\mathbf{1}}$ на $B\_{6}/I$: $\bar\alpha\_{0}(\tau(e\_{\mathbf{1}})) = \bar\alpha\_{0}(e\_{\mathbf{0}}) = 1 - e\_{\mathbf{1}} \otimes e\_{\mathbf{1}} \otimes e\_{\mathbf{1}}$, тогда как $\tau^{\otimes 3}(\bar\alpha\_{0}(e\_{\mathbf{1}})) = \tau^{\otimes 3}(e\_{\mathbf{1}} \otimes e\_{\mathbf{1}} \otimes e\_{\mathbf{1}}) = e\_{\mathbf{0}} \otimes e\_{\mathbf{0}} \otimes e\_{\mathbf{0}}$. В $(B\_{6}/I)^{\otimes 3}$: первое — сумма 7 атомов, второе — один атом $e\_{(\mathbf{0},\mathbf{0},\mathbf{0})}$; различны. Значит $\mathrm{Aut}(B\_{6}/I, \bar\alpha\_{0}) = \{\mathrm{id}\}$.

(5) В обоих случаях фактор-морфизмы не обратимы, информация о $\mathcal{F}$ стирается. Снятие биполярности $\mathbb{F}\_{2}\times\mathbb{F}\_{2} \twoheadrightarrow \mathbb{F}\_{2}$ (отождествление $\mathbf{0} = \mathbf{1}$) уничтожает $V(I)$, так как $0 = 1$ в $\mathbb{F}\_{2}$. $\square$

#### <span class="accent">— [Следствие VIII.1]</span>
{: .courier #cor-VIII-1}

Выбор $\mathcal{G} = (\Sigma, \mathcal{F})$ (искусственная артикуляция, [Раздел I](#prt-I)) получает внутреннее структурное обоснование: открытость начального звена не является внешним дефектом формализма, а следует из двух теорем: невозможности беспрезентационного старта [\[Теорема VIII.1\]](#thm-VIII-1)) и неустранимой неоднозначности при $\mathcal{F}$ [\[Теорема VIII.3\]](#thm-VIII-3)).

***<span class="accent">Доказательство</span>***. Непосредственно [\[Теорема VIII.1\]](#thm-VIII-1) (без выбора $\mathcal{G} \in \mathfrak{P}\_{6}$ динамика I–VI не определена) и [\[Теорема VIII.3\]](#thm-VIII-3) (неустранимая неоднозначность или потеря $\mathcal{F}$ при факторизации). $\square$

---

#### <span class="accent">— [Интуитивное описание VIII]</span>
{: .courier}

**1. <span class="accent">С чего начали и почему</span>?**

С цепи I–VII, оставившей открытое звено — выбор $\mathcal{G} = (\Sigma, \mathcal{F})$ (искусственная артикуляция). Формализм не запрещает рассмотреть класс $\mathfrak{P}\_{6}$ всевозможных презентаций.

**2. <span class="accent">Какие шаги выполнили</span>?**

(а) Определили класс $\mathfrak{P}\_{6}$ [\[Определение VIII.1\]](#def-VIII-1); зафиксировали $(6,3)$ как выбор [\[Замечание VIII.1\]](#rem-VIII-1).

(б) Доказали: невозможность беспрезентационного старта через $\omega\_{\mathrm{deg}} = \varepsilon\cdot(1\otimes 1\otimes 1)$ [\[Теорема VIII.1\]](#thm-VIII-1); единственность минимальной подкоалгебры (с проверкой $\iota\_{0}(B\_{6})$ — подкоалгебра) и $\mathrm{Aut} \cong \mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F})$ через сохранение порядка (для любой $\mathcal{G} \in \mathfrak{P}\_{6}$) [\[Лемма VIII.1\]](#lem-VIII-1); вариативность $\mathbb{Z}\_{2}$ vs $\{\mathrm{id}\}$, проверка $M'^{3} > 0$ для $\mathcal{F}'$ [\[Теорема VIII.2\]](#thm-VIII-2); trade-off с профилем $(\mathbb{Z}\_{2}, \{\mathrm{id}\}, \{\mathrm{id}\})$, коидеал $J\_{\mathrm{sym}}$, явная $\alpha\_{\mathrm{sym}}$ [\[Теорема VIII.3\]](#thm-VIII-3); структурное обоснование [\[Следствие VIII.1\]](#cor-VIII-1).

**3. <span class="accent">К чему пришли</span>?**

$(\mathbb{H}\_{core}(\mathcal{G}), \omega\_{core}(\mathcal{G}))$ определяется $\mathcal{G} \in \mathfrak{P}\_{6}$ с точностью до $\mathrm{Sym}\_{\mathrm{ord}}(\mathcal{F})$. Для $\mathcal{F}$ — $\mathbb{Z}\_{2}$-неоднозначность; для $\mathcal{F}'$ — однозначность. Факторизация по орбитам даёт тривиальную группу, но стирает $\mathcal{F}$.

**4. <span class="accent">Что это значит сейчас</span>?**

Выбор $\mathcal{G}$ получает внутреннее обоснование: его открытость — следствие структуры.

---
