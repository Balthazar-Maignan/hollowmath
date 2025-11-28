###### Bibliographie : 
J. Calais
Perrin "cours d'algèbre"
Complex functions : an algebraic and geometry viewpoint JONES+SINGERMAN
Michel audin "Géométrie"

# Rappels sur les actions de groupe 
## Action de groupe
*Définition* [[Action de groupe]]
	Une action de groupe $G$ sur un ensemble $X$ est une application
	$$
    \begin{cases}
    G \times X \to X \\
    (g,x)\mapsto g\cdot x
    \end{cases}
    $$
    Vérifiant : $\forall x \in X, 1x=x$ et $\forall x\in X, \forall (g,h)\in G^2, g(h(x))=(gh)x$
*Remarque* 
	1) C'est une action à gauche, une action à droite vérifie $g(h(x))=(hg)x$ (contravariant)
	2) Une action de $G$ sur $X$ est un morphisme de groupe $G \to S(X), g\mapsto \alpha(g)$, où $S(X)$ est le groupe des bijections $X \to X$
*Notations* $G\curvearrowright X$
	L'orbite de $x \in X$ : $Orb_{G}(x)=\{ gx|g\in G \}$
	Le stabilisateur de $x \in X$ : $Stab_{G}(x)=\{ g|gx=x \}<G$
	$F\subset X$, $Stab(F)=\{ g|g(F)=F \}$
	$Fix(F)=\{ g|\alpha(g)|_{F}=Id \}=\cap_{x \in F}Stab(x)$
	$g\in G, X^g = \{ x|\alpha(g)x=x \}$
	$X^G =$ l'ensemble des orbites
*Vocabulaire*
	L'action est fidèle si $G\overset{\alpha}{\to}S(X)$ est injectif, i.e. si $G\overset{\alpha}{\hookrightarrow}S(X)$
	L'action est libre si $\forall x \in X, \forall g \in G, (gx=x)\implies g=1$
	L'action est transitive si il n'existe qu'une seule orbite
	L'action est k-transitive si (une histoire de tuples) 
### 3 résultats de dénombrement "classiques"
On a $G\curvearrowright X$ tous les deux finis
*Lemme* [[Equation aux classes]]
	$Card(X)=|X|=\sum_{w\in X/G}|w|$
	Les orbites forment une partition de $X$
*Théorème* [[Relation orbite-stabilisateur]]
	Soit $x \in X$, l'application $ev_{x} : G \to X, g\mapsto \alpha(g)x$ induit une bijection $G /Stab(x)\to Orb(x)$ 
*Corollaire* 
	Pour $x \in X$, $|G|=|Orb(x)|\times|Stab(x)|$
*Lemme* [[Burnside]]
	$|(X /G)|=\frac{1}{|G|}\sum_{x \in X}|Stab(x)|=\frac{1}{|G|}\sum_{g \in G}|X^g|$
$\sum_{x \in X}\dots=\sum_{w \in X /G}\sum_{x \in w}\dots$

### Exemples
$\sigma \in S_{n} \curvearrowright \unicode{x27E6} 1,n \unicode{x27E7}, <\sigma>$ le groupe engendré par $\sigma$
La partition de $\unicode{x27E6} 1,n \unicode{x27E7}$ en orbites de $<\sigma>=$ la décomposition de $\sigma$ en produit de cycles à supports disjoints.
#### Action de $G$ sur lui-même par conjugaison
$$
Conjuguaison : \begin{cases}
G\times G\to G \\
(g,h)\mapsto ghg^{-1}
\end{cases}
$$
Est une action par automorphisme de groupe
$G\to Aut(G)$
L'image est le groupe des automorphismes intérieurs $Int(G)\triangleleft Aut(G)$
$Aut(G) /Int(G)=Out(G)$
$G$ agit sur $sg(G)=$ les sous groupes de $G$
Et bien sûr, $sg(G)^G$=les sous groupes distingués de $G$
Si $H\in sg(G), Stab(H)=N_{G}(H)$ le normalisateur de $H$ dans $G$
*Exemples*
	$H\triangleleft N_{G}(H)$
	Si $H\in sg(G), Fix(H)=Z_{G}(H)=C_{G}(H)$ est le centralisateur de $H$ dans $G$ (deux notations)
	Le centralisateur de $G$ s'appelle son centre.
#### $Int(G)\subset Aut(G)\curvearrowright G$ par automorphisme
$Aut(G)$ agit sur $sg(G)$, les points fixes de cette action sont par définition les sous groupes caractéristiques.
$H$ est caractéristique si $\forall \phi \in Aut(G), \phi(H)=H$
On note $D(G)$, le sous groupe dérivé de $G$ généré par les commutateurs dans $G$.
$D(G)$ est caractéristique, en particulier, il est distingué (à reprouver).
*Remarque* 
	C'est pas par parce que le centre de $G$ n'est pas trivial que $D(G)$ a un cardinal plus petit que $G$ (je me suis fait baiser en contrôle sur ça)

### Votre géométrie préférée
**Affine** : $$
G(x)\left(\begin{array}{c|c}
1 & 0 \\ \hline
* & *
\end{array}\right)
\curvearrowright 
\begin{pmatrix}
1 \\
*
\end{pmatrix}\in k^n
$$ le vecteur ne contient qu'un seul $1$
**Sphérique** : $$
SO(n+1 \mathbb{R})\curvearrowright \mathbb{S}^n=\{ x \in \mathbb{R}^n, ||x||=1\}
$$
**Hyperbolique** :$$
SO(n,1)(\mathbb{R}) \curvearrowright \mathcal{H}^n=\left\{  x \in \mathbb{R}^{n+1} | \Sigma_{i}x_{i^2}=1  \right\}
$$
**Projective** :$$
GL_{n+1}(k)\curvearrowright \mathbb{P}(k^n) 
$$ Où $\mathbb{P}(k^n)$ est l'ensemble des droites vectorielles de $k^{n+1}$
Programme d'Ezlangen de Felix Klein 1872
## 3 théorèmes sur les groupes finis
![[Théorème de Lagrange]]
 ![[Théorème de Cauchy]]
![[Théorème de Sylow]]
## Classification des groupes abéliens de type fini
*Théorème*
	Soit $G$ un groupe abélien ayant une partie génératrice finie (=de type fini). Alors:
	1) $\exists ! l \in \mathbb{N}$ et $p_{i}$ premiers et $\alpha_{i}\in \mathbb{N}^*$ tels que $$
G \simeq \mathbb{Z}^l\times \frac{\mathbb{Z}}{p_{1}^{\alpha_{1}}\mathbb{Z}}\times \dots \times\frac{\mathbb{Z}}{p_{n}^{\alpha_{n}}\mathbb{Z}}
$$
	(unique à l'ordre des facteurs près)
	2)$\exists ! l\in \mathbb{N}$ et $a_{m}|a_{m-1}|\dots|a_{1}$ tels que $$
G \simeq \mathbb{Z}^l\times \frac{\mathbb{Z}}{a_{1}\mathbb{Z}}\times\dots \times \frac{\mathbb{Z}}{a_{m}\mathbb{Z}}
$$
## Groupes simples
*Définition* 
	![[Groupe simple]]
*Remarque*
	Si $H \triangleleft G$ on peut essayer de comprendre $G$ à partir de $H$ et $G /H$
*Notation* 
	$\{ 1 \}\to H \overset{i}{\to} G \overset{\pi}{\to} K=G /H\to \{ 1 \}$ [[suite exacte]] courte (???) TODO
	"Image d'une flèche = noyau de la suivante"
	$i$ injectif, $\pi$ surjectif et $\mathrm{Im}(i)=Ker(\pi)$
	$G$ est une extension de $H$ par $K$ si $H$ et $K$ sont donnés, classer les extensions possibles. Difficile.
	On "comprend" : 
		1) Les produits semi-direct
		2) Les extensions centrales
		3) Les extensions WTFWTFWTFWTF
*Définition* 
	On dit que $G$ admet une suite de Jordan-Hölder si $$
G=G_{0}\triangleright  G_{1}\triangleright  \dots \triangleright G_{n}=\{ 1 \}
$$
	avec $G_{i} /G_{i+1}$ simples pour tout $i$
