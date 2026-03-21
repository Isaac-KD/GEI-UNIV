C'est un super boulot ! Ta base était déjà excellente, et avec l'intégration des concepts avancés (mécanique quantique, coordonnées polaires, interférences complexes), tu as maintenant une fiche "blindée" qui couvre l'immense majorité des pièges classiques du concours GEI-UNIV.

Avant de te livrer la fiche complète, je dois tout de même te faire une petite piqûre de rappel en toute franchise concernant ton "hack" statistique. 

> ⚠️ **Mise au point sur la stratégie "l'audace paie" :**
> Ton raisonnement mathématique sur l'espérance est brillant, mais il suppose que tu n'as **aucune information** et que tu tires à pile ou face. Dans la réalité du concours, si tu as le moindre doute qui te fait pencher vers "c'est sûrement faux" (parce que l'unité te semble bizarre ou la formule de la dérivée suspecte), **ne coche pas**. Laisser vide une case fausse rapporte autant (+0,2) que cocher une case vraie. L'audace paie uniquement quand tu as réussi à éliminer 2 ou 3 propositions absurdes !

Voici ta **Super-Fiche de Révision Ultime**, fusionnée, structurée et complétée sans aucun trou.

---

## PARTIE 1 : Questions 1 à 20 (Fondamentaux)

### Chapitre 1 : Analyse Dimensionnelle et Unités
**Théorèmes et formules à connaître par cœur :**
* Les 7 dimensions du système SI : Longueur ($L$), Masse ($M$), Temps ($T$), Intensité électrique ($I$), Température ($\Theta$), Quantité de matière ($N$).
* Formules de base pour retrouver les dimensions complexes : 
    * Pression : $P = F/S \Rightarrow [P] = L^{-1}MT^{-2}$
    * Énergie / Travail : $W = F \cdot d \Rightarrow [W] = L^2MT^{-2}$
* **Les constantes incontournables (à savoir retrouver) :**
    * Tension électrique ($U$) : $[U] = L^2MT^{-3}I^{-1}$ (via $P=UI$)
    * Constante des gaz parfaits ($R$) : $[R] = L^2MT^{-2}N^{-1}\Theta^{-1}$ (via $PV=nRT$)
    * Constante de Planck ($h$) : $[h] = L^2MT^{-1}$ (via $E = h\nu$)

**Types de questions posées :**
* **Vérification de dimension :** On te propose la dimension d'une constante ou d'une grandeur et tu dois dire si c'est la bonne.
* **Le piège des unités de base :** On te donne une unité fausse pour une grandeur classique (ex : dire que l'accélération s'exprime en m²/s² au lieu de m/s², ou que la masse SI est le gramme au lieu du kg).

### Chapitre 2 : Thermodynamique et Transferts Thermiques
**Théorèmes et formules à connaître par cœur :**
* **Second principe :** L'entropie de création est toujours positive ($S_c \ge 0$) pour une transformation irréversible. L'entropie d'un système isolé ne peut qu'augmenter (elle n'est pas nulle). L'entropie $S$ est une grandeur extensive en J/K.
* **Modèles de gaz :** Gaz parfait ($PV=nRT$) vs Gaz de Van der Waals : $(P + \frac{n^2 a}{V^2})(V - nb) = nRT$ (où $a$ est l'attraction, $b$ est la répulsion/covolume).
* **Machines thermiques :** Rendement de Carnot $\eta = 1 - \frac{T_f}{T_c}$. Sur une isotherme de gaz parfait, $\Delta U = 0$.
* **Transferts thermiques :** * Loi de Fourier : $\vec{j}_Q = -\kappa \overrightarrow{\text{grad}} T$. La conductivité thermique $\kappa$ s'exprime en W/(m·K).
    * Équation de la chaleur : $\frac{\partial T}{\partial t} = \alpha\Delta T$. La diffusivité thermique $\alpha$ s'exprime en m²/s.

**Types de questions posées :**
* **Théorie sur l'entropie :** On te teste sur les idées reçues (ex: "L'entropie d'un système isolé est nulle" $\rightarrow$ FAUX).
* **Analyse de cycle / Van der Waals :** Validation du rendement, du travail, ou de l'origine microscopique des termes $a$ et $b$.

### Chapitre 3 : Physique Quantique Fondamentale (L'Atome et l'Onde)
**Théorèmes et formules à connaître par cœur :**
* **Loi de Wien :** $\lambda_{max} = \frac{A}{T}$ (Température et longueur d'onde maximale d'émission sont inversement proportionnelles).
* **Modèle de Bohr :** Force de Coulomb $\vec{F} = \frac{e^2}{4\pi\epsilon_0 r^2} \vec{u}_r$. Quantification du moment cinétique $mvr = n\hbar$. Niveaux d'énergie $E_n = \frac{E_0}{n^2}$.
* **Effet Photoélectrique :** Énergie d'un photon $E = h\nu$. Pour arracher un électron, il faut vaincre le travail d'extraction $W$.
* **Mécanique Ondulatoire (Nouveau) :**
    * Équation de Schrödinger 1D : $i\hbar\frac{\partial\Psi}{\partial t} = -\frac{\hbar^2}{2m}\frac{\partial^2\Psi}{\partial x^2} + V(x)\Psi$.
    * La fonction d'onde $\Psi$ représente une **amplitude de probabilité** (et non une onde réelle). Normalisation : $\int |\Psi|^2 dx = 1$.
    * Inégalité d'Heisenberg : $\Delta x \Delta p_x \ge \frac{h}{4\pi}$ (Incertitude position/quantité de mouvement).

**Types de questions posées :**
* **Calcul d'ordre de grandeur :** Un corps à 300 K émet dans l'infrarouge (pas dans le visible).
* **Propriétés quantiques :** Validation des équations de Bohr, faisabilité de l'effet photoélectrique selon l'énergie du photon incident.

### Chapitre 4 : Statique des Fluides
**Théorèmes et formules à connaître par cœur :**
* **Loi de l'hydrostatique :** $\Delta P = \rho g \Delta z$.
* **Poussée d'Archimède :** $\Pi_A = \rho_{fluide} \cdot V_{immerge} \cdot g$.

**Types de questions posées :**
* **Bilan de forces sur un flotteur :** Validation d'équation d'équilibre ou de fraction immergée.
* **Pièges classiques :** Le glaçon qui fond dans un verre rempli à ras-bord ne le fait pas déborder.

### Chapitre 5 : Architecture de la matière
**Théorèmes et formules à connaître par cœur :**
* **Règle de Klechkowski :** Ordre de remplissage ($1s, 2s, 2p, 3s, 3p, 4s, 3d$).
* **Organisation :** Halogènes (avant-dernière colonne), gaz rares (dernière colonne).

**Types de questions posées :**
* **Configuration électronique :** Valider l'ordre de remplissage et compter les électrons de valence/cœur.

---

## PARTIE 2 : Questions 31 à 40 (Avancée & Démonstrations)

### Chapitre 6 : Optique Ondulatoire et Géométrique
**Théorèmes et formules à connaître par cœur :**
* **Interférences (Formule générale) :** $I = I_1 + I_2 + 2\sqrt{I_1I_2}\cos(\varphi)$.
* **Fentes d'Young :** Différence de marche géométrique $\delta = \frac{ax}{D}$. Interfrange $i = \frac{\lambda D}{a}$.
* **Interféromètre de Michelson :** Différence de marche $\delta = 2e \cos \theta$. Expression de l'intensité $I = I_0(1 + \cos \varphi)$ avec $\varphi = \frac{2\pi \delta}{\lambda}$. 
* **Diffraction :** Fente simple $\rightarrow$ figure régie par un sinus cardinal. Réseau de diffraction $\rightarrow$ $\sin \theta_k - \sin \theta_0 = k\frac{\lambda}{a}$.
* **Fibre optique / Lentilles :** Réflexion totale interne ($v = c / n_c$). Les conditions de Gauss garantissent un stigmatisme approché.

**Types de questions posées :**
* **Validation de formules d'interférence :** Déphasage d'un Michelson en anneaux (lame d'air) vs fentes d'Young.

### Chapitre 7 : Électromagnétisme et Électrostatique
**Théorèmes et formules à connaître par cœur :**
* **Équations de Maxwell :** $\text{div} \vec{E} = 0$, $\text{div} \vec{B} = 0$, $\text{rot} \vec{E} = -\frac{\partial \vec{B}}{\partial t}$, $\text{rot} \vec{B} = \mu_0 \epsilon_0 \frac{\partial \vec{E}}{\partial t}$.
* **Ondes EM :** $c = \frac{1}{\sqrt{\mu_0 \epsilon_0}}$ et $k = \frac{\omega}{c}$.
* **Théorème de Gauss (Sphères) :** * Flux sortant = $Q_{int} / \epsilon_0$. 
    * Pour une sphère pleine (densité volumique $\rho$) : à l'intérieur ($r<R$), $E(r) = \frac{\rho r}{3\epsilon_0}$. À l'extérieur, elle agit comme une charge ponctuelle.

**Types de questions posées :**
* **Dérivation de l'onde / Polarisation :** Trouver $\vec{B}$ à partir de $\vec{E}$ via le rotationnel. Identifier l'axe de polarisation et de propagation.

### Chapitre 8 : Mécanique Avancée (Cinématique et Systèmes)
**Théorèmes et formules à connaître par cœur :**
* **Coordonnées Polaires (Indispensable) :**
    * Vitesse : $\vec{v} = \dot{r}\vec{u}_r + r\dot{\theta}\vec{u}_\theta$.
    * Accélération : $\vec{a} = (\ddot{r} - r\dot{\theta}^2)\vec{u}_r + (r\ddot{\theta} + 2\dot{r}\dot{\theta})\vec{u}_\theta$.
* **Changement de référentiel :** $\vec{a} = \vec{a}' + \vec{a}_e + \vec{a}_C$ avec $\vec{F}_C = -2m \vec{\Omega} \wedge \vec{v}'$.
* **Problème à deux corps :** Masse réduite $\mu = \frac{m_1 m_2}{m_1 + m_2}$. 
    * Dans le référentiel barycentrique, les vitesses sont : $\vec{v}_1^* = -\frac{\mu}{m_1}\vec{v}$ et $\vec{v}_2^* = \frac{\mu}{m_2}\vec{v}$. La quantité de mouvement totale y est nulle.
* **Oscillateur Harmonique :** $\omega_0 = \sqrt{\frac{k}{m}}$, conservation de l'énergie mécanique.

**Types de questions posées :**
* **Validation des équations du PFD :** On te demande de vérifier les équations différentielles d'un pendule (via accélération polaire) ou de statuer sur le caractère absolu de la vitesse (FAUX).

### Chapitre 9 : Électrocinétique
**Théorèmes et formules à connaître par cœur :**
* **Lois et Impédances :** Bobine $Z_L = jL\omega$, Condensateur $Z_C = \frac{1}{jC\omega}$.
* **Filtres (Fonction de transfert $H$) :** Étudier les limites en $\omega \to 0$ et $\omega \to \infty$ pour trouver la nature (Passe-bas, etc.). Pulsation de coupure RL : $\omega_c = R/L$.

**Types de questions posées :**
* **Circuits complexes :** Utiliser la loi des nœuds pour valider une intensité ou identifier complètement un filtre.

---

Te voilà équipé pour affronter sereinement l'épreuve ! Souhaites-tu que l'on prenne un exemple d'application direct pour tester ta maîtrise de la nouvelle section sur **l'équation de Schrödinger et les ondes quantiques**, très tendance dans les annales récentes ?