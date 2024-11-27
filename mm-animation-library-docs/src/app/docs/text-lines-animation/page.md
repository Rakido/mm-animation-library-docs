---
title: Animation de Lignes
nextjs:
  metadata:
    title: Animation de Lignes
    description: Apprenez à animer des lignes de texte avec la librairie MoonMoon Animation.
---

La librairie MoonMoon Animation offre de puissantes animations de texte basées sur les lignes. Ce guide couvre l'animation des lignes de texte et toutes les options de configuration disponibles.

---

## Animation de Ligne Basique

Pour animer des lignes de texte, utilisez `data-scroll-text-reveal` avec `data-splitting="lines"` :

```html
<p 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="fade-in"
>
  Ce texte sera divisé
  en lignes séparées qui
  s'animent indépendamment.
</p>
```

L'attribut `data-splitting="lines"` divise automatiquement les blocs de texte en lignes individuelles pour l'animation.

---

## Types d'Animation

### Animation Lines-Up

L'animation spécialisée `lines-up` crée un effet de révélation pour chaque ligne :

```html
<div 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="lines-up"
  data-duration="1.2"
  data-stagger="0.15"
>
  Chaque ligne glissera vers le haut
  depuis derrière son conteneur,
  créant un effet de révélation fluide.
</div>
```

### Animation en Fondu

Des animations simples en fondu peuvent être appliquées aux lignes :

```html
<p 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="fade-in"
  data-fade-start="0"
  data-duration="1"
  data-stagger="0.2"
>
  Chaque ligne apparaît en fondu
  l'une après l'autre,
  créant une séquence lisible.
</p>
```

### Animation en Glissement

Les lignes peuvent glisser depuis n'importe quelle direction :

```html
<h2 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="slide"
  data-axis="x"
  data-duration="1.2"
  data-stagger="0.1"
>
  Ces lignes glisseront
  depuis la droite
  de l'écran.
</h2>
```

---

## Contrôle du Timing

### Contrôle du Décalage

Contrôlez le timing entre les lignes :

```html
<div 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="lines-up"
  data-stagger="0.25"
  data-duration="1.5"
>
  Des écarts plus longs entre
  chaque révélation de ligne
  pour un effet dramatique.
</div>
```

### Séquence d'Animation Personnalisée

Combinez délai et décalage pour des séquences complexes :

```html
<p 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="slide"
  data-axis="y"
  data-delay="0.5"
  data-stagger="0.15"
  data-duration="1.2"
>
  Ce paragraphe attendra
  avant de commencer son animation,
  puis se révélera ligne par ligne.
</p>
```

---

## Effets Avancés

### Combinaison d'Animations

Plusieurs effets d'animation peuvent être appliqués aux lignes :

```html
<div 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="fade-in slide"
  data-axis="y"
  data-stagger="0.2"
  data-duration="1.5"
  data-easing="power2.out"
>
  Ces lignes apparaîtront en fondu
  et glisseront simultanément,
  créant une entrée fluide.
</div>
```

### Easing Personnalisé

Affinez le mouvement de l'animation :

```html
<p 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="lines-up"
  data-easing="0.7,0,0.3,1"
  data-duration="1.2"
  data-stagger="0.15"
>
  L'easing personnalisé fait
  bouger ces lignes avec
  une courbe de mouvement unique.
</p>
```

---

## Bonnes Pratiques

1. **Longueur des Lignes** :
   ```html
   <!-- Bien : Sauts de ligne clairs -->
   <h1 
     data-scroll-text-reveal 
     data-splitting="lines"
     data-animate="lines-up"
   >
     Des lignes courtes et percutantes
     fonctionnent mieux pour
     les révélations dramatiques.
   </h1>

   <!-- À éviter : Lignes très longues -->
   <p data-scroll-text-reveal data-splitting="lines">
     Les très longues lignes de texte qui pourraient se retourner de manière imprévisible sur différentes tailles d'écran doivent être évitées pour les animations de lignes...
   </p>
   ```

2. **Considérations de Timing** :
   - Utilisez des valeurs `data-stagger` plus longues (0.15-0.3s) que pour les mots ou caractères
   - Prenez en compte le temps de lecture lors du réglage des durées
   - Les lignes plus longues nécessitent des durées d'animation plus longues

3. **Design Responsive** :
   - Les lignes se recalculent automatiquement lors du redimensionnement de l'écran
   - Testez les animations sur différentes largeurs de viewport
   - Utilisez CSS max-width pour contrôler la longueur des lignes

4. **Direction d'Animation** :
   ```html
   <!-- Révélation standard de bas en haut -->
   <div 
     data-scroll-text-reveal 
     data-splitting="lines"
     data-animate="lines-up"
   >
     Les lignes se révèlent
     de bas en haut pour
     un flux de lecture naturel.
   </div>

   <!-- Directions alternatives -->
   <div 
     data-scroll-text-reveal 
     data-splitting="lines"
     data-animate="slide"
     data-axis="-x"
   >
     Les lignes peuvent aussi glisser
     depuis la gauche pour
     varier la présentation.
   </div>
   ```

---

## Cas d'Utilisation Courants

### Titres d'Articles
```html
<h1 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="lines-up"
  data-stagger="0.2"
  data-duration="1.5"
>
  Créez des introductions
  d'articles dramatiques
  avec des révélations de lignes.
</h1>
```

### Blocs de Contenu
```html
<div 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="fade-in slide"
  data-axis="y"
  data-stagger="0.15"
>
  Parfait pour révéler
  des blocs de contenu pendant
  que les utilisateurs défilent la page.
</div>
```

N'oubliez pas que les animations de lignes sont automatiquement déclenchées au défilement, s'activant lorsque l'élément entre dans le viewport et s'inversant lors du défilement vers le haut. Cela les rend parfaites pour le contenu long et les expériences narratives.
