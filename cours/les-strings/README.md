# Sommaire📚

- [Qu'est-ce qu'un string❔](#quest-ce-quun-string)
- [la methode `len`](#la-methode-len)
- [la methode `is_empty`](#la-methode-is_empty)
- [la methode `split_whitespace`](#la-methode-split_whitespace)
- [la methode `contains`](#la-methode-contains)
- [la methode `push_str`](#la-methode-push_str)

# Les strings📝

## Qu'est-ce qu'un string❔

En programmation, un string est une suite de caracteres. En rust, il y a deux types de strings: `str` et `String`.

`str` est le type primitif de rust, et `String` est un type plus avancé.

Dans cette section, nous nous nous refererons uniquement au type `String`.

## la methode `len`

La methode `len` est utilisee pour obtenir la longueur d'un string, elle retourne un valeur `usize`

```rust
let nom = String::from("Léopold");

println!("Mon nom a {} caracteres", nom.len());
```

Sortie:

```
Mon nom a 8 caracteres
```

## la methode `is_empty`

La methode `is_empty` est utilisee pour verifier si un string est vide, elle retourne un bool

```rust
let nom = String::from("Léopold");
let vide = String::from("");

if nom.is_empty() {
    println!("'{}' est vide", nom);
} else {
    println!("'{}' n'est pas vide", nom);
}

if vide.is_empty() {
    println!("'{}' est vide", vide);
} else {
    println!("'{}' n'est pas vide", vide);
}
```

Sortie:

```
'Léopold' n'est pas vide
'' est vide
```

## la methode `split_whitespace`

La methode `split_whitespace` est utilisee pour separer un string en sous-string, elle retourne un iterateur

```rust
let texte = String::from("Hello world");

for mot in texte.split_whitespace() {
    println!("Mot : {}", mot);
}   
```

Sortie:

```
Mot : Hello
Mot : world
```

## la methode `contains`

La methode `contains` est utilisee pour verifier si un string contient un sous-string, elle retourne un bool

```rust
let texte = String::from("Hello world");

if texte.contains("world") {
    println!("'{}' contient 'world' ✅", texte);
} else {
    println!("'{}' ne contient pas 'world' ⛔", texte);
}
```

Sortie:

```
'Hello world' contient 'world' ✅
```

## la methode `push_str`

La methode `push_str` est utilisee pour ajouter un string a la fin d'un autre string, le string doit etre mutable car on modifie son contenu

```rust
let mut texte = String::from("Hello");

println!("{}", texte);

texte.push_str(" world");

println!("{}", texte);
```

Sortie:

```
Hello
Hello world
```

---

<p align="right"><a href="../..">Accueil 🏠</a> - <a href="../implementation-de-traits">Section suivante ⏭️</a></p>

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>
