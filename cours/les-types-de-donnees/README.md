# Sommaire📚
- [Que sont les types de données ❓](#que-sont-les-types-de-donnees)
- [Spécifier le type de donnée d'une variable](#specifier-le-type-de-donnee-dune-variable)


# Les types de données
## Que sont les types de donnees❓
Quand nous déclarons une variable, par exemple:
```rust
let x = 5;
```
La valeur de `x` est `5`, et `5` est, biensure, un nombre.
Mais plus précisement, c'est une valeur de type `i32`, ce qui signigie que c'est un entier signé de 32 bits.

> ℹ️ Un entier non signé est un entier qui est toujours positif, tandis qu'un entier signé est un entier qui peut etre positif et negatif.

Il y a plein d'autres types de données en Rust
```
i8, i16...     -> entier signés 🔢
u8, u16...     -> entier non signés 🔢
f32, f64       -> nombre à virgule flottante 🔢
char           -> caractère 🔤
bool           -> soit vrai (true) soit faux (false) 👍👎
String         -> chaîne de caractères ✍️
```

## Specifier le type de donnee d'une variable

Quand nous déclarons une variable, nous n'avons pas besoin de spécifier son type contrairement a dans d'autres langages comme Java ou C, parce que Rust est un langage dit `autotypé`, ce qui signifie que Rust va automatiquement determiner le type de la variable.

Mais, nous pouvons quand meme saisir manuellement le type de la variable avec la syntaxe suivente :
```rust
let x: i32 = 5;
```

Il est recommendé de toujours spécifier le type des variables, c'est une bonne habitude pour eviter les erreurs.

par exemple, si l'on sait que `x` ne sera jamais negatif, on peut ecrire
```rust
let x: i32 = 5;
```





---

<p align="right"><a href="https://github.com/SkwalExe/apprendre-rust/tree/main/cours/les-structures-conditionnelles">Section suivante ⏭️</a></p>


---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>