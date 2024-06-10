# Jeu des allumettes

## Consignes 

Écrire un programme pour simuler le jeu des allumettes, où deux joueurs (ou un joueur et un bot) retirent tour à tour 1, 2 ou 3 allumettes. Le joueur qui prend la dernière allumette perd la partie.

## Astuces

:warning: Les astuces suivantes donnent des indications plus ou moins précises sur la manière de résoudre cet exercice. Essayez de les consulter seulement en cas de nécessité

<details>
<summary>Astuce 1</summary>
Réfléchir à la logique du jeu comme une suite d'actions à réaliser.
Décrire simplement en français, point par point, les différentes étapes nécessaires.
</details>

<details>
<summary>Astuce 2</summary>
Essayer de découper le jeu en différentes parties indépendantes en simplifiant les points bloquants.
Commencer par tester et/ou écrire une étape après l'autre. 
</details>

<details>
<summary>Astuce 3</summary>
Un simple bot aurait un comportement similaire à un utilisateur qui choisirait toujours le même nombre d'allumettes ou qui jourait ses coups au hasard
</details>

<details>
<summary>Astuce 4</summary>
Ce que l'on appelle modulo est le reste de la division euclidienne.<br>
Par exemple: <br>
> 17 modulo 5 = 5 x 3 + 2 = 2 

Il existe un opérateur spécifique pour cela.
```python
print( 17 % 5 )
## > 2
```
</details>

## Sous-exercices

1.	Initialiser le nombre d’allumettes
Vérifier et définir le nombre initial d’allumettes (par exemple, 24 allumettes).
2.	Gérer les tours de chaque joueur
Retenir et afficher le nom ou le numéro du joueur pour savoir lequel doit jouer.
Permettre à chaque joueur de retirer 1, 2 ou 3 allumettes par tour.
3.	Déterminer et afficher le perdant
Déterminer le joueur qui prend la dernière allumette.
Afficher un message indiquant que ce joueur a perdu.
4.	Ajouter un bot comme adversaire
Permettre de jouer contre un bot.
Le bot doit retirer un nombre aléatoire d’allumettes (entre 1 et 3) à chaque tour.
5.	Ajouter la décision de qui commence
Permettre aux joueurs de décider qui commence la partie.
Alternativement, déterminer aléatoirement qui commence.
6.	Perfectionner le bot pour qu'il gagne toujours s’il est le deuxième utilisateur
Améliorer l'algorithme du bot pour qu'il prenne toujours le bon nombre d’allumettes afin de garantir sa victoire, s’il commence en deuxième.

## Documentation 

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
