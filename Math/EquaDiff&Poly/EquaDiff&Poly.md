# 📉 BLOC 5b MATHS — Équations Différentielles & Polynômes
> **Fiche auto-suffisante · Réflexes Ingénieur** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet | Partie |
|---|-------|--------|
| [01](#01--équations-différentielles-dordre-1) | Équations Différentielles d'Ordre 1 | A — ED |
| [02](#02--équations-différentielles-dordre-2--coefficients-constants) | Équations Différentielles d'Ordre 2 | A — ED |
| [03](#03--racines--multiplicité) | Racines & Multiplicité | B — Polynômes |
| [04](#04--formules-de-viète--relations-coefficients-racines) | Formules de Viète | B — Polynômes |
| [05](#05--arithmétique-des-polynômes--pgcd--bézout) | PGCD & Arithmétique | B — Polynômes |

---

# Partie A — Équations Différentielles

> Le jury ne veut pas voir une page de calcul. Il te donne l'équation et 5 solutions. Ton but est de **reconnaître la forme générale** ou d'utiliser la *méthode inversée* : tester les solutions proposées.

---

## 01 · Équations Différentielles d'Ordre 1

### 📐 Contexte

La solution générale est toujours :

$$y = \underbrace{y_h}_{\text{homogène}} + \underbrace{y_p}_{\text{particulière}}$$

---

### Forme générale & solution homogène

**Forme générale :**

$$\boxed{y' + a(x)\,y = b(x)}$$

**Solution homogène** *(équation sans second membre, $b = 0$)* :

$$\boxed{y_h(x) = C \cdot \exp\!\left(-\int a(x)\,dx\right)}$$

> ⚠️ Attention au signe **"−"** dans l'exposant — piège classique.
>
> Cas le plus fréquent ($a$ = constante) : $y_h(x) = C \cdot e^{-ax}$

---

### ⚡ Hack Sniper — Méthode QCM infaillible

Prends les 5 formules proposées (A, B, C, D, E), **dérive-les mentalement** et regarde laquelle vérifie $y' + ay = b(x)$. C'est mathématiquement infaillible et **3× plus rapide** que de construire $y_p$ de zéro.

**Exemple :** Pour $y' + 2y = 4$, la solution particulière est $y_p = 2$ (constante). Vérifie : $0 + 2 \times 2 = 4$ ✓.

---

## 02 · Équations Différentielles d'Ordre 2 — Coefficients Constants

### 📐 Contexte

Les 3 cas de l'équation caractéristique sont **cruciaux en Maths ET en Physique** (circuits RLC, oscillateurs mécaniques). La même structure apparaît partout.

---

### Méthode — Équation caractéristique

**Forme générale homogène :**

$$\boxed{ay'' + by' + cy = 0}$$

**Étape 1 — Poser l'équation caractéristique :**

$$\boxed{ar^2 + br + c = 0 \qquad \Delta = b^2 - 4ac}$$

**Étape 2 — Analyser $\Delta$ et écrire la solution :**

---

### Les 3 cas — À connaître par cœur

**Cas 1 — $\Delta > 0$ : Régime apériodique**

> Deux racines réelles distinctes : $r_1$ et $r_2$

$$\boxed{y(x) = A\,e^{r_1 x} + B\,e^{r_2 x}}$$

---

**Cas 2 — $\Delta = 0$ : Régime critique**

> Une racine double : $r_0 = -\dfrac{b}{2a}$

$$\boxed{y(x) = (Ax + B)\,e^{r_0 x}}$$

> ⚠️ **Piège :** ne pas oublier le "$x$" devant le $A$ !

---

**Cas 3 — $\Delta < 0$ : Régime pseudo-périodique / Oscillations**

> Deux racines complexes conjuguées : $r = \alpha \pm i\beta$
> avec $\alpha = -\dfrac{b}{2a}$ et $\beta = \dfrac{\sqrt{-\Delta}}{2a}$

$$\boxed{y(x) = e^{\alpha x}\!\left[A\cos(\beta x) + B\sin(\beta x)\right]}$$

---

### ⚡ Hack Conditions Initiales

Si on te donne $y(0) = 0$ ou $y'(0) = 1$, **injecte directement $x = 0$** dans les propositions du QCM pour éliminer immédiatement les fausses réponses — sans calculer $A$ et $B$.

---

> **Lien Physique :** Δ > 0 = sur-amorti (apériodique), Δ = 0 = critique, Δ < 0 = sous-amorti (oscillations).

---

# Partie B — Polynômes & Arithmétique

> On te donne un polynôme complexe et on te demande ses racines, leur multiplicité, ou le PGCD de deux polynômes.

---

## 03 · Racines & Multiplicité

### 📐 Contexte

Si $\alpha$ est racine d'un polynôme $P$, alors $P$ est factorisable par $(X - \alpha)$. La multiplicité se lit sur les dérivées successives.

---

### Théorème de Multiplicité — Ultra-testé

| Multiplicité | Conditions | Factorisation |
|-------------|-----------|--------------|
| **Racine simple** | $P(\alpha) = 0$ ET $P'(\alpha) \neq 0$ | Factorisable par $(X-\alpha)$ |
| **Racine double** | $P(\alpha) = 0$ ET $P'(\alpha) = 0$ ET $P''(\alpha) \neq 0$ | Factorisable par $(X-\alpha)^2$ |
| **Racine d'ordre $k$** | $P(\alpha) = P'(\alpha) = \cdots = P^{(k-1)}(\alpha) = 0$ ET $P^{(k)}(\alpha) \neq 0$ | Factorisable par $(X-\alpha)^k$ |

---

### ⚡ Hack — Trouver les racines d'un polynôme de degré 3 ou 4

1. Calcule $P'(X)$ — degré inférieur, racines plus faciles à trouver.
2. Trouve les racines de $P'(X)$.
3. Si une racine $\alpha$ de $P'$ vérifie aussi $P(\alpha) = 0$ → c'est une **racine double de $P$** !

---

### ★ Exemple guidé

$P(X) = X^3 - 3X + 2$ → $P'(X) = 3X^2 - 3 = 3(X-1)(X+1)$

Racines de $P'$ : $X = 1$ et $X = -1$.

$P(1) = 1 - 3 + 2 = 0$ ✓ → **$X = 1$ est une racine double** de $P$.

$$P(X) = (X-1)^2(X+2)$$

---

## 04 · Formules de Viète — Relations Coefficients-Racines

### 📐 Contexte

Les formules de Viète permettent de **lier les racines aux coefficients** sans les calculer explicitement.

---

**Polynôme de degré $n$ :** $P(X) = a_n X^n + a_{n-1} X^{n-1} + \cdots + a_0$

$$\boxed{\sum x_i = -\frac{a_{n-1}}{a_n}} \qquad \boxed{\prod x_i = (-1)^n \frac{a_0}{a_n}}$$

---

**Cas fondamental — Degré 2 :** $aX^2 + bX + c$

| Relation | Formule |
|----------|---------|
| **Somme** | $x_1 + x_2 = -\dfrac{b}{a}$ |
| **Produit** | $x_1 \cdot x_2 = \dfrac{c}{a}$ |

> **Application directe :** Trouver deux nombres dont on connaît la somme $S$ et le produit $P$ revient à résoudre $X^2 - SX + P = 0$.

---

## 05 · Arithmétique des Polynômes — PGCD & Bézout

### 📐 Contexte

Tout comme avec les entiers, on peut faire des **divisions euclidiennes** de polynômes. L'algorithme d'Euclide s'applique exactement de la même façon.

---

### Division euclidienne

$$\boxed{A = B \cdot Q + R \quad \text{avec } \deg(R) < \deg(B)}$$

> $Q$ = quotient, $R$ = reste. Si $R = 0$, alors $B$ divise $A$.

---

### Algorithme d'Euclide pour PGCD(A, B)

1. Divise $A$ par $B$ → obtiens un reste $R_1$ avec $\deg(R_1) < \deg(B)$.
2. Divise $B$ par $R_1$ → obtiens un reste $R_2$.
3. Continue jusqu'à obtenir un **reste nul**.
4. ★ Le **PGCD = dernier reste non nul**, rendu *unitaire* (coefficient dominant = 1).

---

### ★ Théorème de Bézout pour les polynômes

Deux polynômes sont **premiers entre eux** si leur PGCD = 1 (polynôme constant).

Dans ce cas :

$$\boxed{A \cdot U + B \cdot V = 1}$$

pour certains polynômes $U$ et $V$.

> Plus généralement, si $\text{PGCD}(A, B) = D$, il existe $U$ et $V$ tels que $A \cdot U + B \cdot V = D$.

---

*Fiche auto-suffisante — Réflexes Ingénieur — Bloc 5b Maths · Équations Différentielles & Polynômes*