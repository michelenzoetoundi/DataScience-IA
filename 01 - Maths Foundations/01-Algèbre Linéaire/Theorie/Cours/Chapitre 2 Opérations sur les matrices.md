# 📘 Chapitre 2 — Opérations sur les matrices

> 🧭 Objectif : Manipuler et raisonner sur les matrices avec addition, multiplication, transposition et opérations avancées.  

---
## 🎯 Objectifs d’apprentissage

- [ ] Additionner deux matrices lorsque c’est possible  
- [ ] Multiplier une matrice par un scalaire  
- [ ] Trouver la matrice opposée  
- [ ] Transposer une matrice  
- [ ] Multiplier deux matrices lorsque c’est possible  
- [ ] Vérifier si une matrice est idempotente ou nilpotente, et trouver l’indice de nilpotence  
- [ ] Interpréter le résultat d’une opération matricielle en contexte  
- [ ] Déterminer l’opération matricielle à effectuer en contexte  
- [ ] Invalider un énoncé relatif aux matrices avec un contre-exemple  
- [ ] Illustrer ou prouver des propriétés matricielles en utilisant la notation Σ  
- [ ] Construire la matrice de transition et le diagramme de transition d’une chaîne de Markov simple  
- [ ] Déterminer la matrice d’état de niveau $m$  
- [ ] Exprimer un système d’équations linéaires sous forme matricielle  
- [ ] Définir et calculer l’inverse d’une matrice carrée d’ordre 2  
- [ ] Résoudre un système d’équations linéaires avec la matrice inverse  
---
## 🧱 Concepts fondamentaux

| Notion ou Concept                            | Utilisation |
| -------------------------------------------- | ----------- |
| Addition de deux matrices                    | 📊 🤖 🧠    |
| Incompatibilité pour l'addition              | 📊 🤖 🧠    |
| Multiplication d’une matrice par un scalaire | 📊 🤖 🧠    |
| Matrice opposée                              | 📊 🤖 🧠    |
| Matrice symétrique                           | 📊 🤖 🧠    |
| Matrice antisymétrique                       | 📊 🤖       |
| Produit de deux matrices                     | 📊 🤖 🧠    |
| Indice de nilpotence                         | 📊 🤖       |
| Matrice nilpotente                           | 📊 🤖       |
| Matrice idempotente                          | 📊 🤖       |
| Chaîne de Markov                             | 📊 🤖 🧠    |
| Diagramme de transition                      | 📊 🤖 🧠    |
| Matrice stochastique                         | 📊 🤖 🧠    |
| Matrice d’état de niveau m                   | 📊 🤖 🧠    |
| Matrice de transition                        | 📊 🤖 🧠    |
| Matrice inverse                              | 📊 🤖 🧠    |
| Transposée d’une matrice                     | 📊 🤖 🧠    |

---

### 📝 Remarques sur l’importance
- Les **opérations de base** (addition, multiplication par un scalaire, produit de matrices, transposition) sont fondamentales pour toutes les manipulations de données et calculs en Machine Learning.  
- Les **matrices particulières** (symétrique, antisymétrique, idempotente, nilpotente) sont importantes pour comprendre certaines propriétés théoriques et la factorisation des matrices.  
- Les **matrices liées aux chaînes de Markov** (stochastique, de transition, d’état) sont essentielles pour modéliser des processus probabilistes et séquentiels.  
- La **matrice inverse** est clé pour résoudre les systèmes d’équations linéaires et pour des méthodes comme la régression linéaire.  

---
## 📝 Légende des emojis
- 📊 = Sciences des données  
- 🤖 = Apprentissage automatique  
- 🧠 = Apprentissage profond

---
## 🚀 Progression du chapitre
- 2.1 Addition de deux matrices
- 2.2 Multiplication d'une matrice par un scalaire 
- 2.3 Transposition d'une matrice 
- 2.4 Propriétés de l'addition, de la multiplication par un scalaire et de la transposition 
- 2.5 Multiplication de matrices 
- 2.6 Propriétés de la multiplication de matrices
- 2.7 Chaînes de Markov
- 2.8 Produit matriciel et système d'équations linéaires
- Résumé

----
## 1️⃣ Forme générale d’une matrice

Une matrice $A$ de format $m \times n$ est :

$$
A = 
\begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn}
\end{bmatrix}
$$

