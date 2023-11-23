# Exercices sur les tableaux (à 2 dimensions)

Pour ces exercices, on travaille à l’aide d’un tableau (à 2 dimensions) d’entiers **t** de taille 10x10 et de deux entiers **m** et **n** dont l’utilisateur choisit les valeurs (<= 10). L’entier **m** donnant le nombre de lignes et l’entier **n** donnant le nombre de colonnes **effectivement utilisées**. On n'utilise donc bien **qu'une partie** du tableau (ou tout le tableau dans le cas où m = n = 10).

**! On devra prendre soin de définir 10 (= taille max du tableau, lignes et colonnes) à l’aide d’un `#define`.**

## Bête exemple pour fixer les idées

```C
#pragma warning(disable:4996)
#include <stdio.h>
#include <stdlib.h>

#define O 10

//NB : "O" comme "Ordre" du tableau (quand le nombre de lignes et de colonnes sont égaux à n, on parle d'un "tableau d'ordre n")

int main()
{
    short t[O][O]={0};
    short m,n,nb;

    printf("nombre de lignes du tableau (<=%d): ",O);
    scanf("%hd",&m);

    printf("nombre de colonnes du tableau (<=%d): ",O);
    scanf("%hd",&n);
	
    printf("nombre a placer tout en bas a droite en derniere case du tableau : ");
    scanf("%hd",&nb);

    t[m-1][n-1] = nb; //on ne considere bien que la partie de t allant de 0,0 jq m-1,n-1 !
	
    printf("Tableau initialise a 0 avec nb en derniere case !");

    return 0;
}
```

## Pour rappel
Visual Studio est disponible gratuitement (https://ecolevirtuelle.provincedeliege.be/ctrl/ctrl_gestion.openDocument?p_idNode=1177603)

Une fois Visual Studio installé, vous pouvez créer **un projet par exercice** !! (Fichiers > Nouveau > Projets...) 

Au départ, vous pouvez toujours commencer par taper (ou copier-coller ;-D) les lignes suivantes :
```c
#pragma warning(disable:4996)
#include <stdio.h>
#include <stdlib.h>

int main()
{

    return 0;
}
```

Ensuite, vous pouvez écrire votre code en ligne 7 juste avant l'instruction `return 0;`

Le bouton "Exécuter sans débogage" (triangle "play" vert) permet de recompiler et exécuter tout votre projet.

À toutes fins utiles, voici à nouveau le document contenant des infos utiles sur l'utilisation du debogueur de Visual Studio&nbsp;: https://ecolevirtuelle.provincedeliege.be/ctrl/ctrl_gestion.openDocument?p_idNode=1177599
