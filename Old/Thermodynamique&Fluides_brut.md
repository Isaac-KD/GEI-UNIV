# BLOC 2 : Thermodynamique & Fluides 

## 1. Les Principes de la Thermodynamique et l'Entropie
**Le contexte physique :** La thermodynamique étudie les échanges d'énergie. Le 1er principe dit que l'énergie se conserve (elle change juste de forme : travail ou chaleur). Le 2nd principe dit que les phénomènes ont un sens irréversible (la chaleur va du chaud vers le froid, jamais l'inverse spontanément) et introduit l'**Entropie ($S$)**, qui mesure le "désordre" ou le sens de l'évolution du système.

**Les Équations Fondamentales :**
* **1er Principe (Bilan d'énergie) :** $\Delta U = W + Q$ 
    *(La variation d'énergie interne $U$ d'un système est la somme du Travail $W$ et de la Chaleur $Q$ reçus).*
* **2nd Principe (Bilan d'entropie) :** $\Delta S = S_{echange} + S_{creation}$
    * **L'entropie échangée :** $S_{echange} = \int \frac{\delta Q}{T_{ext}}$ (Elle a le même signe que la chaleur $Q$. Si le système refroidit, il perd de la chaleur, donc $S_{echange} < 0$).
    * **L'entropie de création :** $S_{creation} \ge 0$. Elle est nulle pour une transformation idéale (réversible) et **strictement positive** pour le monde réel (irréversible).

**Application directe aux questions du concours :**
* *L'unité de $S$ :* Puisque $S_{echange} = Q / T$ (Énergie / Température), l'unité est le **Joule par Kelvin ($J/K$)**.
* *Extensivité :* L'entropie est une grandeur **extensive**. Si tu doubles la taille de ton système, tu doubles son entropie (contrairement à la température qui est intensive).
* *Le piège du "Système Isolé" :* Un système isolé n'échange rien avec l'extérieur. Donc $Q = 0$ et $W = 0$. Par conséquent, $S_{echange} = 0$. Son bilan d'entropie devient $\Delta S = S_{creation}$. Comme $S_{creation} \ge 0$, **l'entropie d'un système isolé ne peut qu'augmenter, elle n'est jamais nulle !** ## 2. Transferts Thermiques (La propagation de la chaleur)
**Le contexte physique :** Comment la chaleur voyage-t-elle dans un solide ? Par conduction. Les atomes chauds vibrent et transmettent cette vibration aux voisins. La chaleur va spontanément des zones chaudes vers les zones froides.

**Les Équations Fondamentales :**
* **Loi de Fourier :** $\vec{j}_Q = -\kappa \overrightarrow{\text{grad}} T$
    *(Le vecteur densité de flux thermique $\vec{j}_Q$ est proportionnel au gradient de température. Le signe "moins" traduit le fait que la chaleur fuit les hautes températures. $\kappa$ est la conductivité thermique en $W \cdot m^{-1} \cdot K^{-1}$).*
* **Équation de la chaleur :** $\frac{\partial T}{\partial t} = \alpha \Delta T$
    *(L'évolution de la température dans le temps dépend de sa répartition spatiale, via le Laplacien $\Delta$. $\alpha$ est la diffusivité thermique en $m^2/s$).*

## 3. Les Modèles de Gaz (Parfait vs. Réel)
**Le contexte physique :** * Le **gaz parfait** est un modèle mathématique idéal : on imagine que les molécules sont des points (sans volume) et qu'elles s'ignorent totalement (aucune force entre elles).
* Le **gaz réel** (modèle de Van der Waals) corrige ça : les molécules ont une vraie taille (elles prennent de la place) et elles s'attirent (forces de Van der Waals) ou se repoussent.

**Les Équations Fondamentales :**
* **Gaz Parfait :** $PV = nRT$
* **Gaz de Van der Waals :** $(P + \frac{n^2 a}{V^2})(V - nb) = nRT$

**L'explication des termes (très testée au concours) :**
* **Le Covolume ($nb$) :** C'est le volume incompressible des molécules. L'espace vraiment disponible pour bouger n'est pas $V$, mais $(V - nb)$. Cela modélise les forces **répulsives** à très courte distance (les molécules refusent de se rentrer dedans).
* **La Pression Interne ($\frac{n^2 a}{V^2}$) :** Les molécules s'attirent. Avant de taper le mur (ce qui crée la pression $P$), une molécule est retenue en arrière par les autres. La pression réelle est donc *plus faible* que la pression idéale. On ajoute ce terme correctif $a$ pour modéliser ces forces **attractives**.

## 4. Machines et Cycles Thermodynamiques
**Le contexte physique :** Pour créer un moteur ou un frigo, on fait subir à un gaz une suite de transformations qui reviennent au point de départ (un cycle). On représente cela sur un diagramme Pression-Volume.
x

**Les Équations Fondamentales et Transformations :**
* **Calcul du Travail :** $\delta W = -P_{ext} dV$. Si le gaz gonfle (détente, $dV > 0$), $W$ est négatif (le gaz se fatigue pour repousser l'extérieur).
* **Transformation Isotherme ($T$ = constante) :** La première loi de Joule dit que l'énergie interne d'un gaz parfait ne dépend que de $T$. Donc $\Delta U = 0$. Le 1er principe donne $0 = W + Q$, donc **$W = -Q$**. Le travail se calcule par $W = -\int_{V_1}^{V_2} \frac{nRT}{V} dV = -nRT \ln(\frac{V_2}{V_1})$.
* **Transformation Adiabatique :** Le système est calorifugé, aucune chaleur ne rentre ou ne sort. **$Q = 0$**. Le 1er principe donne $\Delta U = W$.
* **Le Cycle de Carnot :** C'est le cycle idéal parfait. Il est composé de 2 Isothermes et 2 Adiabatiques. 

## 5. Le Rayonnement Thermique (Le Corps Noir)
**Le contexte physique :** Tout objet ayant une température émet de la lumière. Un "corps noir" est un objet théorique qui absorbe toute la lumière qu'il reçoit et réémet un spectre parfait dépendant *uniquement* de sa température.


**Les Équations Fondamentales :**
* **Formule de Planck :** $\rho(\nu,T) = \frac{8\pi h\nu^3}{c^3}\frac{1}{e^{h\nu/k_BT}-1}$. Elle exprime la densité spectrale d'énergie. Son unité est le $J \cdot m^{-3} \cdot Hz^{-1}$. La présence du "$h$" prouve que l'énergie électromagnétique est **quantifiée**.
* **Loi de Wien :** $\lambda_{max} = \frac{A}{T}$ (ou $\lambda_{max} \cdot T = constante$).
    *(La longueur d'onde de l'émission maximale est inversement proportionnelle à la température. Plus c'est chaud, plus la lumière tire vers les courtes longueurs d'onde).*

**Application au concours :**
* À température ambiante ($T=300K$), l'émission maximale est d'environ $10 \mu m$, ce qui est en plein dans **l'infrarouge** (invisible à l'œil nu).
* Le Soleil ($T=6000K$) émet un maximum autour de $0.5 \mu m$, ce qui est la couleur jaune dans le **spectre visible**.

## 6. Statique des Fluides et Archimède
**Le contexte physique :** Dans un fluide au repos soumis à la gravité, plus on descend profond, plus on a le poids de l'eau au-dessus de nous, donc plus la pression augmente. Cette différence de pression entre le bas et le haut d'un objet immergé crée une force vers le haut : la poussée d'Archimède.


**Les Équations Fondamentales :**
* **Principe fondamental de l'hydrostatique :** $\Delta P = \rho_{fluide} \cdot g \cdot \Delta z$
    *(La pression $P$ augmente linéairement avec la profondeur $z$. Attention, si l'axe $z$ pointe vers le haut, on écrit $dP = -\rho g dz$).*
* **La Poussée d'Archimède :** $\vec{\Pi}_A = - \rho_{fluide} \cdot V_{immerge} \cdot \vec{g}$
    *(La force est égale à l'opposé du poids du volume de fluide que l'objet a déplacé).*

**Application au concours (Exercice du cylindre) :**
Si tu as un cylindre de rayon $R$ plongé d'une profondeur $h$ dans l'eau.
* Le volume immergé est $V_{immerge} = \text{Surface de base} \times \text{hauteur dans l'eau} = \pi R^2 h$.
* La masse d'eau déplacée est $m_{eau} = \rho_{eau} \cdot \pi R^2 h$.
* À l'équilibre, le Poids de l'objet compense la Poussée d'Archimède ($Poids = \Pi_A$).

---

# BLOC 2 : Thermodynamique & Fluides (Le Cours Intégral - Version Ultime 100%)

## 1. Les Principes de la Thermodynamique et l'Entropie
**Le contexte physique :** La thermodynamique étudie les échanges d'énergie. Le 1er principe dit que l'énergie se conserve. Le 2nd principe introduit l'**Entropie ($S$)**, qui mesure le sens irréversible de l'évolution du système.

**Les Équations Fondamentales :**
* **1er Principe :** $\Delta U = W + Q$ 
* **2nd Principe (Bilan d'entropie) :** $\Delta S = S_{echange} + S_{creation}$
    * **$S_{echange}$ :** $\int \frac{\delta Q}{T_{ext}}$ (Même signe que la chaleur $Q$. Unité : $J/K$).
    * **$S_{creation}$ :** $\ge 0$. Nulle pour une transformation réversible, **strictement positive** si irréversible.

**Le Piège du "Système Isolé" (Tombé en 2023 et 2025) :** Un système isolé n'échange rien ($Q = 0 \Rightarrow S_{echange} = 0$). Donc $\Delta S = S_{creation}$. Comme $S_{creation} \ge 0$, **l'entropie d'un système isolé ne peut qu'augmenter, elle n'est jamais nulle !** (C'est une grandeur extensive).

## 2. Le Squelette Calculatoire : Énergie, Enthalpie et Laplace *(Nouveau)*
**Le contexte physique :** Pour calculer concrètement le travail ou la chaleur, il faut lier l'énergie à la température via les capacités thermiques à volume constant ($C_v$) ou pression constante ($C_p$).

**Les Équations "Dures" à connaître par cœur :**
* **Lois de Joule (Gaz Parfait) :** L'énergie interne $U$ et l'enthalpie $H$ ne dépendent que de la température. 
    * $dU = n \cdot C_v \cdot dT$ (Sert à calculer $\Delta U$)
    * $dH = n \cdot C_p \cdot dT$
* **Relation de Mayer :** $C_p - C_v = nR$. 
* **Le coefficient adiabatique :** $\gamma = \frac{C_p}{C_v}$ *(Souvent $\gamma = 1,4$ pour l'air).*
* **Lois de Laplace (Transformation Adiabatique Réversible) :** Puisque $Q=0$, les variables d'état sont liées par ces équations vitales pour trouver un volume ou une température finale :
    * $P \cdot V^\gamma = \text{constante}$ 
    * $T \cdot V^{\gamma - 1} = \text{constante}$

## 3. Les Modèles de Gaz (Parfait vs. Réel)
* **Gaz Parfait :** $PV = nRT$ (Les molécules sont des points sans interaction).
* **Gaz de Van der Waals (Tombé en 2025) :** $(P + \frac{n^2 a}{V^2})(V - nb) = nRT$
    * **$nb$ (Covolume) :** Modélise les forces **répulsives** (le volume propre des molécules).
    * **$\frac{n^2 a}{V^2}$ (Pression interne) :** Modélise les forces **attractives** (qui diminuent la pression exercée sur les parois).

## 4. Machines et Cycles Thermodynamiques
**Le contexte physique :** Un moteur ou un frigo fait subir à un gaz un cycle de transformations (Isotherme, Adiabatique, Isochore, Isobare). 

**Règles et Équations :**
* **Travail d'une Isotherme ($T$ = cste) :** $\Delta U = 0 \Rightarrow W = -Q$. Le calcul donne $W = -nRT \ln(\frac{V_final}{V_initial})$.
* **Le Cycle de Carnot :** C'est le cycle idéal (2 isothermes, 2 adiabatiques).
* **Rendement Maximal de Carnot (Tombé en 2022) :** Pour un moteur fonctionnant entre une source chaude ($T_C$) et une source froide ($T_F$), l'efficacité est :
    * **$\eta = 1 - \frac{T_F}{T_C}$**
    * *🚨 PIÈGE ABSOLU :* Les températures doivent **OBLIGATOIREMENT être en Kelvin** (K = °C + 273,15).

## 5. Le Rayonnement Thermique (Le Corps Noir)
**Le contexte physique :** Un "corps noir" absorbe toute lumière et réémet un spectre parfait dépendant *uniquement* de sa température.
* **Formule de Planck :** Prouve que l'énergie électromagnétique est **quantifiée** (présence de la constante $h$). L'unité de la densité spectrale est le $J \cdot m^{-3} \cdot Hz^{-1}$.
* **Loi de Wien :** $\lambda_{max} = \frac{A}{T}$. La longueur d'onde d'émission maximale est inversement proportionnelle à la température.
    * **T = 300 K** (Ambiant) $\rightarrow$ Émet dans **l'Infrarouge**.
    * **T = 6000 K** (Soleil) $\rightarrow$ Émet dans le **Visible** (Jaune).

## 6. Statique des Fluides et Archimède

**A. Fluides Incompressibles (L'Eau)**
* **Hydrostatique :** $\Delta P = \rho_{eau} \cdot g \cdot \Delta z$ (La pression augmente linéairement).
* **Poussée d'Archimède :** $\vec{\Pi}_A = - \rho_{eau} \cdot V_{immerge} \cdot \vec{g}$. (Égale au poids du volume d'eau déplacé).
* **🧊 LE PIÈGE ULTIME (Tombé en 2022) :** "Un glaçon flotte dans un verre d'eau rempli à ras bord. Il fond. Que fait le niveau de l'eau ?" $\rightarrow$ **Il reste EXACTEMENT LE MÊME.** (Le volume d'eau liquide issu de la fonte est exactement égal au volume immergé du glaçon).

**B. Fluides Compressibles (L'Air atmosphérique) *(Nouveau)***
* **Modèle de l'atmosphère isotherme (Tombé en 2022) :** L'air se compresse sous son propre poids. La pression ne diminue pas linéairement, mais de façon exponentielle selon la loi de nivellement barométrique :
    * **$P(z) = P(0) \cdot e^{-\frac{M \cdot g \cdot z}{R \cdot T}}$** 
    * *(Avec $M$ la masse molaire de l'air, $g$ la gravité, $R$ la constante des gaz, $T$ la température en Kelvin).*

## 7. Transferts Thermiques
* **Loi de Fourier :** $\vec{j}_Q = -\kappa \overrightarrow{\text{grad}} T$ (La chaleur va du chaud vers le froid. Ne fonctionne pas dans le vide).
* **Équation de la chaleur :** $\frac{\partial T}{\partial t} = \alpha \Delta T$ (La diffusivité $\alpha$ est en $m^2/s$).