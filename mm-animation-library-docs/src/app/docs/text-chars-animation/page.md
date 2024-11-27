---
title: Animation de Caractères
nextjs:
  metadata:
    title: Animation de Caractères
    description: Apprenez à animer du texte et des caractères avec la librairie MoonMoon Animation.
---

La librairie MoonMoon Animation offre de puissantes capacités d'animation de texte à travers des attributs de données simples. Ce guide couvre les animations basées sur les caractères et toutes les options de configuration associées.

---

## Animation de Caractères Basique

Pour animer des caractères, vous aurez besoin de deux attributs principaux : `data-scroll-text-reveal` et `data-splitting`.

```html
<h1 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
>
  Animer chaque caractère
</h1>
```

L'attribut `data-scroll-text-reveal` initialise le système d'animation, tandis que `data-splitting="chars"` indique à la librairie de diviser le texte en caractères individuels.

---

## Types d'Animation

### Animation en Fondu

L'animation la plus simple est le fondu. Vous pouvez contrôler l'opacité de départ avec `data-fade-start`.

```html
<p 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-fade-start="0"
  data-duration="1"
  data-stagger="0.05"
>
  Chaque caractère apparaît en séquence
</p>
```

### Animation en Glissement

Les caractères peuvent glisser depuis n'importe quelle direction en utilisant le type d'animation `slide` avec `data-axis`.

```html
<h2 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="slide"
  data-axis="y"
  data-duration="1.2"
  data-stagger="0.03"
>
  Caractères glissant depuis le bas
</h2>
```

Valeurs d'axe disponibles :
- `x` - Glissement depuis la droite
- `-x` - Glissement depuis la gauche
- `y` - Glissement depuis le bas
- `-y` - Glissement depuis le haut

---

## Contrôles de Timing

### Effet de Décalage

L'attribut `data-stagger` contrôle le délai entre l'animation de chaque caractère :

```html
<div 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-stagger="0.1"
>
  Les caractères s'animent avec 0.1s de délai entre chacun
</div>
```

### Durée et Délai

Contrôlez le timing global avec `data-duration` et `data-delay` :

```html
<span 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-duration="2"
  data-delay="0.5"
>
  Animation plus lente qui commence après 0.5s
</span>
```

---

## Easing Personnalisé

### Utilisation des Easings GSAP

L'easing de l'animation peut être personnalisé avec `data-easing` :

```html
<h3 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-easing="power2.inOut"
>
  Animation avec easing fluide
</h3>
```

### Cubic-Bezier Personnalisé

Pour un contrôle précis, utilisez des valeurs cubic-bezier personnalisées :

```html
<p 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-easing="0.7,0,0.3,1"
>
  Animation avec courbe d'easing personnalisée
</p>
```

---

## Combinaison d'Animations

Plusieurs effets d'animation peuvent être combinés :

```html
<h1 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in slide"
  data-axis="y"
  data-stagger="0.04"
  data-duration="1.5"
>
  Combinaison de fondu et glissement
</h1>
```

---

## Bonnes Pratiques

1. **Performance** : Gardez les valeurs `data-stagger` petites (0.02-0.1s) pour des animations plus fluides
2. **Lisibilité** : Pour les blocs de texte plus longs, préférez le découpage en `words` plutôt qu'en `chars`
3. **Timing** : Ajustez `data-duration` en fonction de la longueur du texte - un texte plus long peut nécessiter une durée plus longue
4. **Déclenchement au Défilement** : Les animations se déclenchent automatiquement lorsque les éléments entrent dans le viewport

N'oubliez pas que toutes les animations de caractères sont déclenchées au défilement par défaut, s'activant lorsque l'élément entre dans le viewport et s'inversant lorsqu'il en sort.
