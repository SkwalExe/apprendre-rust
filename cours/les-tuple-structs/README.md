# Sommaire📚
- [Qu'est-ce qu'un tuple struct ❓](#quest-ce-quun-tuple-struct)
- [Comment créer un tuple struct ❓](#comment-creer-un-tuple-struct)
- [Comment utiliser un tuple struct 🤹](#comment-utiliser-un-tuple-struct)
- [Comment modifier un tuple struct ✏️](#comment-modifier-un-tuple-struct)


# Les tuples structs🧱
## Qu'est-ce qu'un tuple struct❔
Les tuples structs sont similaires aux structs, mais ils sont utilisés pour grouper les données dans un tuple, et sans un nom pour les champs.
## Comment créer un tuple struct❔
Nous pouvons créer un tuple struct en utilisant la clé `struct` et ensuite le nom du tuple struct capitalisé, suivi d'un tuple les types des propriétés.
```rust
struct Color(u8, u8, u8);
//           r   g   b
```
## Comment utiliser un tuple struct🤹
Nous pouvons créer une instance du tuple struct avec la syntaxe suivante:
```rust
let black = Color(0, 0, 0);
```
Nous pouvons accéder aux valeurs du tuple struct en utilisant l'opérateur de pointage et l'index `struct.index` :
```rust
println!("🟥 Red value : {}", black.0);
println!("🟩 Green value : {}", black.1);
println!("🟦 Blue value : {}", black.2);
```
Sortie:
```
🟥 Red value : 0
🟩 Green value : 0
🟦 Blue value : 0
```
## Modifier un tuple struct✏️
Par défaut, comme les variables, les tuple structs sont immuables.
Donc nous avons à les rendre mutables en ajoutant la clé `mut` avant le nom du tuple struct lors de sa création.
```rust
// déclarer une instance du tuple struct
let mut black = Color(0, 0, 0);
// modifier la valeur du premier champ
black.0 = 255;
```

<!--

---

<p align="right"><a href="https://github.com/SkwalExe/apprendre-rust/tree/main/cours/les-tuple-structs">Section suivante ⏭️</a></p>
-->

---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>