# Table of Contents 📚

- [Qu'est ce qu'un array❔](#quest-ce-quun-array)
- [Declarer un array](#declarer-un-array)
- [Acceder a un array](#acceder-a-un-array)
- [Iterer sur un array🔁](#iterer-sur-un-array)
  - [Avec la methode iter🛠️](#avec-la-methode-iter️)
  - [Iterer avec la longueur d'un array🔢](#iterer-avec-la-longueur-dun-array)
- [Specifier le type et la longueur d'un array](#specifier-le-type-et-la-longueur-dun-array)
- [Valeurs par defaut d'un array🐧](#valeurs-par-defaut-dun-array)

# Les arrays 📜

## Qu'est ce qu'un array❔

Un array est une collection d'items du meme type. Les arrays sont simimaires au tuples, mais les tuples peuvent contenir des items de different types.

## Declarer un array 

Pour déclarer un array, on utilisa la syntaxe suivante:

```rust 
let array_objets = ['👓', '👕', '🧽', '🩴', '🧲'];
```

## Acceder a un array

Pour acceder a un element d'un array, on utilise l'index de cet element.

```rust
println!("J'aime les {} et les {}", array_objets[0], array_objets[1]);
                                                 ^                ^
```

Sortie: 

```
j'aime les 👓 et les 👕
```

## Iterer sur un array🔁

### Avec la methode iter🛠️

Pour iterer sur un array, on utilise la fonction `.iter()` dans une boucle for.

```rust
for item in array_objets.iter() {
    println!("J'ai acheté des {}", item);
}
```

Sortie: 

```
J'ai acheté des 👓
J'ai acheté des 👕
J'ai acheté des 🧽
J'ai acheté des 🩴
J'ai acheté des 🧲
```

### Iterer avec la longueur d'un array🔢

Pour iterer sur un array, on peut aussi utiliser la fonction `.len()` pour obtenir la longueur de l'array 

```rust
for i in 0..array_objets.len() {
  println!("J'ai acheté des {}", array_objets[i]);
}
```

Ici, nous itérons sur une intervalle de 0 à la longueur de l'array.
Nous accedons ensuite a l'element avec l'index `i` de l'array.

Sortie: 

``` 
J'ai acheté des 👓
J'ai acheté des 👕
J'ai acheté des 🧽
J'ai acheté des 🩴
J'ai acheté des 🧲
```

## Specifier le type et la longueur d'un array

Nous pouvons spécifier le type et la longueur d'un array quand nous le declarons avec la syntaxe suivante : `let array: [type; longueur] = [];`

```rust
let array_objets: [char; 5] = ['👓', '👕', '🧽', '🩴', '🧲'];
```

## Valeurs par defaut d'un array🐧

Nous pouvons aussi remplir un array de taille `x` avec des valeurs par defaut.

```rust
let armee_de_pingouins = ['🐧'; 20];
```

Nous avons ici créé un array de 20 pingouins.

Pour voir a quoi ressemble notre array, on peut utiliser un jocker different pour la fonction `println!`: 

```rust
println!("{:?}", armee_de_pingouins);
```

> ℹ️ Le jocker `:?` permet d'afficher une variable selon ce a quoi elle ressemblerai dans le code.

Sortie:

```
['🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧', '🐧']
```

Nous pouvons voir une armée de pingouins 🔫🐧.

---

<p align="right"><a href="/">Accueil 🏠</a> - <a href="../les-methodes-struct">Section suivante ⏭️</a></p>

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>