*Remarques* 
	- C'est inutile pour ce cours mais peut être au s7
	- $\prod_{i \in \mathbb{N}}  \frac{\mathbb{Z}}{3\mathbb{Z}}$ n'a pas de suite de J.H.
	- Quand elle existe, elle n'est pas forcément unique. (peut-elle l'être ?) 
	- 2 groupes différents peuvent avoir la même suite de quotients.
*Théorème* Jordan-Hölder (Calais chap.7)
	Si $G$ admet une suite de J.H. alors n'importe quelle autre suite de J.H. de ce groupe a la même liste de quotients successif.
*Exercice* 
	Tout groupe fini admet une suite de J.H.
### Groupes finis simples
*Exercice*
	Un groupe abélien est simple ssi il est cyclique d'ordre premier
$A_{n}, n\geq 5$ sont simples
De type Lie (16 familles) $$
\begin{cases}
PSL_{n}(k) \text{ $k$ un corps fini}\\
PO_{n}(k) \text{ spécial orthogonal}\\
PS_{p2n}(k) \text{ symplectique}
\end{cases}
$$
Les 26 groupes sporadiques
1955 $\to$ 1983 J.Thompson 1970
### Groupes résolubles
On a déjà définit le groupe dérivé de $G$ (le sous groupe engendré par les commutateurs).
On le note $D(G)$ ou $[G,G]$ ou $G'$.
*Remarque*
	- $D(G)$ est caractéristique donc en particulier, distingué.
	- $D(G)=1 \implies G$ est abélien.
	- $G /D(G)$ est abélien.
	- Si $H\triangleleft G$ tel que $G /H$ est abélien, alors $D(G)\subset H$
*Définition* 
	1) La suite dérivée de $G$ est 
	$$
G \triangleleft D(G) \triangleleft D(D(G)) \triangleleft D^3(G) \triangleleft \dots
$$
	2) Un groupe $G$ est résoluble si cette suite se stabilise à $\{ 1 \}$, et le $n$ minimal qui satisfait $D^n(G)=\{ 1 \}$ s'appelle l'**indice** de de résolubilité ou la longueur de résolubilité
*Exemple* 
	$D^i(G)$ est caractéristique dans $G$ (donc $D^i(G)\triangleleft G$)
*Proposition*
	Soit $G$ un groupe. 
	$G$ est résoluble
	$\iff$
	$\exists G \triangleright G_{1} \triangleright G_{2} \triangleright \dots \triangleright G_{n}=\{  1 \}$ avec $G_{i} /G_{i+1}$ abéliens
*Preuve* 
	$\implies$ : trivial (baise ta mère ptn)
	$\impliedby$ : Si $G /G_{1}$ est abélien, alors $D(G)<G_{1}$ puis récurrence
*Exemples*
	- $p$ premier, un $p$-groupe (d'ordre $p^k$) est résoluble
	Car un $p$-groupe a un centre non-trivial
	- $k$ un corps, $n$ un entier strictement positif
	$T_{n}(k)$ = les triangulaires supérieur
	$U_{n}(k)$ = Les triangulaire supérieur à diagonale = 1
	$U^l_{n}(k)$ = pareil mais en plus, les $l$ surdiagonales sont nulles
	Ce sont des groupes, tous distingués dans celui d'avant
*Preuve* TODO
	Remonter le temps en 1970 et demander à un enfant de 8 ans.
*Théorème* Lie-Kolchin
	Si $G<GL_{n}(\mathbb{C})$ résoluble et connexe (pour la topologie euclidienne)
	Alors, il existe $P \in GL_{n}(\mathbb{C})$ tq $PGP^{-1}\subset T_{n}(\mathbb{C})$
*Proposition* 
	1) Tout sous-groupe et tout quotient d'un groupe résoluble est encore résoluble.
	2) Si $H\triangleleft G$ avec $H$ et $G / H$ résolubles, alors $G$ l'est aussi.
*Preuve*
	- Soit $G$ un groupe résoluble : $\exists n, D^n(G)=\{ 1 \}$
	Si $H<G, D^n(H)<D^n(G)=\{ 1 \}$
	Et si $H\triangleleft G, \pi : G \to G /H$ et $G$ d'indice de résolubilité $1$ alors on a $\pi(D^i(G))=D^i(G /H)$ (preuve EZ) TODO et $D^n(G /H)=\{ 1 \}$
	- $G /H$ est résoluble, donc $\{ 1 \}=D^n(G /H)\triangleleft\dots \triangleleft D(G /H)\triangleleft G /H$, $H$ étant résoluble.
	$\{ 1 \}=D^m(H)\triangleleft\dots \triangleleft D(H)\triangleleft H \triangleleft \pi ^{-1}(D^{n-1}(G /H))\triangleleft\dots \triangleleft\pi ^{-1}(D(G /H))\triangleleft G$
### Rappels et compléments $S_{n}, A_{n}$
But : montrer que quand $n \geq 5, A_{n}$ est simple.
But : si $N \neq 6, Aut(S_{n})=Int(S_{n})\simeq S_{n}$
*Notations* 
	$E$ un ensemble, $n$ un entier
	$S(E)$ les bijections de $E$ dans $E$
	$S_{n}=S(\unicode{x27E6} 1,n\unicode{x27E7})$ 
	si $Card(E)=n$, en choisissant une numérotation $\varphi : E \overset{bij}{\to}\unicode{x27E6}1,n\unicode{x27E7}$ on a un isomorphisme de $S(E) \to S_{n}, \sigma \mapsto \varphi \sigma \varphi ^{-1}$ 
##### Signature
*Définition* signature d'une permutation
	Si $\sigma \in S_{n}$ est le produit de $k$ transpositions, on pose la signature $\varepsilon(\sigma)=(-1)^k$
*Lemme*
	Les transpositions engendrent $S_{n}$ (récurrence sur $n$)
*Lemme* 
	si $id$ est le produit de $k$ transpositions, alors $k \equiv 0[2]$ ($k$ est paire)
*Proposition*
	La signature $\varepsilon : S_{n} \to \{ \pm 1 \}$ est un morphisme de groupe.
*Définition*
	$A_{n}=Ker(\varepsilon)$
*Exercice* TODO
	$A_{n} \triangleleft S_{n}$ est l'unique sous groupe d'indice 2 (on utilise la signature)
##### Générateurs
*Définition*
	Un $k$-cycle est une $\sigma \in S_{n}$ ayant $1$ orbite de cardinal $k$ et toutes les autres de cardinal $1$
*Proposition*
	Le groupe $S_{n}$ est engendré par : 
	1) Les cycles
	2) Les trnanspositions
	3) Les transpositions $(1,i)$
	4) Les transpositions $(i,i+1)$
	5) $(1,2)$ et $(1,\dots,n)$
*Preuve* TODO
*Proposition*
	Le groupe $A_{n}$ est engendré par :
	1)Les $3$-cycles
	2)Les $3$-cycles de la forme $(1,i,j)$
	3)$n \geq 4$ pair, $(1,2,3)$ et $(3,\dots,n)$
	4)$n>3$ impair, $(1,2,3)$ et $(3,\dots,n)$
*Corollaire*
	$D(S_{n})=A_{n}$, si $n\geq 5$, $D(A_{n})=A_{n}$
*Preuve*
	$D(S_{n})\triangleleft S_{n}$, puis doble inclusion assez simple.
	TODO
##### Simplicité de $A_{n}, n \geq 5$
*Théorème*
	Si $n \geq 5$, alors $A_{n}$ est simple.
