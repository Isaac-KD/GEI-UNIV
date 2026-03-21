# 🔬 BLOC 2 — Thermodynamique & Fluides
> **Fiche auto-suffisante** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet |
|---|-------|
| [01](#01--thermodynamique--entropie) | Thermodynamique & Entropie |
| [02](#02--transferts-thermiques) | Transferts Thermiques |
| [03](#03--modèles-de-gaz--parfait-vs-réel) | Modèles de Gaz — Parfait vs Réel |
| [04](#04--machines--cycles-thermodynamiques) | Machines & Cycles Thermodynamiques |
| [05](#05--rayonnement-thermique--le-corps-noir) | Rayonnement Thermique — Le Corps Noir |
| [06](#06--statique-des-fluides--archimède) | Statique des Fluides & Archimède |

---

## 01 · Thermodynamique & Entropie

### 📐 Contexte physique

La thermodynamique étudie les **échanges d'énergie** dans un système physique. Elle repose sur deux grands principes :

- Le **1er principe** dit que l'énergie se *conserve* : elle change juste de forme (travail ou chaleur), elle ne se crée ni ne se détruit.
- Le **2nd principe** dit que les phénomènes physiques ont un *sens irréversible* : la chaleur va spontanément du chaud vers le froid, jamais l'inverse. Ce principe introduit l'**Entropie $S$**, une grandeur qui mesure le "désordre" du système et indique le sens naturel de son évolution.

---

### ⚡ Équations fondamentales

**1er Principe — Bilan d'énergie**

$$\boxed{\Delta U = W + Q}$$

> La **variation d'énergie interne $U$** d'un système est la somme du **Travail $W$** et de la **Chaleur $Q$** reçus par ce système.

---

**2nd Principe — Bilan d'entropie**

$$\boxed{\Delta S = S_{\text{échange}} + S_{\text{création}}}$$

L'entropie totale varie en fonction de deux contributions distinctes :

**↳ Entropie échangée avec l'extérieur**

$$S_{\text{échange}} = \int \frac{\delta Q}{T_{\text{ext}}}$$

> Elle a le **même signe que la chaleur $Q$**. Si le système refroidit, il perd de la chaleur, donc $S_{\text{échange}} < 0$. C'est l'entropie qui "rentre" ou "sort" via les échanges thermiques avec l'environnement extérieur de température $T_{\text{ext}}$.

**↳ Entropie créée à l'intérieur du système**

$$S_{\text{création}} \geq 0$$

> Elle est **nulle** pour une transformation idéale *(réversible)* et **strictement positive** pour toute transformation du monde réel *(irréversible)*. Elle ne peut jamais être négative : c'est la traduction mathématique du fait que le désordre interne ne peut que croître ou rester stable.

---

### 🔑 Points clés à retenir

| Propriété | Détail |
|-----------|--------|
| **Unité de $S$** | $S_{\text{échange}} = Q / T$ → Énergie / Température → **J/K** |
| **Extensivité** | $S$ est *extensive* : doubler le système double l'entropie. À comparer avec la **température** qui est *intensive* (doubler le système ne change pas sa température) |

---

### ⚠️ Piège classique du concours — Le Système Isolé

Un **système isolé** n'échange *rien* avec l'extérieur : ni travail, ni chaleur.

Donc $Q = 0$ et $W = 0$, par conséquent :

$$S_{\text{échange}} = \int \frac{0}{T_{\text{ext}}} = 0$$

Le bilan d'entropie se réduit alors à :

$$\Delta S = S_{\text{création}} \geq 0$$

**➜ L'entropie d'un système isolé ne peut qu'augmenter — elle n'est jamais nulle !**

Une erreur fréquente est de croire que $\Delta S = 0$ car "il n'y a pas d'échange". C'est faux : l'entropie de *création* interne est toujours non nulle dans le monde réel.

---

## 02 · Transferts Thermiques

### 📐 Contexte physique

**Comment la chaleur voyage-t-elle dans un solide ?** Par **conduction** : les atomes chauds vibrent plus intensément et transmettent cette agitation à leurs voisins, qui la transmettent aux leurs, et ainsi de suite.

La chaleur va *spontanément* des zones chaudes vers les zones froides. Ce sens de propagation est une conséquence directe du 2nd principe de la thermodynamique.

---

### 🌡️ Équations fondamentales

**Loi de Fourier — Flux thermique local**

$$\boxed{\vec{j}_Q = -\kappa \, \overrightarrow{\text{grad}}\, T}$$

> Le **vecteur densité de flux thermique $\vec{j}_{Q}$** est proportionnel au gradient de température. Il indique la direction et l'intensité de la propagation de la chaleur en un point.

| Terme | Signification |
|-------|---------------|
| **Signe −** | Traduit que la chaleur *fuit les hautes températures* : le flux va de chaud vers froid, dans le sens **opposé** au gradient |
| **$\kappa$** | Conductivité thermique du matériau — unité : **W·m⁻¹·K⁻¹**. Plus $\kappa$ est grand, plus le matériau conduit bien la chaleur (ex : les métaux) |

---

**Équation de la chaleur — Évolution temporelle**

$$\boxed{\frac{\partial T}{\partial t} = \alpha \, \Delta T}$$

> Décrit comment la **température évolue dans le temps** en tout point d'un solide. L'évolution temporelle dépend de la répartition spatiale de $T$, capturée par le Laplacien $\Delta$.

| Terme | Signification |
|-------|---------------|
| **$\alpha$ (alpha)** | Diffusivité thermique — unité : **m²/s**. Mesure la vitesse à laquelle la chaleur se répand dans le matériau |
| **$\Delta T$ (Laplacien)** | Opérateur mathématique qui mesure la "courbure" du champ de température dans l'espace. Un Laplacien non nul signifie que la température n'est pas uniformément répartie |

---

## 03 · Modèles de Gaz — Parfait vs Réel

### 📐 Contexte physique

**Le gaz parfait** est un modèle mathématique idéal : on imagine que les molécules sont des *points sans volume* et qu'elles *s'ignorent totalement* (aucune force entre elles). C'est une simplification utile pour les calculs.

**Le gaz réel** (modèle de Van der Waals) corrige ces deux hypothèses irréalistes : les molécules ont une vraie taille (elles prennent de la place dans le récipient) et elles *interagissent* entre elles (forces attractives à longue distance, répulsives à très courte distance).

---

### ⚗️ Équations d'état

| Modèle | Hypothèses physiques | Équation d'état |
|--------|---------------------|-----------------|
| **Gaz Parfait** | Molécules ponctuelles (volume = 0), aucune interaction entre elles | $PV = nRT$ |
| **Van der Waals (gaz réel)** | Molécules avec volume propre + forces attractives et répulsives | $\left(P + \dfrac{n^2 a}{V^2}\right)(V - nb) = nRT$ |

---

### 🔍 Décryptage des termes de Van der Waals — très testé au concours

**↳ Le Covolume : terme $(V - nb)$**

$b$ est le volume propre d'une mole de molécules. Donc $nb$ est le volume total occupé par les molécules elles-mêmes. L'espace vraiment disponible pour que les molécules bougent n'est pas le volume total $V$ du récipient, mais $(V - nb)$.

> Physiquement, cela modélise les forces **répulsives** à très courte distance : deux molécules ne peuvent pas se "rentrer dedans". Elles se repoussent violemment si on essaie de les comprimer trop fort.

**↳ La Pression Interne : terme $\left(P + \dfrac{n^2 a}{V^2}\right)$**

Les molécules **s'attirent** entre elles (forces de Van der Waals). Quand une molécule se dirige vers la paroi pour la frapper (créant ainsi la pression), elle est *retenue en arrière* par l'attraction des autres molécules. Elle arrive donc avec moins d'élan.

> Conséquence : la **pression réelle $P$ est plus faible** que la pression qu'aurait un gaz parfait dans les mêmes conditions. On ajoute le terme correctif $\frac{n^2 a}{V^2}$ pour retrouver la pression équivalente au gaz parfait. Le coefficient $a$ modélise l'intensité de ces forces **attractives**.

---

## 04 · Machines & Cycles Thermodynamiques

### 📐 Contexte physique

Pour créer un moteur ou un réfrigérateur, on fait subir à un gaz une **suite de transformations** qui reviennent exactement au point de départ : c'est un *cycle*. Après un cycle complet, le gaz a l'air de n'avoir rien changé, mais entre-temps il a échangé du travail et de la chaleur avec l'extérieur.

On représente ces cycles sur un **diagramme Pression–Volume $(P, V)$** : l'axe horizontal est le volume du gaz, l'axe vertical est sa pression. **L'aire enfermée par le cycle** sur ce diagramme est directement égale au travail total échangé.

---

### ⚙️ Équations fondamentales & transformations

**Calcul général du travail**

$$\boxed{\delta W = -P_{\text{ext}}\, dV}$$

> - Quand le gaz **se détend** ($dV > 0$, il gonfle) → $W < 0$ : le gaz *fournit* un effort pour repousser l'extérieur, il "se fatigue".
> - Quand le gaz est **comprimé** ($dV < 0$) → $W > 0$ : l'extérieur fournit un travail sur le gaz.

---

**Transformation Isotherme — $T = \text{constante}$**

La **1ère loi de Joule** dit que l'énergie interne d'un gaz parfait ne dépend *que* de la température. Si $T$ est constante, alors $\Delta U = 0$.

$$\Delta U = 0 \;\Rightarrow\; \boxed{W = -Q}$$

> Le travail fourni est exactement compensé par la chaleur absorbée (ou inversement).

Le calcul explicite du travail (en utilisant $P = nRT/V$ depuis $PV = nRT$) :

$$W = -\int_{V_1}^{V_2} \frac{nRT}{V}\,dV = \boxed{-nRT\ln\!\left(\frac{V_2}{V_1}\right)}$$

---

**Transformation Adiabatique — système calorifugé**

Le système est **parfaitement isolé thermiquement** : aucune chaleur ne rentre ni ne sort.

$$Q = 0 \;\Rightarrow\; \boxed{\Delta U = W}$$

> Toute la variation d'énergie interne vient uniquement du travail. Si on comprime le gaz adiabatiquement, il **chauffe** ; si on le détend, il **refroidit**.

---

### ★ Le Cycle de Carnot — Le cycle idéal parfait

> C'est le cycle thermodynamique théoriquement le plus efficace possible.

Il est composé exactement de :
- **2 transformations isothermes** (à température haute $T_H$, puis à température basse $T_C$)
- **2 transformations adiabatiques** (transitions entre les deux températures)

Le cycle de Carnot définit le **rendement maximal atteignable** par tout moteur thermique fonctionnant entre une source chaude $T_H$ et une source froide $T_C$. Aucun moteur réel ne peut dépasser ce rendement.

---

## 05 · Rayonnement Thermique — Le Corps Noir

### 📐 Contexte physique

**Tout objet ayant une température émet de la lumière.** Un fer chauffé à blanc, le Soleil, votre corps — tout rayonne. La couleur et l'intensité de ce rayonnement dépendent de la température de l'objet.

Un **"corps noir"** est un objet théorique idéal qui *absorbe absolument toute* la lumière qu'il reçoit (rien n'est réfléchi). En échange, il réémet un spectre de rayonnement *parfaitement défini*, qui ne dépend *que de sa température* (pas de sa forme, couleur, matière…). C'est le modèle de référence en physique du rayonnement.

---

### ☀️ Équations fondamentales

**Formule de Planck — Distribution spectrale d'énergie**

$$\boxed{\rho(\nu,T) = \frac{8\pi h\nu^3}{c^3}\cdot\frac{1}{e^{h\nu/k_BT}-1}}$$

> Donne la **densité d'énergie par unité de fréquence** rayonnée par le corps noir à la fréquence $\nu$ et la température $T$.
> Unité : **J·m⁻³·Hz⁻¹**

> ⚠️ La présence de la **constante de Planck $h$** dans cette formule est fondamentale : elle prouve que l'énergie électromagnétique est *quantifiée* (elle ne peut prendre que des valeurs discrètes multiples de $h\nu$), et non continue. C'est l'une des portes d'entrée vers la physique quantique.

---

**Loi de Wien — Longueur d'onde dominante**

$$\boxed{\lambda_{\max} \cdot T = \text{constante}} \quad \left(\text{ou } \lambda_{\max} = \frac{A}{T}\right)$$

> La **longueur d'onde de l'émission maximale** est inversement proportionnelle à la température.
> - Plus un objet est **chaud** → émission vers les *courtes longueurs d'onde* (bleu/UV)
> - Plus il est **froid** → émission vers les *grandes longueurs d'onde* (infrarouge)

---

### ★ Applications directes au concours

| Température | Résultat | Interprétation |
|-------------|----------|----------------|
| **$T = 300\,K$** (ambiante, ~27°C) | $\lambda_{\max} \approx 10\,\mu m$ | Plein **infrarouge** — invisible à l'œil nu. C'est pourquoi les caméras thermiques "voient" les humains dans le noir. |
| **$T = 6000\,K$** (surface du Soleil) | $\lambda_{\max} \approx 0{,}5\,\mu m$ | **Jaune-vert visible** — Ce n'est pas un hasard : nos yeux ont évolué pour être maximalement sensibles à la longueur d'onde que le Soleil émet le plus. |

---

## 06 · Statique des Fluides & Archimède

### 📐 Contexte physique

**Pourquoi la pression augmente-t-elle en profondeur ?** Dans un fluide au repos soumis à la gravité, plus on descend, plus il y a de fluide au-dessus de soi qui "pèse". Ce poids du fluide supérieur augmente la pression en chaque point.

**D'où vient la poussée d'Archimède ?** Quand un objet est immergé, la pression sur sa face inférieure (plus profonde, donc plus grande) est plus élevée que sur sa face supérieure. Cette différence de pression crée une force nette verticale orientée vers le *haut* : c'est la **poussée d'Archimède**.

---

### 🌊 Équations fondamentales

**Principe fondamental de l'hydrostatique**

$$\boxed{\Delta P = \rho_{\text{fluide}} \cdot g \cdot \Delta z}$$

> La pression $P$ augmente **linéairement avec la profondeur** $z$.

> ⚠️ **Convention de signe :** si l'axe $z$ pointe vers le *haut* (convention habituelle), alors $dP = -\rho g\, dz$. La pression *diminue* quand on monte.

---

**Poussée d'Archimède**

$$\boxed{\vec{\Pi}_A = -\rho_{\text{fluide}} \cdot V_{\text{immergé}} \cdot \vec{g}}$$

> La force de poussée est égale à l'**opposé du poids du volume de fluide que l'objet a déplacé**. Le signe "−" devant indique que cette force est dirigée vers le haut (opposée à $\vec{g}$ qui pointe vers le bas).

> En d'autres termes : un objet reçoit vers le haut exactement le poids du fluide qu'il a "chassé" de sa place. Si l'objet est *moins dense* que le fluide, ce poids de fluide dépasse son propre poids → **il flotte**.

---

### ★ Exercice type du concours — Cylindre immergé

Soit un cylindre de rayon $R$, plongé d'une profondeur $h$ dans l'eau (seule la partie basse de hauteur $h$ est immergée) :

**1. Volume immergé :**
$$V_{\text{immergé}} = \text{Surface de base} \times h = \pi R^2 h$$

**2. Masse d'eau déplacée :**
$$m_{\text{eau}} = \rho_{\text{eau}} \cdot \pi R^2 h$$

**3. Condition d'équilibre :**

À l'équilibre (objet flottant sans s'enfoncer ni remonter), le poids de l'objet est exactement compensé par la poussée d'Archimède :

$$\text{Poids} = \Pi_A$$

---

*Fiche réalisée pour le concours GEI-UNIV · Bloc 2 · Thermodynamique & Fluides*