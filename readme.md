# Introduction

L'objectif du document est la création d'une *cheat sheet* ou "feuille de triche". 

L'ensemble des fonctions que vous devez documenter se trouvent dans ce document, à vous de  remplir les espaces vides 😉

Ce document pourra vous suivre tout au long de vos études, n'hésitez à le compléter au fur et à mesure.

---

Pour compléter le document, vous utiliserez la fonction **fork** de GitHub pour copier ce projet dans votre espace personnel.

[Si besoin, rendez-vous dans ce dépôt pour revoir les bases de Javascript](https://github.com/Maxence-Machu/javascript-basic-memo)

---

## La fonction GetElementByID()

### Que fait la fonction ?
La méthode getElementById() renvoie un objet qui représente l'élément dont la propriété  id correspond à la chaîne de caractères spécifiée.
Étant donné que les ID d'élément doivent être uniques, s'ils sont spécifiés, ils constituent un moyen utile d'accéder rapidement à un élément spécifique.

### Pourquoi l'utiliser ?
La fonction getElementById doit être utilisée si l'on veut utiliser un élément du DOM en HTML grâce à Javascript 

#### Note supplémentaire
La fonction getElementByID est à ne pas confondre avec la fonction *getElementsByClassName*. 
Les ID dans une page web sont uniques, on ne peut donc pas récupérer plusieurs éléments avec cette fonction. 

### Exemple de code:
```javascript
let element = document.getElementByID('mon-element');
console.log(element);
```

## La fonction GetElementsByClassName()

### Que fait la fonction ?
La méthode getElementById() renvoie un objet de type tableau de tous les éléments enfants qui ont tous les noms de classe donnés. Lorsqu'il est appelé sur l'objet document, le document complet est recherché, y compris le nœud racine. La fonction getElementByID sert à retourner uniquement les éléments qui sont les descendants de l'élément racine spécifié avec les noms de classes donnés.

### Pourquoi l'utiliser ?
"names" est une chaîne représentant le nom de la classe des éléments à trouver. 
getElementsByClassName peut être appelé sur n'importe quel élément, pas seulement sur le document. L'élément sur lequel il est appelé sera utilisé comme racine de la recherche.

### Exemple de code:
```javascript
var element = document.getElementsByClassName(names);
console.log(element);

```

## La fonction querySelector() et querySelectorAll()

### Que fait la fonction ?
La méthode querySelectorAll()  de Element renvoie une NodeList statique représentant une liste des éléments du document qui correspondent au groupe de sélecteurs spécifiés.

### Pourquoi l'utiliser ?
Cette méthode est implémentée à partir de ParentNode, méthode du mixin querySelectorAll().

### Exemple de code:
```javascript
elements = document.querySelectorAll(selecteurs);
console.log(element);
```

## La fonction addEventListener()

### Que fait la fonction ?
La méthode addEventListener() d'EventTarget installe une fonction à appeler chaque fois que l'événement spécifié est envoyé à la cible. Les cibles courantes sont un Element, le Document lui-même et une Window, mais elle peut être tout objet prenant en charge les évènements (comme XMLHttpRequest).

### Pourquoi l'utiliser ?
addEventListener() fonctionne en ajoutant une fonction, ou un objet implémentant EventListener, à la liste des écouteurs d'évènements du type d'évènement spécifié dans la EventTarget dans laquelle il est appelé.

### Exemple de code:
```javascript
target.addEventListener(type, écouteur [, options]);
console.log(target);
```

## La fonction stopPropagation()

### Que fait la fonction ?
La fonctin stopPropagation évite que l'évènement courant ne se propage plus loin dans les phases de capture et de déploiement.

### Pourquoi l'utiliser ?
...

### Exemple de code:
```javascript
event.stopPropagation();
console.log(event);
```

## La fonction addEventListener('mousemove', maFonction)

### Que fait la fonction ?
La méthode addEventListener() d'EventTarget installe une fonction à appeler chaque fois que l'événement spécifié est envoyé à la cible. Les cibles courantes sont un Element, le Document lui-même et une Window, mais elle peut être tout objet prenant en charge les évènements (comme XMLHttpRequest).

### Pourquoi l'utiliser ?
addEventListener() fonctionne en ajoutant une fonction, ou un objet implémentant EventListener, à la liste des écouteurs d'évènements du type d'évènement spécifié dans la EventTarget dans laquelle il est appelé.
il est possible d'écouter ces évènements et de leur attacher des actions personnalisées lorsqu'ils sont déclenchés.

### Exemple de code:
```javascript
document.addEventListener('click', function() { ... });
console.log(document);
```

## La fonction parseInt()

### Que fait la fonction ?
La fonction parseInt() analyse une chaîne de caractère fournie en argument et renvoie un entier exprimé dans une base donnée.

### Pourquoi l'utiliser ?
...

### Exemple de code:
```javascript
function roughScale(x, base) {
  const parsed = parseInt(x, base);
  if (isNaN(parsed)) { return 0; }
  return parsed * 100;
}
console.log(roughScale(' 0xF', 16));

ou 

parseInt(string, base);
```


## La variable "event" dans le code suivant:

### Code:
```javascript
element.addEventListener('event-name', function(event) {
  console.log(event);
});
```

### Qu'est-ce que cette variable ?
...

### Pourquoi l'utiliser ?
C'est pour avoir la possibilité d'écouter des évènements et de leur attacher des actions personnalisées lorsqu'ils sont déclenchés.


