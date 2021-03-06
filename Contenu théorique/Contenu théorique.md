# Contenu théorique

# Préalable

## Classification des formes quadratiques

### Généralités

Est appelée forme quadratique toute forme $f:\mathbb{R}^n\to\mathbb{R}$ de type $$f(x_1,...,x_n)=\sum_{1\leq i,j\leq n}\lambda_{ij}x_ix_j$$

On associe alors à $f$ une matrice diagonale symmétrique $\Lambda$. Or toute matrice symétrique est diagonalisable en une matrice orthogonale: $\exists M \in \mathcal{O}(\mathbb{R}) / \Lambda = M^T\cdot D\cdot M$. Ceci permet donc d'écrire $f(X) = (M\cdot X)^T\cdot D\cdot (M^{-1}\cdot X)$.

*Preuve*: On se ramène au cas où $\lambda_{11} \neq 0$ soit par échange de lignes si un autre terme diagonal est non nul, soit en posant $y_i=\frac{1}{2}(x_i+x_j)$ et $y_j=\frac{1}{2}(x_i-x_j)$ si $\lambda_{ij}\neq 0$. On factorise ensuite l'expression de $f$ par $\lambda_{11}$, et on constate que si l'on note $\mu_{ij}=\frac{\lambda_{ij}}{\lambda_{11}}$, alors les termes en $x_1$ sont exactement:

$$x_1^2+2\sum_{j=2}^n \mu_{1j}x_1x_j=\big(x_1+\sum_{j=2}^n \mu_{1j}x_j\big)^2-\big(\sum_{j=2}^n \mu_{1j}x_j\big)^2$$

En posant $y_1$ égal au premier terme de cette différence, on a une expression du type $f(y)=\lambda_{11}y_1+$ un reste quadratique en $n-1$ variables. Par récurrence, on obtient bien une matrice diagonale.

Par changement de base, on peut donc écrire $f(X) = X\cdot D\cdot X^T$ avec $D$ diagonale. En normalisant, on peut considérer $D$ diagonale à coefficients dans $\{-1,0,1\}$. Enfin, en changeant l'ordre des vecteurs de la base on se ramène au cas où f est de la forme:

$$f(x_1,...,x_n)=x_1^2+x_2^2+...+x_k^2-x_{k+1}^2-...-x_s^2$$

On constate par ailleurs que $s=rg(\Lambda)=rg(f)$ et $sgn(\Lambda)=k-(s-k)=2k-s$. En général, il faut $\frac{n(n+1)}{2}$ coefficients pour décrire une telle forme, mais on se ramène ici à $n$ nombres (1, -1 ou 0) modulo une base.

### Cas de $n=2$

On a alors $f(x,y)=ax^2+2bxy+cy^2$, et $0\leq rg(f)\leq 2$ ainsi que $0\leq k\leq rg(f)$. Comme vu ci-dessus, deux formes quadratiques de rang et signature égaux sont équivalentes à changement de base près. On peut donc catégoriser en $1+2+3=6$ classes les formes quadratiques:

 - $Q_{2,2}$: $x^2+y^2$
 - $Q_{2,0}$: $x^2-y^2$
 - $Q_{2,-2}$: $-x^2-y^2$
 - $Q_{1,1}$: $x^2$
 - $Q_{1,-1}$: $-x^2$
 - $Q_{0,0}$: $0$

## Classification des formes cubiques ($n=2$)

### Noyaux de formes cubiques

Une forme cubique de deux variables est une application $$f: (x,y) \mapsto \alpha x^3+\beta x^2y+\gamma xy^2+\delta y^3$$

Ces applications se divisent en cinq catégories en fonction de $(\alpha,\beta,\gamma,\delta)$. Cherchons une classification à partir du noyau de $f$. Ce noyau est stable par $\cdot$ la loi de composition externe, et peut donc être vu comme un ensemble de droites passant par l'origine dans $\mathbb{R}^2$.

En cherchant l'intersection de ces droites avec $x=1$ (en prenant garde à la droite $x=0$), on cherche à résoudre $\alpha+\beta y+\gamma y^3=0$. Si au moins un coefficient est non nul, cette équation admet au plus 3 solutions réelles (et un nombre pair de racines complexes), donc on distingue cinq catégories de noyaux:

 - $C_{3,0}$: Trois droites distinctes
 - $C_{1,0}$: Une droite unique
 - $C_{3,2}$: Trois droites dont deux coïncidantes (racine double)
 - $C_{3,3}$: Trois droites coïncidantes (racine triple)
 - $C_{\infty,0}$: Le plan en entier (cas où $(\alpha,\beta,\gamma,\delta)=(0,0,0,0)$)