- $a_{ij}$ : élément de la **ligne $i$** et **colonne $j$**  
- $m$ : nombre de lignes  
- $n$ : nombre de colonnes  

---

## 2️⃣ Addition de matrices ➕

- **Définition** : $C = A + B$ possible **si $A$ et $B$ ont le même format**  
- **Forme générale** :

$$
A + B = 
\begin{bmatrix}
a_{11}+b_{11} & a_{12}+b_{12} & \dots & a_{1n}+b_{1n} \\
a_{21}+b_{21} & a_{22}+b_{22} & \dots & a_{2n}+b_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1}+b_{m1} & a_{m2}+b_{m2} & \dots & a_{mn}+b_{mn}
\end{bmatrix}
$$

**Exemple concret** :  
$$
A = \begin{bmatrix}1 & 2\\3 & 4\end{bmatrix}, \quad
B = \begin{bmatrix}5 & 6\\7 & 8\end{bmatrix} 
\implies A+B = \begin{bmatrix}6 & 8\\10 & 12\end{bmatrix}
$$

- **Incompatibilité** : formats différents → addition impossible.

---

## 3️⃣ Multiplication par un scalaire ✖️

- **Définition** : $kA$ multiplie **chaque élément** de $A$ par $k$  

$$
kA = 
\begin{bmatrix}
k a_{11} & k a_{12} & \dots & k a_{1n} \\
k a_{21} & k a_{22} & \dots & k a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
k a_{m1} & k a_{m2} & \dots & k a_{mn}
\end{bmatrix}
$$

**Exemple** :  
$$
2 \begin{bmatrix}1 & 3\\4 & 5\end{bmatrix} = \begin{bmatrix}2 & 6\\8 & 10\end{bmatrix}
$$

---

## 4️⃣ Matrice opposée ➖

- **Définition** : $-A$ telle que $A + (-A) = 0$  

$$
-A = 
\begin{bmatrix}
-a_{11} & -a_{12} & \dots & -a_{1n} \\
-a_{21} & -a_{22} & \dots & -a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
-a_{m1} & -a_{m2} & \dots & -a_{mn}
\end{bmatrix}
$$

**Exemple** :  
$$
A = \begin{bmatrix}2 & -1\\3 & 0\end{bmatrix} \implies -A = \begin{bmatrix}-2 & 1\\-3 & 0\end{bmatrix}
$$

---

## 5️⃣ Transposition 🔄

- **Définition** : $A^T$ échange **lignes et colonnes**  
- **Forme générale** :

Si 
$$
A = 
\begin{bmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23}
\end{bmatrix}_{2 \times 3}
$$

Alors
$$
A^T = 
\begin{bmatrix}
a_{11} & a_{21} \\
a_{12} & a_{22} \\
a_{13} & a_{23}
\end{bmatrix}_{3 \times 2}
$$

- Chaque **ligne devient colonne**, chaque **colonne devient ligne**  

**Exemple concret** :  
$$
\begin{bmatrix}1 & 2 & 3\\4 & 5 & 6\end{bmatrix}^T = \begin{bmatrix}1 & 4\\2 & 5\\3 & 6\end{bmatrix}
$$

---

## 6️⃣ Produit de matrices ✖️✖️

- **Définition** : $C = AB$ possible si $A$ est $m \times p$ et $B$ est $p \times n$  
- **Forme générale** :

$$
C = [c_{ij}], \quad c_{ij} = \sum_{k=1}^{p} a_{ik} b_{kj}
$$
Soient deux matrices :

$$
A = 
\begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1p} \\
a_{21} & a_{22} & \dots & a_{2p} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mp}
\end{bmatrix}_{m \times p}, 
\quad
B = 
\begin{bmatrix}
b_{11} & b_{12} & \dots & b_{1n} \\
b_{21} & b_{22} & \dots & b_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
b_{p1} & b_{p2} & \dots & b_{pn}
\end{bmatrix}_{p \times n}
$$

Alors le produit $C = AB$ est une matrice $m \times n$ :

$$
C = 
\begin{bmatrix}
c_{11} & c_{12} & \dots & c_{1n} \\
c_{21} & c_{22} & \dots & c_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
c_{m1} & c_{m2} & \dots & c_{mn}
\end{bmatrix}
$$

où chaque élément $c_{ij}$ se calcule ainsi :

