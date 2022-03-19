# Sommaire📚

- [Qu'est ce qu'une methode struct❔](#quest-ce-quune-methode-struct)
- [Le mot cle `impl`](#le-mot-cle-impl)
- [Multiple methodes](#multiple-methodes)

# Les methodes struct🛠️

## Qu'est ce qu'une methode struct❔

Les methodes struct sont des fonctions qui sont attachées a un struct, pour les rendre plus facile d'utilisation.

## Le mot cle `impl`

Si l'on a un struct appelé `Personne`

```rust
struct Personne {
    nom: String,
    age: u8,
    passions: Vec<String>,
    pays: String,
    compagnie: String,
}
```

> ℹ️ `passions` est un vecteur d'items de type `String`.

On peut créer une methode pour le struct qui va presenter la personne.

Pour déclarer une methode, on utilise le mot clé `impl`, de la façon suivante:

```rust
impl Personne {
    fn presentation(&self) {
        println!("Bonjour, je m'appelle {}, j'ai {} ans et je vis en {}. Je travaille a {} et mes hobbies sont: {}", self.nom, self.age, self.pays, self.compagnie, self.passions.join(", "));
    }
}
```

> ℹ️ La fonction prend comme parametre `&self`, qui correspond a l'instance du struct sur laquelle on utilise la methode.

> ℹ️ La methode `join` est une methode qui joint les items d'un vecteur avec un séparateur pour créer un string.

Nous pouvons maintenat créer une nouvelle instance du struct et utiliser la methode `presentation`.

```rust
fn main() {
    let personne = Personne {
        nom: String::from("Léopold"),
        age: 13,
        passions: vec![String::from("💻"), String::from("🛌"), String::from("🍔")],
        pays: String::from("France 🇫🇷"),
        compagnie: String::from("Skwal-net"),
    };

    personne.presentation();
}
```

> ℹ️ La fonction `String::from` est une fonction qui crée un `String` depuis un texte de type `str`. Les types `str` et `String` sont deux types differents, mais ils representent tout les deux un texte. Les types `String` ont plus de fonctionnalité que les types `str`, mais ils sont plus lourds. Par defaut, dans le code `"Hello"`, le type `str` est utilisé.

Sortie:

```
Bonjour, je m'appelle Léopold, j'ai 13 ans et je vis en France 🇫🇷. Je travaille a Skwal-net et mes hobbies sont: 💻, 🛌, 🍔
```

## Multiple methodes

On peut aussi creer plusieurs methodes pour un struct.

Ajoutons une methode `est_adulte` pour le struct `Personne`.

```rust
impl Personne {
    fn presentation(&self) {
        ...
    }

    fn est_adulte(&self) -> bool {
        self.age >= 18
    }
}
```

> ℹ️ La fonction `est_adulte` n'a pas besoin du mot clé `return`, car quand une methode renvoie une valeur, la derniere expression est automatiquement retournee.

On peut maintenant utiliser la fonction `est_adulte` pour savoir si la personne est adulte ou pas.

```rust
fn main() {
    let personne = Personne {
        ...
    };

    if personne.est_adulte() {
        println!("{} est adulte ✅", personne.nom);
    } else {
        println!("{} n'est pas adulte ⛔", personne.nom);
    }
}
```

Sortie:

```
Léopold n'est pas adulte ⛔
```

---

<p align="right"><a href="/">Accueil 🏠</a> - <a href="../les-strings">Section suivante ⏭️</a></p>

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>
