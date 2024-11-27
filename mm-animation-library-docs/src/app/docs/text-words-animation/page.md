---
title: Animation de Mots
nextjs:
  metadata:
    title: Animation de Mots
    description: Apprenez à animer des mots avec la librairie MoonMoon Animation.
---

La librairie MoonMoon Animation offre des animations sophistiquées basées sur les mots à travers des attributs de données simples. Ce guide couvre les animations de mots et leurs options de configuration.

---

## Animation de Mots Basique

Pour animer des mots, utilisez `data-scroll-text-reveal` avec `data-splitting="words"` :

```html
<h1 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="fade-in"
>
  Chaque mot s'animera séparément
</h1>
```

L'attribut `data-splitting="words"` indique à la librairie de traiter chaque mot comme un élément animé individuel.

---

## Types d'Animation de Mots

### Animation en Fondu Basique

L'animation la plus simple pour les mots est le fondu :

```html
<p 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="fade-in"
  data-fade-start="0"
  data-duration="1"
  data-stagger="0.1"
>
  Chaque mot apparaît en fondu l'un après l'autre
</p>
```

### Animation en Glissement

Les mots peuvent glisser depuis n'importe quelle direction :

```html
<h2 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="slide"
  data-axis="x"
  data-duration="1.2"
  data-stagger="0.08"
>
  Les mots glissent depuis la droite
</h2>
```

### Effet Store

L'effet store unique est spécialement conçu pour les animations de mots :

```html
<div 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="shutter-word"
  data-color="#4f46e5"
  data-axis="x"
  data-duration="1"
  data-stagger="0.1"
>
  Les mots se révèlent avec un effet store
</div>
```

L'effet store prend en charge :
- `data-color` - Couleur d'arrière-plan du store
- `data-axis` - Direction du mouvement du store (`x`, `-x`, `y`, `-y`)

---

## Timing et Séquence

### Contrôle du Décalage

Contrôlez le timing entre les mots :

```html
<p 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="fade-in"
  data-stagger="0.15"
  data-duration="1"
>
  Les mots s'animent avec des écarts plus longs entre chacun
</p>
```

### Séquence d'Animation Personnalisée

Combinez délai et décalage pour des séquences complexes :

```html
<div 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="slide"
  data-axis="y"
  data-delay="0.5"
  data-stagger="0.08"
  data-duration="1.2"
>
  Cette phrase commence après un délai
</div>
```

---

## Effets Avancés

### Combinaison d'Animations

Plusieurs effets d'animation peuvent être appliqués aux mots :

```html
<h3 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="fade-in slide"
  data-axis="y"
  data-stagger="0.1"
  data-duration="1.5"
  data-easing="power2.out"
>
  Les mots apparaissent en fondu et glissent simultanément
</h3>
```

### Easing Personnalisé

Affinez le mouvement de l'animation :

```html
<p 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="slide"
  data-axis="-x"
  data-easing="0.7,0,0.3,1"
  data-duration="1.2"
  data-stagger="0.1"
>
  Easing personnalisé pour des animations de mots plus fluides
</p>
```

---

## Bonnes Pratiques

1. **Lisibilité** : 
   - Gardez les valeurs `data-stagger` entre 0.05-0.15s pour un flux de lecture naturel
   - Utilisez des durées plus longues pour mettre l'accent sur le texte important

2. **Performance** :
   ```html
   <!-- Bien : Nombre raisonnable de mots -->
   <h1 data-scroll-text-reveal data-splitting="words">
     Titre court et percutant ici
   </h1>

   <!-- À éviter : Trop de mots peuvent impacter la performance -->
   <p data-scroll-text-reveal data-splitting="words">
     Très long paragraphe avec beaucoup de mots...
   </p>
   ```

3. **Timing d'Animation** :
   - Utilisez des animations plus rapides (0.8-1.2s) pour les éléments d'interface
   - Utilisez des animations plus lentes (1.2-2s) pour les sections hero
   - Ajustez `data-stagger` en fonction de la longueur du texte

4. **Direction et Flux** :
   ```html
   <!-- Pour les langues qui se lisent de gauche à droite -->
   <h2 
     data-scroll-text-reveal 
     data-splitting="words"
     data-animate="slide"
     data-axis="-x"
   >
     Les mots glissent depuis la gauche
   </h2>

   <!-- Pour l'emphase verticale -->
   <h2 
     data-scroll-text-reveal 
     data-splitting="words"
     data-animate="slide"
     data-axis="y"
   >
     Les mots glissent depuis le bas
   </h2>
   ```

N'oubliez pas que les animations de mots sont automatiquement déclenchées au défilement, s'activant lorsque l'élément entre dans le viewport et s'inversant lors du défilement vers le haut.

---

## Motifs Courants

### Titres Hero
```html
<h1 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="slide fade-in"
  data-axis="y"
  data-stagger="0.1"
  data-duration="1.5"
>
  Créez de l'impact avec des titres animés
</h1>
```

### Menus de Navigation
```html
<nav 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="fade-in"
  data-stagger="0.05"
  data-duration="0.8"
>
  Accueil À Propos Services Contact
</nav>
```

Ces motifs fournissent un bon point de départ pour les cas d'utilisation courants dans les interfaces web.
