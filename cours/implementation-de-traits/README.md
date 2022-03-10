# Sommaire📚
- [Qu'est ce qu'un trait❔](#quest-ce-quun-trait)
- [Implementer un trait](#implementer-un-trait)
- [Utiliser un trait](#utiliser-un-trait)

# Implémentation de traits
## Qu'est ce qu'un trait❔
Un trait est une collection de methodes communes a chaque type. Les traits sont similaires aux interfaces certains autres langages.
## Implementer un trait
Premierement, nous avons besoins d'un struct sur lequelle implementer le trait : 
```rust
struct Personne {
    nom: String,
    age: u8,
    passions: Vec<String>,
    pays: String,
    compagnie: String,
}
```
Ensuite, nous allons implementer le trait `to_string` pour le struct `Personne`.

Cette methode retourne une représentation textuelle de l'instance d'un struct.

Pour implementer un trait, on utilise le mot clé `impl` avec la syntaxe suivante :
```rust
impl ToString for Personne {
    fn to_string(&self) -> String {
        format!("Bonjour, je m'appelle {}, J'ai {} ans et je vis en {}. Je travaille chez {}, et mes passions sont : {}", self.nom, self.age, self.pays, self.compagnie, self.passions.join(", "))
    }
}
```
> ℹ️ La macro `format!` est utilisee comme la macro `print!` mais retourne un string au lieu d'afficher directement dans la console.

## Utiliser un trait
Nous allons maintenant créer une nouvelle instance de notre struct `Personne` et utiliser la methode `to_string`.
```rust
let personne = Personne {
    nom: String::from("Léopold"),
    age: 13,
    passions: vec![String::from("💻"), String::from("🛌"), String::from("🍔")],
    pays: String::from("France 🇫🇷"),
    compagnie: String::from("Skwal-net"),
};

let presentation = personne.to_string();

println!("{}", presentation);
```
> ℹ️ Les noms des traits et des methodes sont les memes pour tous les types.

Sortie:
```
Bonjour, je m'appelle Léopold, J'ai 13 ans et je vis en France 🇫🇷. Je travaille chez Skwal-net, et mes passions sont : 💻, 🛌, 🍔
```

<!--
---

<p align="right"><a href="https://github.com/SkwalExe/learn-rust/tree/main/course/implementation-de-traits">Next Section ⏭️</a></p>
-->

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>
