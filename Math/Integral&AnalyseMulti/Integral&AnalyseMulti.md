# 🌍 BLOC 5 MATHS — Analyse Multivariable & Intégration
> **Fiche auto-suffisante · Multivariable** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--calcul-différentiel--hessienne--extrema) | Calcul Différentiel — Hessienne & Extrema | Incontournable |
| [02](#02--intégrales-doubles--changements-de-variables) | Intégrales Doubles & Changements de Variables | Tombé 2022 Q16 |
| [03](#03--intégrales-à-paramètres) | Intégrales à Paramètres | |
| [04](#04--champs-de-vecteurs--formes-différentielles) | Champs de Vecteurs & Formes Différentielles | Discriminant |

---

## 01 · Calcul Différentiel — Hessienne & Extrema

### 📐 Contexte

Recherche d'extrema locaux pour une fonction $f(x,y)$. La méthode est **gradient → hessienne**. Un point critique (gradient nul) peut être un minimum local, un maximum local, ou un col — la hessienne tranche.

---

### 🏔️ Méthode Hessienne — 3 étapes incontournables

**① Annuler le gradient**

$$\vec{\nabla}f(x,y) = \vec{0} \iff \begin{cases} \dfrac{\partial f}{\partial x}(x,y) = 0 \\[6pt] \dfrac{\partial f}{\partial y}(x,y) = 0 \end{cases}$$

> Résoudre le système simultané. Les solutions $(x_0, y_0)$ sont les **points critiques** candidats.

---

**② Calculer la matrice Hessienne en chaque point critique**

$$H_f(x_0, y_0) = \begin{pmatrix} r & s \\ s & t \end{pmatrix} = \begin{pmatrix} \dfrac{\partial^2 f}{\partial x^2} & \dfrac{\partial^2 f}{\partial x \partial y} \\[10pt] \dfrac{\partial^2 f}{\partial y \partial x} & \dfrac{\partial^2 f}{\partial y^2} \end{pmatrix}$$

> Le théorème de Schwarz garantit que la hessienne est **symétrique** pour les fonctions $C^2$.

---

**③ Analyser via le discriminant $\Delta = rt - s^2$**

$$\boxed{\Delta = rt - s^2 = \det(H_f)}$$

| Valeur de $\Delta$ | Conclusion |
|--------------------|------------|
| $\Delta < 0$ | **Point Col (selle)** — valeurs propres de signes opposés. Pas d'extremum. |
| $\Delta > 0$ et $r + t > 0$ | **Minimum local** — valeurs propres positives |
| $\Delta > 0$ et $r + t < 0$ | **Maximum local** — valeurs propres négatives |
| $\Delta = 0$ | **Cas douteux** — méthode insuffisante. Vérifier le calcul. |

---

## 02 · Intégrales Doubles & Changements de Variables

### 📐 Contexte

Calculer $\iint_D f(x,y)\,dx\,dy$ où $D$ est un domaine "tordu" (disque, triangle, parabole…). La clé est de bien choisir l'**ordre d'intégration** ou de passer en **coordonnées polaires** quand le domaine a une symétrie circulaire.

---

### ∬ Théorème de Fubini

**Domaine décrit par des fonctions-bornes :**

$$D = \{(x,y) \mid a \le x \le b,\; \phi_1(x) \le y \le \phi_2(x)\}$$

$$\boxed{\iint_D f(x,y)\,dx\,dy = \int_a^b \!\left(\int_{\phi_1(x)}^{\phi_2(x)} f(x,y)\,dy\right) dx}$$

> **Hack :** Commence *toujours* par intégrer par rapport à la variable dont les bornes dépendent de l'autre.

> **Domaine triangulaire *(Annale 2022 Q16)* :** Il faut souvent **changer l'ordre d'intégration** ou couper le domaine en deux. **Dessiner le domaine** est indispensable avant de commencer.

---

### Passage en Coordonnées Polaires

$$\begin{cases} x = r\cos\theta \\ y = r\sin\theta \end{cases} \qquad r \ge 0,\; \theta \in [0, 2\pi[$$

## 🚨 JACOBIEN — Source de 50% des erreurs !

$$\boxed{dx\,dy = r\,dr\,d\theta}$$

> Ne **JAMAIS** oublier le facteur $r$ ! La relation $x^2 + y^2 = r^2$ simplifie les intégrandes de la forme $e^{-(x^2+y^2)}$.

---

### ⚡ Hack — Preuve de l'intégrale de Gauss par polaires

Pour prouver que $\int_{-\infty}^{+\infty} e^{-x^2}dx = \sqrt{\pi}$, on calcule le carré :

**①** $I^2 = \left(\int e^{-x^2}dx\right)\!\left(\int e^{-y^2}dy\right) = \iint_{\mathbb{R}^2} e^{-(x^2+y^2)}\,dx\,dy$

**②** Passage en polaire :

$$I^2 = \int_0^{2\pi}\!\int_0^{+\infty} e^{-r^2}\,r\,dr\,d\theta = 2\pi \cdot \frac{1}{2} = \pi$$

**③** Donc $\boxed{I = \sqrt{\pi}}$.

> La substitution $u = r^2$ donne $\int_0^\infty e^{-r^2} r\,dr = \frac{1}{2}$.

---

## 03 · Intégrales à Paramètres

### 📐 Contexte

On définit $F(x) = \int_a^b f(x,t)\,dt$. La **condition clé** est toujours l'existence d'une *fonction dominante intégrable*.

---

### ∂ Les deux théorèmes fondamentaux

**Théorème de continuité sous le signe $\int$ :**

Conditions suffisantes :

| Condition | Contenu |
|-----------|---------|
| C1 | $t \mapsto f(x,t)$ continue par morceaux sur $[a,b]$ |
| C2 | $x \mapsto f(x,t)$ continue pour presque tout $t$ |
| **C3 ★** | Il existe $\phi(t)$ **intégrable** telle que $\|f(x,t)\| \le \phi(t)$ pour tout $x$ |

> Si C1, C2, C3 sont satisfaites → **$F(x)$ est continue**.

---

**Théorème de Leibniz — Dérivation sous le signe $\int$ :**

$$\boxed{F'(x) = \int_a^b \frac{\partial f}{\partial x}(x,t)\,dt}$$

> Valable si les mêmes conditions de domination s'appliquent à $\dfrac{\partial f}{\partial x}$ (pas seulement à $f$).

> **Utilisation au concours :** On vérifie qu'une solution sous forme intégrale satisfait une équation différentielle en dérivant $F(x)$ à l'aide de Leibniz.

---

> **Résumé :** Les deux théorèmes ont la *même structure*. La seule différence est la condition de domination : pour la continuité, on domine $f$ ; pour la dérivabilité, on domine $\partial f / \partial x$.

---

## 04 · Champs de Vecteurs & Formes Différentielles

### 📐 Contexte

Notions plus avancées qui apparaissent dans les **annales les plus difficiles**. La question centrale est toujours : ce champ dérive-t-il d'un potentiel ?

---

### 🧭 Circulation d'un champ

$$\boxed{\mathcal{C} = \int_\gamma \vec{V} \cdot d\vec{l}}$$

> Intégrale curviligne du champ $\vec{V}$ le long de la courbe orientée $\gamma$. Mesure le "travail" du champ le long du chemin.

---

### Champ qui dérive d'un potentiel

**Condition nécessaire et suffisante *(sur domaine simplement connexe)* :**

$$\boxed{\vec{V} = \vec{\nabla}f \iff \vec{\text{rot}}(\vec{V}) = \vec{0}}$$

**Circulation sur chemin fermé :**

$$\oint_\gamma \vec{\nabla}f \cdot d\vec{l} = 0$$

**Théorème fondamental — Indépendance du chemin :**

$$\boxed{\int_A^B \vec{\nabla}f \cdot d\vec{l} = f(B) - f(A)}$$

> Si le champ dérive du potentiel $f$, la circulation ne dépend *que* des points de départ et d'arrivée — **pas du chemin parcouru**.

---

### ⚡ Hack — Stratégie QCM

1. **Calculer le rotationnel** de $\vec{V}$.
   - Si $\vec{\text{rot}}(\vec{V}) \ne \vec{0}$ → pas de potentiel → les intégrales dépendent du chemin.
   - Si $\vec{\text{rot}}(\vec{V}) = \vec{0}$ et domaine simplement connexe → potentiel existe.

2. **Si potentiel :** pour calculer la circulation, utilise $f(B) - f(A)$ **sans intégrer le long du chemin**.

---

### ★ Rotationnel en 2D — Condition simplifiée

Pour $\vec{V} = (P, Q)$ en 2D, le rotationnel est nul si et seulement si :

$$\boxed{\frac{\partial Q}{\partial x} = \frac{\partial P}{\partial y}}$$

> C'est la **condition d'exactitude** de la forme différentielle $P\,dx + Q\,dy$. Si cette condition est satisfaite, le potentiel $f$ peut être trouvé par intégration.

---

*Fiche auto-suffisante — Bloc 5 Maths · Analyse Multivariable & Intégration*