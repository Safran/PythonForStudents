# Pendu

## Consignes 

Écrire un programme qui sélectionne un mot au hasard dans un tableau de mots et permettre à l’utilisateur de deviner ce mot lettre par lettre.  
Indiquer la position de chaque lettre trouvée dans le mot et le nombre de lettres incorrectes. Afficher un message « Perdu » après 10 ou 12 échecs, et « Gagné » si l’utilisateur trouve le mot.

Votre code devra : 
- Choisir de manière aléatoire un mot parmi une liste de mots
- Demander à l'utilisateur de saisir une lettre
- Sélectionner la première lettre d'un mot
- Vérifier que la lettre saisie par l'utilisateur est dans le mot
- Sauvegarder les lettres trouvées et leur position pour les afficher
- Afficher le caractère "_" pour les lettres non trouvées
- Afficher le nombre d'échecs ou un dessin correspondant au nombre d'échecs 


## Astuces

:warning: Les astuces suivantes donnent des indications plus ou moins précises sur la manière de résoudre cet exercice. Essayez de les consulter seulement en cas de néccessité

<details>
<summary>Astuce 1</summary>
Réfléchir à la logique du jeu comme une suite d'actions à réaliser.
Décrire simplement en français, point par point, les différentes étapes nécessaires.
</details>

<details>
<summary>Astuce 2</summary>
Essayer de découper le jeu en différentes parties indépendantes en simplifiant les points bloquants.
Commencer par tester et/ou écrire une étape après l'autre : afficher une phrase, demander à l'utilisateur une entrée, récupérer un mot, etc.
</details>

<details>
<summary>Astuce 3</summary>
Vous pouvez soit choisir un élément au hasard dans un tableau à l'aide de la fonction [<code>choice</code>](https://www.w3schools.com/python/ref_random_choice.asp) soit choisir au hasard un indice dans le tableau avec la fonction [<code>randint</code>](https://www.w3schools.com/python/ref_random_randint.asp) utilisée dans l'exercice du nombre magique.

```python
from random import choice, randint

tableau = ["1er élément", "2ème élément", "3ème élément", "4ème élément", "5ème élément"]
element_au_hasard = choice( tableau )

# len() donne la taille d'un tableau
# l'indice d'un tableau commence à 0 et termine à la taille du tableau - 1
indice_au_hasard = randint(0, len(tableau)-1 )
autre_element_depuis_un_indice_aleatoire = tableau[indice_au_hasard]
```
</details>

<details>
<summary>Astuce 4</summary>
Quelques petites manipulations possibles avec un tableau ou avec un texte.

```python
texte = "Hunger Games"

# Transformation d'un texte en un tableau de caractères
tableau_depuis_un_texte = list(texte)
print(tableau_depuis_un_texte)
## > ['H','u','n','g','e','r',' ','G','a','m','e','s']

# Par défaut un texte est considéré comme un tableau 
print( texte[0] )
## > 'H' 

# Il est possible de réécrire des éléments d'un tableau avec l'indice de l'élément
tableau_depuis_un_texte[0] = 'h'
tableau_depuis_un_texte[1] = 'U'
print(tableau_depuis_un_texte)
## > ['h','U','n','g','e','r',' ','G','a','m','e','s']

# Transformation du texte en minuscules
print(texte.lower())
## > "hunger games"

# Transformation du texte en majuscules
print(texte.upper())
## > "HUNGER GAMES"
```
</details>

<details>
<summary>Astuce 5</summary>
La logique du jeu peut se retranscrire en français avec les étapes suivantes :

```python 
# Déclarer un tableau contenant des mots possibles 

# Générer un nombre aléatoire entre 0 et la taille du tableau - 1 (l'indice des tableaux en informatique commence toujours à 0) ou choisir au hasard un mot à deviner dans la liste

# Créer la boucle du jeu : c'est-à-dire qu'il faut une boucle avec une condition qui nous permettra au besoin d'arrêter la boucle ou de continuer tant que l'on souhaite
# - Dans la boucle
# - # Afficher le mot mystère en cachant les lettres non trouvées
# - # Demander à l'utilisateur d'entrer une lettre
# - # Vérifier si valeur respecte le critère d'être une lettre
# - # Si l'utilisateur a saisi une seule lettre
# - #  | Vérifier si la lettre est dans le mot
# - #  | Si oui
# - #  |   | Sauvegarder la lettre trouvée 
# - #  |   | Vérifier si le mot est complet
# - #  |     | Si oui 
# - #  |       | Afficher "Gagné" et arrêter la boucle de jeu
# - #  |     | Sinon
# - #  |       | Ajouter 1 au nombre d'erreurs
# - #  |       | Afficher le nombre d'erreurs
# - #  |       | Vérifier si le nombre d'erreurs est égal ( == ) au nombre d'erreurs max
# - #  |         | Si oui 
# - #  |           | Afficher "Perdu" et arrêter la boucle de jeu
# - #  | Sinon
# - #  |  | Ajouter 1 au nombre d'erreurs
# - #  |  | Afficher le nombre d'erreurs
# - #  |  | Vérifier si le nombre d'erreurs est égal ( == ) au nombre d'erreurs max
# - #  |    | Si oui 
# - #  |      | Afficher "Perdu" et arrêter la boucle de jeu
# - # Si l'utilisateur a saisi un mot 
# - #  | Vérifier si le mot entré correspond au mot à deviner
# - #  |   | Si oui 
# - #  |     | Afficher "Gagné" et arrêter la boucle de jeu
# - #  |   | Sinon
# - #  |     | Afficher "Perdu" et arrêter la boucle de jeu

```

