# Exercice 1 : AFFICHAGE D’UN TABLEAU LIGNE PAR LIGNE

+ Lire `m` et `n`, les nombres de lignes et de colonnes utiles d'un tableau `t`.
+ L'initialiser dans le `main()` avec des valeurs aléatoires comprises entre **1** et **100**, par indices.
+ Afficher ces éléments ligne par ligne, via une fonction qui reçoit `t` en paramètre.


<details>
<summary>Spoiler : une solution type !</summary>

```C runnable
#include <stdio.h>

int main() {
	int a = 55, b = 66, c = 77;

	printf("L'adresse de a avant incrémentation : %p\n", &a);
	printf("L'adresse de b avant incrémentation : %p\n", &b);
	printf("L'adresse de c avant incrémentation : %p\n", &c);

	a++;
	b++;
	c++;

	printf("\nL'adresse de a après incrémentation :  %p\n", &a);
	printf("L'adresse de b après incrémentation :  %p\n", &b);
	printf("L'adresse de c après incrémentation :  %p\n", &c);

	return 0;
}

```