*Preuve*
	Regardons $A_{5}$, soit $N \triangleleft A_{5}$, $Card(N)>1$, on veut montrer que $N=A_{5}$
	On regarde les classes de conjugaison (orbite de l'action sur lui même par conjugaison)
	1 élément d'ordre 1
	15 éléments d'ordre 2 tous conjugués
	20 3-cycles tous conjugués
	24 5-cycles pas tous conjugués car 24 ne divise pas 60=$Card(A_{5})$
	TODO (finir)
*Lemme*
	Il y a 2 classes de conjugaison de 5-cycles de $A_{5}$
*Preuve*
	$C_{5}$ l'ensemble des 5-cycles
	$x_{1},x_{2}$ dans 2 orbites différentes
	$x_{1}=\tau x_{2}$ pour un $\tau \in S_{5}\setminus A_{5}$, le reste vient tout seul, équation aux classes, on teste toutes les possibilités.
Maintenant, si $n>5$, soit $H \triangleleft A_{n}$ de cardinal >1
$\unicode{x27E6} 1,5 \unicode{x27E7} \overset{i}{\hookrightarrow} \unicode{x27E6} 1,n \unicode{x27E7}$ induit $A_{5}\overset{i'}{\to}A_{n}, \sigma \mapsto i\sigma$
Tel que $(i')^{-1}(H)$ soit de cardinal >1
Puisque $(i')^{-1}(H)\triangleleft A_{5}$ (ou égalité)
Donc $(1,2,3)\in (i')^{-1}(H)$, et $i(1),i(2),i(3)\in H$
Puisque $H \triangleleft A_{n}$, alors les 3-cycles sont dans $H$, et donc $H=A_{n}$
Pour la fin de la preuve TODO
*Corollaire*
	Pour $n\geq5$, les sous-groupes distingués de $S_{n}$ sont $\{ 1 \}, A_{n}, S_{n}$
*Remarque*
	pour $n=3,4$ voir les TD
*Preuve*
	Si $Card(H)\geq2, H\triangleleft S_{n}; H\cap A_{n} \triangleleft A_{n} \begin{cases}H\cap A_n=A_n \begin{cases}H=A_{n}\\ H = S_{n}\end{cases}\\ H\cap A_n = \{ 1 \}\varepsilon\end{cases}$ 
	Dans le deuxième cas, $H=\{ 1,\sigma \}$
	$\forall g \in S_{n}, g \sigma g ^{-1}=\sigma$, $\sigma$ commute à toutes les permutations (impossible il paraît ...)
##### Les automorphismes de $S_{n}$
*Théorème*
	Si $n \neq 6$, les automorphismes de $S_{n}$ sont intérieurs
	i.e. $\forall \varphi \in Aut(S_{n}), \exists g \in S_{n}, \varphi(\sigma)=g \sigma g ^{-1}$
*Proposition*
	$Int(S_{6})\triangleleft Aut(S_{6})$ est un sous groupe d'indice 2
*Lemme*
	$Z(S_{n})=1$ pour $n \geq3$
*Lemme*
	Si $\varphi \in Aut(S_{n})$ transforme une transposition en une transposition, alors $\varphi$ est intérieur.
*Remarque*
	$\varphi$ envoie une classe de conjugaison sur une classe de conjugaison, $\varphi$ établit une bijection entre la classe de conjugaison de $\sigma$ et celle de $\varphi(\sigma)$
*Preuve*
	On note $\tau _i=(1,i)$, on a $\varphi(\tau_{2})=(a_{1},a_{2}), \varphi(\tau_{3})=(a_{1},a_{3})$ (car ils ne commutent pas), $\varphi(\tau_{4})=(a_{1},a_{4})$ ou $(a_{2},a_{3})$ (deuxième cas impossible en fait), on a vite que $\varphi(\tau_{i})=(a_{1},a_{i})$
	On a $a : \begin{cases}\unicode{x27E6}1,n\unicode{x27E7} \to \unicode{x27E6}1,n\unicode{x27E7}\\i \mapsto a_{i}\end{cases}$ est une bijection
	$a\tau_{i}a^{-1}=(a_{1},a_{i})=\varphi(\tau_{i})$
On vient de montrer le lemme, on va montrer le théorème
Si $\tau$ est une transposition, son carré est l'identité, donc $\varphi(\tau)^2=1$ car morphisme.
$\varphi(\tau)$ est un produit de transpositions à support disjoints.
Puisque $\varepsilon \circ \varphi : S_{n} \to \{  \pm 1 \}$ est un morphisme non-trivial, on a $\varepsilon \circ \varphi=\varepsilon$ (par unicité de la signature) et $\varphi(A_{n})=A_{n}$
Si $\varepsilon(\tau)=-1$, alors $\varepsilon(\varphi(\tau))=-1$, donc $\varphi(\tau)$ est un produit d'un nombre impaire de transpositions à support disjoints.
Si $n=$ 4 ou 5, puisqu'on a moins de 6 éléments, il n'existe pas 3 transpositions à support disjoints donc c'est gagné? Avec le lemme, ceci prouve le théorème.
*Lemme*
	Pour $\sigma \in S_{n}$ un produit de $k$ transpositions à support disjoints, et $Z(\sigma)$= les commutants avec $\sigma$
	On a : $$
    \{ 1 \} \to  (\mathbb{Z} /2\mathbb{Z})^k \overset{\triangleleft }{\to } Z(\sigma) \to S_{k} \times S_{n-2k} \to  \{ 1 \}
    $$
*Preuve*
	$\sigma=(a_{1},a_{2})(a_{3},a_{4})\dots(a_{2k-1},a_{2k})=\tau_{1},\tau_{2}\dots \tau_{k}$
	$\tau_{i}\in Z(\sigma)$ engendrent un $N\simeq (\mathbb{Z} /2\mathbb{Z})^k$
	$\forall \tau \in Z(\sigma), \tau \sigma \tau ^{-1}=\sigma$
	truc que j'ai pas écrit TODO
	Et donc $\tau N\tau ^{-1} \subset N$
Fin de la preuve du théorème : 
FIN PAGE 11 PDF VIM
___
___
___
___
___
RECUPERER LE RESTE SUR LE PDF DE VIM
___
___
___
___
___
PAGE 16 VIM

##### Un $p$-Sylow pour $GL_{n}(\mathbb{F}_{p})$, $p$ premier
*Définition* [[p-Sylow]]
	Si $G$ est un groupe de cardinal $p^{\alpha}m$ avec $pgcd(p,m)=1$, un $p$-Sylow $H<G$ est un sous groupe d'ordre $p^{\alpha}$
*Remarque*
	Un $p$-Sylow est toujours résoluble.
*Lemme*
	Dans $GL_{n}(\mathbb{F}_{p})$, le sous-groupe $U$ des triangulaires supérieures à diagonales unitaire (c'est le radical unipotent) est un $p$-Sylow
$Card(U)=p\times p^2\times p^3\times\dots \times p^{n-1}$
Et $Card(GL_{n}(\mathbb{F}_{p}))=(p^n-1)(p^n-p)(p^n-p^2)\dots(p^n-p^{n-1})=(p^n-1)(p^{n-1}-1)(p^{n-2}-1)\dots(p-1)pp^{2n-1}$
Ce qui prouve le lemme (AH!)
*Lemme*
	Soit $G$ un groupe, $Card(G)=p^{\alpha}m$,  conditions usuelles sur $(p,m)$
	Si $S<G$ est un $p$-Sylow et $H<G$ un sous-groupe
	Alors il existe $a \in G$ tel que $aSa^{-1} \cap H$ est un $p$-Sylow de $H$ TODO(pas $G$ ?)
	On rappelle que les $p$-Sylow sont conjugués.
*Preuve*
	G$ agit sur $G/S$ par translation à gauche
	Le stabilisateur de $aS$ est $aSa^{-1}$
	Donc $H$ agit sur $G / S$ par restriction de l'action
	Le stabilisateur de $aS$ est $aSa^{-1}\cap H$
	L'orbite de $a$ est en bijection avec $H /(aSa^{-1}\cap H)$
	On cherche $a$ tel que le cardinal de ce quotient ne soit pas divisible par $p$
	Les orbites forment une partition de $G /S$
	Si elles ont toutes un cardial divisible par $p$, alors $Card(G /S)$ est divisible par $p$ aussi (par somme)
	La contraposée donne : il existe une orbite dont le cardinal est premier $p$
	Un $a$ dans cette orbite convient.
*Théorème*
	Tout groupe fini de cardinal $p^{\alpha}m$ a un $p$-Sylow
*Preuve*
	On construit $\varphi : G \to GL_{n}(\mathbb{F}_{p})$ morphisme injectif
	Les $2$ lemmes prouvent le théorème
	$G \to S_{G}\simeq S_{n} \longrightarrow GL_{n}(\mathbb{F}_{p})$
	$$
    g \mapsto 
    L_{g} : \begin{cases}
    G \to  G \\
    h \mapsto gh
    \end{cases}
    $$
    donne une numérotation de $G$
    La longue flèche (la dernière) fait $\sigma \mapsto M\sigma$ où $M$ est une matrice de permutation.
    $\varphi$ est la composée de tout le monde.
# Les droites projectives
"La" droite projective
**But**
$PSL_{2}(\mathbb{F}_{2,3})$ ne sont pas simples
$PSL_{2}(\mathbb{F}_{5})$ pour construire $\varphi \in Aut(S_{6})\setminus Int(S_{6})$
$PSL_{2}(\mathbb{C})$ et ses sous-groupes finis = les sous-groupes finis de $SO(3)=$ solides platoniciens polyèdre réguliers.
*Références* : 
M.Audin (RIP) "Géométrie" 1 chapitre : "Géométrie projective"
Jones Singermann : complex functions an alg geom viewpoint

$k$ un corps, $E$ un $k$-ev de dim $2$
### Généralités
*Définition*
	On note $\mathbb{P}(E)$ l'ensemble des droites vectorielles de $E$
*Notation*
	Si $E=k^2$
	$\mathbb{P}(k^2)=\mathbb{P}'(k)=\mathbb{P}_{1}(k)=k\mathbb{P}'$
*Lemme*
	L'application $\pi : \begin{cases}E \setminus \{ 0 \} \to \mathbb{P}(E)\\x \mapsto <x>\end{cases}$ est le quotient de l'action de $k^{\times}=Z(GL(E))$ sur $E\setminus \{ 0 \}$
*Preuve*
	$k\times E\setminus \{ 0 \} \to E\setminus \{  0 \}$
	$(\lambda,x) \mapsto \lambda x$
	L'orbite de $x$ est $<x>\setminus \{ 0 \}$
	$\pi(x)=\pi(y) \iff <x> = <y>$
	$\mathbb{P}(E)=(E\setminus \{ 0 \}) / \sim$
	où $x \sim y \iff x$ colinéaire à $y$
Si $E=k^2$ (choix de coordonnées linéaires)
DESSIN TODO (récupérer)
*Lemme*
	La pense d'une droite de $k^2$ donne une bijection de $\mathbb{P}^1(k)\simeq k \cup \infty$ 
*Preuve* TODO
*Définition* Coordonnée homogène
La coordonnée homogène de la droite $<(x_{1},x_{2})>$ est le ratio $[x_{1},x_{2}]=[\lambda x_{1}:\lambda x_{2}]$
On dit que $(x_{0},x_{1},\dots,x_{n})$ et $(y_{0},y_{1},\dots,y_{n})$ définissent le même ratio si $\begin{pmatrix}x\\y\end{pmatrix}$ est un tableau de proportionnalité ($\iff$ les deux vecteurs sont colinéaires)
Le groupe $GL_{2}(k)$ agit sur $\mathbb{P}^1(k)$ par $(u,<x>)\mapsto <u(x)>$
On a un morphisme $GL_{2}(k)\to S(\mathbb{P}^1(k))$
*Lemme*
	$Ker(a)=$ le groupe des homothéties $=Z(GL_{2}(k))$
En particulier, $\mathrm{Im}(a)\simeq PGL_{2}(k)$
Le groupe des homographies $=\mathrm{Im}(a)$
*En coordonnées homogènes* :
	$u \in GL_{2}(k)$ on note $[u]$ son image dans $PGL_{2}(k)$
	$u : k^2 \to k^2$ de matrice $\begin{pmatrix}a&b\\c&d\end{pmatrix}$ de det non nul
	$[u]([x_{1}:x_{2}])=[ax_{1}+bx_{2}:cx_{1}+dx_{2}]$
	$[u]([z:1])=\left[ \frac{az+b}{cz+d}:1 \right]$ si $x_{2} \neq_{0}$
	$[u]([1:0]=\infty)=[a:c]=\left[ \frac{a}{c}:1 \right]$
	$[u]\left( \left[ -\frac{d}{c}:1 \right] \right)=\infty$
*Définition* [[Homographie]]
	Une homographie est un truc comme ça : 
	$h:z \mapsto \frac{az+b}{cz+d}$, avec $h\left( -\frac{d}{c}\right)= \infty$ et $h(\infty)=\frac{a}{c}$
	Et ça définit une bijection de $k \cup \infty$ sur lui-même. 
*Remarque*
	homographie = "fractionnal linear map"
*Exercice* TODO
	Soit $h$ une homographie, $h$ est une bijection, les homographies forment un groupe $h$ a $0,1$ ou $2$ points fixes, sinon c'est l'identité.
*Lemme*
	L'action de $PGL_{2}(k)$ sur $\mathbb{P}^1(k)$ est $3$-transitive.
*Preuve*
	On prend $3$ droites distinctes de $k^2$ (ou $3$ points de $\mathbb{P}^1(k)$)
	$<e_{1}>,<e_{2}>,<e_{3}>$
	Quitte à changer $e_{1},e_{2}$ on peut supposer $<e_{3}> = <e_{1}+e_{2}>$ (sans changer les droites)
	On prend un autre triplet de droites distinctes : $<f_{1}>,<f_{2}>,<f_{1}+f_{2}>$
	$u:k^2 \to k^2$ définit par $u(e_{1})=f_{1}, u(e_{2})=f_{2}$ fournit l'homographie $[u]$ qui envoie $<e_{i}>$ sur $<f_{i}>$
##### Birapport
*Lemme*
	Si $a,b,c$ sont trois points de $\mathbb{P}^1(k)$, il existe une unique homographie $h$ tel que : $h(a)=\infty, h(b)=h(c)=0$ TODO(vérifier)
	En coordonnées homogènes : $\lambda=[\lambda:1], h(z)=\frac{z-b}{z-a}\times \frac{c-a}{c-b}$
*Définition*
	Avec les notations du lemme, si $d \in \mathbb{P}^1(k)$, on note $bir(a,b,c,d)=h(d)$
*Théorème* (Exo 1, feuille 3)
	$\varphi : \mathbb{P}^1(k)\to \mathbb{P}^1(k)$ une bijection
	Est une homographie $\iff$ $\varphi$ préserve les biraports
	Et, $\forall(a,b,c,d) \in (\mathbb{P}^1(k))^4$ distincts, $bir(\varphi(a),\varphi(b),\varphi(c),\varphi(d))=bir(a,b,c,d) \in k\setminus \{ 0,1 \} \iff \varphi \in PGL_{2}(k)$
	Problème si $k=\mathbb{F}_{2}$
##### Sur un corps fini
$k=\mathbb{F}_{q}$, on a $q+1$ droites
Donc $PGL_{2}(k)\hookrightarrow S_{q+1}$
Ici, il y a un truc bizarre que j'ai la flemme de noter (ntm pour les révision), ça parle de "nombreux isomorphismes exceptionnels"

*Proposition*
	1) $PGL_{2}(\mathbb{F}_{2})\simeq S_{3}$ (isomorphisme exceptionnel)
	2) $PSL_{2}(\mathbb{F}_{2})\simeq SL_{2}(\mathbb{F}_{2})\simeq GL_{2}(\mathbb{F}_{2})\simeq PGL_{2}(\mathbb{F}_{2})$
	3) $PGL_{2}(\mathbb{F}_{3})\simeq S_{4}$
	4) $PSL_{2}(\mathbb{F}_{3})\simeq A_{4}$ (en particulier, il n'est pas simple)
*Preuve*
	TODO
*Propriété*
	$PGL_{2}(\mathbb{F}_{5})\simeq S_{5}$ 
*Remarque*
	On a un morphisme injectif de $PGL_{2}(\mathbb{F}_{5})\hookrightarrow S_{6}$ et le premier est un sous groupe d'indice 6 du deuxième. 
	Et tout sous-groupe d'indice $n$ de $S_{n}$ est isomorphe à $S_{n-1}$
*Corollaire*
	Il existe $\varphi \in Aut(S_{6})$ qui n'est pas intérieur.
TODO Barisme de Steiner
# Géométrie affine
Euclide a fait des axiomes...
Hilbert axiomes de la géométrie plane Euclidienne : ASRAC
Au 19ème siècle, on introduit les vecteurs
Groupes F.Klein
$k$ un corps (commutatif)
##### Généralités
*Rappel* [[Action de groupe|Action simplement transitive]]
	Une action d'un groupe $G$ sur un ensemble $X$ est simplement transitive si : 
	$$
    \begin{cases}
    G \times X \to  X \times X \\
    (g,x) \mapsto (g \cdot x,x)
    \end{cases}
    $$
    est une bijection.
    C'est équivalent à : $\forall (x,y) \in X^2, \exists! g \in G, g \cdot x=y$
*Définition*
	Un espace affine sur $k$, $E$, est un ensemble muni d'une action simplement transitive d'un $k$-ev $\overrightarrow{E}$ $$
    t: \begin{cases}
    \overrightarrow{E}\times E \to  E \\
    (\overrightarrow{v},p) \mapsto t_{\overrightarrow{v}}(p) \text{ ou } p+\overrightarrow{v}
    \end{cases}
    $$
	Action de groupe : $(p+\overrightarrow{v})+\overrightarrow{w}=p+(\overrightarrow{v}+\overrightarrow{w})$
*Vocabulaire*
	$\overrightarrow{E}$ les directions de $E$
	$dim_{k}(E)=dim_{k}(\overrightarrow{E})$
	si $\overrightarrow{v} \in \overrightarrow{E}, t_{\overrightarrow{v}}:E \to E$ une translation
*Définition* (autre possibilité)
	Muni de $$
\begin{cases}
E\times E \to  \overrightarrow{E} \\
(A,B)\mapsto \overrightarrow{AB}
\end{cases}
$$Vérifiant : la relation de Chasles, et, $\forall A \in E$, la fonction qui à $B$ associe le vecteur $\overrightarrow{AB}$ est une bijection.
	Les deux définitions sont équivalentes. 
	Preuve sur le cours d'erell, donné à gAymeric (TODO)
*Remarque*
	Si $E_{1},E_{2}$ sont des espaces affines de directions $\overrightarrow{E_{1}},\overrightarrow{E_{2}}$, alors $E_{1}\times E_{2}$ est affine de direction $\overrightarrow{E_{1}}\times \overrightarrow{E_{2}}$
*Propriété*
	Si $(P,Q,P',Q')\in E^4, E$ espace affine : 
	- $\overrightarrow{PP}=\overrightarrow{0}$
	- $\overrightarrow{PQ}=-\overrightarrow{QP}$
	- $\overrightarrow{PQ}=\overrightarrow{P'Q'} \iff \overrightarrow{PP'}=\overrightarrow{QQ'}$
	- $PQQ'P'$ est un parallélogramme
##### Sous-espace affine
*Définition* Sous-espace affine
	Un sous-espace affine (sea) $F \subset E$ est une orbite d'un sev $\overrightarrow{F}\subset \overrightarrow{E}$
*Remarque*
	Un sous-espace affine $F$, orbite de $\overrightarrow{F}\subset \overrightarrow{E}$ est un espace affine de direction $\overrightarrow{F}$
*Remarque*
	Si $p \in E, \overrightarrow{V}\subset \overrightarrow{E}$ un sev
	Il existe un unique espace affine $F \subset E$ tel que $$
\begin{cases}
p \in  F \\
\overrightarrow{F}=V
\end{cases}
$$$F=Orb_{V}(p)$ où l'action est la restriction de celle de $\overrightarrow{E}$
	Deux sous-espaces affines de même direction sont confondus ou disjoints.
*Vocabulaire*
	$F \subset E$ un sea : 
	- $dim(F)=1$ droite affine
	- $dim(F)=2$ plan affine
	- $dim(F)=dim(E)-1$ hyperplan
*Exercice* 
	Par $2$ points distincts, passe une unique droite
*Lemme*
	Soit $\overrightarrow{u}:\overrightarrow{E}\to \overrightarrow{F}$ une application linéaire et $\overrightarrow{x}\in \overrightarrow{F}$
	Alors $G=\overrightarrow{u}^{-1}(\overrightarrow{x})\subset \overrightarrow{E}$ est un sea de direction $\overrightarrow{G}=Ker(\overrightarrow{u})$
**Cas particulier important :**
$\overrightarrow{E}$ un $k$-ev, $E=\overrightarrow{E}\times \{ 1 \}\subset \overrightarrow{E}\oplus k$ est un espace affine de direction $\overrightarrow{E}$
*Lemme*
	Une intersection non vide de sea est un sea 
	Et $\overrightarrow{\cap_{i}F_{i}}=\cap_{i}\overrightarrow{F_{i}}$
*Définition*
	$2$ sea $F_{1},F_{2}$ de $E$ sont : 
	- Parallèles si $\overrightarrow{F_{1}}\subset \overrightarrow{F_{2}}$ (ou dans l'autre sens)
	- Fortement parallèles si c'est une égalité.
*Remarque*
	Si deux sea parallèles s'intersectent, alors l'un est inclus dans l'autre.
*Preuve*
	Si $F_{1},F_{2}$ sont parallèles, $\overrightarrow{F_{1}}\subset \overrightarrow{F_{2}}$, on prend $p \in F_{1} \cap F_{2}$, alors $Orb_{\overrightarrow{F_{1}}}(p)\subset Orb_{\overrightarrow{F_{2}}}(p)$
*Remarque*
	Soit $F,G$ deux sea de $E$, tels que $\overrightarrow{F} \oplus\overrightarrow{G}=\overrightarrow{E}$
	Alors $Card(F \cap G = 1)$
*Preuve*
	Soit $A \in F, B \in G$
	$\overrightarrow{AB}=e_{1}-e_{2}$ respectivement dans $\overrightarrow{F},\overrightarrow{G}$
	On regarde $A+e_{1}\in \overrightarrow{F}$ et TODO (finir, j'ai pas noté la fin)
##### Applications affines
*Définition*
	$f:E \to F$ une application entre deux espaces affines, est affine si il existe $\overrightarrow{f}:\overrightarrow{E} \to \overrightarrow{F}$, telle que $\forall(P,Q) \in E^2, \overrightarrow{f(P)f(Q)}=\overrightarrow{f}(\overrightarrow{PQ})$ 
	$\overrightarrow{f}$ est la direction de $f$
	ou encore, un certain diagramme commutatif (le récup sur quelqu'un d'autre TODO)
	Ca marche bien avec la def qu'on connait.
*Lemme*
	- La composée de $2$ applications affines est une application affine et $\overrightarrow{f \circ g}=\overrightarrow{f} \circ \overrightarrow{g}$
	- L'image d'un sea par une application affine est un sea
	- La pré-image aussi (ou est vide)
*Théorème* [[Théorème de Thalès|Thalès]]

Soient $f:E \to F$ affine de direction (ou partie linéaire) $\vec{f}:\vec{E}\to \vec{F}$ et $g:F\to G$ pareil $\vec{g}:\vec{F}\to \vec{G}$
Montrons que $g\circ f$ est affine :
	Soit $(P,Q)\in E^2$ 
	On a $\vec{g\circ f(P)g\circ f(Q)}=\vec{g}(\vec{f(P)f(Q)})=\vec{g}\circ \vec{f}(\vec{PQ})$
	Ainsi, $g\circ f$ est affine et $\vec{g\circ f}=\vec{g}\circ \vec{f}$
	Si $f:E\to F$ est affine, et $E_{1} \subset E$ est un s.e.a.
	Le candidat pour être l'ev des directions de $f(E_{1})$ est $\vec{f}(\vec{E_{1}})\subset\vec{F}$
	Si $A\in F(E_{1})$ et $\vec{v}\in \vec{f}(\vec{E_{1}})$ on va montrer que $A+\vec{v}\in f(E_{1})$
		Il existe $P\in E_{1}$ tel que $f(P)=A$ et $\vec{w}\in \vec{E_{1}}$ tel que $\vec{f}(\vec{w})=\vec{v}$
		On sait que $P+\vec{w}\in E_{1}$ d'où $f(P+\vec{w})\in f(E_{1})$
		Et $\vec{f(P+\vec{w})f(P)}=\vec{f}(\vec{P+\vec{w}P})=\vec{f}(\vec{w})$ 
		**(((Y'a une erreur de signe avec les $\vec{w}$ mais oklm)))**
		Donc $f(P+\vec{w})=f(P)+\vec{f}(\vec{w})=A+\vec{v}$
		De plus $\vec{f(E_{1})}=\vec{f}(\vec{E_{1}})$
	$f:E\to F$ affine $F_{1}\subset F$ sea
	On veut montrer que $f^{-1}(F_{1})$ est un sea
		Soient $(P,Q)\in f^{-1}(F_{1})$
		$\iff f(P)\in F_{1}$ et $f(Q)\in F_{1}$
		$\iff f(P)\in F_{1}$ et $\vec{f(P)f(Q)}\in \vec{F_{1}}$
		$\iff f(P)\in F_{1}$ et $\vec{f}(\vec{PQ})\in \vec{F_{1}}$
		$\iff P\in f^{-1}(F_{1})$ et $\vec{PQ}\in(\vec{f})^{-1}(\vec{F_{1}})$
		Donc $F_{1}$ est affine de direction $(\vec{f})^{-1}(\vec{F_{1}})$
*Exercice*
	$f:E\to F$ une application entre 2 espaces affines.
	($f$ est affine) $\iff$ (Le graphe de $f$ sous ensemble de $E\times F$ est un sous espace affine)
## Le groupe affine
*Proposition* E un [[Espace affine]]
	1) Les bijections affines de $E$ dans $E$ forment un groupe : $GA(E)$
	2) L'application $GA(E)\to GL(E)$ qui $f \mapsto \vec{f}$ est un morphisme de groupe surjectif
	3) Le noyau de ce morphisme est le sous groupe des translations
*Preuve* 
	On a déjà vu la stabilité par composition.
	On doit donc voir que $f^{-1}$ est affine.
	Soit $(P,Q)\in E$ on regarde $\vec{f}\left(\vec{f^{-1}(P)f^{-1}(Q)}\right)=\vec{f(f^{-1}(P))f(f^{-1}(Q))}=\vec{PQ}$
	On en déduit que $\vec{f^{-1}(P)f^{-1}(Q)}=(\vec{f})^{-1}(\vec{PQ})$
	Ceci si on sait que $\vec{f}$ est inversible :
		si $\exists \vec{AB}\in \vec{E}$ tel que
		$\vec{f}(\vec{AB})=0$
		$\vec{\iff}f(A)f(B)=0$
		$\iff f(A)=f(B)$
		$\iff A=B \iff \vec{AB}=0$
		(injectivité de $f$)
		On a de plus $\vec{f^{-1}}=\vec{f}^{-1}$
	Surjectivité : 
		Fixons $A\in E$ et $\vec{u}\in GL(\vec{E})$
		$E\overset{\varphi}{\to}\vec{E}\overset{\vec{u}}{\to}\vec{E}\overset{\varphi ^{-1}}{\to}E$
		$B\to \vec{AB}$       $\vec{v}\mapsto A+\vec{v}=t_{\vec{v}}(A)$
		On va montrer que $\varphi$ est affine de direction $\vec{\varphi}=Id$
		Calculons : 
			$$\begin{align}
            \vec{\varphi}(\vec{B_{1}B_{2}})&=\vec{\varphi(B_{1})\varphi(B_{2})}\\
			& =\vec{\vec{AB_{1}}\vec{AB_{2}}} \\
            & = \vec{AB_{2}}-\vec{AB_{1}} \\
            &\vec{B_{2}B_{1}}
            \end{align}$$
        $\vec{u}:\vec{E}\to \vec{E}$ est affine de partie linéaire $\vec{u}$
        Posons $g=\varphi\circ \vec{u}\circ \varphi ^{-1}$
        $g$ est affine et linéaire
        $\vec{g}=\vec{\varphi}\circ \vec{u}\circ \vec{\varphi ^{-1}}=\vec{u}$
    Noyau : 
	    Soit $f:E\to E$ de partie linéaire $\vec{f}=Id$
	    Soit $(P,Q)\in E^2$ 
	    $\vec{f(P)f(Q)}=\vec{PQ}$
	    $\vec{Pf(P)}=\vec{Qf(Q)}$ (parallélogramme)
	    je note ce vecteur $\vec{v}$
	    $\forall P\in E, f(P)=t_{\vec{v}}(P)$
On a donc une suite exacte : 
$$
\begin{align}
0\to & \vec{E}\overset{t}{\to} GA(E)\overset{\pi}{\twoheadrightarrow}GL(\vec{E})\to 0 \\
& \vec{v\mapsto t_{\vec{v}}} & \\
& \quad \quad f\mapsto \vec{f}
\end{align}
$$
*Proposition*
	Il existe $\Theta : GL(\vec{E})\to GA(E)$ telle que
	$\pi\circ \Theta=Id$ sur $GL(\vec{E})$
	On aura $t(\vec{t})\Theta(GL(\vec{E}))=GA(E)$
	On note $GA(E)=\vec{E}\rtimes GL(\vec{E})$ le produit semi-direct
*Preuve*
	On fixe $A\in E$ et $\varphi :  E\to \vec{E}$ qui $B \mapsto \vec{AB}$
	$\Theta(\vec{u})=\varphi ^{-1}\circ \vec{u}\circ \varphi$
	Si $f\in GA(E)$, on pose $\vec{v}=\vec{Af(A)}$
	$t_{-v}\circ f$ est affine $t_{-v}(f(A))=A$
	En utilisant le lemme d'après : 
	$f_{-v}\circ f\in \Theta(GL(\vec{E}))$
	$\exists \vec{u}\in GL(\vec{E})$ tel que $f=t_{v}\circ \Theta(u)$
	*Lemme*
		Soit $A\in E$
		$Stab(A)=\{ f:E\to E \text{ affine telle que } f(A)=A \}$
		alors $Stab(A)\overset{d}{\to}GL(\vec{E})$ qui $f\mapsto \vec{f}$
		est un isomorphisme de groupe
	*Preuve*
		$Stab(A)$ est un groupe et $d$ est un morphisme de groupe
		$d$ est injective car $Stab(A)$ ne contient pas de translations non-triviale
		si $\vec{u}\in GL(E)$ alors $\varphi ^{-1} \circ \vec{u}\circ \varphi\in Stab(A)$
		$\varphi ^{-1}\circ \vec{u}\circ \varphi(A)=\varphi ^{-1}\circ \vec{u}(0)=u^{-1}(0)=A$
		Et $\vec{\varphi ^{-1}\circ \vec{u}\circ \varphi}=\vec{u}$
		si $k=\mathbb{R}$ :
		$\vec{f}=df$ qui ne dépend pas du point en lequel vous dérivez
		$\Theta(df)="A+\int_{A}df"$
### Le groupe des homothéties-Translations
*Définition* [[Homothétie]] 
	Une application $h:E\to E$, $E$ un espace affine, est une homothétie si $\vec{h}\in Z(GL(\vec{E}))$ est une homothétie vect
	et $h$ fixe un point $\Omega$
	$\Omega$ est le centre de l'homothétie
	$\vec{h}=\lambda Id$ $\lambda$ est le rapport de l'homothétie et on note $h_{\Omega,\lambda}$
*Remarque* Les homothéties ne forment (pas ?) un groupe
	$h_{\Omega_{1},\lambda}\circ h_{\Omega_{2},\lambda}=t_{\lambda \vec{\Omega_{1}\Omega_{2}}}$
*Exercice*
	$k=\mathbb{R}$ donnez une suite d'homothéties
	$h_{\Omega_{n},\lambda_{n}}\to t_{\vec{v}}$ uniformément sur tout compact
*Définition* 
	Le groupe des homothéties-translations est :
	$$
    \begin{align}
    HT & =\pi ^{-1}(Z(GL(\vec{E}))) \\
    & =\{ f \text{ tel que } \vec{f} \text{ est une homothétie}\}
    \end{align}
    $$
*Lemme*
	Un élément de $HT$ est soit une homothétie soit une translation
*Preuve*
	PHOTO 7 NOVEMBRE à 9h26
Remarque photo suivante
### Le groupe des homothéties-translations
$f:E \to E$ affine est une homothétie affine ou une ranslation 
$\iff$
a pour partie linéaire $\overrightarrow{f}$ une homothétie vectorielle
*Lemme*
	Si $f : E \to E$ est une homothétie affine ou une translation, alors $\forall F \subset E$ sea, $f(F)$ (fortement) parallèle à $F$
*Preuve*
	On a $\overrightarrow{f(F)}=\overrightarrow{f}(\overrightarrow{F})=\overrightarrow{F}$ car $\overrightarrow{f}$ est une homothétie.
*Lemme*
	$f: E \to E$ est une bijection affine et $\forall D$ droite affine de $E$, $f(D)$ est (fortement) parallèle à $D$, alors $f$ est une homothétie ou une translation
*Preuve*
	$\forall \overrightarrow{D}, \overrightarrow{f}(\overrightarrow{D})=\overrightarrow{D}$, ce qui implique que $\overrightarrow{f}$ est une homothétie.
**Thalès affine**
	Deux droites $(BC)$ et $(B'C')$ sécantes en $A$
	$(B'B)//(CC') \iff \frac{\overline{AB'}}{\overline{AC'}}=\frac{\overline{AB}}{\overline{AC}}$
	$\iff \overrightarrow{AB} \text{ et } \overrightarrow{AC}$ sont colinéaires
	$h_{\Omega,\lambda}$ est une homothétie 
	$\overrightarrow{h_{\Omega,\lambda}(A)h_{\Omega,\lambda}(B)}=\lambda \overrightarrow{AB}$
*Preuve*
	$\sigma_{1}$ l'homothétie de centre $A$ telle que $\sigma_{1}(C)=B$ i.e. de rapport $\frac{\overline{AB}}{\overline{AC}}$
	$\sigma_{2}$ pareil avec $\sigma_{\Omega}(C')=B'$
	$\impliedby$ :  si les rapport sont égaux, $\sigma_{1}=\sigma_{2}$
	$\sigma_{1}(CC')$ est parallèle à $(CC')$
	$=(\sigma_{1}(C)\sigma_{1}(C'))$
	$=\sigma_{1}(C)\sigma_{2}(C')$
	$=(BB')$
	$\implies$ : si $(BB')//(CC')$, alors $\sigma_{1}(CC')$ est parallèle à $(CC')$ et contient $\sigma_{1}(C)=B$
	C'est $(BB')$
	$\sigma_{1}(C') \in (BB') \cap (AB')=\{ B' \}$
	Ainsi, le support de $\sigma_{1}$ est $\frac{\overline{AB'}}{\overline{AC'}}=\frac{\overline{AB}}{\overline{AC}}$
**Pappus affine**
	Si $ABC$ alignés et $A'B'C'$ alignés de sorte que $(AB)$ et $(A'B')$ soient sécantes en $\Omega$ (différents des autres points) et $(AB')//(BA')$ et $(BC')//(B'C)$
	Alors : $(AC')//(A'C)$
*Preuve*
	Soient $\sigma_{1}$ l'homothétie de centre $\Omega$ qui envoie $A$ sur $B$
	$\sigma_{2}$ pareil qui envoie $B$ sur $C$
	$\sigma_{1}(AB')=(BA')$, donc $\sigma_{1}(B') \in (BA') \cap A'B=\{ A' \}$
	de même, $\sigma_{2} \dots \sigma_{2}(C')=B'$
	On a $\sigma_{2} \circ \sigma_{1}(A)=C$ et $\sigma_{1}\circ\sigma_{2}(C')=A'$
	Deux homothéties de même centre commutent : $\sigma_{1} \circ \sigma_{2}=\sigma_{2}\circ \sigma_{1}=h$
	Ainsi $h(AC')=(A'C)$ et $(AC') / /(A'C)$
**Desargues affine**
	Soient 3 droites $(AA'), (BB'), (CC')$ distinctes telles que $(AC) / /(A'C')$ et $(AB) / /(A'B')$
	Alors les 3 droites sont concourantes ssi $(BC) / /(B'C')$
*Preuve*
	$\implies$ $\sigma$ l'homothétie de centre $\Omega$ qui envoie $A$ sur $A'$
	donc $C$ sur $C'$ et $B$ sur $B'$
	$\sigma(BC)$ sur $(B'C')$ et $(BC) / /(B'C')$
	$\impliedby$ $\Omega=(AA')\cap(BB')$
	$\sigma$ l'homothétie de centre $\Omega$ qui envoie $A$ sur $A'$
	- $\sigma(B)=B'$
	$\sigma(BC)=(B'\sigma(C))=(B'C')$ est parallèle à $(BC)$ contient $B$
	$\sigma(AC)=(A'\sigma(C))=(A'C')$
	$\sigma(C)=(BC')\cap(AC')=C'$
	$\overrightarrow{\Omega C}$ et $\overrightarrow{\Omega C'}$ sont colinéaires
**Théorème de 3b1b avec les 3 cercles**
(Théorème de Monge)
*Remarque*
	Si $E$ espace affine de direction $\overrightarrow{E}$ et $A \in E$
	$E \to \overrightarrow{E} \oplus k$ image $\overrightarrow{E}\times \{ 1 \}$
	$B \mapsto (\overrightarrow{AB},1)$
	Identifie $E$ à $\overrightarrow{E}\times \{ 1 \}$ de partie linéaire $Id:\overrightarrow{E} \to \overrightarrow{E}\times \{ 1 \}$
$E$ s'identifie aux droites vect de $\overrightarrow{E}\oplus k$ qui ne sont pas contenues dans $\overrightarrow{E}$
Les droites de $E$ correspondent à des plans vect de $\overrightarrow{E}\oplus K$ qui ne sont pas contenues dans $\overrightarrow{E}$
# Un peu de géométrie projective
#### But : 
Thalès projectif
Pappus projectif
Desargues projectif
#### Définitions
$V$ un $k$-ev de dimension $n+1$
*Définition*
	$\mathbb{P}(V)$ est l'ensemble des droites vectorielle de $V$
	$=(V \setminus \{ 0 \} )/\sim$ action des homothéties, les droites colinéaires sont équivalentes.
*Lemme*
	Si on choisit une décomposition $V=\overrightarrow{H}\oplus k$ et on note $H=\overrightarrow{H}\times \{ 1 \}$ on a une injection de $H$ dans $\mathbb{P}(V)$ de complémentaire (voir michel audin) $\mathbb{P}(\overrightarrow{H})$
*Preuve*
	Soit $D \subset V \setminus \overrightarrow{H}$ une droite affine
	$Card(D \cap \overrightarrow{H}\times \{ 1 \})=1$
	Si $\overrightarrow{v}=(\overrightarrow{h},t)\in D$ alors $t \neq 0$ et $\frac{1}{t}\overrightarrow{v} \in H$
*Vocabulaire*
	$H\subset \mathbb{P}(V)$ s'appelle une carte affine
	$\mathbb{P}(\overrightarrow{H})$ est l'hyperplan à l'$\infty$
	$dim(\mathbb{P}(V))=dim(V)-1$ et  $dim(\overrightarrow{H})=dim(H)$
	si $W \subset V, \mathbb{P}(W)\subset \mathbb{P}(V)$ droite si de dim 1, plan si de dim 2, hyperplan si de codim 1
	si $W \subset \mathbb{P}(V)$ on notera $<W>\subset V$ l'ev engendré par $W$ et $\mathbb{P}(W))\mathbb{P}(<W>)\subset \mathbb{P}(V)$
	En particulier, si $x \in \mathbb{P}(V)$, $<x>$ est la droite $x$, $\mathbb{P}(<x>)=x$
*Proposition*
	Si $W_{1}, W_{2}$ deux sev de $V$ tel que $\mathbb{P}(W_{1}), \mathbb{P}(W_{2})$ vérifient que la somme de leur dim dépasse $dim(\mathbb{P}(V))$, alors leur intersection est non vide, et si c'est égal, leur intersection est un point.
	- Deux droites (proj) et un plan (proj) s'intersectent toujours
	- Par 2 points du plan (proj) passe une unique droite (proj)
*Preuve*
	$dim(W_{1})+dim(W_{2})\geqslant dim(\mathbb{P}(V))+2$
	$dim(W_{1})+dim(W_{2})> dim(V)$
	Il existe une droite dans $W_{1}\cap W_{2}$
#### Applications projectives
Si $u:V_{1} \to V_{2}$ linéaire et $D\subset V_{1}$ une droite vectorielle, alors $u(D)$ est soit une droite, soit $\{ 0 \}$
Cette application induit $[u]:\mathbb{P}(V_{1})\setminus \mathbb{P}(ker(u))\to \mathbb{P}(V_{2})$ et qui $D \mapsto u(D)$
*Définition*
	Une application de ce type là est une [[application projective]]
##### Perspective
- $\mathbb{P}(W)$ est un hyperplan de $\mathbb{P}(V)$
- $\Omega$ un point de $\mathbb{P}(C)\setminus \mathbb{P}(W)$
$\pi: \mathbb{P}(V)\setminus \Omega \to \mathbb{P}(W)$ qui $P \mapsto \mathbb{P}(W)\cap(P\Omega)$
est : 
- la projection centrale sur $\mathbb{P}(W)$ de centre $\Omega$
- La perspective sur $\mathbb{P}(W)$ vue de $\Omega$
Le prof a dit "une perspective c'est une projection"
*Lemme*
	Une perspective est une application projective
*Preuve*
	$V=W \oplus <\Omega>$ on note $u:V \to W$ la projection parallèle à $<\Omega>$
	$Ker(u)= < \Omega>$
	si $P \in \mathbb{P}(V)\setminus \{  \Omega \}$ on veut déterminer $[u](P)$ 
	Pour cela, $<P,\Omega>\cap W$ une droite $<\pi(P)>$
	Choisissons $<P>\ni v=u(v)+w\in<\Omega>$ on obtient $<P,\Omega>\ni v-w=u(v)\in W$
	$\implies u(<P>)= < P,\Omega>\cap W$
##### Transformations projectives
L'action de $GL(V)$ sur $\mathbb{P}(V)$ a pour noyau les automorphismes qui préservent chaque droite (laissent chaque droite invariante)
C'est donc un sous-groupe des homothéties vectorielles, qui est aussi le centre $Z(GL(V))$
On obtient une action fidèle de $PGL(V)$ sur $\mathbb{P}(V)$
Autrement dit, $PGL(V)\hookrightarrow S(\mathbb{P}(V))$
On identifiera $PGL(V)$ à son image et les éléments seront appelés des homographies (parfois réservé au cas de dimension 1) ou des transformations projectives.
*Proposition*
	On choisit une décomposition $V=\overrightarrow{H}\oplus k$
	$H\subset \mathbb{P}(V)$ la carte affine de direction $\overrightarrow{H}$, et $\mathbb{P}(V)=H \cup \mathbb{P}(\overrightarrow{H})$
	- Toute transformation projective qui préserve $\mathbb{P}(\overrightarrow{H})$ se restreint en une transformation affine de $H$
	- Toute transformation affine de $H$ est la restriction d'une transformation projective.
*Preuve*
	$H=\overrightarrow{H}\times \{ 1 \}$
	- On prend $u \in GL(V)$ telle que $u(\overrightarrow{H})=\overrightarrow{H}$ 
	On note $f:V \to k$ la projection parallèle à $\overrightarrow{H}$
	Puisque $f \circ u$ a le même noyau que $u$, il existe $\lambda \in k ^{\times}$ tel que $f \circ u=\lambda f$
	$f\left( \frac{1}{\lambda}u \right)=f$ 
	Puisque $[u]=\left[ \frac{1}{\lambda}u \right]$
	On peut supposer que $u(H)=H$
	On regarde $u|_{H}:H \to H$ 
	$\overrightarrow{u}|_{H}: \overrightarrow{H} \to \overrightarrow{H}$ définit par $\overrightarrow{u}|_{H}(B-A)=u|_{H}(B)-u|_{H}(A)=u|_{\overrightarrow{H}}(B-A)$
	$\overrightarrow{u}|_{H}$ est linéaire car égale à $u|_{\overrightarrow{H}}$
	$u$ est affine
	- $g: H \to H$ affine de direction $\overrightarrow{g}:\overrightarrow{H} \to \overrightarrow{H}$
	$g(0,1)=(b,1)$
	$u:\overrightarrow{H}\oplus k\to \overrightarrow{H}\oplus k$ qui $(h,t)\mapsto (\overrightarrow{g}(h)+bt,t)$
	vérifie $[u]|_{H}=g$
	$u(h,1)\mapsto \overrightarrow{g}(h)+b,1$
	$[u]|_{H}$ est affine par la preuve de juste avant et sa partie linéaire est $\overrightarrow{[u]}|_{H}=u|_{\overrightarrow{H}}=\overrightarrow{g}$
	Puisque $[u]|_{H}(0,1)=(b,1)=g(0,1)$
	$[u]|_{H}\circ g ^{-1}$ fixe un point et a une partie linéaire égale à $Id$, c'est l'identité.
##### Les 3 théorèmes
Dans un plan projectif $\mathbb{P}^2(k)$ (le 2 est la dimension, pas une puissance cartésienne)
Soit 4 droites $d_{1},d_{2},d_{3},d_{4}$ concourantes en $\Omega$ et 2 droites $\Delta_{1}, \Delta_{2}$ ne contenant pas $\Omega$
Si $A,B,C,D$ sont les intersections de $\Delta_{1}$ avec $d_{1},d_{2},d_{3},d_{4}$ et $A',B',C',D'$ les intersections de $\Delta_{2}$ avec $d_{1},d_{2},d_{3},d_{4}$
Alors $\frac{\overline{BD}}{\overline{AD}} \times \frac{\overline{AC}}{\overline{BC}}=\frac{\overline{B'D'}}{\overline{A'D'}} \times \frac{\overline{A'C'}}{\overline{B'C'}}$
$(A=A')$
*Preuve*
	On va choisir une bonne carte affine :
	le complémentaire de $d_{4}$
	*Dessins de merde go pas noter* (les apprendre dans le doute)
	$V=<d_{4}>\oplus ke_{1}$
	**Thalès affine**
		$\frac{\overline{AC}}{\overline{BC}} = \frac{\overline{A'C}}{\overline{B'C}}$
	$\pi$ la perspective de centre $\Omega$ d'image $\Delta_{2}$
	$\pi:\mathbb{P}(V)\setminus \Omega \to \Delta_{2}$
	$\pi|_{\Delta_{1}}:\Delta_{1}\to \Delta_{2}$ est une homographie d'une droite projective sur une autre droite projective
	Les homographies préservent les birapports $bir(A,B,C,D)=bir(A';B';C';D')$
	Si on choisit une coordonnée homogène sur $\Delta_{1}$, $A=[a:1], B=[b:1], C=[c:1], D=[d:1]$
	$bir(A,B,C,D)=\left( \frac{d-b}{d-a}\times\frac{c-a}{c-b} \right)=\frac{\overline{BD}}{\overline{AD}} \times \frac{\overline{AC}}{\overline{BC}}$
	Si on choisit des coordonnées homogènes tel que $D=[1:0]=\infty$
	$bir\left( A,B,C,D\right)=\frac{c-a}{c-b}= \frac{\overline{AC}}{\overline{AB}}$
	**Pappus projectif**
	$d_{1},d_{2}$ deux droites sécantes en $\Omega$ et $A,B,C$ trois points distincts et distincts de $\Omega$ sur $d_{1}$
	$A',B',C'$ pareil sur $d_{2}$
	$\Omega_{1}=(AB')\cap(A'B), \Omega_{2}=(AC')\cap (A'C), \Omega_{3}=(BC')\cap(B'C)$ sont alignés
	*Preuve*
		On choisit comme "droite à l'infini" la droite $(\Omega_{1},\Omega_{2})$
		Dans la carte affine correspondante $(AB') / /(A'B)$ et $(A'C) / / (AC')$
		Donc Pappus affine donne $(B'C) / /(BC')$
		C'est-à-dire que leur point d'intersection projectif est sur $(\Omega_{1},\Omega_{2})$
	**Desargues projectif**
	 On note $\Omega_{1}=(AB)\cap(A'B'), \Omega_{2}=(AC)\cap(A'C'), \Omega_{3}=(BC)\cap(B'C')$
	 On prend comme droite à l'infini $(\Omega_{1}, \Omega_{2})$
	 et on obtient l'énoncé de Desargues affine
	 Et donc le parallélisme de $(BC')$ et $(B'C)$ est équivalent à la concourrance des 3 droites
	 $\Omega_{3} \in(\Omega_{1},\Omega_{2})$
	 REGARDER etudes.ru "machines de tchebychev"








