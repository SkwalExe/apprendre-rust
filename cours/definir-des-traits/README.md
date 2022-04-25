# Définir des traits

Nous allons créer un trait appelé `GetType` que nous allons utiliser pour obtenir le type de donné d'une variable sous forme de string.

Pour definir un trait, on utlise le mot clé `trait`, le nom du trait, suivi par le prototype des methodes que ce trait va implémenter.

```rust
trait GetType {
    fn get_type(&self) -> &str;
}
```

Nous allons implementer ce trait pour les `String`

```rust
impl GetType for String { 
    fn get_type(&self) -> &str {
        "String"
    }
}
```

Dès maintenant, chaque fois que la methode `get_type` est appelée sur une variable de type `String`, elle retourne la chaine de caractère `String`.

```rust
let s = String::from("Hello");
println!("Bonjour, je suis la variable s et mon type est : {}", s.get_type());
```

Resultat:

```rust
Bonjour, je suis la variable s et mon type est : String
```



<!--
---

<p align="right"><a href="https://skwalexe.github.io/apprendre-rust/">Accueil 🏠</a> - <a href="../les-vecteurs">Section suivante ⏭️</a></p>
-->

---

<p align="right">Course created by <a href="https://github.com/SkwalExe/" target="_blank">SkwalExe</a> and inspired by <a href="https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL" target="_blank">Dcode</a></p>