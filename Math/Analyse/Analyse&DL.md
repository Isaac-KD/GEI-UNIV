# 📈 BLOC 1 — Analyse, Développements Limités & Fonctions à 2 Variables
> **Fiche auto-suffisante · Boss Final** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--les-dl-usuels-en-0) | Les DL Usuels en 0 | Tombé en 2012 & 2020 |
| [02](#02--le-hack-de-la-tangente--de-lasymptote) | Hack Tangente & Asymptote | Tombé en 2022 & 2023 |
| [03](#03--le-hack-des-limites) | Le Hack des Limites | |
| [04](#04--convexité--pièges-de-dérivabilité) | Convexité & Pièges de Dérivabilité | Tombé en 2019 |
| [05](#05--fonctions-à-2-variables--le-boss-final) | Fonctions à 2 Variables — Le Boss Final | Tombé chaque année |

---

## 01 · Les DL Usuels en 0

### 📐 Contexte physique

Un **développement limité** (DL) est une approximation polynomiale d'une fonction autour d'un point (ici 0). Les DL sont l'outil universel du concours : ils servent à calculer des **limites** indéterminées, trouver des **asymptotes**, étudier la position par rapport à la **tangente**, et comparer des infiniment petits.

---

### 📊 Formulaire complet — À connaître par cœur

| Fonction | DL en 0 | Mnémotechnique |
|----------|---------|----------------|
| $e^x$ | $1 + x + \dfrac{x^2}{2} + \dfrac{x^3}{6} + o(x^3)$ | Tout positif, dénominateurs = factorielles |
| $\ln(1+x)$ | $x - \dfrac{x^2}{2} + \dfrac{x^3}{3} - \dfrac{x^4}{4} + o(x^4)$ | Signe **alterné**, dénominateurs = entiers |
| $\ln(1-x)$ | $-x - \dfrac{x^2}{2} - \dfrac{x^3}{3} - \dfrac{x^4}{4} + o(x^4)$ | **Tout négatif !** (remplace $x$ par $-x$) |
| $\sin(x)$ | $x - \dfrac{x^3}{6} + \dfrac{x^5}{120} + o(x^5)$ | Puissances **impaires**, alterné |
| $\cos(x)$ | $1 - \dfrac{x^2}{2} + \dfrac{x^4}{24} + o(x^4)$ | Puissances **paires**, alterné |
| $\dfrac{1}{1-x}$ | $1 + x + x^2 + x^3 + o(x^3)$ | Le plus simple : tout positif, coeff = 1 |
| $(1+x)^\alpha$ | $1 + \alpha x + \dfrac{\alpha(\alpha-1)}{2}x^2 + o(x^2)$ | Binôme généralisé |
| $\sqrt{1+x}$ | $1 + \dfrac{x}{2} - \dfrac{x^2}{8} + o(x^2)$ | Cas $\alpha = 1/2$ du binôme |
| **$\tan(x)$** 🚨 | $x + \dfrac{x^3}{3} + o(x^3)$ | **Tombé 2012 & 2020 — Tout positif !** |
| **$\arctan(x)$** 🚨 | $x - \dfrac{x^3}{3} + \dfrac{x^5}{5} + o(x^5)$ | **Tombé 2012 & 2020 — Alterné** |

> **Comment retrouver $\arctan$ :** $(\arctan x)' = \frac{1}{1+x^2}$. Substitue $u = -x^2$ dans $\frac{1}{1-u}$, intègre terme à terme.

---

## 02 · Le Hack de la Tangente & de l'Asymptote

### 📐 Contexte physique

Le GEI-UNIV adore donner un DL et demander : *"La courbe est-elle au-dessus ou en dessous de sa tangente ?"* (**tombé en 2022 Q2, 2023 Q2**). La réponse se lit directement sur le premier terme non nul après la partie linéaire.

---

### ⚡ Règle Zéro Brouillon — Position par rapport à la tangente

Si tu calcules un DL et que tu trouves :

$$f(x) = \underbrace{A + Bx}_{\text{tangente en 0}} + \underbrace{Cx^k}_{\text{1er terme correctif}} + o(x^k)$$

1. La **tangente en 0** a pour équation : $y = A + Bx$.
2. Pour savoir **qui est au-dessus** : regarde le signe de $Cx^k$.
   - Si $Cx^k > 0$ → la courbe est **au-dessus** de la tangente.
   - Si $Cx^k < 0$ → la courbe est **en dessous**.
3. **Piège absolu :** Si $k$ est *impair* (ex : $x^3$), le signe change selon que $x > 0$ ou $x < 0$. La courbe *traverse* la tangente → **c'est un point d'inflexion !**

---

### Asymptote en l'infini ($x \to \pm\infty$) — *Tombé en 2022 Q3*

**Méthode — Substitution $h = 1/x$ :**

Quand $x \to \infty$, pose $h = 1/x$ (donc $h \to 0$). Fais un DL en $h$ autour de 0, puis remplace $h$ par $1/x$. **L'équation de l'asymptote et sa position apparaissent seules !**

**Exemple :** $f(x) = x\sqrt{1 + 1/x^2}$

Pose $h = 1/x^2$ : $\sqrt{1+h} = 1 + h/2 + \ldots$

Donc $f(x) = x\left(1 + \frac{1}{2x^2} + \ldots\right) = x + \frac{1}{2x} + \ldots$

Asymptote : $y = x$, et la courbe est **au-dessus** (terme $+1/(2x) > 0$ pour $x > 0$).

---

## 03 · Le Hack des Limites

### 📐 Contexte physique

Face à une limite indéterminée $0/0$ ou $\infty/\infty$, la règle de l'Hôpital est tentante mais **dangereuse** : l'appliquer 3 fois sur des expressions trigonométriques génère des erreurs de signe quasi-certaines. Les DL sont infiniment plus sûrs et rapides.

---

### ⚡ Règle d'or — N'applique JAMAIS l'Hôpital plus d'une fois

**Méthode :** Remplace numérateur et dénominateur par leur DL au *premier ordre non nul*, puis simplifie.

---

### Exemple — 15 secondes chrono

Calculer $\displaystyle\lim_{x \to 0} \frac{\sin(x) - x}{x^3}$

**Étape 1 — DL du numérateur :**

$$\sin(x) - x = \left(x - \frac{x^3}{6} + o(x^3)\right) - x = -\frac{x^3}{6} + o(x^3)$$

**Étape 2 — Division et simplification :**

$$\lim_{x \to 0} \frac{-x^3/6 + o(x^3)}{x^3} = \lim_{x \to 0}\left(-\frac{1}{6} + o(1)\right) = \boxed{-\frac{1}{6}}$$

---

### ★ Limites classiques à connaître

| Expression | DL clé | Limite |
|------------|--------|--------|
| $\dfrac{1 - \cos x}{x^2}$ | $\cos x = 1 - x^2/2 + \ldots$ | $\mathbf{1/2}$ |
| $\dfrac{\tan x - x}{x^3}$ | $\tan x = x + x^3/3 + \ldots$ | $\mathbf{1/3}$ |
| $\dfrac{e^x - 1 - x}{x^2}$ | $e^x = 1 + x + x^2/2 + \ldots$ | $\mathbf{1/2}$ |
| $\dfrac{\ln(1+x)}{x}$ | $\ln(1+x) = x - x^2/2 + \ldots$ | $\mathbf{1}$ |

---

## 04 · Convexité & Pièges de Dérivabilité

### Convexité — Les règles dures

| Condition | Nature | Image |
|-----------|--------|-------|
| $f''(x) > 0$ | **Convexe** — au-dessus de ses tangentes | La courbe "sourit" 😊 |
| $f''(x) < 0$ | **Concave** — en dessous de ses tangentes | La courbe "pleure" 😢 |
| $f''$ s'annule et **change de signe** | **Inflexion** | La courbure s'inverse |

---

### ⚠️ Piège — $f''(a) = 0$ ne suffit PAS pour conclure à un inflexion

**Contre-exemple classique :** $f(x) = x^4$.

$f''(x) = 12x^2$ → $f''(0) = 0$. Pourtant $f''(x) \geq 0$ *partout* : elle ne change pas de signe. Donc $x = 0$ est un **minimum**, pas un point d'inflexion.

**Règle :** Pour un inflexion, $f''$ doit s'annuler *ET changer de signe*.

---

### Le Piège du Raccordement de Dérivabilité *(tombé en 2019 Q4)*

**La méthode du théorème :** Si $\lim_{x \to a} f'(x)$ existe → $f$ est dérivable et $f'(a)$ vaut cette limite.

**Le cas difficile :** $f(x) = x^2 \sin(1/x)$ avec $f(0) = 0$.

$$f'(x) = 2x\sin(1/x) - \cos(1/x) \quad \text{pour } x \neq 0$$

Le terme $\cos(1/x)$ oscille sans jamais converger. On croirait que $f'(0)$ n'existe pas. **FAUX.**

---

### ⚡ Hack — Revenir au taux d'accroissement quand $f'$ oscille

Si $f'(x)$ n'a pas de limite (oscillations), **abandonne $f'(x)$** et calcule directement le taux d'accroissement :

$$\frac{f(x) - f(0)}{x - 0} = \frac{x^2 \sin(1/x)}{x} = x\underbrace{\sin(1/x)}_{\text{borné entre -1 et 1}}$$

Le sinus est **borné** et $x \to 0$ → produit $\to 0$.

**→ $f$ EST dérivable en 0 et $f'(0) = 0$.** La dérivée existe même si elle n'est pas continue !

---

## 05 · Fonctions à 2 Variables — Le Boss Final

### 📐 Contexte physique

Le GEI-UNIV pose **chaque année** un exercice sur la recherche des extrema locaux d'une fonction $f(x,y)$ (**tombé en 2019 Q18, 2020 Q20, 2022 Q4, 2025 Q9**). La méthode est toujours la même : gradient nul → Hessienne.

Un **point critique** (gradient nul) n'est pas forcément un extremum — il peut aussi être un *point col* (ou point selle), qui ressemble à une montagne dans une direction et une vallée dans l'autre.

---

### 🗻 Méthode Hessienne (Notations de Monge) — 3 étapes

**① Trouver les points critiques — Annuler le gradient**

$$\frac{\partial f}{\partial x} = 0 \quad \textbf{ET} \quad \frac{\partial f}{\partial y} = 0$$

> Résoudre le système simultané. Les solutions $(x_0, y_0)$ sont les candidats à être des extrema. Les **deux conditions doivent être satisfaites ensemble**.

---

**② Calculer les dérivées secondes en ce point**

$$r = \frac{\partial^2 f}{\partial x^2}\bigg|_{(x_0,y_0)} \qquad t = \frac{\partial^2 f}{\partial y^2}\bigg|_{(x_0,y_0)} \qquad s = \frac{\partial^2 f}{\partial x \partial y}\bigg|_{(x_0,y_0)}$$

---

**③ Calculer le discriminant et conclure**

$$\boxed{\Delta = r \cdot t - s^2}$$

| Valeur de $\Delta$ | Conclusion |
|--------------------|------------|
| $\Delta < 0$ | **Point Col** (point selle) → **pas d'extremum**. Montagne dans une direction, vallée dans l'autre. |
| $\Delta > 0$ et $r > 0$ | **Minimum local** (surface "sourit") |
| $\Delta > 0$ et $r < 0$ | **Maximum local** (surface "pleure") |
| $\Delta = 0$ | **Cas douteux** — méthode insuffisante. Vérifier le calcul. |

---

### ★ Résumé stratégique

- Calculer proprement $\partial f/\partial x$ et $\partial f/\partial y$ et résoudre le système.
- Calculer $r$, $s$, $t$ et $\Delta = rt - s^2$ au point critique.
- Conclure : col si $\Delta < 0$, extremum si $\Delta > 0$ (puis signe de $r$).
- Ne pas oublier que **plusieurs points critiques** sont possibles — tester chacun séparément.

---

*Fiche auto-suffisante — Boss Final — Bloc 1 · Analyse, DL & Fonctions à 2 Variables*