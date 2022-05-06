# CSS
Le Cascading Style Sheet (CSS) est un langage qui nous permet de définir la forme, d'appliquer du style à un document, en général, une page web. <br/>
Tous comme le langage HTML, le CSS est un langage pas trop complexe. Il y a beaucoup de vocabulaire à comprendre et beaucoup de syntaxe à maîtriser. C'est donc un langage qui demande beaucoup de pratique afin de le maîtriser. <br/>
La syntaxe d'un code CSS ressemble à ceci :<br/>

```css
h1 {
    color: black;
    font-size: 24px;
}
```

On a globalement trois (3) composants principaux :
- le **sélecteur** : elle permet de définir quel élément doit être affecté par les styles que l'on veut définir. Dans notre cas ici, on pointe sur les `h1`. Donc, le style qu'on va définir en dessous va affecter tous les `h1` de ma page web.

- Les **propriétés** : correspondent aux propriétés d'un élément. Dans cet exemple, on a `color` et `font-size` qui sont deux des propriétés d'un élément `h1`. Ce dernier étant un élément de type texte. La propriété `color` permet de changer la couleur du texte et `font-size` permet de changer la taille des écritures (police) du texte.

- La **valeur** : c'est elle qui définie le style d'un élément à travers ses propriétés. Dans ce cas, la valeur `black` prise par la propriété `color` met le texte de l'élément `h1` en noir (black = `noir` en anglais), et la valeur `24px` de la propriété `font-size` de l'élément `h1` met chacune de toutes les lettres du texte de `h1` à une taille de 24 pixels.

