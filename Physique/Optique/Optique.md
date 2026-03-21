# 🌈 BLOC 4 — Optique Ondulatoire & Géométrique
> **Fiche auto-suffisante · Version Zéro Faille** · Aucun prérequis nécessaire · Tout le contexte est inclus

---

## Sommaire

| # | Sujet | Statut |
|---|-------|--------|
| [01](#01--optique-géométrique--dioptres-fibres--lentilles) | Optique Géométrique — Dioptres, Fibres & Lentilles | Tombé en 2021 & 2025 |
| [02](#02--théorie-générale-des-interférences) | Théorie Générale des Interférences | |
| [03](#03--les-fentes-dyoung) | Les Fentes d'Young | |
| [04](#04--linterféromètre-de-michelson--lumière-blanche) | L'Interféromètre de Michelson & Lumière Blanche | |
| [05](#05--diffraction--réseaux) | Diffraction & Réseaux | |

---

## 01 · Optique Géométrique — Dioptres, Fibres & Lentilles

### 📐 Contexte physique

L'optique géométrique modélise la lumière comme des **rayons rectilignes**. Elle est valide lorsque les dimensions des obstacles et ouvertures sont très grandes devant la longueur d'onde. Dès que ce n'est plus le cas, la diffraction apparaît.

Les **conditions de Gauss** sont la condition pour que les lentilles forment des images nettes. En dehors de ces conditions, l'image est floue : c'est l'aberration sphérique.

---

### 🔭 Lentilles minces *(tombé en 2021 & 2025)*

**Conditions de Gauss :**

Pour avoir un **stigmatisme approché** (image nette), les rayons doivent être *paraxiaux* : proches de l'axe optique ET peu inclinés par rapport à cet axe. En dehors de ces conditions, une lentille donne des images floues (aberrations).

**Relation de conjugaison de Descartes :**

$$\boxed{\frac{1}{\overline{OA'}} - \frac{1}{\overline{OA}} = \frac{1}{f'}}$$

| Variable | Signification |
|----------|---------------|
| $\overline{OA}$ | Distance algébrique O → objet A. *Négative* si l'objet est à gauche. |
| $\overline{OA'}$ | Distance algébrique O → image A'. *Positive* si l'image est à droite (réelle). |
| $f'$ | Distance focale image. Convergente : $f' > 0$. Divergente : $f' < 0$. |

**Grandissement transversal $\gamma$ :**

$$\boxed{\gamma = \frac{\overline{A'B'}}{\overline{AB}} = \frac{\overline{OA'}}{\overline{OA}}}$$

| Signe/Valeur | Interprétation |
|-------------|----------------|
| $\gamma > 0$ | Image **droite** (même sens que l'objet) |
| $\gamma < 0$ | Image **renversée** |
| $|\gamma| > 1$ | Image **agrandie** |
| $|\gamma| < 1$ | Image **réduite** |

---

### Fibre Optique — Réflexion Totale Interne

Une fibre optique guide la lumière par **réflexion totale interne** : la lumière est piégée dans le cœur car elle rebondit à chaque interface cœur/gaine sans jamais en sortir. Deux conditions doivent être réunies.

**Loi de Snell-Descartes :**

$$\boxed{n_1 \sin(i_1) = n_2 \sin(i_2)}$$

**Condition 1 — Indice :**

$$\boxed{n_{\text{cœur}} > n_{\text{gaine}}}$$

> Le cœur doit être **plus réfringent** que la gaine. C'est la condition nécessaire pour que la réflexion totale soit possible.

**Condition 2 — Angle limite :**

$$\boxed{\sin(i_{\text{lim}}) = \frac{n_{\text{gaine}}}{n_{\text{cœur}}}}$$

> L'angle d'incidence doit être **supérieur** à $i_{\text{lim}}$ pour que la lumière soit totalement réfléchie.

**Ouverture Numérique (ON) :**

$$\boxed{\text{ON} = \sin(\theta_{\max}) = \sqrt{n_{\text{cœur}}^2 - n_{\text{gaine}}^2}}$$

> Caractérise le **cône d'acceptance** de la fibre : angle maximal sous lequel la lumière peut entrer et être guidée.

---

## 02 · Théorie Générale des Interférences

### 📐 Contexte physique

Deux ondes lumineuses qui se superposent peuvent **interférer** : s'additionner (constructives → lumière) ou se soustraire (destructives → obscurité). Ce phénomène prouve la nature ondulatoire de la lumière.

Pour observer des interférences stables, les deux sources doivent être **cohérentes** : même fréquence et différence de phase constante dans le temps.

---

### 〰️ Formules dures

**Formule de Fresnel — Intensité résultante :**

$$\boxed{I = I_1 + I_2 + 2\sqrt{I_1 I_2}\cos(\Delta\phi)}$$

> Le troisième terme est le terme d'interférence. Il peut être positif (renforcement) ou négatif (affaiblissement). L'énergie est *redistribuée* dans l'espace, pas perdue.

**Cas particulier** — sources identiques ($I_1 = I_2 = I_0$) :

$$I = 2I_0(1 + \cos(\Delta\phi))$$

> Maximum : $I = 4I_0$. Minimum : $I = 0$.

---

**Lien vital — Différence de marche / Déphasage :**

$$\boxed{\Delta\phi = \frac{2\pi\,\delta}{\lambda}}$$

| Variable | Signification |
|----------|---------------|
| $\delta$ | Différence de marche (en m) : différence de longueur de chemin optique. |
| $\Delta\phi$ | Déphasage (en rad) : conséquence de la différence de marche. |
| $\lambda$ | Longueur d'onde *dans le milieu* ($\lambda_n = \lambda_0/n$ dans un milieu d'indice $n$). |

---

**Conditions d'interférence :**

| Type | Condition | Résultat |
|------|-----------|----------|
| **Constructives** | $\delta = p\lambda$ ($p$ entier) | Lumière maximale — ondes en phase |
| **Destructives** | $\delta = \left(p + \tfrac{1}{2}\right)\lambda$ | Obscurité totale — opposition de phase |

---

## 03 · Les Fentes d'Young

### 📐 Contexte physique

Le dispositif de Young est l'expérience fondatrice de l'optique ondulatoire. Deux fentes distantes de $a$ éclairées par une source cohérente produisent des **franges d'interférence** alternativement brillantes et sombres sur un écran à distance $D$.

---

### 🟰 Formules dures

**Différence de marche géométrique :**

$$\boxed{\delta = \frac{a\,x}{D}}$$

| Variable | Signification |
|----------|---------------|
| $a$ | Distance entre les deux fentes |
| $x$ | Coordonnée du point M sur l'écran (depuis le centre) |
| $D$ | Distance fentes–écran. Doit être $\gg a$ (approximation paraxiale). |

**Interfrange $i$ — distance entre deux franges brillantes consécutives :**

$$\boxed{i = \frac{\lambda\,D}{a}}$$

> **Plus les fentes sont proches** ($a$ petit), **plus les franges sont espacées** ($i$ grand) — et inversement.

---

### ⚡ Hack — L'expérience dans l'eau

Si l'on plonge le dispositif dans un milieu d'indice $n$, la longueur d'onde effective est divisée par $n$ :

$$\lambda_{\text{milieu}} = \frac{\lambda_0}{n} \;\Rightarrow\; i_{\text{milieu}} = \frac{i_0}{n}$$

**→ Les franges se resserrent !** L'interfrange diminue d'un facteur $n$.

---

### ★ Effet de chaque paramètre sur les franges

| Paramètre | Variation | Effet sur les franges |
|-----------|-----------|----------------------|
| $\lambda$ | ↑ | Plus **écartées** (rouge > violet) |
| $D$ | ↑ | Plus **écartées** |
| $a$ | ↑ | Plus **resserrées** |
| $n$ (indice du milieu) | ↑ | Plus **resserrées** |

---

## 04 · L'Interféromètre de Michelson & Lumière Blanche

### 📐 Contexte physique

Le Michelson est un interféromètre à deux bras : une lame séparatrice divise un faisceau en deux, chaque bras le réfléchit sur un miroir, puis les deux faisceaux se recombinent pour interférer. La différence de marche $\delta$ dépend de la **configuration des miroirs**.

---

### 🪞 Les deux configurations *(hack)*

| Configuration | Différence de marche | Figures obtenues | Localisation |
|---------------|---------------------|-----------------|--------------|
| **Lame d'air** (miroirs parallèles) | $\delta = 2e\cos(i)$ | **Anneaux** concentriques | À l'**infini** (foyer d'une lentille) |
| **Coin d'air** (miroirs inclinés d'angle $\alpha$) | $\delta = 2\alpha x$ | **Franges rectilignes** | Sur les **miroirs** |

> Lame d'air : $e$ = épaisseur de la lame d'air, $i$ = angle d'incidence.  
> Coin d'air : $x$ = distance au sommet du coin. Interfrange : $i = \lambda / 2\alpha$.

---

### ⚠️ Le Piège de la Lumière Blanche — très testé

La lumière blanche est une superposition de toutes les longueurs d'onde du visible. Les interférences se produisent indépendamment pour chaque $\lambda$, mais les franges ne coïncident pas aux mêmes endroits :

> **Au contact optique exact ($\delta = 0$) :**
> Toutes les $\lambda$ interfèrent constructivement *simultanément*. On observe une frange centrale **blanche brillante** — le "blanc d'ordre zéro". C'est la *seule* frange vraiment blanche.

> **Autour du centre :**
> Chaque couleur a ses propres franges décalées → les couleurs se mélangent de façon irrégulière → on observe des **irisations** (arc-en-ciel).

> **À grande différence de marche ($\delta$ élevé) :**
> Les franges de toutes les couleurs se brouillent complètement, sauf celles dont $\lambda$ est tel que $\delta = p\lambda$.
> Au spectroscope : on observe un **spectre cannelé** — arc-en-ciel continu barré de bandes noires aux longueurs d'onde destructives.

---

## 05 · Diffraction & Réseaux

### 📐 Contexte physique

La **diffraction** est l'étalement d'une onde lorsqu'elle passe par une ouverture ou contourne un obstacle dont la taille est comparable à la longueur d'onde. C'est le régime où l'optique géométrique ne fonctionne plus.

**Règle intuitive :** Plus une ouverture est *petite*, plus la lumière s'y *étale*. Un laser avec une petite ouverture diverge fortement. Une grande ouverture donne une tache quasi-ponctuelle.

---

### 🌈 Diffraction par une fente simple de largeur $a$

**Ouverture angulaire de la tache centrale :**

$$\boxed{\theta = \frac{\lambda}{a}}$$

> Demi-angle de la tache centrale. Les premiers minima se trouvent à cet angle de part et d'autre du centre.

**Taille de la tache centrale sur l'écran (distance $D$) :**

$$\boxed{L = \frac{2\lambda D}{a}}$$

> La tache centrale est **deux fois plus large** que les taches secondaires. Plus la fente est petite, plus la tache s'étale — c'est contre-intuitif mais fondamental.

---

### Profil d'intensité — Sinus Cardinal au carré

$$\boxed{I(\theta) = I_0 \cdot \text{sinc}^2\!\left(\frac{\pi a \sin\theta}{\lambda}\right)}$$

> Avec $\text{sinc}(u) = \sin(u)/u$. Les *zéros* d'intensité se trouvent aux angles $\sin\theta = k\lambda/a$ pour $k$ entier non nul.

---

### ⚡ Hack Vrai/Faux — Largeur des taches

> La tache centrale de diffraction est **strictement deux fois plus large** que les taches secondaires.
>
> Tache centrale : de $-\lambda/a$ à $+\lambda/a$ → largeur angulaire $2\lambda/a$.  
> Taches secondaires : largeur angulaire $\lambda/a$ chacune.  
> Ratio = **2**.

---

### Réseaux de diffraction

Un réseau est un ensemble périodique de fentes de pas $a$. Il produit des **maxima principaux très intenses et étroits** à des angles définis.

**Formule des maxima principaux :**

$$\boxed{\sin(\theta_k) - \sin(\theta_0) = k\frac{\lambda}{a}}$$

| Variable | Signification |
|----------|---------------|
| $a$ | Pas du réseau (distance entre deux traits consécutifs) |
| $k$ | Ordre de diffraction (entier : 0, ±1, ±2…). Ordre 0 = non-dévié. |
| $\theta_0$ | Angle d'incidence du faisceau incident |
| $\theta_k$ | Angle du maximum d'ordre $k$ à la longueur d'onde $\lambda$ |

---

### ★ Application — Dispersion des couleurs

Chaque longueur d'onde $\lambda$ donne un maximum d'ordre $k$ à un angle différent. Le réseau **sépare les couleurs** de la lumière blanche : le rouge (grande $\lambda$) est dévié plus que le violet (petite $\lambda$) pour un même ordre $k > 0$.

**Application directe :** un réseau de diffraction est au cœur des **spectromètres** — instruments qui analysent la composition spectrale de la lumière (étoiles, matériaux, atmosphères).

---

*Fiche auto-suffisante — Bloc 4 · Optique Ondulatoire & Géométrique*