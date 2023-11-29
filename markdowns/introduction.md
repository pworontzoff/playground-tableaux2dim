# Introduction

Les exercices de cette séance portent sur les consultations et modifications de données d'un tableau à 2 dimensions (lignes et colonnes). Ceci en utilisant des fonctions qui utilisent la notation [][] afin d'accéder par indices aux cellules de tableaux.
Les tableaux seront passés par paramètre aux fonctions via un pointeur "masqué" en utilisant la notation ```nomTab[][N]``` dans l'en-tête (et prototype) de la fonction, pour lui passer le tableau.
+ ```nomTab``` est le nom du tableau
+ ```N``` est le nombre de colonnes du tableau.
+ **pour appeler la fonction f qui manipule le tableau ```nomTab``` :

```c
f(nomTab, nl, nc); //nl et nc = nombre de lignes et de colonnes réellement utilisées
```

Pour ces exercices, on travaille à l’aide d’un tableau (à 2 dimensions) d’entiers **t** de taille 10x10 et de deux entiers **m** et **n** dont l’utilisateur choisit les valeurs (<= 10). L’entier **m** donnant le nombre de lignes et l’entier **n** donnant le nombre de colonnes **effectivement utilisées**. On n'utilise donc bien **qu'une partie** du tableau (ou tout le tableau dans le cas où m = n = 10).

**! On devra prendre soin de définir 10 (= taille max du tableau, lignes et colonnes) à l’aide d’un `#define`.**

Pour réaliser ces exercices, vous veillerez également à employer les techniques vues lors des précédentes séances.

Sauf si l'énoncé permet d'encoder directement du code, cette série d'exercice est à résoudre avec Visual Studio.

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


## Bête exemple pour fixer les idées

```C
#pragma warning(disable:4996)
#include <stdio.h>
#include <stdlib.h>

#define O 10

void changeValEnBasADroite(short t[][O], short nl, short nc, short val);

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
    
    changeValEnBasADroite(t, m, n, nb);
    
    printf("Tableau initialise a 0 avec nb en derniere case !");

    return 0;
}

void changeValEnBasADroite(short t[][O], short nl, short nc, short val)
{
    t[nl-1][nc-1] = val; //on ne considere bien que la partie de t allant de 0,0 jq m-1,n-1 !

    return;
}

```