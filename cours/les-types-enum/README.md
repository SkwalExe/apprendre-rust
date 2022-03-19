# Sommaire📚

- [Qu'est ce qu'un enum❓](#quest-ce-quun-enum)
- [Declarer un enum](#declarer-un-enum)
- [Matcher un enum](#matcher-un-enum)
  - [Qu'est ce qu'une expression match❓](#quest-ce-quune-expression-match)
  - [Usage](#usage)
  - [Matcher un enum](#matcher-un-enum-1)

# Les types enum

## Qu'est ce qu'un enum❓

Les enums sont un moyen d'exprimer son code d'une facon descriptive et simple.
Ce sont un moyen de regrouper des valeurs similaires.

## Declarer un enum

Un enum est déclaré avec le mot clé `enum`, suivi du nom de l'enum et d'une liste de variantes.

Exemple:

```rust
enum Animal {
    Singe,
    Chien,
    Licorne
}
```

> ℹ️ Le nom de l'enum et des variantes sont conventionnellement capitalisés.

Nous pouvons maintenant utiliser l'enum pour déclarer des variables de types `Animal`.

```rust
let animal:Animal = Animal::Singe;
```

> ℹ️ On utilise l'operatuer `::` pour indiquer qu'on veut utiliser un variante de l'enum (`Singe` dans notre cas).

## Matcher un enum

### Qu'est ce qu'une expression match❓

Le mot clé `match` permet d'executer differents blocs de code en fonction de la valeur d'une variable.

> ℹ️ C'est similaire aux `switch` en d'autres langages.

### Usage

```rust
match variable {
    valeur => {
        // Bloc de code à executer si variable est egale a valeur
    }
    valeur2 => {
        // Bloc de code à executer si variable est egale a valeur2
    }
    _ => {
        // faire quelque chose d'autre
    }
}
```

> ℹ️ On peut ignorer les `{}` si l'on n'attend qu'une line de code.

> ℹ️ Le `_` est un jocker, il est la valeur par defaut si aucune autre valeur de match. 

### Matcher un enum

On peut utiliser le mot clé `match` pour matcher un enum.

```rust
match animal {
    Animal::Singe => println!("🐒 Le Singe"),
    Animal::Chien => println!("🐕 Le Chien"),
    Animal::Licorne => println!("🦄 La Licorne"),
    _ => println!("🤔 Je ne connais pas cet animal")
}
```

Voici l'execution de ce code avec les differentes valeurs que peut avoir la variaable `animal`:

| Valeur            | Sortie                           |
| ----------------- | -------------------------------- |
| `Animal::Singe`   | `🐒 Le Singe`                     |
| `Animal::Chien`   | `🐕 Le Chien`                     |
| `Animal::Licorne` | `🦄 La Licorne`                   |
| Autre             | `🤔 Je ne connais pas cet animal` |

---

<p align="right"><a href="../les-constantes">Section suivante ⏭️</a></p>

---

<p align="right">Cours créé par <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a></p>