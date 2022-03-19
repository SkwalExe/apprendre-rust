# Sommaire📚

- [Qu'est ce qu'un vecteur❔](#quest-ce-quun-vecteur)
- [Declarer un vecteur](#declarer-un-vecteur)
- [Declarer un vecteur avec des valeurs](#declarer-un-vecteur-avec-des-valeurs)
- [Acceder aux elements](#acceder-aux-elements)
- [Joindre des elements](#joindre-des-elements)
- [Ajouter des elements](#ajouter-des-elements)
- [Retirer des elements🗑](#retirer-des-elements)

# Les vecteurs

## Qu'est ce qu'un vecteur❔

Un vecteur est une structure de données qui peut contenir plusieurs éléments du meme types.

## Declarer un vecteur

Pour déclérer un vecteur, on utilise le type `Vec<T>` ou `T` est le type des elements du vecteur.

```rust
let mut my_vector: Vec<String> = Vec::new();
```

> ℹ️ Nous devons rendre le vecteur mutable pour utiliser les methodes qui le modifient.

> ℹ️ La macro `Vec::new()` crée un vecteur vide.

## Declarer un vecteur avec des valeurs

Déclarer un vecteur avec des valeurs par defaut est beaucoup plus simple.

Et le type des elements du vecteur sera determiné automatiquement.

```rust
let mut my_vector = vec!["Hello", "World"]; 
```

> ℹ️ La macro `vec!` crée un vecteur avec des valeurs données.

## Acceder aux elements

```rust
let mut my_vector = vec!["Hello", "World"];
println!("{} 👋", my_vector[0]);
```

> ℹ️ On utiliser `[]` pour acceder a un element du vecteur avec son index.

Sortie:

```
Hello 👋
```

## Joindre des elements

Pour joindre les elements d'un vecteur avec un separateur spécific, on utilise la methode `join`, cette methode renvoie une chaine de caractere.

```rust
let mut my_vector = vec!["Hello", "World"];
println!("{}", my_vector.join("!"));
println!("{}", my_vector.join("->"));
println!("{}", my_vector.join(" "));
```

Sortie:

```
Hello!World
Hello->World
Hello World
```

## Ajouter des elements

Pour ajouter des elements a la fin d'un vecteur, on utilise la methode `push`.

```rust 
let mut my_vector = vec!["I", "Love"];
my_vector.push("Rust");
println!("{} 💖", my_vector.join(" "));
```

Sortie:

```
I Love Rust 💖
```

## Retirer des elements🗑

Pour retirer un element du vecteur avec son index, on utilise la methode `remove`.

```rust
let mut my_vector = vec!["I", "Love", "Rust"];
my_vector.remove(1);
println!("{} 💖", my_vector.join(" "));
```

Sortie:

```
I 💖 Rust
```

---

<p align="right"><a href="https://skwalexe.github.io/apprendre-rust/">Accueil 🏠</a> - <a href="../lire-un-fichier">Section suivante ⏭️</a></p>

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>
