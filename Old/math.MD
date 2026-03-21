# L'ARCHITECTURE DU QCM DE MATHÉMATIQUES GEI-UNIV

## BLOC 1 : Probabilités et Dénombrement (Les points à sécuriser)
**Le contexte :** Il y a toujours 3 à 5 questions de probabilités. Le jury adore tester ta capacité à faire la différence entre combinaisons et arrangements, ainsi que ta connaissance parfaite des lois continues.

**Les "Hacks" et Formules dures :**
* **Le Piège Dénombrement (Tombé en 2020 - Q3) [cite: 2122-2125]:** * "Choisir 2 délégués parmi 10" (l'ordre n'importe pas) $\rightarrow$ C'est une combinaison : $\binom{10}{2} = \frac{10 \times 9}{2} = 45$.
  * "Choisir 1 président et 1 vice-président" (l'ordre importe) $\rightarrow$ C'est un arrangement : $10 \times 9 = 90$.
* **Lois Continues Usuelles (Tombées en 2020 et 2019) [cite: 2099-2101, 2126-2128, 2145-2147]:**
  * *Loi Uniforme sur $[0,1]$ :* L'espérance est $1/2$ et la variance est **$V(X) = 1/12$**.
  * *Somme de variables (Le grand classique) :* Si $X$ et $Y$ sont uniformes sur $[0,1]$, la densité de $Z = X+Y$ n'est PAS uniforme sur $[0,2]$ ! C'est une fonction "tente" (triangle) sur $[0,2]$ avec un maximum en 1 ($g(x)=x$ pour $x \in [0,1]$).
* **Théorème de Bayes (Tombé en 2019 - Q8) [cite: 2084-2087]:** Probabilité des causes. Si $10\%$ des dés sont pipés (font "6" 1 fois sur 2) et $90\%$ sont normaux (font "6" 1 fois sur 6). Si je tire un "6", la probabilité que le dé soit pipé s'obtient avec la formule de Bayes : $P(Pipé | "6") = \frac{P("6" | Pipé) \cdot P(Pipé)}{P("6")}$.
* **Inégalités (Tombé en 2025 - Q5) [cite: 1654-1655]:** * Bienaymé-Tchebychev : $\mathbb{P}(|X - \mathbb{E}[X]| > a) \le \frac{\mathbb{V}(X)}{a^2}$ (Attention au carré sur le $a$, c'était le piège en 2025 !).

## BLOC 2 : Séries (Numériques, Entières, Fonctions)
**Le contexte :** C'est le bloc le plus lourd (4 à 6 questions). Il faut jongler entre les convergences simples, uniformes et les rayons de convergence.

**Les "Hacks" et Formules dures :**
* **Rayon de Convergence (Somme) [cite: 2082-2083]:** Si on somme deux séries entières de rayons $R_1$ et $R_2$, le rayon de la somme $R$ vérifie **$R \ge \min(R_1, R_2)$**. L'égalité est stricte $R = \min(R_1, R_2)$ uniquement si $R_1 \ne R_2$.
* **Sommes de Riemann (Tombé en 2019 - Q10) [cite: 2088-2089]:**
  * Savoir repérer une somme de Riemann : $S_n = \frac{1}{n}\sum_{k=1}^{n} f(\frac{k}{n})$. 
  * Sa limite quand $n \to \infty$ est l'intégrale $\int_0^1 f(x)dx$. (Ex: $\frac{1}{n}\sum e^{k/n} \to \int_0^1 e^x dx = e-1$).
* **Suites de Fonctions (Tombé en 2021 - Q16) [cite: 2194-2196]:**
  * La suite $f_n(x) = x^n$ sur $[0,1]$. Elle converge *simplement* vers 0 sur $[0,1[$ et vers 1 en $x=1$. La limite n'étant pas continue, la convergence ne peut **absolument pas** être uniforme sur $[0,1]$.

## BLOC 3 : Algèbre Linéaire et Géométrie
**Le contexte :** Matrices, noyaux, déterminants et géométrie de l'espace. Beaucoup de calculs matriciels rapides.

**Les "Hacks" et Formules dures :**
* **Propriété des Noyaux (Tombé en 2020 - Q11) [cite: 2136-2138]:** Pour tout endomorphisme $f$, on a **toujours** l'inclusion : **$\ker(f) \subset \ker(f^2)$** et $Im(f^2) \subset Im(f)$. (Une phrase gratuite à cocher).
* **Le Rang des Matrices pièges (Tombé en 2020 - Q2) [cite: 2120-2121]:** Si une matrice a toutes ses lignes (ou colonnes) colinéaires ou identiques (ex: une matrice $4\times4$ remplie de $1, 2, 3, 4$), son rang est de **1**. Le théorème du rang ($dim(E) = \ker + rang$) donne immédiatement $dim(\ker) = 4 - 1 = 3$.
* **Distance d'un point à un plan (Tombé en 2019 et 2021) [cite: 2095-2096]:**
  * La distance d'un point $A(x_A, y_A, z_A)$ au plan $(P)$ d'équation $ax+by+cz+d=0$ est : 
    **$d(A, P) = \frac{|ax_A + by_A + cz_A + d|}{\sqrt{a^2+b^2+c^2}}$**.

## BLOC 4 : Analyse (Intégrales, DL, Équa-Diff et Fonctions à 2 variables)
**Le contexte :** Dérivations composées, intégrales classiques (Gaussiennes) et optimisation de fonctions de plusieurs variables.

**Les "Hacks" et Formules dures :**
* **Extrema locaux de $f(x,y)$ (Tombé en 2019, 2020, 2021) [cite: 2102-2104, 2152-2153, 2200-2204]:**
  1. Trouver les points critiques : $\frac{\partial f}{\partial x} = 0$ et $\frac{\partial f}{\partial y} = 0$.
  2. Matrice Hessienne (ou notations de Monge $r, s, t$) : On calcule le déterminant $\Delta = rt - s^2 = (\frac{\partial^2 f}{\partial x^2})(\frac{\partial^2 f}{\partial y^2}) - (\frac{\partial^2 f}{\partial x \partial y})^2$.
  3. *Si $\Delta < 0$* $\rightarrow$ Point selle (ni max, ni min). *Si $\Delta > 0$* $\rightarrow$ Extremum local (minimum si $r>0$, maximum si $r<0$).
* **L'intégrale de Gauss (Tombée en 2020 - Q15) [cite: 2147-2148]:** * Il faut savoir par cœur que **$\int_{-\infty}^{+\infty} e^{-x^2} dx = \sqrt{\pi}$**.
* **Intégrales paramétriques (Tombé en 2019 et 2020) [cite: 2107-2108, 2149-2150]:**
  * Si on a $\varphi(x) = \int e^{tx} e^{-t^2} dt$, la dérivée $\varphi'(x)$ s'obtient en dérivant sous l'intégrale (par rapport à $x$, donc le $t$ "tombe" du produit scalaire/exponentielle).
* **Équations différentielles (Tombé en 2019, 2021, 2025) [cite: 2096-2098, 2191-2193, 1699-1703]:**
  * Toujours chercher la solution sous la forme $y = \text{Solution Homogène} + \text{Solution Particulière}$. 

