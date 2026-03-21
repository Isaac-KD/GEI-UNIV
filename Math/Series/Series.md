# 🧠 BLOC 2 MATHS — Séries, Intégrales & Convergence
> **Fiche auto-suffisante** · 20–30% de la note en maths 

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--séries-numériques--le-boss-des-qcm) | Séries Numériques — Le Boss des QCM | ~4–6 questions/an |
| [02](#02--intégrales-généralisées--le-jumeau-des-séries) | Intégrales Généralisées — Le Jumeau | Tombé en 2019 |
| [03](#03--séries-entières--rayon-de-convergence) | Séries Entières & Rayon de Convergence | Tombé en 2019 & 2021 |
| [04](#04--suites-de-fonctions--convergence-uniforme) | Suites de Fonctions & Convergence Uniforme | Tombé en 2021 |

---

## 01 · Séries Numériques — Le Boss des QCM

### 📐 Contexte

Le GEI-UNIV adore donner une série $\sum u_n$ et demander si elle converge. **4 à 6 questions par an** (soit 20–30% de la note en maths) portent sur ce sujet. La méthode : descendre la checklist dans l'ordre jusqu'à trouver le critère applicable.

---

### ∑ La Checklist Infaillible — Arbre de décision

**① Condition nécessaire — Test préliminaire**

$$\lim_{n \to \infty} u_n = 0 \; ?$$

> Si cette limite est **non nulle ou n'existe pas** → **Divergence Grossière** immédiate.

---

**② Séries à termes positifs ($u_n \ge 0$)**

**Critère de Riemann — LE PLUS IMPORTANT :**

$$\boxed{\sum \frac{1}{n^\alpha} \;\text{converge} \iff \alpha > 1}$$

| Série | $\alpha$ | Nature |
|-------|----------|--------|
| $\sum 1/n^2$ | $2 > 1$ | **Converge** |
| $\sum 1/n$ (harmonique) | $1$ | **Diverge** |
| $\sum 1/\sqrt{n}$ | $1/2 < 1$ | **Diverge** |

**Critère d'équivalence — Hack DL :**

> Si $u_n \sim v_n$ en $+\infty$, alors $\sum u_n$ et $\sum v_n$ ont la **même nature**.

Utilise les DL pour trouver l'équivalent :
- $\ln(1 + 1/n^2) \sim 1/n^2$ → Riemann $\alpha=2>1$ → **Converge**
- $\sin(1/n) \sim 1/n$ → Riemann $\alpha=1$ → **Diverge**
- $1 - \cos(1/n) \sim 1/(2n^2)$ → Riemann $\alpha=2>1$ → **Converge**

**Critère de d'Alembert — Pour les factorielles et exponentielles :**

$$\boxed{L = \lim_{n \to \infty} \left|\frac{u_{n+1}}{u_n}\right|}$$

| Valeur de $L$ | Conclusion |
|---------------|------------|
| $L < 1$ | **Converge** |
| $L > 1$ | **Diverge** |
| $L = 1$ | **Inconclus** — utilise Riemann ou équivalence |

---

**③ Séries à termes quelconques — avec $(-1)^n$**

**Convergence Absolue — Premier réflexe :**

> Si $\sum |u_n|$ converge → alors $\sum u_n$ **converge absolument** (et donc converge).

**Critère des Séries Alternées (CSSA) :**

$$\boxed{\sum (-1)^n v_n \;\text{converge si :}\; v_n > 0,\; v_n \text{ décroissante},\; v_n \to 0}$$

> Attention : la convergence n'est *pas nécessairement absolue* → convergence **semi-convergente** (ex : $\sum (-1)^n/n$).

---

### ⚡ Hack — Utilise les DL pour trouver l'équivalent

Pour les séries du type $u_n = f(1/n)$, développe $f$ en 0 (car $1/n \to 0$). Le premier terme non nul du DL donne l'équivalent, puis on applique Riemann.

---

## 02 · Intégrales Généralisées — Le Jumeau des Séries

### 📐 Contexte

Les intégrales généralisées sont le **miroir continu** des séries numériques. Les critères sont exactement les mêmes, transposés du discret au continu.

---

### ∫ Les Critères Miroir

| Critère | Pour $\sum u_n$ | Pour $\int f\,dt$ |
|---------|-----------------|-------------------|
| **Riemann en $+\infty$** | $\sum 1/n^\alpha$ converge $\iff \alpha > 1$ | $\int_1^{+\infty} dt/t^\alpha$ converge $\iff \alpha > 1$ |
| **Riemann en $0$** | N/A | $\int_0^1 dt/t^\alpha$ converge $\iff \alpha < 1$ |
| **Équivalence** | $u_n \sim v_n$ → même nature | $f(t) \sim g(t)$ à la borne → même nature |

> ⚠️ Cas en 0 : le critère est **inversé** par rapport à $+\infty$. Pour converger en 0, il faut $\alpha < 1$.

**IPP (Intégration Par Parties) — Tombé en 2019 Q5 :**

> L'IPP est souvent la clé pour les **intégrales semi-convergentes** (oscillantes). Exemple : $\int_1^{+\infty} \frac{\sin t}{t}\,dt$ — non monotone, donc Riemann inapplicable directement. On intègre par parties pour faire apparaître $\frac{\cos t}{t^2}$ qui converge absolument.

---

### Intégrales de Référence — À savoir par cœur

**Intégrale de Gauss :**

$$\boxed{\int_{-\infty}^{+\infty} e^{-x^2}\,dx = \sqrt{\pi}} \qquad \text{et} \qquad \int_0^{+\infty} e^{-x^2}\,dx = \frac{\sqrt{\pi}}{2}$$

> Résultat à mémoriser directement. Ne se calcule pas par les méthodes classiques (pas de primitive élémentaire).

**Intégrale de Bertrand — Piège classique :**

$$\int_2^{+\infty} \frac{dt}{t^\alpha (\ln t)^\beta}$$

Converge si et seulement si :

| Cas | Condition | Nature |
|-----|-----------|--------|
| Cas 1 | $\alpha > 1$ (peu importe $\beta$) | **Converge** — $t^\alpha$ domine |
| Cas 2 | $\alpha = 1$ ET $\beta > 1$ | **Converge** — $\ln t$ assure la convergence |
| Sinon | $\alpha < 1$, ou $\alpha = 1$ et $\beta \leq 1$ | **Diverge** |

---

## 03 · Séries Entières & Rayon de Convergence

### 📐 Contexte

Une série entière $\sum a_n z^n$ est le pont entre les séries numériques et les fonctions analytiques. Les DL usuels ne sont que des séries entières tronquées ! Chaque série entière a un **rayon de convergence $R$** qui délimite la zone de convergence.

---

### 🌀 Rayon de convergence — Règle de d'Alembert

$$\boxed{R = \frac{1}{\displaystyle\lim_{n \to \infty} \left|\dfrac{a_{n+1}}{a_n}\right|}}$$

> Si la limite vaut $L$ : $R = 1/L$. Si $L = 0$ → $R = +\infty$. Si $L = +\infty$ → $R = 0$.

---

### Propriétés du rayon R *(tombé en 2021 & 2019)*

| Zone | Condition | Comportement |
|------|-----------|-------------|
| **Intérieur** | $\|z\| < R$ | **Convergence absolue.** $S(x)$ est $C^\infty$, dérivable et intégrable terme à terme. |
| **Extérieur** | $\|z\| > R$ | **Divergence grossière.** |
| **Cercle** | $\|z\| = R$ | **Cas douteux** — étude au cas par cas. |

---

### Le Piège du rayon de la somme

$$\boxed{R(S_1 + S_2) \ge \min(R_1, R_2)}$$

> **L'égalité est garantie si $R_1 \ne R_2$** : le rayon de la somme = le plus petit des deux.  
> Si $R_1 = R_2$, le rayon peut être **strictement plus grand** (annulation des termes dominants).

---

### Développements en Série Entière (DSE) usuels

| Fonction | DSE | Rayon |
|----------|-----|-------|
| $\dfrac{1}{1-x}$ | $\displaystyle\sum_{n=0}^{\infty} x^n$ | $R = 1$ |
| $e^x$ | $\displaystyle\sum_{n=0}^{\infty} \dfrac{x^n}{n!}$ | $R = +\infty$ |
| $\sin(x)$ | $\displaystyle\sum_{n=0}^{\infty} \dfrac{(-1)^n x^{2n+1}}{(2n+1)!}$ | $R = +\infty$ |
| $\cos(x)$ | $\displaystyle\sum_{n=0}^{\infty} \dfrac{(-1)^n x^{2n}}{(2n)!}$ | $R = +\infty$ |

---

## 04 · Suites de Fonctions & Convergence Uniforme

### 📐 Contexte

La convergence uniforme est la "bonne" convergence — celle qui **préserve les propriétés** (continuité, intégration, dérivation). La convergence simple est plus faible : elle peut exister sans préserver ces propriétés.

**Intuition :** convergence uniforme = toutes les fonctions $f_n$ restent à une distance $\varepsilon$ *simultanément* de la limite $f$, peu importe le point $x$.

---

### 〰️ Les 3 Hacks pour les QCM

**① Hack de la Continuité — Tombé en 2021**

> Si les $f_n(x)$ sont continues et que la limite simple $f(x)$ est **discontinue** → la convergence est **JAMAIS uniforme**.
>
> Exemple classique : $f_n(x) = x^n$ sur $[0,1]$. Limite = 0 si $x < 1$, = 1 si $x = 1$ → discontinue → **non uniforme**.

---

**② Interversion des limites (Double Limite)**

> S'il y a convergence uniforme, on peut **intervertir les limites** :
>
> $$\lim_{x \to a}\!\Big(\lim_{n \to \infty} f_n(x)\Big) = \lim_{n \to \infty}\!\Big(\lim_{x \to a} f_n(x)\Big)$$
>
> Si ces deux membres sont *différents* sur un exemple → **pas** de convergence uniforme.

---

**③ Interversion Intégrale et Limite**

> S'il y a convergence uniforme sur $[a,b]$ :
>
> $$\lim_{n \to \infty} \int_a^b f_n(x)\,dx = \int_a^b \!\Big(\lim_{n \to \infty} f_n(x)\Big)\,dx$$
>
> Sans convergence uniforme, cette interversion peut être **fausse**.

---

### ⚠️ Pièges Vrai/Faux

> **"La limite de fonctions continues est continue."** → **FAUX** (sans convergence uniforme). Contre-exemple : $x^n$ sur $[0,1]$.

> **"Si convergence simple mais pas uniforme, on ne peut pas intervertir intégrale et limite."** → **VRAI** (en général). La convergence uniforme est suffisante, pas nécessaire — mais en QCM sans elle, on ne peut pas conclure.

---

### ★ Récapitulatif — Ce que la convergence uniforme permet

| Propriété | Résultat |
|-----------|----------|
| **Continuité** | Si les $f_n$ sont continues → la limite $f$ est **continue** |
| **Intégration** | $\int \lim f_n = \lim \int f_n$ ✓ |
| **Dérivation** | Terme à terme (avec conditions sur $f_n'$) ✓ |
| **Doubles limites** | Commutent ✓ |

---

*Fiche auto-suffisante — Cœur du sujet — Bloc 2 Maths · Séries, Intégrales & Convergence*