$$
c_{ij} = a_{i1}b_{1j} + a_{i2}b_{2j} + \dots + a_{ip}b_{pj} = \sum_{k=1}^{p} a_{ik} b_{kj}
$$

### Exemple concret avec m = p = n = 3

$$
A = 
\begin{bmatrix}
a & b & c \\
d & e & f \\
g & h & i
\end{bmatrix}, \quad
B = 
\begin{bmatrix}
j & k & l \\
m & n & o \\
p & q & r
\end{bmatrix}
$$

Le produit $C = AB$ :

- Premier élément $c_{11}$ : **ligne 1 de $A$ × colonne 1 de $B$**

$$
c_{11} = a*j + b*m + c*p
$$

- $c_{12}$ : ligne 1 de $A$ × colonne 2 de $B$

$$
c_{12} = a*k + b*n + c*q
$$

- $c_{13}$ : ligne 1 de $A$ × colonne 3 de $B$

$$
c_{13} = a*l + b*o + c*r
$$

- $c_{21}$ : ligne 2 de $A$ × colonne 1 de $B$

$$
c_{21} = d*j + e*m + f*p
$$

- $c_{22}$ : ligne 2 de $A$ × colonne 2 de $B$

$$
c_{22} = d*k + e*n + f*q
$$

- $c_{23}$ : ligne 2 de $A$ × colonne 3 de $B$

$$
c_{23} = d*l + e*o + f*r
$$

- $c_{31}$ : ligne 3 de $A$ × colonne 1 de $B$

$$
c_{31} = g*j + h*m + i*p
$$

- $c_{32}$ : ligne 3 de $A$ × colonne 2 de $B$

$$
c_{32} = g*k + h*n + i*q
$$

- $c_{33}$ : ligne 3 de $A$ × colonne 3 de $B$

$$
c_{33} = g*l + h*o + i*r
$$

Donc le produit complet est :

$$
C = AB = 
\begin{bmatrix}
a*j + b*m + c*p & a*k + b*n + c*q & a*l + b*o + c*r \\
d*j + e*m + f*p & d*k + e*n + f*q & d*l + e*o + f*r \\
g*j + h*m + i*p & g*k + h*n + i*q & g*l + h*o + i*r
\end{bmatrix}
$$

**Remarque :** chaque élément de $C$ est obtenu **en multipliant une ligne de $A$ par une colonne de $B$** et en **sommant les produits**.  

**Exemple pas à pas** :  
$$
A = \begin{bmatrix}1 & 2\\3 & 4\end{bmatrix}, \quad 
B = \begin{bmatrix}5 & 6\\7 & 8\end{bmatrix}
$$

Calcul de $C = AB$ :

- $c_{11} = 1*5 + 2*7 = 19$  
- $c_{12} = 1*6 + 2*8 = 22$  
- $c_{21} = 3*5 + 4*7 = 43$  
- $c_{22} = 3*6 + 4*8 = 50$

Donc
$$
AB = \begin{bmatrix}19 & 22\\43 & 50\end{bmatrix}
$$

---

## 7️⃣ Propriétés combinées ⚙️

- **Addition** : commutative, associative, élément neutre $0$, opposé $-A$  
- **Multiplication par un scalaire** : distributive, associative, neutre $1$  
- **Transposition** : $(A^T)^T = A$, $(A+B)^T = A^T + B^T$, $(kA)^T = kA^T$, $(AB)^T = B^T A^T$  

---

## 8️⃣ Matrices spéciales 🧮

| Concept | Définition |
|---------|------------|
| Symétrique | $A = A^T$ |
| Antisymétrique | $A = -A^T$ |
| Idempotente | $A^2 = A$ |
| Nilpotente | $A^k = 0$ pour un certain $k$ |
| Indice de nilpotence | plus petit $k$ tel que $A^k = 0$ |
| Inverse | $AA^{-1} = A^{-1}A = I$ |
| Stochastique | $p_{ij} \ge 0$, somme de chaque **colonne** = 1 |

---

## 9️⃣ Chaînes de Markov 📈

### 📌 Idée fondamentale
Une **chaîne de Markov** modélise l’évolution d’un système **dont l’état futur dépend uniquement de l’état présent**, et **pas du passé**.

👉 C’est le **principe de mémoire nulle** (ou propriété de Markov).

---

### 🔹 États du système
Les **états** sont les situations possibles du système.

