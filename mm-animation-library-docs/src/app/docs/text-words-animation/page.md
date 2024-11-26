---
title: Words Animation
nextjs:
  metadata:
    title: Words Animation
    description: Learn how to animate words using MoonMoon Animation Library.
---

The MoonMoon Animation Library provides sophisticated word-based animations through simple data attributes. This guide covers word animations and their configuration options.

---

## Basic Word Animation

To animate words, use `data-scroll-text-reveal` with `data-splitting="words"`:

```html
<h1 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="fade-in"
>
  Each word will animate separately
</h1>
```

The `data-splitting="words"` attribute tells the library to treat each word as an individual animated element.

---

## Word Animation Types

### Basic Fade Animation

The simplest word animation is fade-in:

```html
<p 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="fade-in"
  data-fade-start="0"
  data-duration="1"
  data-stagger="0.1"
>
  Each word fades in one after another
</p>
```

### Slide Animation

Words can slide in from any direction:

```html
<h2 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="slide"
  data-axis="x"
  data-duration="1.2"
  data-stagger="0.08"
>
  Words sliding in from the right
</h2>
```

### Shutter Effect

The unique shutter effect is specifically designed for word animations:

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
  Words reveal with a shutter effect
</div>
```

The shutter effect supports:
- `data-color` - Background color of the shutter
- `data-axis` - Direction of the shutter movement (`x`, `-x`, `y`, `-y`)

---

## Timing and Sequence

### Stagger Control

Control the timing between words:

```html
<p 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="fade-in"
  data-stagger="0.15"
  data-duration="1"
>
  Words animate with longer gaps between each
</p>
```

### Custom Animation Sequence

Combine delay and stagger for complex sequences:

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
  This sentence starts after a delay
</div>
```

---

## Advanced Effects

### Combining Animations

Multiple animation effects can be applied to words:

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
  Words fade and slide simultaneously
</h3>
```

### Custom Easing

Fine-tune the animation motion:

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
  Custom easing for smoother word animations
</p>
```

---

## Best Practices

1. **Readability**: 
   - Keep `data-stagger` values between 0.05-0.15s for natural reading flow
   - Use longer durations for emphasis on important text

2. **Performance**:
   ```html
   <!-- Good: Reasonable number of words -->
   <h1 data-scroll-text-reveal data-splitting="words">
     Short impactful headline here
   </h1>

   <!-- Avoid: Too many words can impact performance -->
   <p data-scroll-text-reveal data-splitting="words">
     Very long paragraph with many words...
   </p>
   ```

3. **Animation Timing**:
   - Use faster animations (`0.8-1.2s`) for UI elements
   - Use slower animations (`1.2-2s`) for hero sections
   - Adjust `data-stagger` based on text length

4. **Direction and Flow**:
   ```html
   <!-- For languages that read left-to-right -->
   <h2 
     data-scroll-text-reveal 
     data-splitting="words"
     data-animate="slide"
     data-axis="-x"
   >
     Words slide in from left
   </h2>

   <!-- For vertical emphasis -->
   <h2 
     data-scroll-text-reveal 
     data-splitting="words"
     data-animate="slide"
     data-axis="y"
   >
     Words slide up from bottom
   </h2>
   ```

Remember that word animations are automatically scroll-triggered, activating when the element enters the viewport and reversing on scroll up.

---

## Common Patterns

### Hero Headlines
```html
<h1 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="slide fade-in"
  data-axis="y"
  data-stagger="0.1"
  data-duration="1.5"
>
  Create impact with animated headlines
</h1>
```

### Navigation Menus
```html
<nav 
  data-scroll-text-reveal 
  data-splitting="words"
  data-animate="fade-in"
  data-stagger="0.05"
  data-duration="0.8"
>
  Home About Services Contact
</nav>
```

These patterns provide a good starting point for common use cases in web interfaces.
