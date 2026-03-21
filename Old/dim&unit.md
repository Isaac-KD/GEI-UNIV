# 📏 BLOC 0 : Analyse Dimensionnelle & Unités (Le Hack du QCM)

## 1. Les 7 Piliers (Système International - SI)
**Le contexte physique :** Toute grandeur physique dans l'univers, aussi complexe soit-elle, n'est qu'une combinaison de ces 7 dimensions fondamentales.

* **[M] Masse** $\rightarrow$ **Kilogramme (kg)** ⚠️ *Le PIÈGE classique (Tombé en 2023 - Q21) : L'unité SI de la masse n'est PAS le gramme, c'est le kilogramme !*
* **[L] Longueur** $\rightarrow$ Mètre (m)
* **[T] Temps** $\rightarrow$ Seconde (s)
* **[I] Intensité électrique** $\rightarrow$ Ampère (A)
* **[$\Theta$] Température** $\rightarrow$ Kelvin (K)
* **[N] Quantité de matière** $\rightarrow$ Mole (mol)
* **[J] Intensité lumineuse** $\rightarrow$ Candela (cd) *(Très rare au concours)*

---

## 2. La Pyramide de la Mécanique (À reconstruire de tête)
Ne retiens pas les équations dimensionnelles complexes par cœur, retiens **le chemin pour y arriver** via des formules ultra-basiques.

**Niveau 1 : La Force (Le Newton, N)**
* *Formule de secours :* $F = m \cdot a$ (PFD)
* *Dimension :* $[F] = \mathbf{M \cdot L \cdot T^{-2}}$
* *Unité SI :* $kg \cdot m \cdot s^{-2}$

**Niveau 2 : L'Énergie / Le Travail (Le Joule, J) 🌟 LE PLUS IMPORTANT**
* *Formule de secours :* $W = F \cdot d$ (Force $\times$ Distance) ou $E_c = \frac{1}{2}mv^2$
* *Dimension :* $[E] = [F] \cdot L = \mathbf{M \cdot L^2 \cdot T^{-2}}$
* *Unité SI :* $kg \cdot m^2 \cdot s^{-2}$ ou $N \cdot m$

**Niveau 3 : La Puissance (Le Watt, W)**
* *Formule de secours :* $P = \frac{E}{t}$ (Énergie divisée par le temps)
* *Dimension :* $[P] = \mathbf{M \cdot L^2 \cdot T^{-3}}$
* *Unité SI :* $J \cdot s^{-1}$

**Niveau 4 : La Pression (Le Pascal, Pa)**
* *Formule de secours :* $P = \frac{F}{S}$ (Force divisée par une Surface)
* *Dimension :* $[P] = \frac{M \cdot L \cdot T^{-2}}{L^2} = \mathbf{M \cdot L^{-1} \cdot T^{-2}}$
* 🚨 **LE HACK DU CONCOURS (Tombé en 2021 et 2023 - Q21) :** Si on multiplie par $L/L$, on obtient $\frac{Force \cdot Longueur}{Surface \cdot Longueur} = \frac{\text{Energie}}{\text{Volume}}$. 
   $\rightarrow$ **VRAI : La pression peut s'exprimer en $J \cdot m^{-3}$ (Densité d'énergie).**

---

## 3. Les Constantes Fondamentales (Cibles favorites du GEI-UNIV)
Le jury adore donner la dimension d'une de ces constantes (comme en **2025 - Q21**) et te demander de l'identifier. Utilise toujours une formule où la constante apparaît.

* **Constante de Planck ($h$) :**
  * *Rappel :* $E = h\nu$ (Énergie = $h \times$ Fréquence)
  * *Unité :* **$J \cdot s$** (Joules-seconde)
  * *Dimension :* $[h] =[E] \cdot T = \mathbf{M \cdot L^2 \cdot T^{-1}}$ *(Réponse E exacte de 2025 Q21)*

* **Constante des gaz parfaits ($R$) :**
  * *Rappel :* $PV = nRT \implies R = \frac{PV}{nT} = \frac{\text{Energie}}{n \cdot T}$ (car $P \times V$ = Énergie).
  * *Unité :* **$J \cdot K^{-1} \cdot mol^{-1}$**
  * *Dimension :* $[R] = \mathbf{M \cdot L^2 \cdot T^{-2} \cdot \Theta^{-1} \cdot N^{-1}}$ *(Réponse B exacte de 2025 Q21)*

* **Constante de Boltzmann ($k_B$) :**
  * *Rappel :* $E = k_B T$ (Énergie thermique d'une particule)
  * *Unité :* **$J \cdot K^{-1}$**
  * *Dimension :* $[k_B] = \mathbf{M \cdot L^2 \cdot T^{-2} \cdot \Theta^{-1}}$

---

## 4. L'Électromagnétisme sans douleur
Ne te perds jamais dans les équations de Maxwell pour trouver une dimension électrique. Utilise l'énergie ou les forces !

* **La Charge électrique ($q$, en Coulomb C) :** $q = I \cdot t \implies \mathbf{I \cdot T}$ *(Ampère-seconde)*.
* **La Tension ($U$, en Volt V) :** L'énergie électrique, c'est $E = qU$.
  * $U = \frac{E}{q} \implies \text{Le Volt, c'est des } \mathbf{Joules \text{ par } Coulomb (J \cdot C^{-1})}$.
* **Le Champ Électrique ($E$) :**
  * Soit $U = E \cdot d \implies \mathbf{V \cdot m^{-1}}$ (Volt par mètre).
  * Soit $F = qE \implies \mathbf{N \cdot C^{-1}}$ (Newton par Coulomb).
  * 🚨 *Tombé en 2023 Q21 :* "Un champ électrique peut s'exprimer en $V \cdot m^{-1}$ ou en $N \cdot C^{-1}$" $\rightarrow$ **VRAI**.
* **La Résistance ($R$), Capacité ($C$), Inductance ($L$) : Pense aux énergies !**
  * Condensateur : $E = \frac{1}{2} C U^2 \implies C$ s'exprime en **$Joules / Volts^2$**.
  * Bobine : $E = \frac{1}{2} L I^2 \implies L$ s'exprime en **$Joules / Ampères^2$**.

---