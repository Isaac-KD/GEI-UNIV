# 🎲 BLOC 4 MATHS — Probabilités & Dénombrement
> **Fiche auto-suffisante · Version Universelle** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--dénombrement--la-méthode-infaillible) | Dénombrement — La Méthode Infaillible | Fondamental |
| [02](#02--probabilités-conditionnelles--indépendance) | Probabilités Conditionnelles & Indépendance | Piège niveau L3 |
| [03](#03--espérance-variance--inégalités) | Espérance, Variance & Inégalités | |
| [04](#04--les-lois-de-probabilité-à-maîtriser) | Les Lois de Probabilité à Maîtriser | |
| [05](#05--bonus-analyse--jensen--convexité) | Bonus Analyse — Jensen & Convexité | |

---

## 01 · Dénombrement — La Méthode Infaillible

### 📐 Contexte

Tout exercice de probabilités sur un univers fini commence par un **"Combien ?"**. Une erreur ici et tout le reste est faux. La clé : se poser deux questions dans l'ordre — *l'ordre compte-t-il ?* puis *peut-on répéter ?*

---

### 🎲 Organigramme — À dérouler mentalement

**① L'ordre compte ET répétition possible → Tirages avec remise**

$$\boxed{\text{p-liste} : n^k}$$

> Tirages successifs où on remet l'élément à chaque fois.

**② L'ordre compte ET pas de répétition → Tirages sans remise**

$$\boxed{\text{Arrangement} : A_n^k = \frac{n!}{(n-k)!}}$$

> Podium, anagrammes avec contrainte d'ordre.

**③ L'ordre ne compte pas → Tirage simultané**

$$\boxed{\text{Combinaison} : \binom{n}{k} = \frac{n!}{k!(n-k)!}}$$

> Main de cartes, comité, échantillon — on choisit sans tenir compte de l'ordre.

---

### ★ Valeurs utiles à retenir

| Expression | Valeur | Note |
|------------|--------|------|
| $\binom{n}{0}$ | $1$ | Une seule façon de choisir 0 éléments |
| $\binom{n}{n}$ | $1$ | Une seule façon de tout prendre |
| $\binom{n}{1}$ | $n$ | |
| $\binom{n}{k}$ | $= \binom{n}{n-k}$ | **Symétrie** des combinaisons |

---

## 02 · Probabilités Conditionnelles & Indépendance

### 📐 Contexte

C'est le cœur de la modélisation probabiliste. Le concours teste la différence subtile entre **indépendance** (propriété forte) et **non-corrélation** (propriété faible). Ces deux notions sont souvent confondues — c'est le piège de niveau L3.

---

### 🔀 Les 3 formules fondamentales

**Probabilité conditionnelle :**

$$\boxed{P(A \mid B) = \frac{P(A \cap B)}{P(B)}}$$

> "Probabilité de A sachant que B est réalisé." Définie uniquement si $P(B) > 0$.

**Formule des Probabilités Totales :**

$$\boxed{P(A) = \sum_i P(A \mid B_i)\,P(B_i)}$$

> Valable si les $(B_i)$ forment une **partition de l'univers** (mutuellement exclusifs, d'union = Ω). On décompose A selon les scénarios possibles.

**Théorème de Bayes — Inverser la condition :**

$$\boxed{P(B_i \mid A) = \frac{P(A \mid B_i)\,P(B_i)}{P(A)}}$$

> On connaît $P(A|B_i)$ et on veut $P(B_i|A)$ : c'est l'**inversion causale**. Utilisé en diagnostics médicaux, tests, détection.

---

### Indépendance vs Non-Corrélation — Le piège niveau L3

**Définition rigoureuse de l'indépendance :**

$$X, Y \text{ indépendantes} \iff \forall\, f, g \text{ bornées : } E(f(X)\,g(Y)) = E(f(X))\,E(g(Y))$$

> L'indépendance est une propriété **très forte** : elle doit valoir pour *toutes* les fonctions bornées.

**Covariance :**

$$\boxed{\text{Cov}(X,Y) = E(XY) - E(X)\,E(Y)}$$

> Mesure la corrélation **linéaire** entre X et Y.

**Le lien à sens unique :**

$$X, Y \text{ indépendantes} \;\Rightarrow\; \text{Cov}(X,Y) = 0$$

$$\text{Cov}(X,Y) = 0 \;\not\Rightarrow\; X, Y \text{ indépendantes} \quad \textbf{FAUX en général !}$$

---

### ⚠️ Contre-exemple classique

> Soit $X \sim \mathcal{N}(0,1)$ et $Y = X^2$. Par symétrie : $\text{Cov}(X,Y) = 0$. Pourtant $Y$ est **entièrement déterminée** par $X$ — elles sont parfaitement dépendantes !

---

## 03 · Espérance, Variance & Inégalités

### 📐 Contexte

Il ne suffit pas de calculer $E(X)$ et $V(X)$ — il faut aussi connaître les théorèmes qui les **encadrent**. Les inégalités de Markov et Bienaymé-Tchebychev permettent de majorer des probabilités sans connaître la loi complète.

---

### Formules de calcul

$$E(X) = \sum_k k \cdot P(X=k) \quad \text{(discret)} \qquad E(X) = \int_{-\infty}^{+\infty} t \cdot f(t)\,dt \quad \text{(continu)}$$

**Variance — Théorème de Koenig-Huygens :**

$$\boxed{V(X) = E(X^2) - [E(X)]^2}$$

**Propriétés linéaires :**

| Propriété | Formule |
|-----------|---------|
| $E(aX+b)$ | $= aE(X) + b$ — l'espérance est linéaire |
| $V(aX+b)$ | $= a^2 V(X)$ — la constante $b$ n'influe pas |

---

### Espérance par la fonction de survie *(pour $X \ge 0$)*

$$\text{Discret :}\quad E(X) = \sum_{k=1}^{\infty} P(X \ge k) \qquad \text{Continu :}\quad E(X) = \int_0^{+\infty} P(X > t)\,dt$$

---

### Inégalités de concentration

**Inégalité de Markov** *(pour $X \ge 0$ et $a > 0$)* :

$$\boxed{P(X \ge a) \le \frac{E(X)}{a}}$$

> **Majore une probabilité par l'espérance.** N'utilise que $E(X)$.

**Inégalité de Bienaymé-Tchebychev** *(pour tout $a > 0$)* :

$$\boxed{P\big(|X - E(X)| \ge a\big) \le \frac{V(X)}{a^2}}$$

> **Contrôle l'écart à la moyenne par la variance.** Plus précise que Markov mais nécessite $V(X)$.

> **Propriété fondamentale :** Une variable aléatoire *bornée* ($|X| \le M$) admet toujours des moments de tous ordres — donc une espérance et une variance finies.

---

## 04 · Les Lois de Probabilité à Maîtriser

### 📐 Contexte

Le concours attend que vous **reconnaissiez immédiatement** une situation et la loi associée. Mémoriser les *contextes d'application*, pas seulement les formules.

---

### Lois discrètes

| Loi | Contexte | Espérance | Variance |
|-----|---------|-----------|----------|
| **Bernoulli($p$)** | 1 épreuve : succès (prob $p$) ou échec | $p$ | $p(1-p)$ |
| **Binomiale($n,p$)** | $n$ épreuves de Bernoulli *indépendantes* | $np$ | $np(1-p)$ |
| **Géométrique($p$)** | Rang du 1er succès | $1/p$ | $(1-p)/p^2$ |
| **Poisson($\lambda$)** | Comptage d'événements rares | $\lambda$ | $\lambda$ |

> Poisson : **espérance = variance = $\lambda$** — à retenir !

> Poisson($\lambda$) est la limite de Binomiale($n$, $\lambda/n$) quand $n \to \infty$.

---

### Lois continues

| Loi | Contexte | Densité $f(x)$ | Espérance | Variance |
|-----|---------|----------------|-----------|----------|
| **Uniforme $[a,b]$** | Tirage "au hasard" dans un intervalle | $\dfrac{1}{b-a}$ | $\dfrac{a+b}{2}$ | $\dfrac{(b-a)^2}{12}$ |
| **Exponentielle($\lambda$)** | Durée de vie "sans mémoire" | $\lambda e^{-\lambda x}$ (pour $x\ge0$) | $1/\lambda$ | $1/\lambda^2$ |
| **Normale $\mathcal{N}(\mu,\sigma^2)$** | Somme de VA (TCL), mesures | $\dfrac{e^{-(x-\mu)^2/2\sigma^2}}{\sigma\sqrt{2\pi}}$ | $\mu$ | $\sigma^2$ |

---

### ⚡ Hack — Reconnaître la loi en 5 secondes

- **Binomiale → Poisson :** $n$ grand et $p$ très petit → Poisson avec $\lambda = np$.
- **Exponentielle :** le mot "**sans mémoire**" dans l'énoncé → forcément exponentielle.
- **Normale :** "somme de $n$ VA i.i.d." pour $n$ grand → **Théorème Central Limite** → normale.

---

## 05 · Bonus Analyse — Jensen & Convexité

### 📐 Contexte

Certains QCM testent des propriétés d'analyse ayant des **applications directes en probabilités**. L'inégalité de Jensen est le pont entre la convexité des fonctions et les inégalités sur les espérances.

---

### 📐 Inégalité de Jensen

$$\boxed{\text{Si } f \text{ est convexe : } f(E(X)) \le E(f(X))}$$

> Jensen dit que pour une fonction convexe, "la valeur en la moyenne" est plus petite que "la moyenne des valeurs".

**Application directe — Preuve que $V(X) \ge 0$ :**

$f(x) = x^2$ est convexe. Jensen donne :

$$(E(X))^2 \le E(X^2) \;\Rightarrow\; V(X) = E(X^2) - (E(X))^2 \ge 0$$

> Jensen fournit une **preuve élégante** que la variance est toujours positive.

---

### Propriétés des fonctions convexes utiles

| Propriété | Détail |
|-----------|--------|
| **Strictement convexe** | Coupe une droite en *au plus 2 points*. Unicité de solutions. |
| **Somme** | La somme de deux fonctions convexes est convexe. |
| **Concave** | Si $f$ est *concave* : $f(E(X)) \ge E(f(X))$ (Jensen inversé). |

---

### ★ Applications QCM fréquentes de Jensen

| Fonction | Nature | Inégalité |
|----------|--------|-----------|
| $e^x$ | Convexe | $e^{E(X)} \le E(e^X)$ |
| $x^2$ | Convexe | $(E(X))^2 \le E(X^2)$ → $V(X) \ge 0$ ✓ |
| $\|x\|$ | Convexe | $\|E(X)\| \le E(\|X\|)$ |
| $\ln(x)$ | **Concave** | $\ln(E(X)) \ge E(\ln(X))$ (Jensen inversé) |

---

*Fiche auto-suffisante — Version Universelle — Bloc 4 Maths · Probabilités & Dénombrement*