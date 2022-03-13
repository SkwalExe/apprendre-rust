# Sommaire📚
- [Qu'est ce qu'un tuple ❓](#quest-ce-quun-tuple)
- [Déclarer un tuple](#declarer-un-tuple)
- [Acceder aux valeurs d'un tuple](#acceder-aux-valeurs-dun-tuple)
- [Extraire les valeurs d'un tuple](#extraire-les-valeurs-dun-tuple)

# Les tuples
## Qu'est-ce qu'un tuple❓
Une tuples est un type de données qui peut contenir plusieurs valeurs qui peuvent être de n'importe quel type.
> ℹ️ Les tuples sont souvent utilisés pour retourner plusieurs valeurs d'une fonction.

> ℹ️ Les tuples peuvent contenir d'autres tuples.
## Déclarer un tuple
Un tuple peut etre déclaré avec la syntaxe suivante:
```rust
let zoo = ("🦍 Gorille", "🦊 Renard", "🦓 Zebre", "🐘 Elephant");
```
## Acceder aux valeurs d'un tuple
Nous pouvons acceder aux valeurs d'un tuple avec la syntaxe suivante: `tuple.index`

Exemple, afficher la premiere valeur d'un tuple:
```rust
let zoo = ("🦍 Gorille", "🦊 Renard", "🦓 Zebre", "🐘 Elephant");

println!("Le premier animal du zoo est le {}", tuple.0);
```
Sortie:
```
Le premier animal du zoo est le 🦍 Gorille
```
## Extraire les valeurs d'un tuple🚪
Nous pouvons extraire les valeurs d'un tuple et les stocker dans des variables avec la syntaxe suivante:
```rust
let zoo = ("🦍 Gorille", "🦊 Renard", "🦓 Zebre", "🐘 Elephant");

let (a, b, c, d) = zoo;

println!("Dans le zoo il y a un {}, un {}, un {}, et un {}", a, b, c, d);
```
Sortie:
```
Dans le zoo il y a un 🦍 Gorille, un 🦊 Renard, un 🦓 Zebre, et un 🐘 Elephant
```


---

<p align="right"><a href="../les-fonctions">Section suivante ⏭️</a></p>


---


<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>