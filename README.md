# CSS
Le Cascading Style Sheet (CSS) est un langage qui nous permet de définir la forme, d'appliquer du style à un document, à la base, une page web. <br/>
C'est en effet, un langage qui a été élaboré pour la mise en forme des page WEB d'un site internet. Tous comme le langage HTML, le CSS est un langage pas trop complexe. Il y a beaucoup de vocabulaire à comprendre et beaucoup de syntaxe à maîtriser. C'est donc un langage qui demande beaucoup de pratique afin de le maîtriser. <br/>
La syntaxe d'un code CSS ressemble à ceci :<br/>

```css
h1 {
    color: black;
    font-size: 24px
}
```

On a globalement trois (3) composants principaux :
- le **sélecteur** : elle permet de définir quel élément doit être affecté par les styles que l'on veut définir. Dans notre cas ici, on pointe sur les `h1`. Donc, le style qu'on va définir en dessous va affecter tous les `h1` de ma page web.

- Les **propriétés** : correspondent aux propriétés d'un élément. Dans cet exemple, on a `color` et `font-size` qui sont deux des propriétés d'un élément `h1`. Ce dernier étant un élément de type texte. La propriété `color` permet de changer la couleur du texte et `font-size` permet de changer la taille des écritures (police) du texte.

- La **valeur** : c'est elle qui définie le style d'un élément à travers ses propriétés. Dans ce cas, la valeur `black` prise par la propriété `color` met le texte de l'élément `h1` en noir (black = `noir` en anglais), et la valeur `24px` de la propriété `font-size` de l'élément `h1` met chacune de toutes les lettres du texte de `h1` à une taille de 24 pixels.

> **NOTE**: À la fin de la ligne de chaque définition de propriété (nom-de-propriété: valeur), on met un `;`. À la fin de la ligne de définition de la dernière propriété d'un élément, on peut `omettre` le `;`. Exactement comme dans l'exemple de code ci-dessus.

<br/>

Dans la réalisation d'une page web, on peut écrire le CSS à `trois (3)` endroits. Considérons le code HTML suivant pour illustrer cette information.

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset='utf-8'/>
        <title>Ma page WEB</title>
    </head>
    <body>
        <h1>Mon gros titre</h1>
    </body>
</html>
```

1. Dans ce code HTML, on peut injecter directement le CSS à l'intérieur des éléments qu'on souhaite mettre en forme.

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset='utf-8'/>
        <title>Ma page WEB</title>
    </head>
    <body>
        <!-- on definit tout simplement un attribut `style` à l'intérieur de l'élément. -->
        <h1 style="color: black; font-size: 24px">Mon gros titre</h1>
    </body>
</html>
```

Dans ce cas, pas besoin de mettre le sélecteur `h1`, car le style est directement définit dans l'élément `h1`.

2. Toujour dans le code HTML, on peut utiliser une balise ouvrante et fermante nommé `style` qu'on place dans l'entête de notre document HTML.

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset='utf-8'/>
        <title>Ma page WEB</title>
        <!-- on doit utiliser le sélecteur pour indexer l'élément à mettre en forme -->
        <style>
            h1 {
                color: black;
                font-size: 24px
            }
        </style>
    </head>
    <body>
        <h1>Mon gros titre</h1>
    </body>
</html>
```

3. Dernière méthode, c'est de mettre le code CSS dans un fichier séparé de celui du HTML. Donc, dans un premier temps, nous avons le code CSS contenu dans un fichier qu'on peut par exemple nommer `mon_style.css` :

```css
h1 {
    color: black;
    font-size: 24px
}
```

et dans un second temps, on a le fichier contenant le code HTML linké avec le fichier CSS, qu'on peut par exemple nommer `ma_page.html` :

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset='utf-8'/>
        <title>Ma page WEB</title>
        <!-- on utilise la balise `link` pour faire le lien vers un fichier externe, ici, notre fichier `mon_style.css` -->
        <link href="mon_style.css" rel="stylesheet" />
    </head>
    <body>
        <h1>Mon gros titre</h1>
    </body>
</html>
```

Dans la balise `link`, on spécifie le type du document qu'on veut linker. C'est le rôle de l'attribut `rel`. Dans le cas, d'un fichier CSS, on définit l'attribut `rel` à `stylesheet`. Ce dernier signifie **feuille de style** en français.

> **NOTE**: On suppose ici que les deux fichiers `mon_style.css` et `ma_page.html` sont dans le même repertoire de fichier, au même niveau. C'est dans ce cas de figure que les deux codes que je vous ai proposé fonctionnent.

