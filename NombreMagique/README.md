# Nombre Magique

## Consignes 

Écrire un programme qui génère un nombre aléatoire entre 0 et 500 et demander à l’utilisateur de deviner ce nombre. À chaque tentative, le programme indique si le nombre deviné est plus petit ou plus grand que le nombre recherché. Si l'utilisateur trouve le bon nombre, le programme affiche « Gagné ».

Votre code devra : 
- Générer un nombre aléatoire entre 0 et 500
- Demander à l'utilisateur de saisir un nombre
- Vérifier que le nombre saisi par l'utilisateur est entre 0 et 500 
- Afficher les consignes à l'utilisateur pour qu'il sache qu'il lui faut deviner un nombre et dans quelles conditions
- Afficher un message si le nombre est plus petit
- Afficher un message si le nombre est plus grand 
- Afficher un message si le nombre ne répond pas à la consigne (entre 0 et 500)
- Afficher un message en cas de réussite
- Répeter la partie "Demande à l'utilisateur" et "Vérification du nombre saisi" tant qu'il n'a pas trouvé la solution

## Astuces

:warning: Les astuces suivantes donnent des indications plus ou moins précises sur la manière de résoudre cet exercice. Essayez de les consulter seulement en cas de nécessité

<details>
<summary>Astuce 1</summary>
Réfléchir à la logique du jeu comme une suite d'actions à réaliser.
Décrire simplement en français, point par point, les différentes étapes nécessaires.
Pour commencer, vous pouvez définir un nombre fixe à deviner comme "42" par exemple.
</details>

<details>
<summary>Astuce 2</summary>
Commencer par tester et/ou écrire une étape après l'autre : afficher une phrase, demander à l'utilisateur un nombre, etc.
</details>

<details>
<summary>Astuce 3</summary>
La logique du jeu peut se retranscrire en français avec les étapes suivantes :

```python 
# Générer un nombre aléatoire ou définir un nombre puis stocker la valeur dans une variable 

# Créer la boucle du jeux : c'est-à-dire qu'il faut une boucle avec une condition qui nous permettra au besoin d'arrêter la boucle ou de continuer tant qu'on le souhaite
# - Dans la boucle
# - # Demander à l'utilisateur d'entrer une valeur
# - # Vérifier si la valeur respecte les critères d'être entre 0 et 500 
# - # Si oui 
# - #  | Vérifier si le nombre de l'utilisateur est égal au "nombre magique"
# - #  | Si oui 
# - #  |   | Afficher le message "Gagné !" et mettre fin à la boucle
# - #  | 
# - #  | Sinon 
# - #  |   | Vérifier si le nombre est plus petit
# - #  |   | Si oui
# - #  |   |   | Afficher que le nombre saisi est plus petit 
# - #  |   | Sinon
# - #  |       | Afficher que le nombre saisi est plus grand 
# - # Sinon
# - #  | Afficher que le nombre saisi n'est pas entre 0 et 500
```

Il faut maintenant essayer point par point de traduire le texte précédent en instructions python.

</details>

## Sous-exercices

1.	Génération du nombre aléatoire <br>
Générer un nombre aléatoire compris entre 0 et 500 et le stocker dans une variable.
2.	Lire une entrée de l’utilisateur en Python <br>
Utiliser une fonction pour lire une entrée de l'utilisateur.
3.	Demander à l’utilisateur de saisir un nombre et afficher ce nombre <br>
Demander à l'utilisateur de saisir un nombre.<br>
Afficher ce nombre pour confirmer la saisie.
4.	Comparer le nombre entré avec le nombre sélectionné à l'étape 1 et afficher le résultat <br>
Comparer le nombre entré par l'utilisateur avec le nombre aléatoire généré. <br>
Afficher « Plus grand » si le nombre entré est plus petit que le nombre aléatoire.<br>
Afficher « Plus petit » si le nombre entré est plus grand que le nombre aléatoire.
5.	Ajouter une boucle pour continuer tant que le nombre n’est pas trouvé <br>
Utiliser une boucle pour répéter les étapes de saisie et de comparaison jusqu'à ce que l'utilisateur trouve le bon nombre.
6.	Ajouter un cas d’arrêt lorsque le nombre est trouvé <br>
Ajouter une condition pour sortir de la boucle lorsque l'utilisateur a trouvé le nombre.<br>
Afficher « Gagné » lorsque le nombre est correctement deviné.


## Documentation 

### Fonction de génération de nombre aléatoire 

```python
# -- Déclaration avant utilisation d'une fonction dans une librairie existante
from random import randint

# -- Valeur aléatoire entre 0 et 10 
valeur_aleatoire = randint(0, 10)
```

Vous pouvez trouver la documentation officielle de cette fonction [ici](https://docs.python.org/3/library/random.html#random.randint) ou une autre documentation avec des exemples d'utilisation via ce [lien](https://www.w3schools.com/python/ref_random_randint.asp).

### Rappels 

#### Condition IF-ELSE

```python
if nombre > 5 :
    # Ce code est utilisé seulement si la valeur qui correspond à la variable "nombre" est supérieure à 5
    print(ꞋLe nombre est plus grand que 5Ꞌ)
else :
    # Sinon c'est ce code qui est utilisé
    print(ꞋLe nombre est inférieur ou égal à 5Ꞌ)

```

#### Boucle conditionnelle WHILE

```python
# Si la condition est vraie le code ci-dessous est utilisé
# on exécute le code tant que la condition est vraie
# Sinon on sort de la boucle
while (compteur < 5) : 
    print(compteur)
    compteur += 1
```
