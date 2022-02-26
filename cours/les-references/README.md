# Sommaire📚
- [Qu'est ce qu'une reference ❔](#quest-ce-quune-reference)
- [Comment créer une reference ❔](#comment-creer-une-reference)
- [Comment utiliser une reference 🤹](#comment-utiliser-une-reference)
- [Modifier une reference ✏️](#modifier-une-reference)
    - [Premierement](#premierement)
    - [Deuxiemement](#deuxiemement)
- [Attention ⚠️](#attention)
    - [Premierement](#premierement)
    - [Deuxiemement](#deuxiemement)


# Les references🔗
## Qu'est ce qu'une reference❔
Une reference est juste un autre moyen d'acceder a une variable, les references sont similaires aux pointeurs dans d'autres langages.

Par exemple si votre chien 🐕 s'appelle `Domenic`, et que vous l'appelez `Dom`, vous vous referez toujours au lui. Donc `Dom` est une reference vers `Domenic`.

```
Dom ---------> Domenic
               Votre chien 🐕
```

Ce principe est le meme pour les variables.

## Comment creer une reference❔
Premièrement, on doit creer une variable.
```rust
let domenic = "Petit chien 🐶";
```
Puis, nous créons une reference a la variable en ajoutant un `&` avant le nom de la variable.
```rust
let mut dom = &domenic;
```
Le signe `&` indique que nous voulons avoir une reference a la variable.

Nous avons donc maintenant une variable `dom` qui contient une reference vers la variable `domenic`.

## Comment utiliser une reference🤹
Nous pouvons utiliser la reference pour, par exemple, acceder a la valeur de la variable.
Par exemple, si nous voulons afficher la valeur de la variable `domenic` en utilisant la reference `dom`, nous allons faire:
```rust
println!("La valeur de dom est {}", dom);
println!("La valeur de domenic est {}", domenic);
```
La sortie sera:
```
La valeur de dom est Petit chien 🐶
La valeur de domenic est Petit chien 🐶
```

> ℹ️ Nous pouvons avoir plusieurs references a la meme variable.

## Modifier une reference✏️
`dom`, etant une reference vers la variable `domenic`, on pourrait croire que nous pouvons modifier sa valeur en faisant:
```rust
dom = "Gros chien 🐕";
```
Cependant, cela ne marhera pas.
### Premierement
Car par defaut, une reference est immutable, nous ne pouvons donc pas modifier la valeur de la variable a laquelle elle fait reference.

Pour faire une reference mutable, nous devons ajouter un `mut` avant le nom de la variable.

```rust
let dom = &mut domenic;
```
Maintenant, nous pouvons modifier la valeur de la variable.

## Deuxiemement
Quand nous faisons 
```rust
dom = "Gros chien 🐕";
```
Nous ne modifions pas la valeur de la variable `domenic` mais la valeur de la variable `dom` qui est une reference vers `domenic`.

#### **Avant**
```
Dom             Domenic
--------------> "Petit chien 🐶"
```
#### **Après**
```
Dom              Domenic
"Gros chien 🐕"  "Petit chien 🐶"
```

Pour modifier la valeur de la variable `domenic`, nous devons utiliser le signe `*` devant le nom de la variable.
```rust
*dom = "Gros chien 🐕";
```

Parce que `*dom` veut dire que nous nous referons a **la valeur** de `domenic` et non a la reference `dom`.

## Attention⚠️
### Premierement
Nous ne pouvons pas avoir plus d'une reference mutable a la meme variable.
### Deuxiemement
Nous ne pouvons utiliser qu'une reference mutable en meme temps selon la version de rustc.

Dans l'exemple suivant
```rust
let mut username = "Username super cool 💪";
let mut username_ref = &mut username;

println!("L'username est : {}", username);
```

Nous rencontrerons une erreur car la macro `println!` empreinte la variable `username` mais nous avont deja une reference mutable a la variable `username`.

<!--

---

<p align="right"><a href="https://github.com/SkwalExe/apprendre-rust/tree/main/cours/les-references">Section suivante ⏭️</a></p>
-->

---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>