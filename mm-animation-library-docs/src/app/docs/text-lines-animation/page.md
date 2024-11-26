---
title: Lines Animation
nextjs:
  metadata:
    title: Lines Animation
    description: Learn how to animate text lines using MoonMoon Animation Library.
---

The MoonMoon Animation Library provides powerful line-based text animations. This guide covers how to animate text lines and all available configuration options.

---

## Basic Line Animation

To animate lines of text, use `data-scroll-text-reveal` with `data-splitting="lines"`:

```html
<p 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="fade-in"
>
  This text will be split
  into separate lines that
  animate independently.
</p>
```

The `data-splitting="lines"` attribute automatically splits text blocks into individual lines for animation.

---

## Line Animation Types

### Lines-Up Animation

The specialized `lines-up` animation creates a revealing effect for each line:

```html
<div 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="lines-up"
  data-duration="1.2"
  data-stagger="0.15"
>
  Each line will slide up
  from behind its container,
  creating a smooth reveal effect.
</div>
```

### Basic Fade Animation

Simple fade animations can be applied to lines:

```html
<p 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="fade-in"
  data-fade-start="0"
  data-duration="1"
  data-stagger="0.2"
>
  Each line fades in
  one after another,
  creating a readable sequence.
</p>
```

### Slide Animation

Lines can slide in from any direction:

```html
<h2 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="slide"
  data-axis="x"
  data-duration="1.2"
  data-stagger="0.1"
>
  These lines will slide
  in from the right side
  of the screen.
</h2>
```

---

## Timing and Sequence

### Stagger Control

Control the timing between lines:

```html
<div 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="lines-up"
  data-stagger="0.25"
  data-duration="1.5"
>
  Longer gaps between
  each line reveal
  for dramatic effect.
</div>
```

### Custom Animation Sequence

Combine delay and stagger for complex sequences:

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
  This paragraph will wait
  before starting its animation,
  then reveal line by line.
</p>
```

---

## Advanced Effects

### Combining Animations

Multiple animation effects can be applied to lines:

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
  These lines will fade
  and slide simultaneously,
  creating a smooth entrance.
</div>
```

### Custom Easing

Fine-tune the animation motion:

```html
<p 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="lines-up"
  data-easing="0.7,0,0.3,1"
  data-duration="1.2"
  data-stagger="0.15"
>
  Custom easing makes
  these lines move with
  a unique motion curve.
</p>
```

---

## Best Practices

1. **Line Length**:
   ```html
   <!-- Good: Clear line breaks -->
   <h1 
     data-scroll-text-reveal 
     data-splitting="lines"
     data-animate="lines-up"
   >
     Short, impactful lines
     work best for
     dramatic reveals.
   </h1>

   <!-- Avoid: Very long lines -->
   <p data-scroll-text-reveal data-splitting="lines">
     Very long lines of text that might wrap unpredictably on different screen sizes should be avoided for line animations...
   </p>
   ```

2. **Timing Considerations**:
   - Use longer `data-stagger` values (0.15-0.3s) than with words or characters
   - Consider reading time when setting durations
   - Longer lines need longer animation durations

3. **Responsive Design**:
   - Lines will automatically recalculate on screen resize
   - Test animations at different viewport widths
   - Consider using CSS max-width to control line length

4. **Animation Direction**:
   ```html
   <!-- Standard bottom-up reveal -->
   <div 
     data-scroll-text-reveal 
     data-splitting="lines"
     data-animate="lines-up"
   >
     Lines reveal from
     bottom to top for
     natural reading flow.
   </div>

   <!-- Alternative directions -->
   <div 
     data-scroll-text-reveal 
     data-splitting="lines"
     data-animate="slide"
     data-axis="-x"
   >
     Lines can also slide
     in from the left for
     variety in presentation.
   </div>
   ```

---

## Common Use Cases

### Article Headlines
```html
<h1 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="lines-up"
  data-stagger="0.2"
  data-duration="1.5"
>
  Create dramatic
  article introductions
  with line reveals.
</h1>
```

### Content Blocks
```html
<div 
  data-scroll-text-reveal 
  data-splitting="lines"
  data-animate="fade-in slide"
  data-axis="y"
  data-stagger="0.15"
>
  Perfect for revealing
  blocks of content as
  users scroll down the page.
</div>
```

Remember that line animations are automatically scroll-triggered, activating when the element enters the viewport and reversing on scroll up. This makes them perfect for long-form content and storytelling experiences.
