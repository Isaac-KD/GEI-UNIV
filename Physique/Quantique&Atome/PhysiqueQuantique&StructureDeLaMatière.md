# ⚛️ BLOC 3 — Physique Quantique & Structure de la Matière
> **Fiche auto-suffisante · 100% QCM** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--latome--la-règle-de-klechkowski) | L'Atome & La Règle de Klechkowski | Tombé en 2023 |
| [02](#02--le-modèle-de-bohr--énergies--mécanique) | Le Modèle de Bohr — Énergies & Mécanique | Tombé en 2025 |
| [03](#03--dualité-onde-corpuscule--effet-photoélectrique) | Dualité Onde-Corpuscule & Effet Photoélectrique | ↑ Mis à jour |
| [04](#04--le-puits-de-potentiel-infini) | Le Puits de Potentiel Infini | ✦ Nouveau |
| [05](#05--mécanique-quantique--schrödinger--heisenberg) | Mécanique Quantique — Schrödinger & Heisenberg | Tombé en 2025 |

---

## 01 · L'Atome & La Règle de Klechkowski

### 📐 Contexte physique

Pour construire la configuration électronique d'un atome, on remplit les sous-couches dans un **ordre précis** dicté par la règle de Klechkowski (règle $n+l$). Chaque sous-couche a une capacité maximale d'électrons déterminée par sa lettre.

Les **électrons de valence** sont ceux de la couche de plus grand $n$ : ce sont eux qui participent aux liaisons chimiques et qui partent en premier lors de l'ionisation — sauf piège des métaux de transition !

---

### ⚛️ Ordre de remplissage

$$1s \to 2s \to 2p \to 3s \to 3p \to \mathbf{4s} \to \mathbf{3d} \to 4p \to \ldots$$

> ⚠️ Le **4s se remplit avant le 3d** ! On remplit par ordre de $(n+l)$ croissant, puis par $n$ croissant en cas d'égalité.

**Capacités maximales :**

| Sous-couche | Orbitales | Électrons max |
|-------------|-----------|---------------|
| **s** | 1 | **2** |
| **p** | 3 | **6** |
| **d** | 5 | **10** |
| **f** | 7 | **14** |

---

### ⚡ Hack — L'ionisation des métaux de transition *(tombé en 2023)*

**Règle générale :** Électrons de valence = ceux du $n$ le plus élevé + sous-couche en cours.

**Le piège du Fer :** Configuration du fer neutre : $\text{Fe} = [\text{Ar}]\,4s^2\,3d^6$.

On penserait que le fer perd ses électrons $3d$ en s'ionisant. **FAUX.**

Quand le fer s'ionise en $\text{Fe}^{2+}$, **il perd d'abord ses électrons $4s$** :

$$\text{Fe}^{2+} = [\text{Ar}]\,4s^0\,3d^6$$

> Raison : une fois les électrons $4s$ présents, la répulsion électronique rend les électrons $3d$ plus stables (plus liés) que les $4s$. L'ionisation retire toujours les électrons les *moins liés*.

---

## 02 · Le Modèle de Bohr — Énergies & Mécanique

### 📐 Contexte physique

Le modèle de Bohr décrit l'atome d'hydrogène comme un électron tournant sur des **orbites circulaires quantifiées** autour du noyau. Ce n'est pas la mécanique quantique complète, mais il prédit correctement les énergies des niveaux de l'hydrogène et les raies spectrales.

En 2025, le jury a posé des questions non seulement sur les énergies, mais sur la **mécanique de l'électron en orbite** : force, vitesse, moment cinétique.

---

### 🔵 Formules mécaniques dures *(tombé en 2025 — Q29)*

**Force de Coulomb — Le piège du signe :**

$$\boxed{\vec{F} = -\frac{e^2}{4\pi\varepsilon_0 r^2}\,\vec{u}_r}$$

> L'électron $(-e)$ est **attiré** par le proton $(+e)$. La force est attractive → dirigée vers le centre → le signe "$-$" sur $\vec{u}_r$ (vecteur *sortant*). Une force répulsive aurait un signe "$+$".

**Quantification — Postulat de Bohr :**

$$\boxed{L = m_e v r = n\frac{h}{2\pi} = n\hbar}$$

> Le moment cinétique $L$ ne prend que des valeurs **discrètes**, multiples entiers de $\hbar = h/2\pi$. Avec $n = 1, 2, 3, \ldots$

**Vitesse sur l'orbite $n$ :**

$$\boxed{v = \frac{e}{\sqrt{4\pi\varepsilon_0\, m_e\, r}}}$$

> S'obtient en égalisant l'accélération centripète $(v^2/r)$ et la force de Coulomb. Plus l'orbite est grande, plus l'électron va *lentement*.

---

### Énergies des niveaux

$$\boxed{E_n = -\frac{13{,}6}{n^2}\;\text{eV}}$$

> - L'énergie est **négative** (état lié).
> - Proportionnelle à $1/n^2$ : les niveaux se *resserrent* en montant (contrairement au puits infini).
> - À $n \to \infty$ : $E = 0$ → électron ionisé (libre).

| Niveau | Énergie |
|--------|---------|
| $n = 1$ (fondamental) | $-13{,}6\;\text{eV}$ |
| $n = 2$ | $-3{,}4\;\text{eV}$ |
| $n = 3$ | $-1{,}51\;\text{eV}$ |
| $n \to \infty$ | $0\;\text{eV}$ (ionisé) |

---

### ★ Émission et absorption de photons

- Un électron qui **descend** ($n_i \to n_f$, $n_f < n_i$) **émet** un photon.
- Un électron qui **monte** de niveau **absorbe** un photon.

$$\boxed{E_{\text{photon}} = |E_{\text{final}} - E_{\text{initial}}| = h\nu}$$

> Exemple : transition $n=3 \to n=1$ → photon d'énergie $|{-1{,}51} - ({-13{,}6})| = 12{,}09\;\text{eV}$.

---

## 03 · Dualité Onde-Corpuscule & Effet Photoélectrique

### 📐 Contexte physique

La physique quantique révèle que la distinction "onde" vs "particule" est une fausse dichotomie. **Toute particule matérielle se comporte aussi comme une onde** (de Broglie), et **toute onde EM se comporte aussi comme un flux de particules** (photons, Einstein).

---

### 🌊 Longueur d'onde de De Broglie *(tombé en 2023)*

$$\boxed{\lambda = \frac{h}{p} = \frac{h}{mv}}$$

> Toute particule possédant une quantité de mouvement $p = mv$ est associée à une onde de longueur $\lambda$. **Valable pour tout objet** : électron, proton, atome, balle de tennis — mais pour les objets macroscopiques, $\lambda$ est inobservable.

---

### Effet Photoélectrique — Einstein

**Bilan énergétique :**

$$\boxed{E_{\text{photon}} = W_{\text{extraction}} + E_{\text{cinétique max}}}$$

$$h\nu = W_{\text{extraction}} + \tfrac{1}{2}m_e v_{\max}^2$$

> Un photon incident cède son énergie $h\nu$ à un électron. $W_{\text{extraction}}$ (travail de sortie, propre au matériau) est utilisé pour arracher l'électron. Le reste devient énergie cinétique.

---

### ⚠️ Piège — Fréquence seuil

> Si la lumière incidente a une fréquence **trop faible** ($h\nu < W_{\text{extraction}}$) :
>
> - **Aucun électron n'est arraché**, même si tu augmentes l'intensité à l'infini.
> - L'intensité (nombre de photons) n'a *aucun rôle* : c'est la **fréquence** (énergie individuelle du photon) qui compte.
> - C'est la preuve expérimentale que la lumière est quantifiée en photons d'énergie $h\nu$.

---

### Constantes à connaître

| Constante | Valeur |
|-----------|--------|
| $h$ (Planck) | $6{,}626 \times 10^{-34}\;\text{J·s}$ |
| $\hbar = h/2\pi$ | $1{,}055 \times 10^{-34}\;\text{J·s}$ |
| $1\;\text{eV}$ | $1{,}6 \times 10^{-19}\;\text{J}$ |

---

## 04 · Le Puits de Potentiel Infini
> ✦ **Section nouvelle** — classique incontournable des QCM

### 📐 Contexte physique

On enferme une particule (ex : un électron) dans une **boîte unidimensionnelle de largeur $L$** dont les murs sont impénétrables (potentiel infini aux bords). À l'intérieur, la particule est libre.

Ce modèle montre que la quantification des niveaux d'énergie est une *conséquence naturelle* des conditions aux limites imposées à la fonction d'onde — pas une hypothèse ad hoc comme chez Bohr.

---

### 📦 Formules dures *(tombé en 2023 — Q24)*

**Niveaux d'énergie quantifiés :**

$$\boxed{E_n = \frac{n^2 h^2}{8mL^2}} \quad \text{avec } n = 1, 2, 3, \ldots$$

> L'énergie est proportionnelle à **$n^2$** : plus on monte dans les niveaux, plus les écarts *augmentent*. C'est l'inverse de l'atome de Bohr.

**Fonction d'onde (solution) :**

$$\Psi_n(x) = \sqrt{\frac{2}{L}}\sin\!\left(\frac{n\pi x}{L}\right)$$

> Sinusoïde qui s'annule aux bords ($x=0$ et $x=L$). Le coefficient $\sqrt{2/L}$ assure la normalisation.

---

### Comparaison Puits infini vs Atome de Bohr

| Propriété | Puits infini | Atome de Bohr |
|-----------|-------------|---------------|
| Énergie ∝ | $n^2$ | $1/n^2$ |
| Niveaux en montant | S'**écartent** | Se **resserrent** |
| Énergie fondamentale | $E_1 > 0$ | $E_1 = -13{,}6\;\text{eV}$ |

---

### ⚠️ Deux pièges classiques du concours

> **Piège 1 — Proportionnalité :** Ne pas confondre $E_n \propto n^2$ (puits) avec $E_n \propto 1/n^2$ (Bohr).

> **Piège 2 — Énergie du niveau fondamental :**
>
> *"L'énergie du niveau fondamental est nulle."* → **FAUX !**
>
> Le premier niveau est $n=1$ → $E_1 = h^2/(8mL^2) > 0$.
>
> **Une particule quantique enfermée ne peut jamais être totalement immobile.** C'est une conséquence du principe d'Heisenberg : si la position est connue (dans la boîte), l'impulsion ne peut pas être exactement nulle.

---

## 05 · Mécanique Quantique — Schrödinger & Heisenberg

### 📐 Contexte physique

L'équation de Schrödinger est la **loi fondamentale de la mécanique quantique** : elle gouverne l'évolution de la fonction d'onde $\Psi$ dans le temps. $\Psi$ n'est pas directement observable — c'est une *amplitude de probabilité* dont le carré donne des probabilités réelles.

---

### 🎲 L'Équation de Schrödinger *(tombé en 2025)*

$$\boxed{i\hbar\frac{\partial\Psi}{\partial t} = -\frac{\hbar^2}{2m}\frac{\partial^2\Psi}{\partial x^2} + V(x)\Psi}$$

| Terme | Rôle |
|-------|------|
| $i\hbar\,\partial_t\Psi$ | Évolution temporelle de la fonction d'onde |
| $-\dfrac{\hbar^2}{2m}\partial_{xx}\Psi$ | Énergie cinétique quantique |
| $V(x)\Psi$ | Énergie potentielle (dépend du problème) |

---

### ⚡ Hack — La Linéarité *(hack Q31 — 2025)*

L'équation de Schrödinger est une équation **linéaire**. Cela implique le **principe de superposition** :

$$\boxed{\text{Si } \Psi_1 \text{ et } \Psi_2 \text{ sont solutions} \Rightarrow \alpha\Psi_1 + \beta\Psi_2 \text{ est aussi une solution.}}$$

> C'est le fondement mathématique de la *superposition quantique* (chat de Schrödinger, ordinateur quantique, interférences quantiques…).

---

### La Fonction d'Onde $\Psi$ — Radar à Vrai/Faux

**Densité de probabilité de présence :**

$$\boxed{dP = |\Psi(x,t)|^2\,dx}$$

> $|\Psi|^2$ est réelle, positive, et physiquement mesurable.  
> $\Psi$ elle-même est complexe et *non mesurable directement*.

**Condition de normalisation :**

$$\boxed{\int_{-\infty}^{+\infty} |\Psi(x,t)|^2\,dx = 1}$$

> La particule *existe quelque part* : la probabilité totale vaut 1. L'unité de $\Psi$ en 1D est le **m$^{-1/2}$**.

---

### Principe d'Incertitude d'Heisenberg

$$\boxed{\Delta x \cdot \Delta p_x \geq \frac{\hbar}{2}}$$

> On ne peut pas connaître *simultanément* et avec précision arbitraire la **position** et la **quantité de mouvement**. Plus $\Delta x \to 0$, plus $\Delta p_x \to \infty$.
>
> C'est ce principe qui explique pourquoi $E_1 > 0$ dans le puits : si la particule est dans la boîte ($\Delta x = L$), alors $\Delta p \geq \hbar/2L > 0$, donc elle bouge.

---

### ⚠️ Pièges Vrai/Faux récurrents

> **"La fonction d'onde $\Psi$ est directement observable."** → **FAUX.** Seul $|\Psi|^2$ a un sens physique.

> **"Le principe d'incertitude est dû à l'imprécision des instruments."** → **FAUX.** C'est une propriété *fondamentale de la nature*, indépendante de tout appareil.

> **"Une particule dans le niveau fondamental d'un puits est au repos."** → **FAUX.** Son énergie $E_1 > 0$ implique une énergie cinétique non nulle.

---

*Fiche auto-suffisante — Bloc 3 · Physique Quantique & Structure de la Matière*