# Exercice 1 : AFFICHAGE D’UN TABLEAU LIGNE PAR LIGNE

+ Lire `m` et `n`, les nombres de lignes et de colonnes utiles d'un tableau `t`.
+ L'initialiser dans le `main()` avec des valeurs aléatoires comprises entre **1** et **100**, par indices.
+ Afficher ces éléments ligne par ligne, via une fonction qui reçoit `t` en paramètre.


<details>
<summary>Spoiler : une solution type !</summary>

```C runnable
#include <stdio.h>

#define O 10
#define RANDMAX 100

void afficheTableau(short t[][O], short nl, short nc);

//NB : "O" comme "Ordre" du tableau (quand le nombre de lignes et de colonnes sont égaux à n, on parle d'un "tableau d'ordre n")

int main()
{
    short t[O][O] = { 0 };
    short m, n, i, j;

    printf("nombre de lignes du tableau (<=%d): ", O);
    scanf("%hd", &m);

    printf("nombre de colonnes du tableau (<=%d): ", O);
    scanf("%hd", &n);

    // Parcours classique, lignes x colonnes, par indices :
    for (i = 0; i < m; i++) { // pour chaque ligne :
        for (j = 0; j < n; j++) {
            t[i][j] = rand() % RANDMAX + 1;
        }
    }

    printf("\n\n\nLe tableau :\n");

    afficheTableau(t, m, n);

    return 0;
}

void afficheTableau(short t[][O], short nl, short nc)
{
    short i, j;

    for (i = 0; i < nl; i++) {
        for (j = 0; j < nc; j++) {
            printf("%3.hd ", t[i][j]);
        }
        printf("\n");
    }

    return;
}

```