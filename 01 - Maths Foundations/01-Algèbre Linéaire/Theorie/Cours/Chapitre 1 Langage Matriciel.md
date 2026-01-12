# Chapitre 1 – Langage Matriciel
## Objectifs
- [ ] Illustrer à l'aide d'exemples de la vie courante ce qu'est une matrice
- [ ] Utiliser le langage matriciel pour décrire un contexte
- [ ] interpréter, en contexte, un élément, une ligne ou une colonne d'une matrice
- [ ] Écrire la matrice des coefficients d'un système d'équations linéaires
- [ ] Définir le concept de matrice et les termes (format, élément, diagonale principale, trace, etc.) qui s'y rattachent
- [ ] Déterminer les conditions auxquelles deux matrices sont égales 
- [ ] Utiliser la notation appropriée pour donner l'expression du terme général d'une matrice, d'un élément d'une matrice ou la valeur de celui-ci 
- [ ] Construire une matrice à partir de l'expression de son terme général 
- [ ] Utiliser la notation X pour représenter une somme 
- [ ] Calculer la trace d'une matrice carrée
- [ ] Donner le type (carrée, symétrique, ligne, etc.) d'une matrice
- [ ] Prouver des énoncés relatifs aux matrices
## Concepts
- matrice
- élément d’une matrice
- format d’une matrice
- matrice carrée 
- ordre d’une matrice carrée
- diagonale principale
- égalité de deux matrices
- matrice nulle - matrice triangulaire supérieure - matrice triangulaire inférieure -
- matrice diagonale - matrice scalaire - matrice identité - 
- matrice symétrique - matrice antisymétrique 
- matrice échelonnée - pivot d'une ligne - matrice échelonnée réduite
## Notes

#### **Définitions Fondamentales**

1. **Matrice**  
    Un tableau ordonné de éléments (scalaires) disposés en m lignes et n colonnes. On note l'ensemble des matrices m×n à coefficients réels par Mm×n​(R).
    
2. **Élément d’une matrice**  
    Soit A ∈ Mm×n​(R). L'élément à l'intersection de la ligne i et de la colonne j est noté aij​ A[i,j] ou (A)ij​, où 1 ≤ i≤ m, 1 ≤ j ≤ n.
    
3. **Format (Dimension) d’une matrice**  
    Le format de A est le couple (m,n) où m est le nombre de lignes et n le nombre de colonnes. On dit aussi « matrice de taille m×n ».
    
4. **Matrice carrée**  
    Matrice dont le nombre de lignes est égal au nombre de colonnes (m=n). On note Mn​(R) l'ensemble des matrices carrées d’ordre n.
    
5. **Ordre d’une matrice carrée**  
    Pour une matrice carrée, son ordre est le nombre n de ses lignes (ou colonnes).
    
6. **Diagonale principale**  
    Dans une matrice carrée A ∈ Mn​(R), la diagonale principale est l'ensemble des éléments a11​,a22​,…,ann​.
    
7. **Égalité de deux matrices**  
    Soient A,B ∈ Mm×n​(R).
    
    A = B ⟺aij ​= bij ​∀i ∈ {1,…,m},  ∀j ∈ {1,…,n}.
    

---

#### **Familles Remarquables de Matrices (Matrices Carrées)**

8. **Matrice nulle** Om×n​ Matrice dont tous les éléments sont nuls. Si m = n, on note On​.
    
9. **Matrice triangulaire supérieure**Matrice carrée dont tous les éléments **sous** la diagonale principale sont nuls :  
    aij​ = 0 pour i>j.
    
10. **Matrice triangulaire inférieure**Matrice carrée dont tous les éléments **au-dessus** de la diagonale principale sont nuls :  
    aij​ = 0 pour i<j.
    
11. **Matrice diagonale**  
    Matrice carrée à la fois triangulaire supérieure et inférieure :  
    aij ​= 0 pour i = ! j.  
    Seuls les éléments de la diagonale peuvent être non nuls.  
    On note diag(d1​,d2​,…,dn​).
    
12. **Matrice scalaire**  
    Matrice diagonale dont tous les éléments diagonaux sont égaux :  
    aij​=λ si i=j, et 0 sinon. C'est un multiple de l'identité : λIn​.
    
13. **Matrice identité** In​  
    Matrice scalaire avec λ=1.  
    (In​)ij​=δij​ où δij​ est le symbole de Kronecker (δii​=1, δij​=0 si i = ! j).
    
14. **Matrice symétrique**  
    Matrice carrée égale à sa transposée :  
    A⊤= A, i.e. aij​ = aji​ ∀i,j.
    
15. **Matrice antisymétrique (ou skew-symétrique)**  
    Matrice carrée égale à l'opposée de sa transposée :  
    A⊤=−A, i.e. aij​ =−aji​  ∀i,j.  
    En conséquence, les éléments diagonaux sont nuls : aii​=0.
    

---

#### **Formes Utiles pour la Résolution de Systèmes**

16. **Matrice échelonnée (en escalier)**  
    Matrice (non nécessairement carrée) satisfaisant :
    
    - Toutes les lignes nulles (si elles existent) sont en bas.
        
    - Le **pivot** (premier élément non nul) d’une ligne non nulle est strictement à droite du pivot de la ligne précédente.
        
17. **Pivot d’une ligne**  
    Dans une matrice échelonnée, premier élément non nul d’une ligne non nulle.
    
18. **Matrice échelonnée réduite (forme de Gauss-Jordan)**  
    Matrice échelonnée qui satisfait de plus :
    
    - Chaque pivot vaut 1.
        
    - Chaque pivot est le seul élément non nul de sa colonne.
        

---

**Remarque Fondamentale :**

Ces structures ne sont pas des curiosités abstraites. Une matrice **triangulaire** rend la résolution de systèmes **rétro-substituable**. Une matrice **diagonale** représente un découplage complet des inconnues. La forme **échelonnée réduite** donne directement la solution d’un système linéaire.
Étudier ces matrices particulières n'est pas un exercice de classification gratuite. C'est une démarche **stratégique et pragmatique** qui répond au cœur même de l'algèbre linéaire : **résoudre des problèmes complexes en les ramenant à des problèmes simples.**

## Résumé


