# Chiffrement de César

## Consignes 

Écrire un programme qui chiffre et déchiffre un message en utilisant le chiffrement de César. Tester le programme sur un ensemble de données fournies pour retrouver tous les textes originaux sans connaître la valeur de la clef de chiffrement.

Chacun des textes suivants ont été encodés avec une clef différente. Il faut essayer de retrouver le texte d'origine.

```python
textes = [
    'Fkyiiubuiehjlekiujhuvqlehqrbu',
    'Cfzuonvyuowiojxywioluayjioluzzlihnylmymyhhygcmgucmcfyhzuonnionuonuhnjioluzzlihnylmymugcm',
    'Nmmdunhsahdmptzudbkdbtqkdrrdmshdkdrshmuhrhakdontqkdrxdtw',
    'Bqhufediuqbqwhqdtugkuijyedtubqlyutubkdyluhiujtujekjbuhuijuuijgkqhqdjutukn',
    'Qsbsghdogzodsftsqhwcbeiwqcadhsqsghzozihhsdcifrsjsbwfeiszeiibrsawsileisqseisbciggcaasg'
]
```

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
Commencer par tester et/ou écrire une étape après l'autre. 
Tester la méthode "brute-force" qui consiste à afficher le texte avec toutes les clés possibles.
</details>

<details>
<summary>Astuce 3</summary>
Dans la langue française, on utilise des lettres plus fréquemment que d'autres (cf: [Fréquence d'apparition des lettres](https://fr.wikipedia.org/wiki/Fr%C3%A9quence_d%27apparition_des_lettres)). C'est le cas par exemple pour le 'e', 'a', 'i' ou le 's'.

Avec cette information, ajouter de l'intelligence à votre programme pour n'afficher que le bon texte en cas de décodage mais laissez le choix à l'utilisateur de choisir une clef pour encoder un message avec le même programme.
</details>

## Sous-exercices

1.	Associer les lettres de l'alphabet à leur position
Créer une correspondance entre chaque lettre de l'alphabet et sa position (A = 0, B = 1, ..., Z = 25).
Définir une clef de chiffrement entre 1 et 26
Choisir une clef de chiffrement aléatoire ou spécifiée par l'utilisateur.
2.	Chiffrer un texte avec la clef donnée
Pour chaque lettre du texte, additionner sa position avec la clef, puis appliquer le modulo 26.
Remplacer chaque lettre par la nouvelle lettre obtenue.
3.	Déchiffrer un texte avec la clef donnée
Pour chaque lettre du texte chiffré, soustraire la clef de sa position, puis appliquer le modulo 26.
Remplacer chaque lettre par la lettre obtenue.
4.	Tester sur un ensemble de données fournies pour retrouver tous les textes originaux sans connaître la valeur de la clef de chiffrement
Pour chaque texte chiffré, essayer toutes les valeurs de clef possibles (1 à 26) pour retrouver le texte original.
Afficher tous les textes déchiffrés pour chaque valeur de clef.
5.	Bonus : Ajouter de l’intelligence avec l’étude du nombre d’occurrences des e, s ou t en français
Analyser la fréquence des lettres dans le texte déchiffré.
Utiliser les lettres les plus fréquentes en français (comme 'e', 's', 't') pour déterminer plus simplement la clef de chiffrement si celle-ci n’a pas été donnée.


## Documentation 

### Rappels 

#### Modulo

Ce qu'on appelle modulo est le reste de la division euclidienne.<br>
Par exemple: <br>
> 17 modulo 5 = 5 x 3 + 2 = 2 

Il existe un opérateur spécifique pour cela.
```python
print( 17 % 5 )
## > 2
```


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
