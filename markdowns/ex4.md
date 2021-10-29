# Exercice 4 (vecteurs) : COUPER-COLLER-MÉLANGER UN VECTEUR

+ Déclarer deux vecteurs `v[50]` et `vM[50]` (`vM` pour « Vecteur Mélangé ») et demander `n` (<=50) ainsi que `d` (>=0, un nombre entier positif de départ) et remplir les `n` cases de `v` et `vM` de la façon suivante :
  + Remplir `v` avec les valeurs d+0,d+1, ..., d+n-1 
  + Afficher `v`
  + Remplir chacune des `n` valeur de `vM` avec une des `n` valeur de `v` prise au hasard. A chaque itération, on prend un indice au hasard (entre 0 et n-1 inclus). Si l'indice est inédit : mettre la valeur -1 à cette case, sinon parcourir le reste du vecteur (et éventuellement le début) jursqu'à trouver la première valeur différente de -1 
  + Afficher `vM`