Il faut maintenant essayer point par point de traduire le texte précédent en instructions python.

</details>

## Sous-exercices

1.	Sélectionner un mot au hasard dans un tableau contenant des mots <br>
Créer une liste de mots.<br>
Sélectionner un mot au hasard dans cette liste et le stocker dans une variable.
2.	Questionner l’utilisateur pour récupérer une lettre<br>
Demander à l'utilisateur de saisir une lettre.<br>
S'assurer que l'utilisateur entre une seule lettre.
3.	Indiquer la position de chaque lettre trouvée dans le mot<br>
Comparer la lettre saisie avec les lettres du mot.<br>
Si la lettre se trouve dans le mot, afficher sa position dans le mot.
4.	Indiquer le nombre de lettres qui n’appartiennent pas au mot<br>
Garder une trace du nombre de tentatives incorrectes.<br>
Afficher le nombre de lettres incorrectes après chaque tentative.
5.	Ajouter une boucle pour continuer tant que le mot n’est pas trouvé ou que le nombre d’échecs n’est pas atteint<br>
Utiliser une boucle pour permettre à l'utilisateur de continuer à deviner les lettres.<br>
Arrêter la boucle si l'utilisateur trouve le mot ou atteint le nombre maximal d'échecs.
6.	Ajouter un cas d’arrêt lorsque le mot est trouvé ou que le nombre d’échecs est atteint<br>
Afficher un message « Gagné » si l'utilisateur trouve toutes les lettres du mot.<br>
Afficher un message « Perdu » si l'utilisateur atteint le nombre maximal d'échecs.

 


## Documentation 

### Fonction de génération de nombre aléatoire 

```python
# -- Déclaration avant utilisation d'une fonction dans une librairie existante
from random import randint

# -- Valeur aléatoire entre 0 et 10 
valeur_aleatoire = randint(0, 10)
```

Vous pouvez trouver la documentation officielle de cette fonction [ici](https://docs.python.org/3/library/random.html#random.randint) ou une autre documentation avec des exemples d'utilisation via ce [lien](https://www.w3schools.com/python/ref_random_randint.asp).

### Fonction de sélection aléatoire d'élément dans une liste ou un tableau
```python
from random import choice

liste = ["1er élément", "2ème élément", "3ème élément", "4ème élément", "5ème élément"]
element_au_hasard = choice( liste )
```

Vous pouvez trouver la documentation officielle de cette fonction [ici](https://docs.python.org/3/library/random.html#random.choice) ou une autre documentation avec des exemples d'utilisation via ce [lien](https://www.w3schools.com/python/ref_random_choice.asp).

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

#### Boucle dans un ensemble de valeurs FOR IN

```python
# On exécute le code pour chaque élément de la liste
for lettre in ['l','i', 's', 't', 'e']: 
    print(lettre)
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

#### Manipulation de liste

```python
liste = [0, 1, 2, 3, 4]

# Ajout d'un élément au début d'une liste
liste.insert(0, -1)

# Ajout d'un élément à la fin d'une liste 
liste.append(5)

print(liste)
## > [-1, 0, 1, 2, 3, 4, 5]

# Modification 
liste[0] = 10 

print(liste)
## > [10, 0, 1, 2, 3, 4, 5]

## Suppression avec l'indice dans la liste
liste.pop(1)

print(liste)
## > [10, 1, 2, 3, 4, 5]

## Suppression avec un élément dans la liste
liste.remove(10)

print(liste)
## > [1, 2, 3, 4, 5]
```

Documentation :
- [Ajout dans une liste](https://www.w3schools.com/python/python_lists_add.asp)
- [Suppression dans une liste](https://www.w3schools.com/python/python_lists_remove.asp)
