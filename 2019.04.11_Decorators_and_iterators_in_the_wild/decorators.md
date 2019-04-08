---

# Les décorateurs

---

# C'est quoi?

## Un décorateur permet de modifier le fonctionnement d'une fonction, sans modifier son code source.

![](https://d2t3xdwbh1v8qy.cloudfront.net/content/B000SEIBB8/resources/673342348)

---

# A quoi ça ressemble?

```python
def hello(name):
    print(f"Hello {name}")

hello("world")

# "Hello world"
```

{.column}

```python
@uppercase
def hello(name):
    print(f"Hello {name}")

hello("world")

# "HELLO WORLD"
```

---

# Pour quoi faire?

- Ne pas exécuter la fonction
- Exécuter la fonction plusieurs fois
- Changer la sortie de la fonction
- Changer les entrées de la fonction

---

# Créons notre premier décorateur

def my_decorator(func):  # <= func=hello
  def wrapper():
    func() # <= hello() => print("hello")

  return wrapper  # <= Retourne la fonction wrapper

---

# Real world

---

# Module séparé

---

# Passer des arguments

---

# Retourner des valeurs

---

# Real world

---

# Exemples d'utilisation

---

