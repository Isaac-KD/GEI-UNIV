# BLOC 4 : Optique Ondulatoire et Géométrique (Version Intégrale "Zéro Faille")

## 1. Optique Géométrique : Dioptres, Fibres et Lentilles

**Les Lentilles Minces et les Conditions de Gauss (Tombé en 2021 et 2025) :**
* **Conditions de Gauss :** Pour avoir un stigmatisme approché (image nette), les rayons doivent être **paraxiaux** (proches de l'axe et peu inclinés).
* **Relation de conjugaison (Descartes) :** $\frac{1}{\overline{OA'}} - \frac{1}{\overline{OA}} = \frac{1}{f'}$
* **Grandissement ($\gamma$) :** $\gamma = \frac{\overline{A'B'}}{\overline{AB}} = \frac{\overline{OA'}}{\overline{OA}}$. *(Si $\gamma < 0$, l'image est renversée).*

**La Fibre Optique (Réflexion Totale Interne) :**

* **Lois de Snell-Descartes :** $n_1 \sin(i_1) = n_2 \sin(i_2)$
* **Condition n°1 :** Le cœur doit être **plus réfringent** que la gaine : **$n_{coeur} > n_{gaine}$**.
* **Condition n°2 :** L'angle d'incidence doit dépasser l'angle limite : **$\sin(i_{lim}) = \frac{n_{gaine}}{n_{coeur}}$**.
* **Ouverture Numérique (ON) :** $\text{ON} = \sin(\theta_{max}) = \sqrt{n_{coeur}^2 - n_{gaine}^2}$.

## 2. Théorie Générale des Interférences
**Les Formules "Dures" :**
* **Formule de Fresnel (Intensité) :** $I = I_1 + I_2 + 2\sqrt{I_1 I_2}\cos(\Delta\phi)$. 
  *(Si $I_1 = I_2 = I_0$, on a $I = 2I_0(1 + \cos(\Delta\phi))$).*
* **Le lien vital Différence de marche ($\delta$) / Déphasage ($\Delta\phi$) :** **$\Delta\phi = \frac{2\pi\delta}{\lambda}$** * **Les conditions :**
  * *Constructives (Lumière max) :* $\delta = p\lambda$ (avec $p$ entier).
  * *Destructives (Obscurité) :* $\delta = (p + \frac{1}{2})\lambda$.

## 3. Les Fentes d'Young
**Les Formules "Dures" :**
* **Différence de marche géométrique :** $\delta = \frac{ax}{D}$ 
* **L'interfrange ($i$) :** **$i = \frac{\lambda D}{a}$**
* **Le "Hack" de l'eau :** Plonger l'expérience dans l'eau (indice $n$) divise la longueur d'onde par $n$ ($\lambda_{eau} = \lambda/n$). Conséquence : l'interfrange diminue, **les franges se resserrent !**

## 4. L'Interféromètre de Michelson et la Lumière Blanche
**Le "Hack" de la Configuration (Monochromatique) :**
* **LAME D'AIR (Miroirs parallèles) :** $\delta = 2e\cos(i)$. Ce sont des **Anneaux**, localisés à **l'infini**.
* **COIN D'AIR (Angle $\alpha$) :** $\delta = 2\alpha x$. Ce sont des **Franges rectilignes**, localisées **sur les miroirs**.

**⚠️ LE PIÈGE DE LA LUMIÈRE BLANCHE :**

* **Au centre exact ($\delta = 0$) :** Toutes les longueurs d'onde interfèrent de manière constructive. On observe le **Blanc d'ordre zéro**.
* **Autour du centre :** Les franges se brouillent très vite $\rightarrow$ on observe des **irisations** (arc-en-ciel).
* **Au spectroscope :** Pour un $\delta$ élevé, on observe un **spectre cannelé** (arc-en-ciel continu barré de bandes noires).

## 5. Diffraction et Réseaux
**La Diffraction par une fente simple (Largeur $a$) :**
* **L'ouverture angulaire :** Le demi-angle de la tache centrale est **$\theta = \frac{\lambda}{a}$**.
* **La taille de la tache centrale ($L$) :** Sur un écran à distance $D$, **$L = \frac{2\lambda D}{a}$**. *(Plus la fente est petite, plus la tache s'étale).*

**Le Profil d'intensité de la Diffraction :**

* **La Forme mathématique :** Suit une loi en **Sinus Cardinal au carré** : 
  **$I(\theta) = I_0 \cdot \text{sinc}^2\left(\frac{\pi a \sin\theta}{\lambda}\right)$**
* **Le "Hack" Vrai/Faux :** La tache centrale de diffraction est **strictement deux fois plus large** que les taches secondaires.

**Les Réseaux de diffraction :** * Formule des maxima principaux : **$\sin(\theta_k) - \sin(\theta_0) = k\frac{\lambda}{a}$** (où $a$ est le pas du réseau et $k$ l'ordre).