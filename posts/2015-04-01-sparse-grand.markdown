---
title: Grande matrices creuses
author: PacoTille
tags: matrices
---

<h1>R�solution degrands syst�mes linaires creux</h1>

<h2>Repr�sentation compacte de la matrice</h2>

<h2>Pivot de Gauss</h2>

~~~ {.cpp}
 Gauss-Jordan
     r = 0 (r est l'indice de ligne du dernier pivot trouv�)
     Pour j de 1 jusqu'� m (j d�crit tous les indices de colonnes)
     |   Rechercher max(|A[i,j]|, r+1 = i = n), noter k la position du maximum
     |   A[k,j] est le pivot
     |   Si A[k,j]?0 alors
     |   |   r=r+1
     |   |   Diviser la ligne k par A[k,j]
     |   |   �changer les lignes k et r
     |   |   Pour i de 1 jusqu'� n
     |   |   |   Si i?r alors
     |   |   |   |   Soustraire � la ligne i la ligne r multipli�e par A[i,j] (de fa�on � annuler A[i,j])
     |   |   |   Fin Si
     |   |   Fin Pour
     |   Fin Si
     Fin Pour
  Fin Gauss-Jordan
~~~


# Les liens

-[Liste de matrices test](http://www.cise.ufl.edu/research/sparse/matrices/list_by_dimension.html)
-[La lib CSparce](http://www.cise.ufl.edu/research/sparse/CSparse/)
-[Algorithmique des matrices creuses](http://perso.ens-lyon.fr/bora.ucar/CR09/linear-algebra-basics.pdf)
-[La lib PasTix](http://pastix.gforge.inria.fr/files/README-txt.html)
-[MUMPS](http://mumps.enseeiht.fr/)
-[SuperLU](http://crd-legacy.lbl.gov/~xiaoye/SuperLU/)
-[UMFPACK](http://www.cise.ufl.edu/research/sparse/umfpack/)
-[TAUCS](http://www.tau.ac.il/~stoledo/taucs/)
-[PARDISO](http://www.pardiso-project.org/)
-[WSMP](http://researcher.ibm.com/view_project.php?id=1426)
-[PSPASES](http://www-users.cs.umn.edu/~mjoshi/pspases/)
-[HSL](http://www.hsl.rl.ac.uk/)
-[BCSLib](http://www.boeing.com/phantom/bcslib/)
