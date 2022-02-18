# Sommaire📚
- [Qu'est ce qu'une boucle for ❓](#quest-ce-quune-boucle-for)
- [Le mot clé `for` 🔁](#le-mot-cle-for)
- [Iteration de vecteurs](#iteration-de-vecteurs)
    - [Qu'est ce qu'un vecteur ❓](#quest-ce-quun-vecteur)
    - [Déclarer un vecteur](#declarer-un-vecteur)
    - [Iterer sur un vecteur](#iterer-sur-un-vecteur)
    - [Iterer sur un vecteur avec l'indice 🔢](#iterer-sur-un-vecteur-avec-lindice)


# Les boucles for🔢
## Qu'est ce qu'une boucle for❓
Les boucles for sont utilisées pour itérer sur une sequence de valeurs.
## Le mot clé for🔑
Le mot clé `for` est utilisé pour créer une boucle for.

Exemple:
```rust
for count in 0..5 {
    println!("🔢 -> {}", count);
}
```
Ici, `count` est la variable qui contient la valeur courante de la boucle, et `0..5` est l'expression qui génère la séquence de valeurs à itérer.

`0..5` correspond a l'interval des nombres de 0 à 5 (5 exclus).

Sortie:
```
🔢 -> 0
🔢 -> 1
🔢 -> 2
🔢 -> 3
🔢 -> 4
```

**Il est possible de stocker une intervale dans une variable.**
```rust
let range = 0..5;
for count in range {
    println!("📢 {}", count);
}
```
Sortie:
```
📢 0
📢 1
📢 2
📢 3
📢 4
```
## Iteration de vecteurs
### Qu'est ce qu'un vecteur❓
Un vecteur est une collection de valeurs qui peuvent être itérés.
### Declarer un vecteur
Un vecteur est déclaré avec la macro `vec!` et ses valeurs sont séparées par des virgules.

Exemple:
```rust
let animals = vec!["🐒 Le Singe", "🐕 Le Chien", "🦄 La Licorne"];
```
### Iterer sur un vecteur
Pour itérer sur un vecteur, nous utilisons la boucle for.

Exemple:
```rust
let animals = vec!["🐒 Le Singe", "🐕 Le Chien", "🦄 La Licorne"];

for animal in animals.iter() {
    println!("Mon 💫 Animal Préféré 💫 est {}", animal);
}
```
Sortie:
```
Mon 💫 Animal Préféré 💫 est 🐒 Le Singe
Mon 💫 Animal Préféré 💫 est 🐕 Le Chien
Mon 💫 Animal Préféré 💫 est 🦄 La Licorne
```
> ℹ️ On utilise la méthode `iter()` pour obtenir un itérateur sur le vecteur et eviter que l'ownership du vecteur soit déplacé pour pouvoir l'utiliser apres la boucle
### Iterer sur un vecteur avec l'indice🔢
Il est possible d'itérer sur un vecteur en connaissant l'indice de la valeur courante
> ℹ️ L'indice correspond à la position de la valeur dans le vecteur et commence à 0. Il est egalement appelé index.

Nous pouvons faire ca avec la methode `enumerate()`

Exemple:

```rust
let fruits = vec!["🍎 Pomme", "🍌 Banane", "🍓 Fraise"];

for (index, fruit) in fruits.iter().enumerate() {
    println!("J'adore les {} à l'indice {}", fruit, index);
}
```
Sortie:
```
J'adore les 🍎 Pomme à l'indice 0
J'adore les 🍌 Banane à l'indice 1
J'adore les 🍓 Fraise à l'indice 2
```

> ℹ️ On utilise `(index, fruit)` car la method `enumerate()` renvoie un tuple avec l'indice et la valeur.


<!--

---

<p align="right"><a href="https://github.com/SkwalExe/apprendre-rust/tree/main/cours/les-boucles-for">Section suivante ⏭️</a></p>
-->

---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>