Exemples :
- météo : {soleil, pluie, nuageux}
- client : {fidèle, occasionnel, perdu}
- machine : {fonctionnelle, en panne}

On les numérote :
$$
E_1, E_2, \dots, E_n
$$

---

### 🔹 Probabilités de transition
La probabilité de passer de l’état $E_j$ à l’état $E_i$ est notée :

$$
p_{ij} = P(X_{n+1} = E_i \mid X_n = E_j)
$$

👉 **Important** : l’indice **j = état actuel**, **i = état futur**

---

### 🔹 Matrice de transition $P$
On regroupe toutes les probabilités $p_{ij}$ dans une **matrice de transition** :

$$
P = [p_{ij}]
$$

où :
- chaque **colonne correspond à un état actuel**
- chaque **ligne correspond à un état futur**

---

### 🔹 Matrice stochastique
Une matrice $P$ est dite **stochastique** si :

1. Tous ses éléments sont **non négatifs** :
$$
p_{ij} \ge 0
$$

2. La somme des éléments de **chaque colonne vaut 1** :
$$
\sum_{i=1}^{n} p_{ij} = 1
$$

👉 Cela traduit le fait que **depuis un état donné, on va forcément vers un des états possibles**.

---

### 📌 Exemple de matrice de transition

$$
P =
\begin{bmatrix}
0.7 & 0.2 \\
0.3 & 0.8
\end{bmatrix}
$$

Interprétation :
- depuis l’état $E_1$ :
  - 70 % de chances de rester en $E_1$
  - 30 % de chances d’aller en $E_2$
- depuis l’état $E_2$ :
  - 20 % vers $E_1$
  - 80 % rester en $E_2$

---

### 🔹 Diagramme de transition
Le **diagramme de transition** est une représentation graphique :

- les **nœuds** = états
- les **flèches** = transitions
- les **poids** = probabilités

👉 Il permet une **lecture intuitive** du système.

---

### 🔹 Matrice d’état (ou vecteur d’état)
À l’instant $n$, l’état du système est décrit par un **vecteur colonne** :

$$
S_n =
\begin{bmatrix}
s_1 \\
s_2 \\
\vdots \\
s_n
\end{bmatrix}
$$

où $s_i$ est la probabilité d’être dans l’état $E_i$ à l’instant $n$.

---

### 🔹 Évolution du système
L’évolution du système obéit à la relation fondamentale :

$$
S_{n+1} = P S_n
$$

👉 **La dynamique du système est entièrement portée par le produit matriciel.**

---

### 🔹 Matrice d’état de niveau $m$
Après $m$ transitions :

$$
S_m = P^m S_0
$$

où :
- $S_0$ est l’état initial
- $P^m$ est la **puissance $m$ de la matrice de transition**

---

### 📌 Exemple détaillé

Soit :
$$
P =
\begin{bmatrix}
0.6 & 0.4 \\
0.4 & 0.6
\end{bmatrix}, \quad
S_0 =
\begin{bmatrix}
1 \\
0
\end{bmatrix}
$$

👉 Le système commence **certainement** dans l’état $E_1$.

Calcul de $S_1$ :
$$
S_1 = P S_0 =
\begin{bmatrix}
0.6 \\
0.4
\end{bmatrix}
$$

Calcul de $S_2$ :
$$
S_2 = P S_1 =
\begin{bmatrix}
0.6 & 0.4 \\
0.4 & 0.6
\end{bmatrix}
\begin{bmatrix}
0.6 \\
0.4
\end{bmatrix}
=
\begin{bmatrix}
0.52 \\
0.48
\end{bmatrix}
$$

👉 Le système tend vers un **équilibre probabiliste**.

---

### 🔹 Interprétation conceptuelle
- Une chaîne de Markov est un **système dynamique discret**
- La matrice de transition encode :
  - les **règles du système**
  - les **contraintes probabilistes**
- Les puissances de $P$ montrent :
  - la **stabilisation**
  - ou la **dynamique à long terme**

---
##  📝 Produit matriciel et systèmes linéaires

**Système linéaire général** :  
Un système de $m$ équations à $n$ inconnues peut s’écrire sous forme matricielle :

$$
A X = B
$$

où :  

- $A = [a_{ij}]$ est la **matrice des coefficients** de dimension $m \times n$  
$$
A =
\begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn}
\end{bmatrix}
$$

