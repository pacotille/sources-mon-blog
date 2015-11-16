---
title: Calcul de volumes nurbs
author: PacoTille
tags: Maths, Algorithmes
---

#  Bézier


 $$b^{m,n}(u,v)=\sum^{m}_{i=0}\sum^{n}_{j=0}b_{i,j}B^{m}_{i}(u)B^{n}_{j}(v)$$ 

$$\frac{\partial }{\partial u}b^{m,n}(u,v)= \sum^{n}_{j=0}\left[\frac{\partial }{\partial u}\sum^{m}_{i=0}b_{i,j}B^{m}_{i}(u)\right]B^{n}_{j}(v)$$ 

$$\frac{\partial }{\partial v}b^{m,n}(u,v)= \sum^{m}_{i=0}\left[\frac{\partial }{\partial v}\sum^{n}_{j=0}b_{i,j}B^{n}_{i}(v)\right]B^{m}_{i}(u)$$ 
Cette formule est générale, et permet d'exprimer le volume V du domaine bordé par une surface S continue.

On prend  $\overrightarrow{e}=\overrightarrow{z}$

$$P(t)=\begin{vmatrix}1 & u & u^2 & u^3\end{vmatrix}$$
# Un exemple

Calcul du volume de la sphere unité $x^2+y^2+z^2=1$

On prend $\overrightarrow{F}(x,y,z)=x\overrightarrow{i}+y\overrightarrow{j}+z\overrightarrow{k}$

Description paramétrique de la sphère :

$\overrightarrow{r}(\phi, \theta)=\sin \phi \cos \theta \overrightarrow{i}+\sin \phi sin \theta \overrightarrow{j}+ \cos \phi \overrightarrow{k}$ avec $D=\{(\phi, \theta)\vert 0 \leq \phi \leq \pi, 0 \leq \theta \leq 2\pi\}$

$$
\overrightarrow{r}_{\phi}^{\prime}\wedge \overrightarrow{r}_{\theta}^{\prime}=
\begin{vmatrix}\overrightarrow{i} & \overrightarrow{j} & \overrightarrow{k}\\
\frac{\partial x}{\partial \phi} & \frac{\partial y}{\partial \phi} & \frac{\partial z}{\partial \phi}\\
\frac{\partial x}{\partial \theta} & \frac{\partial y}{\partial \theta} & \frac{\partial z}{\partial \theta}
\end{vmatrix}=
\begin{vmatrix}\overrightarrow{i} & \overrightarrow{j} & \overrightarrow{k}\\
\cos \phi \cos \theta & \cos \theta \sin \phi & -\sin \phi \\
-\sin \phi \sin \theta & \sin \phi \cos \theta & 0
\end{vmatrix}$$
$$=\sin^2 \phi \cos \theta \overrightarrow{i}+\sin^2 \phi sin \theta \overrightarrow{j}+ \cos \phi \overrightarrow{k}$$

On a :

$\overrightarrow{F}(\overrightarrow{r}(\phi, \theta))=\sin \phi \cos \theta \overrightarrow{i}+\sin \phi sin \theta \overrightarrow{j}+ \cos \phi \overrightarrow{k}$ 

On a donc :

$\overrightarrow{F}(\overrightarrow{r}(\phi,\theta)).(\overrightarrow{r}_{\phi}^{\prime}\wedge \overrightarrow{r}_{\theta}^{\prime})=\cos \phi \sin^2 \phi \cos \theta +\sin^3 \phi sini^2 \theta + \sin^2 \phi \cos \phi \cos \theta$ 


$$\int_S \overrightarrow{F}.\,d\overrightarrow{S}=\int_D\overrightarrow{F}(\overrightarrow{r}(\phi,\theta)).(\overrightarrow{r}_{\phi}^{\prime}\wedge \overrightarrow{r}_\theta^{\prime})\,d A$$ 
$$=\int_D\overrightarrow{F}(\overrightarrow{r}(\phi,\theta)).(\overrightarrow{r}_{\phi}^{\prime}\wedge \overrightarrow{r}_\theta^{\prime})\,d A$$ 

# Conclusion

# Les liens et références 
- Curves and surfaces for CAGD, A pratical guide Fifth Edition, Gerarald Farin ISBN  : 1-55860-737-4
