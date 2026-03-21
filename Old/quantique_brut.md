# BLOC 3 : Physique Quantique & Architecture de la Matière 

## 1. L'Atome et la Règle de Klechkowski (Le classique de Chimie)
**Le contexte physique :** Remplissage des sous-couches électroniques. 

**Les Règles "Dures" :**
* **L'ordre (Klechkowski) :** $1s \rightarrow 2s \rightarrow 2p \rightarrow 3s \rightarrow 3p \rightarrow 4s \rightarrow 3d \rightarrow 4p$
* **Capacité :** $s = 2$, $p = 6$, $d = 10$.

**Le "Hack" de l'Ionisation (Tombé en 2023) :**
* *Électrons de Cœur vs Valence :* Valence = $n$ le plus élevé + sous-couche en cours.
* *Le Piège des métaux de transition :* Quand le Fer ($Fe = [Ar] 4s^2 3d^6$) s'ionise en $Fe^{2+}$, **il perd d'abord ses électrons $4s$** avant ses $3d$ ! $\implies Fe^{2+} = [Ar] 4s^0 3d^6$.

## 2. Le Modèle de Bohr : Énergies et Mécanique 

**Le contexte physique :** En 2025, le jury n'a pas seulement posé des questions sur l'énergie, mais sur la mécanique de l'électron en orbite autour du noyau.

**Les Formules Mécaniques "Dures" (Tombé en 2025 - Q29) :**
* **Force de Coulomb (Le piège du signe) :** L'électron ($-e$) est attiré par le proton ($+e$). La force est donc **attractive**, ce qui impose un signe "$-$" sur le vecteur unitaire sortant $\vec{u}_r$ : 
  **$\vec{F} = -\frac{e^2}{4\pi\epsilon_0 r^2}\vec{u}_r$**
* **Quantification (Postulat de Bohr) :** Le moment cinétique $L$ ne prend que des valeurs discrètes : 
  **$L = m_e v r = n\frac{h}{2\pi} = n\hbar$**
* **Vitesse sur l'orbite $n$ :** En égalisant $ma$ (accélération centripète $v^2/r$) et la force de Coulomb : 
  **$v = \frac{e}{\sqrt{4\pi\epsilon_0 m_e r}}$**

**Les Énergies "Dures" :**
* Énergie de l'hydrogène : $E_n = -\frac{13,6}{n^2}$ (en $eV$). (L'énergie est proportionnelle à **$1/n^2$**).
* Émission d'un photon : Un électron qui *descend* de niveau ($n=3 \rightarrow n=1$) **émet** un photon d'énergie $E_{photon} = |E_{final} - E_{initial}| = h\nu$.

## 3. Dualité Onde-Corpuscule et Effet Photoélectrique *(Mise à jour)*
**Le pont Matière/Lumière (De Broglie - Tombé en 2023) :**
* Toute particule (même un électron ou toi-même) possédant une quantité de mouvement $p$ se comporte comme une onde dont la longueur $\lambda$ est :
  **$\lambda = \frac{h}{p} = \frac{h}{mv}$**

**L'Effet Photoélectrique (Einstein) :**
* **$E_{photon} = W_{extraction} + E_{cinetique\_max}$**
* *Hack de résolution :* Si la lumière incidente a une fréquence trop faible ($h\nu < W_{extraction}$), **aucun électron n'est arraché**, même si tu augmentes l'intensité lumineuse à l'infini !

## 4. Le Puits de Potentiel Infini *(Nouveau - Le classique quantique)*

**Le contexte physique :** On enferme une particule (ex: un électron) dans une boîte unidimensionnelle de largeur $L$ dont les murs sont impénétrables.

**Les Formules et Pièges "Durs" (Tombé en 2023 - Q24) :**
* **Énergie quantifiée :** **$E_n = \frac{n^2 h^2}{8mL^2}$** (avec $n=1, 2, 3...$)
* **Le Piège de Proportionnalité :** Contrairement à l'atome de Bohr, ici l'énergie est proportionnelle à **$n^2$** (plus on monte, plus les niveaux s'écartent).
* **Le Piège du Zéro Absolu :** "L'énergie du niveau fondamental est nulle." $\rightarrow$ **FAUX !** Le premier niveau est $n=1$, donc $E_1 > 0$. Conséquence philosophique et physique : *une particule quantique enfermée ne peut jamais être totalement immobile.*

## 5. Vraie Mécanique Quantique : Schrödinger et Heisenberg 

**L'Équation de Schrödinger et ses conséquences (Tombé en 2025) :**
* **$i\hbar\frac{\partial\Psi}{\partial t} = -\frac{\hbar^2}{2m}\frac{\partial^2\Psi}{\partial x^2} + V(x)\Psi$**
* **La Linéarité (Le hack Q31 - 2025) :** L'équation est linéaire. Cela implique le **principe de superposition**. Si $\Psi_1$ et $\Psi_2$ sont deux états possibles, alors **$\Psi_1 + \Psi_2$ est aussi une solution valide** de l'équation !

**La Fonction d'Onde $\Psi$ (Le radar à Vrai/Faux) :**
* *Signification :* Représente une **amplitude de probabilité** (non mesurable, contient des nombres complexes).
* *Probabilité réelle :* $dP = |\Psi(x,t)|^2 dx$.
* *Normalisation (La particule existe) :* $\int_{-\infty}^{+\infty} |\Psi|^2 dx = 1$. L'unité légale de $\Psi$ en 1D est donc le **$m^{-1/2}$**.

**L'Inégalité d'Heisenberg :**
* **$\Delta x \cdot \Delta p_x \ge \frac{\hbar}{2}$** (On ne peut pas connaître précisément et simultanément la position et la vitesse).

---