- $X = [x_j]$ est le **vecteur colonne des inconnues**  
$$
X =
\begin{bmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{bmatrix}
$$

- $B = [b_i]$ est le **vecteur des termes constants**  
$$
B =
\begin{bmatrix}
b_1 \\
b_2 \\
\vdots \\
b_m
\end{bmatrix}
$$

---

### 💡 Résolution via la matrice inverse (cas où $A$  est carrée et inversible)

Si $A$ est **carrée ($n=m$) et inversible**, on peut résoudre le système par :

$$
X = A^{-1} B
$$

**Étapes détaillées** :

1. **Écrire la matrice des coefficients** $A$ et le vecteur des constantes $B$.
2. **Calculer l’inverse $A^{-1}$** :
   - Pour $n=2$ :  
     $$
     A =
     \begin{bmatrix}a & b \\ c & d\end{bmatrix} \implies
     A^{-1} = \frac{1}{ad - bc}
     \begin{bmatrix}d & -b \\ -c & a\end{bmatrix}, \quad ad - bc \neq 0
     $$
   - Pour $n>2$ : utiliser méthodes de Gauss-Jordan ou formule générale via cofacteurs.
3. **Multiplier $A^{-1}$ par $B$** pour obtenir $X$ :
$$
X = A^{-1} B
$$

---

### 📌 Exemple général $2 \times 2$

Soit le système :

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 = b_1 \\
a_{21}x_1 + a_{22}x_2 = b_2
\end{cases}
$$

**Forme matricielle** :

$$
A =
\begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix}, \quad
X =
\begin{bmatrix}x_1 \\ x_2\end{bmatrix}, \quad
B =
\begin{bmatrix}b_1 \\ b_2\end{bmatrix}
$$

**Inverse de $A$** :

$$
A^{-1} = \frac{1}{a_{11}a_{22}-a_{12}a_{21}}
\begin{bmatrix}
a_{22} & -a_{12} \\
-a_{21} & a_{11}
\end{bmatrix}, \quad a_{11}a_{22}-a_{12}a_{21} \neq 0
$$

**Solution** :

$$
X = A^{-1}B = 
\frac{1}{a_{11}a_{22}-a_{12}a_{21}}
\begin{bmatrix}
a_{22} & -a_{12} \\
-a_{21} & a_{11}
\end{bmatrix}
\begin{bmatrix}b_1 \\ b_2\end{bmatrix} =
\begin{bmatrix}
\dfrac{a_{22}b_1 - a_{12}b_2}{a_{11}a_{22}-a_{12}a_{21}} \\
\dfrac{-a_{21}b_1 + a_{11}b_2}{a_{11}a_{22}-a_{12}a_{21}}
\end{bmatrix}
$$

---

### 📌 Exemple numérique

$$
\begin{cases}
2x_1 + 1x_2 = 5 \\
3x_1 + 4x_2 = 6
\end{cases} \implies
A = 
\begin{bmatrix}2 & 1 \\ 3 & 4\end{bmatrix}, \quad
B = 
\begin{bmatrix}5 \\ 6\end{bmatrix}
$$

**Calcul de $A^{-1}$** :

$$
\det(A) = 2\cdot4 - 1\cdot3 = 5 \neq 0
$$

$$
A^{-1} = \frac{1}{5} 
\begin{bmatrix}4 & -1 \\ -3 & 2\end{bmatrix}
$$

**Solution** :

$$
X = A^{-1}B = \frac{1}{5}
\begin{bmatrix}4 & -1 \\ -3 & 2\end{bmatrix}
\begin{bmatrix}5 \\ 6\end{bmatrix} =
\frac{1}{5}
\begin{bmatrix}14 \\ -3\end{bmatrix} =
\begin{bmatrix}2.8 \\ -0.6\end{bmatrix}
$$

---

✨ *Cette méthode montre comment passer de la forme générale d’un système à sa solution en utilisant la matrice inverse, étape par étape.*

---

## 🧾 Résumé

- Les **opérations matricielles** sont fondamentales pour représenter et résoudre des problèmes linéaires et probabilistes.  
- Les **propriétés** garantissent la cohérence et la simplification des calculs.  
- Les **chaînes de Markov** permettent de modéliser des processus stochastiques.  

---

✨ *Les opérations matricielles ne sont pas seulement des calculs : elles révèlent la structure et la logique des systèmes réels.*
