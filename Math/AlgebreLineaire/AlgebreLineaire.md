# ⚙️ BLOC 3 MATHS — Algèbre Linéaire & Géométrie
> **Fiche auto-suffisante** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--le-scan-rapide-dune-matrice) | Le Scan Rapide d'une Matrice | Fondamental |
| [02](#02--réduction--diagonalisation) | Réduction — Diagonalisation | Tombé en 2021 |
| [03](#03--espaces-vectoriels--noyau-image--rang) | Espaces Vectoriels — Noyau, Image & Rang | |
| [04](#04--géométrie-euclidienne) | Géométrie Euclidienne | Tombé en 2025 |

---

## 01 · Le Scan Rapide d'une Matrice

### 📐 Contexte

On te donne une matrice $A$. Avant de calculer quoi que ce soit, tu dois en extraire un maximum d'informations **"visuelles"** en 30 secondes. Cette checklist peut te donner la réponse sans aucun calcul.

---

### 🔍 Checklist Zéro Calcul

**① Est-elle symétrique réelle ($A^T = A$) ?**

> → **Théorème Spectral !** Elle est diagonalisable dans une base orthonormée. Ses valeurs propres sont réelles. Ses sous-espaces propres sont orthogonaux.

**② Est-elle triangulaire (ou diagonale) ?**

> → **Valeurs propres = termes diagonaux.** Det = produit des termes diagonaux. Rang = nombre de pivots non nuls.
> Pas besoin de calculer $\det(A - \lambda I)$ : les VP se lisent directement.

**③ Y a-t-il des lignes/colonnes proportionnelles ou nulles ?**

> → **Matrice non inversible.** $\det(A) = 0$. $0$ est une valeur propre. Rang < taille de la matrice.
>
> **Hack :** Le nombre de relations de dépendance linéaire entre les colonnes donne $\dim(\ker(A))$. Si 3 colonnes sur 4 sont identiques, $\dim(\ker(A)) \ge 2$.

---

### ⚡ Hack Trace & Déterminant — Vérificateurs ultra-rapides

Pour une matrice avec valeurs propres $\lambda_1, \ldots, \lambda_n$ :

$$\text{Tr}(A) = \sum_i \lambda_i \qquad \det(A) = \prod_i \lambda_i$$

> Après avoir trouvé tes valeurs propres, vérifie immédiatement que leur somme = Tr(A) et leur produit = det(A). Toute erreur sera détectée instantanément.

---

## 02 · Réduction — Diagonalisation

### 📐 Contexte

Le GEI-UNIV adore donner une matrice et demander si elle est diagonalisable et quelles sont ses valeurs propres. La méthode est **toujours la même** : polynôme caractéristique → analyse des racines → dimension des sous-espaces propres.

---

### ⬡ L'Arbre de Décision de la Diagonalisabilité

**① Calculer le polynôme caractéristique**

$$\boxed{P_A(\lambda) = \det(A - \lambda I)}$$

> Les racines de ce polynôme sont les **valeurs propres**. La multiplicité de chaque racine = multiplicité algébrique $m_k$.

**② Analyser les racines et conclure**

| Cas | Condition | Conclusion |
|-----|-----------|------------|
| ✅ | Polynôme scindé à **racines simples** (toutes de multiplicité 1) | **Diagonalisable** — fin de l'histoire |
| ✅ | Pour chaque VP multiple $\lambda_k$ : $\dim(E_{\lambda_k}) = m_k$ | **Diagonalisable** |
| ❌ | Il existe une VP pour laquelle $\dim(E_{\lambda_k}) < m_k$ | **Non diagonalisable** |

> Pour calculer $E_{\lambda_k} = \ker(A - \lambda_k I)$ : résoudre le système $(A - \lambda_k I)\mathbf{x} = \mathbf{0}$.

---

### Théorèmes raccourcis — À connaître par cœur

**Polynôme annulateur *(tombé en 2021)* :**

Si tu trouves un polynôme $P$ tel que $P(A) = 0$, alors les valeurs propres de $A$ sont **obligatoirement parmi les racines de $P$**.

$$\text{Exemple : } A^2 - 3A + 2I = 0 \implies P(X) = (X-1)(X-2)$$

> Les seules VP possibles sont **1 et 2**. De plus, $P$ est scindé à racines simples → $A$ est **diagonalisable** !

**Trace et Déterminant :**

| Relation | Formule |
|----------|---------|
| $\text{Tr}(A)$ | $= \sum_i \lambda_i$ — somme des VP comptées avec multiplicité |
| $\det(A)$ | $= \prod_i \lambda_i$ — produit des VP comptées avec multiplicité |

---

## 03 · Espaces Vectoriels — Noyau, Image & Rang

### 📐 Contexte

Questions de cours pures mais **fondamentales** sur les dimensions. Le théorème du rang est la formule la plus importante de l'algèbre linéaire.

---

### 🗺️ Le Théorème du Rang

Pour une application linéaire $u : E \to F$ :

$$\boxed{\dim(E) = \dim(\ker(u)) + \dim(\text{Im}(u))}$$

$$\dim(E) = \underbrace{\dim(\ker(u))}_{\text{noyau}} + \underbrace{\text{rang}(u)}_{\text{image}}$$

| Terme | Définition |
|-------|-----------|
| $\ker(u)$ | Noyau : $\{x \in E \mid u(x) = \mathbf{0}\}$ — vecteurs envoyés sur 0 |
| $\text{Im}(u)$ | Image : tous les vecteurs atteignables = espace engendré par les colonnes |
| $\text{rang}(u)$ | $= \dim(\text{Im}(u))$ = nombre de colonnes indépendantes |

---

### Hacks QCM — Injectivité, Surjectivité, Bijectivité

| Propriété | Condition équivalente | Sens intuitif |
|-----------|----------------------|---------------|
| **Injective** | $\ker(u) = \{\mathbf{0}\}$ | Chaque élément de F a *au plus* un antécédent |
| **Surjective** | $\text{Im}(u) = F$ | Chaque élément de F a *au moins* un antécédent |
| **Bijective** | Injective ET surjective | Chaque élément de F a *exactement* un antécédent |

> **Si $\dim(E) = \dim(F)$ (endomorphisme) :** Injective $\iff$ Surjective $\iff$ Bijective. Il suffit de vérifier l'une des trois !

---

### ★ Application directe — QCM type

Matrice $A$ de taille $4 \times 4$ de rang 3. Alors :
- $\dim(\ker(A)) = 4 - 3 = 1$ → noyau = droite vectorielle.
- $0$ est valeur propre de $A$.
- $A$ n'est pas inversible ($\det = 0$).
- $A$ n'est pas injective, pas bijective.

---

## 04 · Géométrie Euclidienne

### 📐 Contexte

Le concours 2025 a fortement insisté sur les notions d'**orthogonalité**, de **projections** et de **bases orthonormées**. Les définitions sont précises et les pièges nombreux.

---

### Sous-espace orthogonal $F^\perp$

$$F^\perp = \{v \in E \mid \langle v, w \rangle = 0 \;\text{pour tout}\; w \in F\}$$

> L'ensemble des vecteurs orthogonaux à **tous** les vecteurs de F (pas seulement à certains).

**Propriétés fondamentales :**

| Propriété | Formule/Résultat |
|-----------|-----------------|
| **Dimension** | $\dim(F) + \dim(F^\perp) = \dim(E)$ |
| **Involutivité** | $(F^\perp)^\perp = F$ en dimension finie |
| **Décomposition** | $E = F \oplus F^\perp$ — tout vecteur se décompose de façon unique |

---

### Projecteur Orthogonal $p_F$

> Associe à chaque vecteur $x$ son "ombre" sur $F$. Minimise la distance $\|x - p_F(x)\|$.

**Un projecteur $p$ est orthogonal si et seulement si :**

1. $p \circ p = p$ — c'est un projecteur (idempotent).
2. $p$ est **symétrique** — sa matrice dans une base orthonormée vérifie $p^T = p$.

> **Hack :** $\ker(p) = \text{Im}(p)^\perp$. Le noyau du projecteur orthogonal sur F est exactement $F^\perp$.

---

### Matrices Orthogonales

Une matrice de passage $P$ entre deux bases **orthonormées** est une **matrice orthogonale**.

$$\boxed{P^{-1} = P^T} \qquad \boxed{\det(P) = \pm 1}$$

| Valeur | Interprétation |
|--------|----------------|
| $\det(P) = +1$ | **Rotation** — orientation conservée |
| $\det(P) = -1$ | **Réflexion** — orientation inversée |

---

### Méthode de Gram-Schmidt — Orthonormalisation

Transforme une base quelconque $(e_1, e_2, \ldots)$ en une base orthonormée $(u_1, u_2, \ldots)$ :

**① Normaliser le premier vecteur :**

$$u_1 = \frac{e_1}{\|e_1\|}$$

**② Retirer à $e_2$ sa projection sur $u_1$ (orthogonaliser) :**

$$v_2 = e_2 - \langle e_2, u_1 \rangle\, u_1$$

**③ Normaliser le résultat :**

$$u_2 = \frac{v_2}{\|v_2\|}$$

> Répéter pour chaque vecteur suivant : projeter sur tous les $u_i$ déjà construits, soustraire, normaliser.

---

### ⚠️ Pièges classiques

> **"Un projecteur est toujours symétrique."** → **FAUX.** Un projecteur $p \circ p = p$ n'est symétrique que s'il est *orthogonal*. Un projecteur oblique n'est pas symétrique.

> **"Si $P^{-1} = P^T$, alors $\det(P) = 1$."** → **FAUX.** On a $\det(P) = \pm 1$. Le déterminant $-1$ correspond aux réflexions.

---

*Fiche auto-suffisante — Bloc 3 Maths · Algèbre Linéaire & Géométrie*