# Simon - Jeu de rythme

Vous pouvez tester un exemple de ce jeu via ce [lien](https://codepen.io/shynonagons/pen/dGWRwV)

## Consignes 

Écrire un programme qui simule le jeu de Simon où l’utilisateur doit reproduire une séquence de symboles de plus en plus longue. À chaque tour, un nouveau symbole est ajouté à la séquence. L’utilisateur doit reproduire la séquence correctement pour continuer.

Votre code devra : 
- Choisir de manière aléatoire un caractère parmi une liste de caractères
- Definir une liste de caractères et sauvegarder cette liste pour l'enrichir
- Demander à l'utilisateur de saisir une séquence
- Vérifier que la séquence saisie par l'utilisateur est la même que celle générée
- Après un certain temps, effacer la séquence générée avant de demander à l'utilisateur de saisir la même séquence


## Astuces

:warning: Les astuces suivantes donnent des indications plus ou moins précises sur la manière de résoudre cet exercice. Essayez de les consulter seulement en cas de néccssité

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
# Déclarer un nombre maximum de caractères dans une séquence pour gagner

# Déclarer un tableau contenant des caractères possibles 

# Générer un nombre aléatoire entre 0 et la taille du tableau - 1 (l'indice des tableaux en informatique commence toujours à 0) ou choisir au hasard un caractère à deviner dans la liste

# Créer la boucle du jeu : c'est-à-dire qu'il faut une boucle avec une condition qui nous permettra au besoin d'arrêter la boucle ou de continuer tant qu'on le souhaite
# - Dans la boucle
# - # Ajouter un caractère à la séquence qu'il faut reproduire
# - # Afficher la séquence  
# - # Effacer le terminal
# - # Demander à l'utilisateur d'entrer une séquence
# - # Vérifier si l'utilisateur a saisi la bonne séquence
# - # Si oui 
# - #  | Vérifier si la taille de la séquence est égale au nombre max défini
# - #  | Si oui 
# - #     | Afficher "Gagné" et terminer la boucle 
# - # Sinon
# - # | Afficher "Perdu" et terminer la boucle
```

Il faut maintenant essayer point par point de traduire le texte précédent en instructions python.

</details>

## Sous-exercices

1.	Sélectionner au hasard un symbole dans un tableau contenant tous les symboles possibles et l’ajouter à la série déjà diffusée <br>
Créer une liste de symboles possibles.
À chaque tour, sélectionner un symbole au hasard et l’ajouter à la séquence existante.
2.	Attendre un certain temps avant d’effacer la séquence et demander à l’utilisateur de reproduire la séquence <br>
Afficher la séquence de symboles.<br>
Attendre un certain temps avant de l'effacer.<br>
Demander à l'utilisateur de saisir la séquence.
3.	Comparer la séquence de l’utilisateur avec la séquence générée<br>
Comparer la séquence entrée par l'utilisateur avec la séquence générée.<br>
Si la séquence est correcte, continuer le jeu ; sinon, terminer.
4.	Définir une taille maximale de séquence pour afficher un message de victoire quand l’utilisateur l’a atteinte <br>
Définir une longueur maximale pour la séquence.<br>
Afficher un message de victoire lorsque l'utilisateur atteint cette longueur.
 

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


# Autres opérateurs permettant de faire des conditions
test_egaux = (1 == 2)       # False
test_differents = (1 != 2)   # True
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

# Suppression avec l'indice dans la liste
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
