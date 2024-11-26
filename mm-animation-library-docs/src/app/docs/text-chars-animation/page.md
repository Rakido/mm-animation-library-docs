---
title: Text & Characters Animation
nextjs:
  metadata:
    title: Text & Characters Animation
    description: Learn how to animate text and characters using MoonMoon Animation Library.
---

The MoonMoon Animation Library provides powerful text animation capabilities through simple data attributes. This guide covers character-based animations and all related configuration options.

---

## Basic Character Animation

To animate characters, you'll need to use two core attributes: `data-scroll-text-reveal` and `data-splitting`.

```html
<h1 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
>
  Animate each character
</h1>
```


The `data-scroll-text-reveal` attribute initializes the animation system, while `data-splitting="chars"` tells the library to split the text into individual characters.

---

## Animation Types

### Fade Animation

The simplest animation is fade-in. You can control the starting opacity using `data-fade-start`.

```html
<p 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-fade-start="0"
  data-duration="1"
  data-stagger="0.05"
>
  Each character fades in sequence
</p>
```

### Slide Animation

Characters can slide in from any direction using the `slide` animation type with `data-axis`.

```html
<h2 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="slide"
  data-axis="y"
  data-duration="1.2"
  data-stagger="0.03"
>
  Characters sliding from bottom
</h2>
```

Available axis values:
- `x` - Slide from right
- `-x` - Slide from left
- `y` - Slide from bottom
- `-y` - Slide from top

---

## Timing Controls

### Stagger Effect

The `data-stagger` attribute controls the delay between each character's animation:

```html
<div 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-stagger="0.1"
>
  Characters animate with 0.1s delay between each
</div>
```

### Duration and Delay

Control the overall timing with `data-duration` and `data-delay`:

```html
<span 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-duration="2"
  data-delay="0.5"
>
  Slower animation that starts after 0.5s
</span>
```

---

## Custom Easing

### Using GSAP Easings

The animation easing can be customized using `data-easing`:

```html
<h3 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-easing="power2.inOut"
>
  Smooth easing animation
</h3>
```

### Custom Cubic-Bezier

For precise control, use custom cubic-bezier values:

```html
<p 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in"
  data-easing="0.7,0,0.3,1"
>
  Custom easing curve animation
</p>
```

---

## Combining Animations

Multiple animation effects can be combined:

```html
<h1 
  data-scroll-text-reveal 
  data-splitting="chars"
  data-animate="fade-in slide"
  data-axis="y"
  data-stagger="0.04"
  data-duration="1.5"
>
  Fade and slide combination
</h1>
```

---

## Best Practices

1. **Performance**: Keep `data-stagger` values small (0.02-0.1s) for smoother animations
2. **Readability**: For longer text blocks, consider using `words` splitting instead of `chars`
3. **Timing**: Adjust `data-duration` based on text length - longer text might need longer duration
4. **Scroll Trigger**: Animations automatically trigger when elements enter the viewport

Remember that all character animations are scroll-triggered by default, playing when the element enters the viewport and reversing when it leaves.
