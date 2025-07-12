# Frontend Mentor - Skilled e-learning landing page solution

This is a solution to the [Skilled e-learning landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/skilled-elearning-landing-page-S1ObDrZ8q). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements


### Links

- Live Site URL: (https://melodic-fairy-b11899.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

```html
  <picture>
    <!-- Tablet -->
    <source
      srcset="./assets/image-hero-tablet.webp 1x, ./assets/image-hero-tablet@2x.webp 2x"
      media="(min-width: 768px)"
      type="image/webp" />
    <!-- Mobile -->
    <source
      srcset="./assets/image-hero-mobile.webp 1x, ./assets/image-hero-mobile@2x.webp 2x"
      type="image/webp" />
    <!-- Fallback -->
    <img
      src="./assets/image-hero-mobile.webp"
      alt="Hero image" />
  </picture>
```
Used <picture> for the first time in a project
  -Different image types for different screen sizes & density

```css
.hero {
        padding: 4rem 2.75rem;
        gap: 1.5rem;
        display: grid;
        position: relative;
        z-index: 1;
        grid-template-columns: minmax(min-content, 1fr) 1fr;
        max-width: 1120px;
    }

Z-index 1 to place hero image on the top of the stacking context 
  -Hero image is inside .hero 

Minmax(min-content, 1fr) to limit the text to its content, while allowing picture to reflect the rest of the grid.
  -Used grid over flex because grid allows for sizing of the text box whereas   flex does not and will size it to whatever it is sized.

.hero-img-wrapper {
    position: relative;
    z-index: -1;
}

Positioned wrapper behind in the stacking context to prevent it interfering with user interaction

    .hero picture img {
        min-width: 760px;
        display: block;
        position: absolute;
        top: calc(-450px + 3vw);
        aspect-ratio: 1 / 1;
        z-index: -1;
        right: calc(-410px + 5%);
    }

Used calc for:
  top: to allow image to gradually descend as screen gets wider from -450px.
  right: to ensure image remains to the right of the screen.

```

### Continued development

Learn how to position and design more complex designs like the hero image on this one
Maybe a bit of grid layout.

## Author

- Frontend Mentor - [@lemz100](https://www.frontendmentor.io/profile/lemz100)