# Tests Unitaire en Ruby
## Exercice 1: **Tests sur une Fonction de Calcul**
```
def addition(a, b)
  a + b
end
```

## Exercice 2: **Tests sur une Fonction de Tri**
```
def tri_croissant(array)
  array.sort
end
```

## Exercice 3: **Tests sur une Fonction de vérification d’e-mail**
```
def email_valide?(email)
  email.include?('@') && email.split('@').last.include?('.')
end
```

## Exercice 4: **Tests sur une Classe Personne**
```
class Personne
  attr_reader :nom, :age

  def initialize(nom, age)
    @nom = nom
    @age = age
  end

  def anniversaire
    @age += 1
  end
end
```

## Exercice 5: **Tests sur une Classe Panier avec Promotions**
```
class Article
  attr_reader :nom, :prix

  def initialize(nom, prix)
    @nom = nom
    @prix = prix
  end
end

class Panier
  def initialize
    @articles = []
  end

  def ajouter(article)
    @articles << article
  end

  def total
    total = @articles.sum(&:prix)
    total > 100 ? total * 0.9 : total
  end
end
```