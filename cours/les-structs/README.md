# Sommaire📚
- [Qu'est ce qu'un struct ❔](#quest-ce-quun-struct)
- [Comment créer un struct ❔](#comment-creer-un-struct)
- [Comment utiliser un struct 🤹](#comment-utiliser-un-struct)
- [Modifier un struct ✏️](#modifier-un-struct)

# Les structs🧱
## Qu'est ce qu'un struct❔
Les structs sont un moyen de regrouper les valeurs en relation dans un seul type de données.
## Comment creer un struct❔
On sait qu'un utilisateur peut avoir un nom d'utilisateur et un email.
Donc nous pouvons creer un struct pour représenter ces données plutot que d'avoir deux variables.

Pour créer un struct, on utilise le mot clé `struct` suivi du nom du struct.
```rust
struct User {
    username: str,
    email: str,
}
```
> ℹ️ Les structs sont déclarés en dehors de la fonction main.

> ℹ️ Les noms des structs doivent etre capitalisés.

## Comment utiliser un struct🤹
Maintenant que nous avons un struct, nous pouvons en créer une instance.
Imaginons avoir un utilisateur avec le nom `Bob 🐡` et l'email `boblepoisson@skwal.net`
```rust
let bob = User {
    username: "Bob 🐡",
    email: "boblepoisson@skwal.net",
};
```
Nous pouvons acceder aux valeurs d'un struct avec la syntaxe `struct.nom_de_la_valeur`.
```rust
println!("Le nom de l'utilisateur est {}", bob.username);
```
La sortie sera:
```
Le nom de l'utilisateur est Bob 🐡
```

## Modifier un struct✏️
Par defaut, comme les variables, les structs sont immutable.
Nous devons donc les rendre mutable en ajoutant un `mut` avant le nom du struct quand en crée une instance.

```rust
let mut bob = User {
    username: "Bob 🐡",
    email: "boblepoisson@skwal.net",
};

bob.username = "Bob le poisson 🐡";

println!("Le nouveau nom d'utilisateur est : {}", bob.username);
```
Sortie:
```
Le nouveau nom d'utilisateur est : Bob le poisson 🐡
```


---

<p align="right"><a href="https://github.com/SkwalExe/apprendre-rust/tree/main/cours/les-tuple-structs">Section suivante ⏭️</a></p>


---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>