Ceci découle du fait que si la droite $x=0$ est dans le noyau, alors $\delta=0$ et on se retrouve avec un polynôme du second degré en $y$, et donc bien au plus trois droites.

Ces catégories en sont bien, car aucun changement de coordonnées ne fera varier le `nombre de droites du noyau' (à voir en termes de déformation du plan, les droites coïncidantes coïncident toujours et celles distinctes restent distinctes).

### Equivalence des classes

Deux fonctions appartenant à la même catégorie de noyau ont la même expression à changement de coordonées linéaire près. Une analyse de chaque cas donne:

 - $C_{3,0}$: $f(x,y)=x^2y-y^3$
 - $C_{1,0}$: $f(x,y)=x^2y+y^3$
 - $C_{3,2}$: $f(x,y)=x^2y$
 - $C_{3,3}$: $f(x,y)=x^3$
 - $C_{\infty,0}$: $f=0$

*Preuve*: Un changement de base dans le premier cas permet de déformer le plan de manière à obtenir un carré: les trois droites correspondent aux abscisses, ordonées et l'identité. Alors, $f$ est divisible par $xy(x-y)$, et à changement de base supplémentaire ($(x',y')=\frac{1}{2}((x+y),(x-y))$) on obtient $f(x,y)=x^2y-y^3$.

Dans les autres cas, on considère une des droites, d'expression $lx+my=0$. $f$ peut être factorisée par cette expression, et l'on obtient une de trois catégories de formes quadratiques: $Q_{1,1}$ et $Q_{1,-1}$ ainsi que $Q_{2,2}$ et $Q_{2,-2}$ peuvent être fusionées, car le signe peut être compensé par le changement $(x,y)=-(x,y)$.

Par changement de coordonées, on est donc ramené à l'un des cas: $(Lx+My)(x^2-y^2)$ ou $(Lx+My)x^2$ ou $(Lx+My)(x^2+y^2)$. Le premier de ces cas nous ramène soit aux trois droites, soit au second cas (selon si $(Lx+My)$ est multiple de $(x-y)$ ou $(x+y)$ ou non). Le second cas mène soit à $x^3$ (si $M=0$) ou $xy^2$. Le troisième est $(x^2+y^2)y$ (soit $LM=0$, ou on procède à une *rotation des axes* $(x',y')=\frac{1}{\sqrt{L^2+M^2}}(Ly-Mx,Lx+My)$).

## Fonctions inverses et implicites

### Développement limités

On introduit la notion de *k-jet*, la fonction polynomiale formée par les $k$ premiers termes du développement de Taylor d'une fonction en un point $y$, noté: $$(j^k_y f)(y+x) = f(y) + xf'(y)+...+\frac{x^n f^{(n)}(y)}{n!}$$

Pour une fonction à $n$ variables, on définit son dévelopmmeent de Taylor et son *k-jet* par: $$(j^k_y f)(y+x) = f(y) + df_y(x)+...+\frac{(df^{(k)}_y)(x)(x)...(x)}{k!}$$

On peut réecrire le terme d'ordre $k$ sous la forme $$\frac{1}{k!}\sum_{i_1,...,i_k} \frac{\partial^k f}{\partial x_{i_1}...x_{i_k}} x_{i_1}...x_{i_k}$$

### Théorème d'inversion locale

Si $f\in\mathcal{C}^{\infty}(U,\mathbb{R}^m)$, et que $df_a$ est bijective (ou de déterminant non nul), alors f est un **difféomorphisme local** (ou localement bijective de réciproque $\mathcal{C}^{\infty}$).

\bigskip

*Preuve*: On se ramène à un voisinage de 0 où $df_0=Id_E$ (et donc $F=E$) en prenant pour fonction $df_a^{-1}(f(a+x)-f(a))$ que l'on notera $f$. Sur $B_r$, on a $\Vert df_x-Id_E \Vert \leq \frac{1}{2}$. On peut alors écrire $df_x=Id_E-u$ et donc avoir $df_x^{-1}=Id_E+u+u^2+...$ (ça converge puisque la norme est subordonnée).

On pose, pour $y$ fixé de $B_{\frac{r}{2}}$, $h:x\mapsto x+y-f(x)$. On a par les acroissements finis sur $B_r, \Vert h(x) - h(x')\Vert\leq\frac{\Vert x-x' \Vert}{2}$, donc h contractante. Elle est de plus à images dans $B_r$ donc y admet un unique point fixe: $y$ admet un antécédent unique par $f$ dans $B_r$. $f$ est donc bijective $f^{-1}(B_\frac{r}{2}) \cap B_r \to B_{\frac{r}{2}}$.

Quant à la continuité de la réciproque, on pose $g:x\mapsto x-f(x)$. *L'inégalité des accroissements finis* donne $\Vert x-x' \Vert\leq 2\Vert f(x) - f(x')\Vert$ et donc en appliquant à $f^{-1}(y)$ et $f^{-1}(y')$ on obtient $f^{-1}$ 2-lipschitzienne.

Enfin, pour la différentiabilité, on choisit $k$ proche de 0 et on montre $\Vert f^{-1}(y+k)-f^{-1}(y)-(df_x)^{-1}(k) \Vert=o(k)$ en posant $h=f^{-1}(y+k)-f^{-1}(y)$ puis en constatant $f(x+h)=y+k$ et $h=o(k)$.

\bigskip

*Corollaire classique*: si $f\in\mathcal{C}^{\infty}$ est injective et $df_a$ est inversible, alors il existe un voisinage de $a$ dont l'image par $f$ est un ouvert, et $f$ est un difféomorphisme local.

### Théorème des fonctions implicites

Si $f\in\mathcal{C}^{\infty}(\mathbb{R}^n\times\mathbb{R}^m,\mathbb{R}^p)$, et que le noyau de $df_{(x,y)}$ est localement le graphe d'une fonction $y=g(x)$, alors le noyau de $f$ est localement le graphe d'une application $y=h(x)$.

Plus formellement, si l'on note $f_2(y) = f(x_0, y)$, et que $df_{2,y_0}$ est difféomorphisme local (donc $f_2$ est localement inversible), alors on a une application $\phi$ telle que $f(x,\phi(x))=c$ sur un voisinage de $(x_0,y_0)$, et ce pour tout $c$ au voisinage de $f(x_0,y_0)$.

Cela signifie que $c$ admet un unique antécédent par $y\mapsto f(x,y)$ pour $x$ suffisament proche de $x_0$.

\bigskip

On notera que ces deux théorèmes restent valables sous des hypothèses moins fortes de régularité, et que ces hypothèses sont héritées par $\phi$ et $f^{-1}$ dans ce cas. De plus, le lien entre ceux-ci est fort: l'un peut se déduire de l'autre.

## Points critiques

Un point critique $a$ est dit non dégénéré si $\forall x, rg(d^2f_a(x))=n$ (c'est à dire que $x\mapsto(y\mapsto d^2f_a(x,y))$ est isomorphisme), ou de manière équivalente si le déterminant Hessien de $f$ est non nul.

### Lemme d'\textsc{Hadamard}

Si $f(0)=0$ et $f$ est infiniment différentiable, alors il existe un voisinage de 0 sur lequel $f$ peut s'écrire: $f(x)=g_1(x)x_1+...+g_n(x)x_n$ avec $g_i(0) = \frac{\partial f}{\partial x_i}(0)$.

Si 0 est point critique, on peut même écrire (toujours sur un voisinage de 0): $$f(x)=\sum_{i,j} x_ix_jh_{ij}(x)$$

### Lemme de \textsc{Morse}

Si $f\in\mathcal{C}^\infty(\mathbb{R}^n,\mathbb{R})$ admet un point critique non dégénéré en $u$, alors il existe un voisinage de $u$ et un $\mathcal{C}^\infty$-difféomorphisme (donc un changement de coordonnées) $y=(y_1,...,y_n)$ tel que: $$f=f(u)+y_1^2+...+y_l^2-y_{l+1}^2-...-y_n^2$$

\bigskip

*Preuve*: On montre par récurrence sur $r$ que $f$ s'écrit $$f(x)=\pm u_1^2 \pm...\pm u_{r-1}^2 + \sum_{i,j\geq r} u_iu_jH_{ij}(u)$$

Le rang 0 se déduit du *lemme d'\textsc{Hadamard}*. On peut de plus rendre $H_{ij}$ symétrique en $i$ et $j$. On pose alors $$u_r' =\sqrt{\mid H_{rr}\mid}\big(u_r+\sum_{i>r}u_i\frac{H_{ir}}{H_{rr}}\big)$$

On peut supposer $H_{rr}\neq 0$ par un changement de coordonées comme vu en *1.1*. Il s'agit bien d'un difféomorphisme selon le *théorème d'inversion locale*, et donc il s'agit bien d'un changement de coordonnées. On réécrit alors $f$ comme précédemment mais en allant jusqua'au rang $v_r$ au lieu de $u_{r-1}$ (attention, $(u_r')^2$ donne un reste à ajouter pour former de nouveaux $H_{ij}$).

\bigskip

Une application du type $a+y_1^2+...+y_k^2-y_{k+1}^2-...-y_n^2$ est appelée *k-saddle de \textsc{Morse}*. De plus, on note que si $f$ est *0-saddle* alors $u$ est minimum local, et si $f$ est *n-saddle*, alors $u$ est maximum local.

$u$ est alors un point critique isolé (il existe un voisinage sans autre points critiques), et puisque le changement de coordonées conserve l'isolation, on en déduit que tout point critique non dégénéré est isolé. De plus, $l$ est invariant par changement de coordonnées (donc par difféomorphisme, c'est une propriété topologique intrinsèque à $f$).

### Cas de $n=1$

Si $f(0)=f'(0)=...=f^{(k-1)}=0$ et $f^{(k)}(0)\neq 0$ alors, il existe un voisinage de 0 et un changement de coordonées pour lesquels $f(x)=\pm x^k$ (qui est un $+$ si $k$ est impair).

On définit la relation d'équivalence *en 0* sur $\mathcal{C}^\infty$ où $f \mathcal{R} g$ si et seulement si $g=f\circ y + \gamma$ sur un voisinage de 0, avec $y$ $\mathcal{C}^\infty$-difféomorphisme et $\gamma$ une constante pour pallier aux éventuelles différences de valeur en 0.

Deux fonctions sont en relation si et seulement si leurs écritures en ces coordonnées $\pm x^k$ et $\pm x^l$ ont le même signes et $k=l$. Ceci fournit une classification des points critiques en dimension 1, en fonction de leurs dérivées successives.

### Cas de $n\geq 2$

En dimension supérieure ce n'est pas forcément le cas: deux fonction ayant les mêmes $k$-jet ne sont pas forcément équivalentes. Une fonction est dite *déterminée* si un de ses $k$-jets permet de dire si toute autre fonction lui est équivalente ou non. Ce $k$-jet est alors dit *suffisant*.

### Théorème de décomposition

Si f admet 0 pour point critique et $H(f)_0$ est de rang $r$, alors $f$ est équivalente (au sens défini ci-dessus) au voisinage de 0 à une fonction de la forme $$g(x)=\pm x_1^2\pm x_2^2\pm ... \pm x_r^2 + h(x_{r+1},...,x_n)$$

*Preuve (en dimension deux)*: On suppose $H(f)_0$ de rang 1. Via un changement de base, on peut supposer $\frac{\partial f}{\partial x}(0,0) \neq 0$. On applique alors le *théorème des fonctions implicites* à $\frac{\partial f}{\partial x}$ pour obtenir $\varphi$ telle que $\frac{\partial f}{\partial x}(\varphi(y), y)=0$ pour tout $y$ proche de 0.

Le difféomorphisme local $\Phi: (x,y) \mapsto (x+\varphi(y), y)$ permet de poser $F(u,v) = f\circ\Phi(u,v)$ vérifiant $\frac{\partial F}{\partial u}=\frac{\partial f}{\partial x}$ et $\frac{\partial F}{\partial u}=0 \iff u=0$.

Le *lemme d'\textsc{Hadamard}* nous permet alors d'écrire $F(u,v)=\alpha(v)+u^2\beta(u, v)$ (car ?)

\bigskip

*Preuve*: On travaille dans $\mathcal{C}^\infty$. Alors $H(f)_0$ peut être mise sous la forme d'un bloc diagonal de 1 et de -1 de format $r\times r$ par un changement de base (selon le *lemme de Morse*) et des 0 partout ailleurs. On applique le *théorème des fonctions implicites* en (0,0) (d'image 0) à $$(x_1,...,x_r),(x_{r+1},...,x_n)\mapsto \big(\frac{\partial f}{\partial x_1}(x), ..., \frac{\partial f}{\partial x_r}(x)\big)$$

On obtient alors $g$ telle que $(g(x_{r+1},...,x_n),x_{r+1},...,x_{r})$ soit l'ensemble des points pour lesquels l'image de la fonction précendente soit nulle. Notons alors $F: x\mapsto ((x_1,...,x_r)+g(x_{r+1},...,x_n),x_{r+1},...,x_{r})$ qui correspond à $f$ à un changement de coordonées près, puisque

Tout a était fait afin que F

### Stabilité structurelle

Une application $f$ est dit **structurellement stable** si pour toute application $p$ suffisament proche de 0 (et infiniment continue), $f+p$ a le même type de point critique que $f$ à translation près (c'est à dire qu'elles sont équivalentes). Un point critique est en fait structurellement stable si et seulement si il est non dégénéré.
La **stabilité structurelle** signifie plus généralement que le comportement qualitatif ne change pas malgré une perturbation suffisament petite.

## Variétés

Une **variété** est un ensemble de $\mathbb{R}^n$ qui est localement homéomorphe à $\mathbb{R}^m$ et qui a un unique plan tangent en tout point, où $m\leq n$ est appelé la *dimension de la variété*. On parle alors d'un *système de coordonées locales* lorsqu'on considère une application de la variété vers $\mathbb{R}^m$.

### Typicalité



### Transversalité

Deux sous-espaces vectoriels de $\mathbb{R}^n$ sont dit **transverses** s'ils s'intersectent en un espace de dimension minimale. En l'occurence, $U$ et $V$ sont transverses si et seulement si $dim(U\cap V)=max(0;dim(U)+dim(V)-n)$. Cette formulation est équivalente à $dim(U+V)=min(dim(U)+dim(V); n)$.

Cette notion se généralise aux espaces affines, qui sont transverses si l'intersection est vide ou si $dim(U)+dim(V)\geq n$ et $dim(U\cap V)=dim(U)+dim(V)-n$. On constate que si la somme des dimensions est inférieure à $n$, les espaces ne peuvent se rencontrer.

On généralise ensuite la définition à deux variétés: elles sont transverses *en un point* si elles ne s'intersectent pas ou leurs plans tangents sont transverses.

Enfin, on généralise la définition aux applications: $f:\mathbb{R}^m\mapsto\mathbb{R}^n$ est transverse avec $g$ si leurs graphes sont transverses dans $\mathbb{R}^m\times\mathbb{R}^n$.
Ceci équivaut à dire que l'image des espaces tangents à l'antécédent de chaque point d'intersection génèrent l'espace ambient.

### Théorème d'isotopie de \textsc{Thom}

**Theorème d'isotopie (admis)**: Les intersections transverses sont structurellement stables.

### Variétés et théorème des fonctions implicites

On a vu que si $f:\mathbb{R}^m\mapsto\mathbb{R}^n$ est de rang $m$ en un de ses zéros, alors son noyau peut être paramétré de manière continue.
La réciproque est en fait vraie: toute variété suffisament continue dans $\mathbb{R}^n$ de dimension $m$ peut localement être vue comme $f^{-1}(0)$ avec $f:\mathbb{R}^m\mapsto\mathbb{R}^n$.

Ceci crée donc une équivalence entre les variétés de dimension $(n-m)$ et les ensembles définis par $m$ équations (le noyau de chaque composante de $f$).

### Théorème de transversalité de \textsc{Thom}

Il y a deux versions (*en choisir une?*).

**1. Théorème de transversalité (très admis)**: Deux variétés `aléatoirement choisies' ont infiniment peu de `chances' de se rencontrer de manière non transverse: c'est atypique.
De plus, les dérivées d'une application $f$ rencontrent typiquement transversement une certaine variété transversement.

**2. Théorème de transversalité (très admis)**: Une application peut être déformée de manière arbitrairement fine en une application transverse à toute variété donnée.

La transversalité est donc un `positionnement générique', car courant.
Deux variétés
