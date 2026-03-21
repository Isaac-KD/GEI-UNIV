# 📏 BLOC 0 — Analyse Dimensionnelle & Unités
> **Fiche auto-suffisante · Le Hack du QCM** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--les-7-piliers-du-système-international-si) | Les 7 Piliers du Système International (SI) | Tombé en 2023 |
| [02](#02--la-pyramide-de-la-mécanique) | La Pyramide de la Mécanique | Tombé en 2021 & 2023 |
| [03](#03--les-constantes-fondamentales) | Les Constantes Fondamentales | Tombé en 2025 |
| [04](#04--lélectromagnétisme-sans-douleur) | L'Électromagnétisme Sans Douleur | Tombé en 2023 |

---

## 01 · Les 7 Piliers du Système International (SI)

### 📐 Contexte physique

Toute grandeur physique dans l'univers, aussi complexe soit-elle, n'est qu'une **combinaison de ces 7 dimensions fondamentales**. Les connaître permet de vérifier n'importe quelle formule ou d'identifier n'importe quelle constante par simple analyse dimensionnelle.

L'analyse dimensionnelle est le **super-pouvoir du QCM** : quand on ne sait pas quelle formule appliquer, on regarde quelle réponse a les bonnes unités — et on élimine toutes les autres.

---

### Les 7 unités fondamentales

| Symbole | Dimension | Unité SI | Piège |
|---------|-----------|----------|-------|
| **[M]** | Masse | **Kilogramme (kg)** | ⚠️ Tombé 2023 Q21 : c'est le **kg**, PAS le gramme ! |
| **[L]** | Longueur | Mètre (m) | |
| **[T]** | Temps | Seconde (s) | |
| **[I]** | Intensité électrique | Ampère (A) | |
| **[Θ]** | Température | Kelvin (K) | |
| **[N]** | Quantité de matière | Mole (mol) | |
| **[J]** | Intensité lumineuse | Candela (cd) | Très rare au concours |

---

### ⚡ Méthode — Utiliser l'analyse dimensionnelle en QCM

1. Identifie la grandeur à trouver et ses **dimensions attendues**.
2. Calcule les dimensions de chaque réponse proposée.
3. **Élimine** toutes celles dont les dimensions ne correspondent pas.
4. Si une seule reste → c'est forcément la bonne.

---

## 02 · La Pyramide de la Mécanique

### 📐 Contexte physique

Ne retiens pas les équations dimensionnelles complexes par cœur — retiens **le chemin pour y arriver** via des formules ultra-basiques. Chaque grandeur se déduit de la précédente par une opération simple.

La clé : **tout part de $F = ma$** (le PFD). Force × distance = énergie. Énergie / temps = puissance. Force / surface = pression.

---

### 🔺 Les 4 niveaux

**① Force — Le Newton (N)**

> Formule de secours : $F = m \cdot a$ (PFD)

$$\boxed{[F] = M \cdot L \cdot T^{-2}} \quad = \text{kg·m·s}^{-2}$$

---

**② Énergie / Travail — Le Joule (J) 🌟 LE PLUS IMPORTANT**

> Formule de secours : $W = F \cdot d$ ou $E_c = \frac{1}{2}mv^2$

$$\boxed{[E] = M \cdot L^2 \cdot T^{-2}} \quad = \text{kg·m}^2\text{·s}^{-2} = \text{N·m}$$

> C'est la **dimension pivot** : presque toutes les autres en découlent. À retenir absolument.

---

**③ Puissance — Le Watt (W)**

> Formule de secours : $P = E/t$ (énergie par unité de temps)

$$\boxed{[P] = M \cdot L^2 \cdot T^{-3}} \quad = \text{J·s}^{-1}$$

---

**④ Pression — Le Pascal (Pa)**

> Formule de secours : $P = F/S$ (force divisée par une surface)

$$\boxed{[P] = M \cdot L^{-1} \cdot T^{-2}} \quad = \text{N·m}^{-2} = \text{kg·m}^{-1}\text{·s}^{-2}$$

---

### 🚨 Hack du concours — Pression = Densité d'énergie *(tombé en 2021 & 2023 Q21)*

La pression a les mêmes dimensions que l'énergie par unité de volume. Preuve :

$$\frac{F}{S} = \frac{F \cdot L}{S \cdot L} = \frac{\text{Énergie}}{\text{Volume}} \;\Rightarrow\; [P] = \mathbf{J \cdot m^{-3}}$$

**→ VRAI : La pression peut s'exprimer en J·m⁻³ (densité d'énergie).** Cette équivalence apparaît directement en thermodynamique : $PV$ a les dimensions d'une énergie.

---

### ★ Récapitulatif dimensionnel mécanique

| Grandeur | Formule-clé | Dimension | Unité SI |
|----------|-------------|-----------|----------|
| **Force** | $F = ma$ | $M \cdot L \cdot T^{-2}$ | N = kg·m·s⁻² |
| **Énergie** ⭐ | $W = Fd$ | $M \cdot L^2 \cdot T^{-2}$ | J = kg·m²·s⁻² |
| **Puissance** | $P = E/t$ | $M \cdot L^2 \cdot T^{-3}$ | W = J·s⁻¹ |
| **Pression** | $P = F/S$ | $M \cdot L^{-1} \cdot T^{-2}$ | Pa = N·m⁻² |

---

## 03 · Les Constantes Fondamentales

### 📐 Contexte physique

Le jury adore donner la dimension d'une constante et te demander de l'identifier — comme en **2025 Q21**. La méthode est toujours la même : **trouve une formule où la constante apparaît isolée**, puis exprime sa dimension à partir de ce qu'elle égale.

Ne mémorise pas les dimensions par cœur : mémorise la *formule de secours* pour les retrouver en 10 secondes.

---

### 🔬 Constante de Planck $h$ — *Réponse exacte 2025 Q21*

> Formule de secours : $E = h\nu$ (énergie d'un photon)

$$h = \frac{E}{\nu} \;\Rightarrow\; [h] = \frac{M \cdot L^2 \cdot T^{-2}}{T^{-1}} = \boxed{M \cdot L^2 \cdot T^{-1}}$$

| Propriété | Valeur |
|-----------|--------|
| **Unité SI** | **J·s** (Joules-seconde) |
| **Valeur** | $h = 6{,}626 \times 10^{-34}\;\text{J·s}$ |
| **Note** | Même dimension qu'un *moment cinétique* |

---

### Constante des gaz parfaits $R$ — *Réponse exacte 2025 Q21*

> Formule de secours : $PV = nRT$ → $R = PV/(nT)$ = Énergie / (n × T)

$$[R] = \frac{M \cdot L^2 \cdot T^{-2}}{N \cdot \Theta} = \boxed{M \cdot L^2 \cdot T^{-2} \cdot \Theta^{-1} \cdot N^{-1}}$$

| Propriété | Valeur |
|-----------|--------|
| **Unité SI** | **J·K⁻¹·mol⁻¹** |
| **Valeur** | $R = 8{,}314\;\text{J·mol}^{-1}\text{·K}^{-1}$ |

> ⚠️ Le fait que $PV$ ait les dimensions d'une énergie est lui-même un hack : c'est la même conséquence que Pression = Densité d'énergie (section 02).

---

### Constante de Boltzmann $k_B$

> Formule de secours : $E = k_B T$ (énergie thermique d'une particule)

$$k_B = \frac{E}{T} \;\Rightarrow\; [k_B] = \boxed{M \cdot L^2 \cdot T^{-2} \cdot \Theta^{-1}}$$

| Propriété | Valeur |
|-----------|--------|
| **Unité SI** | **J·K⁻¹** |
| **Valeur** | $k_B = 1{,}38 \times 10^{-23}\;\text{J·K}^{-1}$ |

> **Relation utile :** $R = N_A \cdot k_B$ où $N_A = 6{,}022 \times 10^{23}\;\text{mol}^{-1}$. $R$ est à l'échelle molaire, $k_B$ est à l'échelle d'une seule particule.

---

## 04 · L'Électromagnétisme Sans Douleur

### 📐 Contexte physique

Ne te perds jamais dans les équations de Maxwell pour trouver une dimension électrique. La méthode est toujours la même : **ramène tout à l'énergie ou à la force**, que tu sais déjà exprimer en M, L, T, I.

---

### ⚡ Grandeurs électriques fondamentales

**Charge électrique $q$ — Le Coulomb (C) :**

$$\boxed{q = I \cdot t \;\Rightarrow\; [q] = I \cdot T}$$

> 1 Coulomb = 1 Ampère × 1 seconde.

**Tension $U$ — Le Volt (V) :**

$$E = qU \;\Rightarrow\; U = \frac{E}{q} \;\Rightarrow\; \boxed{[U] = M \cdot L^2 \cdot T^{-3} \cdot I^{-1}}$$

> **Le Volt, c'est des Joules par Coulomb (J·C⁻¹).**

**Champ électrique $\vec{E}$ — *(tombé en 2023 Q21)* :**

$$\boxed{U = E \cdot d \;\Rightarrow\; [E] = V \cdot m^{-1}} \quad \text{et aussi} \quad \boxed{F = qE \;\Rightarrow\; [E] = N \cdot C^{-1}}$$

> Ces deux unités sont **strictement équivalentes** : $V\cdot m^{-1} = N\cdot C^{-1}$.  
> "Un champ électrique peut s'exprimer en N·C⁻¹" → **VRAI** ✓

---

### Composants passifs — Pense aux énergies stockées !

**Condensateur $C$ — Le Farad (F) :**

$$E = \tfrac{1}{2}CU^2 \;\Rightarrow\; C = \frac{2E}{U^2} \;\Rightarrow\; \boxed{[C] = J \cdot V^{-2}}$$

**Bobine $L$ — Le Henry (H) :**

$$E = \tfrac{1}{2}LI^2 \;\Rightarrow\; L = \frac{2E}{I^2} \;\Rightarrow\; \boxed{[L] = J \cdot A^{-2}}$$

**Résistance $R$ — L'Ohm (Ω) :**

$$U = RI \;\Rightarrow\; R = \frac{U}{I} \;\Rightarrow\; \boxed{[R] = V \cdot A^{-1} = \Omega}$$

---

### ★ Cheat sheet électrique complète

| Grandeur | Formule-clé | Unité pratique |
|----------|-------------|----------------|
| Charge $q$ | $q = It$ | C = A·s |
| Tension $U$ | $E = qU$ | V = J·C⁻¹ |
| Champ $\vec{E}$ | $U = Ed$ ou $F = qE$ | **V·m⁻¹ = N·C⁻¹** ✓ |
| Résistance $R$ | $U = RI$ | Ω = V·A⁻¹ |
| Capacité $C$ | $E = \frac{1}{2}CU^2$ | F = J·V⁻² |
| Inductance $L$ | $E = \frac{1}{2}LI^2$ | H = J·A⁻² |

---

### ⚠️ Le piège classique — Unité SI de la masse

> L'unité SI de la masse est le **kilogramme (kg)**, PAS le gramme.
>
> Conséquence : quand tu calcules une dimension, utilise des **kg** et non des g. Utiliser des grammes donne un résultat faux d'un facteur 1000.
>
> **Tombé en 2023 Q21** — ne pas rater ce point facile.

---

*Fiche auto-suffisante — Bloc 0 · Analyse Dimensionnelle & Unités*