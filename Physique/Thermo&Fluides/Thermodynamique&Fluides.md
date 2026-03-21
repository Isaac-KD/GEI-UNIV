# 🔬 BLOC 2 — Thermodynamique & Fluides
> **Fiche auto-suffisante · Version Ultime** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--thermodynamique--entropie) | Thermodynamique & Entropie | |
| [02](#02--squelette-calculatoire--énergie-enthalpie--laplace) | Squelette Calculatoire — Énergie, Enthalpie & Laplace | ✦ Nouveau |
| [03](#03--modèles-de-gaz--parfait-vs-réel) | Modèles de Gaz — Parfait vs Réel | |
| [04](#04--machines--cycles-thermodynamiques) | Machines & Cycles Thermodynamiques | + Carnot |
| [05](#05--rayonnement-thermique--le-corps-noir) | Rayonnement Thermique — Le Corps Noir | |
| [06](#06--statique-des-fluides--archimède) | Statique des Fluides & Archimède | + Glaçon + Atmosphère |
| [07](#07--transferts-thermiques) | Transferts Thermiques | |

---

## 01 · Thermodynamique & Entropie

### 📐 Contexte physique

La thermodynamique étudie les **échanges d'énergie** dans un système physique. Elle repose sur deux grands principes :

- Le **1er principe** dit que l'énergie se *conserve* : elle change juste de forme (travail ou chaleur), elle ne se crée ni ne se détruit.
- Le **2nd principe** dit que les phénomènes ont un *sens irréversible* : la chaleur va spontanément du chaud vers le froid, jamais l'inverse. Il introduit l'**Entropie $S$**, grandeur qui mesure le "désordre" et le sens naturel de l'évolution du système.

---

### ⚡ Équations fondamentales

**1er Principe — Bilan d'énergie**

$$\boxed{\Delta U = W + Q}$$

> La **variation d'énergie interne $U$** = Travail $W$ reçu + Chaleur $Q$ reçue.

---

**2nd Principe — Bilan d'entropie**

$$\boxed{\Delta S = S_{\text{échange}} + S_{\text{création}}}$$

**↳ Entropie échangée avec l'extérieur**

$$S_{\text{échange}} = \int \frac{\delta Q}{T_{\text{ext}}}$$

> Même signe que $Q$. Si le système refroidit : $S_{\text{échange}} < 0$. C'est l'entropie qui "rentre" ou "sort" via les échanges thermiques avec l'environnement de température $T_{\text{ext}}$. Unité : **J/K**.

**↳ Entropie créée à l'intérieur**

$$S_{\text{création}} \geq 0$$

> **Nulle** pour une transformation réversible (idéale). **Strictement positive** pour toute transformation réelle (irréversible). Elle ne peut jamais être négative.

---

### 🔑 Points clés

| Propriété | Détail |
|-----------|--------|
| **Unité de $S$** | $S = Q/T$ → Énergie / Température → **J/K** |
| **Extensivité** | Grandeur *extensive* : doubler le système double $S$. La température est *intensive* (doubler le système ne change pas $T$). |

---

### ⚠️ Piège — Système Isolé *(tombé en 2023 & 2025)*

Un système isolé n'échange *rien* : $Q = 0$ et $W = 0$ → $S_{\text{échange}} = 0$.

Le bilan devient :

$$\Delta S = S_{\text{création}} \geq 0$$

**➜ L'entropie d'un système isolé ne peut qu'augmenter — elle n'est jamais nulle !**

L'erreur classique : croire que $\Delta S = 0$ car "pas d'échange". Faux : $S_{\text{création}}$ reste positive dans le monde réel.

---

## 02 · Squelette Calculatoire — Énergie, Enthalpie & Laplace
> ✦ **Section nouvelle** — indispensable pour les calculs numériques

### 📐 Contexte physique

La thermodynamique, c'est d'abord des concepts, mais c'est ensuite un "squelette calculatoire" implacable. Pour **calculer concrètement** le travail ou la chaleur d'une transformation et obtenir une **valeur numérique**, il faut lier l'énergie à la température via les **capacités thermiques**.

Il en existe deux selon les conditions : à *volume constant* ($C_v$) ou à *pression constante* ($C_p$).

---

### 🧮 Lois de Joule — Gaz Parfait

Pour un gaz parfait, l'énergie interne $U$ et l'enthalpie $H$ ne dépendent **que de la température** (pas du volume, ni de la pression). C'est la propriété fondamentale du gaz parfait.

**Énergie interne :**

$$\boxed{dU = n \cdot C_v \cdot dT}$$

> Sert à calculer $\Delta U$. $C_v$ = capacité thermique à *volume constant*.

**Enthalpie :**

$$\boxed{dH = n \cdot C_p \cdot dT}$$

> $C_p$ = capacité thermique à *pression constante*.

---

### Relations entre $C_v$, $C_p$ et $\gamma$

**Relation de Mayer :**

$$\boxed{C_p - C_v = nR}$$

> Toujours vraie pour un gaz parfait. Permet de calculer l'une si l'autre est connue. $R = 8{,}314\;\text{J·mol}^{-1}\text{·K}^{-1}$.

**Coefficient adiabatique $\gamma$ (gamma) :**

$$\boxed{\gamma = \frac{C_p}{C_v}}$$

> Rapport des capacités thermiques. **Pour l'air (diatomique) : $\gamma = 1{,}4$** — à retenir par cœur.

---

### Lois de Laplace — Transformation Adiabatique Réversible

Lors d'une transformation **adiabatique réversible** ($Q = 0$ + réversible), les variables $P$, $V$, $T$ sont liées. Ces équations sont **vitales** pour trouver un volume ou une température finale :

**Relation P–V :**

$$\boxed{P \cdot V^\gamma = \text{constante}}$$

**Relation T–V :**

$$\boxed{T \cdot V^{\gamma - 1} = \text{constante}}$$

> Ces deux relations découlent des lois de Joule + 1er principe + $PV = nRT$. C'est le squelette calculatoire de toute adiabatique réversible.

---

## 03 · Modèles de Gaz — Parfait vs Réel

### 📐 Contexte physique

**Le gaz parfait** est un modèle idéal : molécules *ponctuelles sans volume*, *aucune interaction* entre elles. Utile pour les calculs, mais irréaliste.

**Le gaz réel — modèle de Van der Waals *(tombé en 2025)*** : les molécules ont une vraie taille et *interagissent* (forces attractives à longue distance, répulsives à très courte distance).

---

### ⚗️ Équations d'état

| Modèle | Hypothèses | Équation |
|--------|------------|----------|
| **Gaz Parfait** | Molécules ponctuelles, aucune interaction | $PV = nRT$ |
| **Van der Waals** | Volume propre + forces attractives/répulsives | $\left(P + \dfrac{n^2 a}{V^2}\right)(V - nb) = nRT$ |

---

### 🔍 Décryptage des termes — très testé

**↳ Le Covolume : terme $(V - nb)$**

$b$ = volume propre d'une mole de molécules → l'espace réellement disponible est $(V - nb)$.

> Modélise les forces **répulsives** à courte distance : deux molécules ne peuvent pas se "rentrer dedans".

**↳ La Pression Interne : terme $\left(P + n^2a/V^2\right)$**

Les molécules **s'attirent**. Avant d'atteindre la paroi, une molécule est *retenue en arrière*. La **pression réelle $P$ est plus faible** que la pression idéale. Le terme $\frac{n^2 a}{V^2}$ corrige cet écart. Le coefficient $a$ mesure l'intensité des forces **attractives**.

---

## 04 · Machines & Cycles Thermodynamiques

### 📐 Contexte physique

Pour créer un moteur ou un réfrigérateur, on fait subir à un gaz une **suite de transformations** qui reviennent au point de départ : c'est un *cycle*. On représente ces cycles sur un **diagramme P–V** : **l'aire enfermée = travail total échangé**.

---

### ⚙️ Équations fondamentales

**Travail général :**

$$\boxed{\delta W = -P_{\text{ext}}\, dV}$$

> - Détente $(dV > 0)$ → $W < 0$ : le gaz fournit un effort.
> - Compression $(dV < 0)$ → $W > 0$ : l'extérieur comprime le gaz.

---

**Transformation Isotherme — $T = \text{constante}$**

La loi de Joule garantit $\Delta U = 0$ si $T$ est constante.

$$\Delta U = 0 \;\Rightarrow\; W = -Q$$

$$\boxed{W = -nRT\ln\!\left(\frac{V_2}{V_1}\right)}$$

> On substitue $P = nRT/V$ (gaz parfait) avant d'intégrer.

---

**Transformation Adiabatique — système calorifugé**

$$Q = 0 \;\Rightarrow\; \boxed{\Delta U = W}$$

> Compression adiabatique → le gaz **chauffe**. Détente → il **refroidit**. Les lois de Laplace s'appliquent (cf. section 02).

---

### ★ Cycle de Carnot & Rendement Maximal *(tombé en 2022)*

Le **cycle de Carnot** (2 isothermes + 2 adiabatiques) est le cycle idéal parfait. Il définit le **rendement maximal théorique** de tout moteur thermique. Aucun moteur réel ne peut dépasser ce rendement.

**Rendement de Carnot :**

$$\boxed{\eta = 1 - \frac{T_F}{T_C}}$$

| Variable | Signification |
|----------|---------------|
| $T_C$ | Température de la source **chaude** — obligatoirement en **Kelvin** |
| $T_F$ | Température de la source **froide** — obligatoirement en **Kelvin** |

---

### 🚨 Piège absolu — Unités de température

> Les températures dans $\eta = 1 - T_F/T_C$ doivent **OBLIGATOIREMENT être en Kelvin**.
>
> **Conversion :** $T(\text{K}) = T(°\text{C}) + 273{,}15$
>
> Utiliser des °C donne un résultat faux. C'est l'erreur la plus fréquente sur ce concours.

---

## 05 · Rayonnement Thermique — Le Corps Noir

### 📐 Contexte physique

**Tout objet ayant une température émet de la lumière.** La couleur et l'intensité dépendent de $T$. Un **"corps noir"** théorique absorbe *toute* la lumière reçue et réémet un spectre parfaitement défini ne dépendant *que* de sa température (pas de sa forme ni de sa matière).

---

### ☀️ Équations fondamentales

**Formule de Planck — Distribution spectrale**

$$\boxed{\rho(\nu,T) = \frac{8\pi h\nu^3}{c^3}\cdot\frac{1}{e^{h\nu/k_BT}-1}}$$

> Densité d'énergie par unité de fréquence. Unité : **J·m⁻³·Hz⁻¹**
>
> ⚠️ La constante de Planck **$h$** prouve que l'énergie EM est *quantifiée* (valeurs discrètes multiples de $h\nu$) — c'est la porte d'entrée vers la physique quantique.

---

**Loi de Wien — Longueur d'onde dominante**

$$\boxed{\lambda_{\max} \cdot T = \text{constante}} \quad \left(\lambda_{\max} = \frac{A}{T}\right)$$

> - Plus **chaud** → émission vers les *courtes longueurs d'onde* (UV/bleu)
> - Plus **froid** → émission vers les *grandes longueurs d'onde* (infrarouge)

---

### ★ Applications directes au concours

| Température | $\lambda_{\max}$ | Domaine | Interprétation |
|-------------|-----------------|---------|----------------|
| **$T = 300\,K$** (ambiante) | $\approx 10\,\mu m$ | **Infrarouge** | Invisible à l'œil. Principe des caméras thermiques. |
| **$T = 6000\,K$** (Soleil) | $\approx 0{,}5\,\mu m$ | **Jaune-vert visible** | Nos yeux ont évolué pour être sensibles à cette longueur d'onde. |

---

## 06 · Statique des Fluides & Archimède

### A — Fluides Incompressibles (L'eau)

#### 📐 Contexte physique

Plus on descend, plus il y a de fluide qui "pèse" au-dessus → pression augmente. La **poussée d'Archimède** naît de la différence de pression entre la face inférieure d'un objet (plus de pression) et sa face supérieure → force nette vers le *haut*. Si l'objet est moins dense que le fluide → il flotte.

---

#### 🌊 Équations fondamentales

**Hydrostatique — Pression en profondeur :**

$$\boxed{\Delta P = \rho_{\text{fluide}} \cdot g \cdot \Delta z}$$

> La pression augmente **linéairement** avec la profondeur.
> ⚠️ Si l'axe $z$ pointe vers le *haut* : $dP = -\rho g\, dz$.

**Poussée d'Archimède :**

$$\boxed{\vec{\Pi}_A = -\rho_{\text{fluide}} \cdot V_{\text{immergé}} \cdot \vec{g}}$$

> Force = opposé du poids du volume de fluide déplacé. Orientée vers le haut.

---

#### ★ Exercice type — Cylindre de rayon $R$ immergé sur hauteur $h$

1. **Volume immergé :** $V_{\text{immergé}} = \pi R^2 h$
2. **Masse d'eau déplacée :** $m_{\text{eau}} = \rho_{\text{eau}} \cdot \pi R^2 h$
3. **Condition d'équilibre :** $\text{Poids} = \Pi_A$

---

#### 🧊 Piège ultime — Le glaçon *(tombé en 2022)*

> **Situation :** Un glaçon flotte dans un verre d'eau rempli à ras bord. Il fond. Que fait le niveau de l'eau ?
>
> **Réponse : Il reste exactement le même.**
>
> En flottant, le glaçon déplace un volume d'eau *égal à son poids*. En fondant, il donne exactement ce volume en eau liquide. Le volume d'eau liquide issu de la fonte est *exactement égal* au volume immergé du glaçon. Bilan : zéro changement de niveau.

---

### B — Fluides Compressibles (L'atmosphère) ✦ Nouveau

#### 📐 Contexte physique

L'air est *compressible* : sa densité change avec la pression. Sous son propre poids, l'air en bas est plus comprimé (plus dense) qu'en haut. La pression ne diminue donc **pas** linéairement avec l'altitude, mais de façon **exponentielle**.

---

#### Loi de Nivellement Barométrique — Atmosphère Isotherme *(tombé en 2022)*

$$\boxed{P(z) = P(0) \cdot e^{-\dfrac{M \cdot g \cdot z}{R \cdot T}}}$$

| Variable | Signification |
|----------|---------------|
| $P(0)$ | Pression au sol (référence) |
| $M$ | Masse molaire de l'air ≈ **0,029 kg/mol** |
| $g$ | Accélération gravitationnelle ≈ **9,81 m/s²** |
| $R$ | Constante des gaz : **8,314 J·mol⁻¹·K⁻¹** |
| $T$ | Température en **Kelvin** — supposée constante dans ce modèle |

---

## 07 · Transferts Thermiques

### 📐 Contexte physique

**Comment la chaleur voyage-t-elle dans un solide ?** Par **conduction** : les atomes chauds vibrent et transmettent leur agitation à leurs voisins. La chaleur va spontanément des zones *chaudes → froides*. ⚠️ La conduction *ne fonctionne pas dans le vide* : il faut un milieu matériel.

---

### 🌡️ Équations fondamentales

**Loi de Fourier — Flux thermique local :**

$$\boxed{\vec{j}_Q = -\kappa \, \overrightarrow{\text{grad}}\, T}$$

> Le **vecteur densité de flux thermique $\vec{j}_Q$** est proportionnel au gradient de température.

| Terme | Signification |
|-------|---------------|
| **Signe −** | La chaleur *fuit les hautes températures* : flux orienté du chaud vers le froid, en sens **opposé** au gradient |
| **$\kappa$ (kappa)** | Conductivité thermique — unité : **W·m⁻¹·K⁻¹** |

---

**Équation de la chaleur — Évolution temporelle :**

$$\boxed{\frac{\partial T}{\partial t} = \alpha \,\Delta T}$$

> Décrit comment la température évolue dans le temps en tout point du solide.

| Terme | Signification |
|-------|---------------|
| **$\alpha$ (alpha)** | Diffusivité thermique — unité : **m²/s**. Vitesse à laquelle la chaleur se répand. |
| **$\Delta T$ (Laplacien)** | Mesure la "courbure" du champ de T dans l'espace. Non nul = répartition spatiale non uniforme. |

---

*Fiche auto-suffisante — Version Ultime — Bloc 2 · Thermodynamique & Fluides*
