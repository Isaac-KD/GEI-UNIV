# ⚙️ BLOC 5 — Mécanique & Électromagnétisme
> **Fiche auto-suffisante · Version Définitive "Zéro Faille"** · Aucun prérequis nécessaire

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--mécanique--coordonnées--pendules) | Mécanique : Coordonnées & Pendules | |
| [02](#02--référentiels-non-galiléens) | Référentiels Non-Galiléens | Tombé en 2025 |
| [03](#03--mécanique-spatiale--orbites) | Mécanique Spatiale & Orbites | ✦ Hack intégré |
| [04](#04--électrostatique--théorème-de-gauss) | Électrostatique — Théorème de Gauss | Tombé 2023 & 2025 |
| [05](#05--magnétostatique--théorème-dampère) | Magnétostatique — Théorème d'Ampère | ✦ Hack intégré |
| [06](#06--électromagnétisme--maxwell-opph--poynting) | Électromagnétisme — Maxwell, OPPH & Poynting | ✦ Hack intégré |
| [07](#07--électrocinétique--impédances--filtres) | Électrocinétique — Impédances & Filtres | Tombé en 2023 |

---

## 01 · Mécanique : Coordonnées & Pendules

### 📐 Contexte physique

Le concours privilégie les problèmes de **rotation** (pendules, planètes, satellites) qui exigent les coordonnées polaires ou cylindriques. Le piège classique est de mal dériver les vecteurs unitaires mobiles $\vec{u}_r$ et $\vec{u}_\theta$, qui *changent de direction* au cours du temps, contrairement aux vecteurs cartésiens fixes.

---

### 🌀 Coordonnées cylindriques — Équations dures à réécrire

**Vecteur position :**

$$\boxed{\vec{OM} = r\vec{u}_r + z\vec{u}_z}$$

**Vecteur vitesse :**

$$\boxed{\vec{v} = \dot{r}\vec{u}_r + r\dot{\theta}\vec{u}_\theta + \dot{z}\vec{u}_z}$$

> Le terme $r\dot{\theta}$ est la **vitesse tangentielle** — il apparaît car $\vec{u}_r$ tourne avec le point.

**Vecteur accélération — Le grand classique :**

$$\boxed{\vec{a} = \underbrace{(\ddot{r} - r\dot{\theta}^2)}_{\text{composante radiale}}\vec{u}_r + \underbrace{(r\ddot{\theta} + 2\dot{r}\dot{\theta})}_{\text{composante transverse}}\vec{u}_\theta + \ddot{z}\vec{u}_z}$$

| Terme | Signification |
|-------|---------------|
| $-r\dot{\theta}^2$ | Terme **centripète** : accélération orientée vers le centre, due à la rotation. Toujours présent sur une trajectoire courbe. |
| $2\dot{r}\dot{\theta}$ | Terme de **Coriolis** en coordonnées cylindriques. Apparaît dès que le rayon varie ET que le point tourne. |

---

### Pendule Simple *(tombé en 2023)*

Longueur $L$ constante : $\dot{r} = 0$ et $\ddot{r} = 0$. L'accélération se simplifie mais conserve son terme centripète :

$$\vec{a} = -L\dot{\theta}^2\vec{u}_r + L\ddot{\theta}\vec{u}_\theta$$

**Équation du mouvement — PFD projeté sur $\vec{u}_\theta$ :**

$$\boxed{\ddot{\theta} + \frac{g}{L}\sin\theta = 0}$$

> C'est l'équation **exacte** (non linéaire). Pour les petites oscillations ($\sin\theta \approx \theta$), on obtient un mouvement harmonique de pulsation $\omega_0 = \sqrt{g/L}$.

---

## 02 · Référentiels Non-Galiléens

### 📐 Contexte physique

**Tombé en 2025.** Dans un repère en rotation (la Terre, un manège, un carrousel), les lois de Newton ne s'appliquent pas directement car le repère est *accéléré*. Des **forces d'inertie "fantômes"** apparaissent pour l'observateur solidaire du repère tournant. Ces forces n'ont pas de cause physique réelle — elles compensent l'accélération du référentiel lui-même.

---

### 🌍 Équations fondamentales

**Composition des accélérations :**

$$\boxed{\vec{a}_{\text{absolue}} = \vec{a}_{\text{relative}} + \vec{a}_{\text{entraînement}} + \vec{a}_{\text{Coriolis}}}$$

| Variable | Signification |
|----------|---------------|
| $\vec{a}_{\text{absolue}}$ | Accélération vue depuis un référentiel *Galiléen fixe* (les étoiles) |
| $\vec{a}_{\text{relative}}$ | Accélération vue par l'observateur *dans le repère tournant* |
| $\vec{a}_{\text{entraînement}}$ | Accélération due au mouvement du repère (inclut le terme centripète) |
| $\vec{a}_{\text{Coriolis}}$ | Terme de couplage entre la rotation et le mouvement relatif |

**Force de Coriolis :**

$$\boxed{\vec{F}_C = -2m\,\vec{\Omega} \wedge \vec{v}_{\text{relative}}}$$

> $\vec{\Omega}$ = vecteur rotation du repère. $\vec{v}_{\text{relative}}$ = vitesse de l'objet *vue depuis le repère tournant*. La force est perpendiculaire à $\vec{v}_{\text{relative}}$.
>
> C'est la force de Coriolis qui **dévie les vents** à la surface de la Terre et crée les **cyclones** (rotation anti-horaire dans l'hémisphère Nord).

---

### ⚠️ Pièges Vrai / Faux — très testés

> **"Un référentiel en rotation uniforme est Galiléen."** → **FAUX.**
>
> Il possède une accélération centripète $-r\Omega^2 \vec{u}_r$ non nulle. Seule la *translation rectiligne uniforme* préserve le caractère Galiléen.

> **"La force de Coriolis est trop faible pour être observée."** → **FAUX.**
>
> Elle est directement responsable des cyclones, des vents dominants et de la déviation des missiles balistiques.

---

## 03 · Mécanique Spatiale & Orbites
> ✦ **Hack intégré** — élimine 3 réponses sur 5 sans calcul

### 📐 Contexte physique

Modéliser l'orbite d'un **satellite** autour d'un astre de masse $M$. L'orbite circulaire est le cas de base : la force gravitationnelle sert d'accélération centripète.

---

### 🛰️ Formules dures — Orbites circulaires de rayon r

**Vitesse orbitale :**

$$\boxed{v = \sqrt{\frac{GM}{r}}}$$

> S'obtient en égalisant accélération centripète $(v^2/r)$ et champ de gravité $(GM/r^2)$. Plus l'orbite est haute, plus le satellite va *lentement*.

**3ème Loi de Kepler :**

$$\boxed{\frac{T^2}{r^3} = \frac{4\pi^2}{GM}}$$

> Ce rapport est *constant* pour tous les satellites du même astre.

---

### ⚡ Hack — Astuce d'énergie *(élimine 3 réponses sur 5 sans calcul)*

Sur une **orbite circulaire**, les trois énergies sont rigoureusement liées. L'énergie mécanique est *strictement négative* (état lié : le satellite ne peut pas s'échapper) :

$$\boxed{E_m = \frac{1}{2}E_p = -E_c}$$

**Conséquences directes pour les QCM :**
- Si une formule donne $E_m > 0$ → **éliminée immédiatement**.
- $E_c > 0$ toujours → $E_m = -E_c < 0$ → l'énergie mécanique est *toujours négative*.
- Si le satellite monte (rayon augmente) → $E_p$ augmente, $E_c$ diminue (il ralentit), $E_m$ augmente (devient moins négative).

---

### Problème à 2 corps

**Masse réduite :**

$$\boxed{\mu = \frac{m_1\, m_2}{m_1 + m_2}}$$

> Permet de ramener le problème à deux corps à un problème à un seul corps de masse $\mu$. Dans le **référentiel barycentrique**, la quantité de mouvement totale est toujours *nulle*.

---

## 04 · Électrostatique — Théorème de Gauss

### 📐 Contexte physique

Le théorème de Gauss est le **roi des QCM** en électrostatique. Il permet de calculer $\vec{E}$ créé par une distribution de charges *très symétrique* (sphère, cylindre, plan) sans intégrer Coulomb directement. Il suffit de choisir astucieusement une surface fermée exploitant les symétries.

---

### ⚡ Équation fondamentale

$$\boxed{
\displaystyle ∯ \vec{E} \cdot d\vec{S} = \frac{Q_{\text{intérieure}}}{\varepsilon_0}}$$

> Le flux du champ électrique à travers une surface fermée = charge totale *enfermée à l'intérieur* / $\varepsilon_0$. Les charges **extérieures** ne contribuent pas.

---

### Sphère pleine — densité volumique ρ, rayon R *(tombé en 2023 & 2025)*

| Zone | Formule | Interprétation |
|------|---------|----------------|
| **Extérieur** ($r \geq R$) | $E(r) = \dfrac{Q_{\text{totale}}}{4\pi\varepsilon_0 r^2}$ | Agit comme une **charge ponctuelle centrale** |
| **Intérieur** ($r < R$) | $E(r) = \dfrac{\rho\, r}{3\varepsilon_0}$ | **Croissance linéaire** — seule la charge dans la sphère de rayon $r$ compte |

---

### Sphère creuse — densité surfacique σ, rayon R

| Zone | Formule | Interprétation |
|------|---------|----------------|
| **Extérieur** ($r \geq R$) | $E(r) = \dfrac{\sigma R^2}{\varepsilon_0 r^2}$ | Même comportement que la sphère pleine |
| **Intérieur** ($r < R$) | $E(r) = 0$ | **Aucune charge enfermée** → champ nul. Principe de la cage de Faraday. |

---

## 05 · Magnétostatique — Théorème d'Ampère
> ✦ **Hack intégré**

### 📐 Contexte physique

Le théorème d'Ampère est le **jumeau magnétique** du théorème de Gauss. Là où Gauss calcule $\vec{E}$ via un *flux* à travers une **surface** fermée, Ampère calcule $\vec{B}$ via une *circulation* sur un **contour** fermé. Il s'applique aux distributions de courants symétriques : fil infini, solénoïde, bobine toroïdale.

---

### 🧲 Équation fondamentale

$$\boxed{\oint \vec{B} \cdot d\vec{l} = \mu_0\, I_{\text{enlacé}}}$$

> La circulation du champ magnétique sur un contour fermé = $\mu_0$ × **somme algébrique des courants** traversant la surface délimitée par ce contour. Les courants *extérieurs* ne contribuent pas.

---

### Applications directes — à connaître

**Fil infini parcouru par I :**

$$\boxed{B(r) = \frac{\mu_0 I}{2\pi r}}$$

> Champ en $1/r$. Contour d'Ampère = cercle de rayon $r$ coaxial au fil.

**Solénoïde infini (n spires/m) :**

$$\boxed{B = \mu_0 n I}$$

> Champ **uniforme** à l'intérieur, **nul** à l'extérieur.

> **Constante :** $\mu_0 = 4\pi \times 10^{-7}\;\text{T·m·A}^{-1}$

---

## 06 · Électromagnétisme — Maxwell, OPPH & Poynting
> ✦ **Hack intégré**

### 📐 Contexte physique

Les **équations de Maxwell** unifient l'électricité, le magnétisme et l'optique. Elles prédisent l'existence des ondes électromagnétiques (lumière, radio, WiFi…). Dans le vide, elles se propagent à $c = 3 \times 10^8\;\text{m/s}$.

---

### 📡 Les 4 Équations Locales de Maxwell

**① Maxwell-Gauss**

$$\boxed{\text{div}\,\vec{E} = \frac{\rho}{\varepsilon_0}}$$

> Les charges électriques sont les *sources* du champ $\vec{E}$. Forme locale du théorème de Gauss.

**② Maxwell-Thomson**

$$\boxed{\text{div}\,\vec{B} = 0}$$

> **Il n'existe pas de monopôle magnétique.** Les lignes de champ $\vec{B}$ se referment toujours sur elles-mêmes.

**③ Maxwell-Faraday (Induction)**

$$\boxed{\text{rot}\,\vec{E} = -\frac{\partial \vec{B}}{\partial t}}$$

> Un champ magnétique *variable dans le temps* crée un champ électrique. Principe des alternateurs et des transformateurs.

**④ Maxwell-Ampère**

$$\boxed{\text{rot}\,\vec{B} = \mu_0 \vec{j} + \mu_0\varepsilon_0 \frac{\partial \vec{E}}{\partial t}}$$

> Un courant $\vec{j}$ *ou* un champ électrique variable crée un champ magnétique. Le terme $\mu_0\varepsilon_0 \partial\vec{E}/\partial t$ est le "courant de déplacement" de Maxwell — il permet la propagation des ondes EM dans le vide.

---

### Onde Plane Progressive Harmonique (OPPH)

**Relation de structure :**

$$\boxed{\vec{B} = \frac{\vec{k} \wedge \vec{E}}{\omega}}$$

> $\vec{E}$, $\vec{B}$ et le vecteur d'onde $\vec{k}$ (direction de propagation) forment un **trièdre direct orthogonal**. Relation de dispersion dans le vide : $k = \omega/c$.

---

### ⚡ Hack — Vecteur de Poynting

$$\boxed{\vec{\Pi} = \frac{\vec{E} \wedge \vec{B}}{\mu_0}}$$

Le vecteur de Poynting $\vec{\Pi}$ indique la **direction de propagation de l'énergie** électromagnétique. Sa norme donne la **puissance surfacique transportée** (en W/m²).

**À retenir pour les QCM :**
- $\vec{\Pi}$ est toujours **perpendiculaire** à $\vec{E}$ et à $\vec{B}$.
- $\vec{\Pi}$ est dans la même direction que $\vec{k}$.
- $\|\vec{\Pi}\|$ en W/m² = intensité lumineuse pour une onde EM.

---

## 07 · Électrocinétique — Impédances & Filtres

### 📐 Contexte physique

En régime sinusoïdal forcé, on remplace les grandeurs temporelles par leurs **représentations complexes**. Chaque composant a une impédance complexe $\underline{Z}$ qui se comporte comme une résistance généralisée. Le "hack des asymptotes" permet d'identifier la nature d'un filtre *sans calcul*.

---

### 🔌 Impédances des composants

| Composant | Impédance | Comportement |
|-----------|-----------|--------------|
| Résistance $R$ | $\underline{Z}_R = R$ | Indépendante de la fréquence |
| Bobine $L$ | $\underline{Z}_L = jL\omega$ | **Augmente** avec $\omega$ |
| Condensateur $C$ | $\underline{Z}_C = \dfrac{1}{jC\omega}$ | **Diminue** avec $\omega$ |

---

### ⚡ Hack des asymptotes — Identifier un filtre sans calcul *(tombé en 2023)*

Pour deviner la nature d'un filtre, remplace chaque composant par son comportement aux fréquences extrêmes :

| Composant | $\omega \to 0$ (basse fréquence) | $\omega \to \infty$ (haute fréquence) |
|-----------|----------------------------------|---------------------------------------|
| **Bobine L** | $\underline{Z}_L \to 0$ → **Fil** | $\underline{Z}_L \to \infty$ → **Interrupteur ouvert** |
| **Condensateur C** | $\underline{Z}_C \to \infty$ → **Interrupteur ouvert** | $\underline{Z}_C \to 0$ → **Fil** |

**Méthode :** Dessine le circuit aux deux extrêmes. Si le signal passe à basse fréquence mais pas à haute → **passe-bas**. L'inverse → **passe-haut**.

---

### ★ Récapitulatif — Ce que le concours adore tester

- Un condensateur **bloque le courant continu** ($\omega = 0$ → ouvert) mais le laisse passer en haute fréquence.
- Une bobine **laisse passer le courant continu** ($\omega = 0$ → fil) mais bloque les hautes fréquences.
- Fréquence de coupure d'un filtre RC passe-bas : $f_c = \dfrac{1}{2\pi RC}$

---

*Fiche auto-suffisante — Version Définitive "Zéro Faille" — Bloc 5 · Mécanique & Électromagnétisme*