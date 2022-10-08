# Théorie des graphes

## Quelques rappels
### Définitions :
- Un chemin : $s_{0},\dots,s_{n} \ | \ \forall i \in [|1, n-1|] : \set{s_{i}, s_{i+1}} \in A$
- Un chemin élémentaire : c'est un chemin dont toutes les arêtes sont distinctes, ie $s_{0},\dots,s_{n} \ | \ \neg \exists i < j \mid \set{s_{i}, s_{i+1}} =  \set{s_{j}, s_{j+1}}$
- Un chemin simple : c'est un chemin dont tous les sommets sont distincts, ie c'est un chemin ne passant pas deux fois par un même sommet.
- Un chemin fermé : $s_{0} = s_{n}$
- Un circuit : c'est un chemin fermé avec $n \ne 0$
- Un cycle : c'est un circuit élémentaire, ie un chemin fermé non trivial dont toutes les arêtes sont distinctes.

## I. Parcours de graphes
### I.1 - Généralités
#### I.1.1 - Définition : parcours d'un graphe non orienté connexe)

Soient $G = (S, A)$ un graphe non orienté connexe et $s \in S$. Un parcours de G à partir de $s$ est une suite finie de sommets $s_{0},\dots,s_{n-1}$ telle que :
$$s_0 = s$$
$$n = |S|, \set{s_{i} \ | \ i \in [|0, n-1|]} = S$$
$$\forall i \in [|1, n-1|] : \exists j < i \ | \ \set{s_i, s_j} \in A$$

#### I.1.2 - Définition : une bordure

Soient $G = (S, A)$ un graphe et $E \subseteq S$. On appelle bordure de E l'ensemble suivant :
$$B(E) = \set{s \in S\backslash E, \exists s' \in E \ | \ \set{s, s'} \in A}$$
C'est donc l'ensemble des sommets qui ne sont pas dans $E$ connectés à $E$.

#### I.1.3 - Définition : un arbre

Un arbre est un graphe non orienté connexe et acyclique.

#### I.1.4 - Définition : sous graphe induit / couvant

Soit $G = (S, A)$.

- Le sous graphe induit par $S' \subseteq S$ est un graphe $G_{S'} = (S', A')$ où $A' = \set{a \in A \ | \ \forall s \in a : s \in S'}$. L'ensemble des sommets du sous-graphe $G_{S'}$ est un sous-ensemble de l'ensemble des sommets de $G$ et l'ensemble des arcs de $G_{S'}$ est un sous-ensemble de l'ensemble des arcs de $G$ ayant leur origine ou leur extrémité parmi les sommets de $G_{S'}$.

- Un sous graphe $G' = (S', A')$ de $G$ est couvrant si et seulement si $S = S'$.
