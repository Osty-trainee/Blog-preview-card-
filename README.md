# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://frontendmentor.io). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of Contents

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

- See hover and focus states for all interactive elements on the page (specifically the main card title).
- View the optimal layout depending on their device's screen size.

### Screenshot

![My final solution screenshot of the Blog Preview Card](<img width="1919" height="994" alt="Screenshot_2" src="https://github.com/user-attachments/assets/733b9d45-4ead-4766-a1bc-9a44b45f1927" />)
*Fig 1. Final look of my responsive web card implementation with fluid typography and precise shadow alignment.*

### Links

- Solution URL: [https://github.com](https://github.com)
- Live Site URL: https://github.io

## My process

### Built with

- Semantic HTML5 markup (including `<main>` and `<time>` tags for accessibility)
- CSS custom properties (variables for design system/spacing guide)
- CSS Flexbox (for layout positioning and absolute vertical alignment)
- Fluid typography using the CSS `clamp()` function

### What I learned

During this project, I ran into a few real-world frontend challenges and learned how to overcome them without using legacy hacks:

1. **Accessibility (A11y):** Originally, I styled the `.card-title` directly, but realized it prevented keyboard users from interacting with it. I fixed this by nesting an `<a>` tag inside the `<h1>` and moving all state transitions (`:hover`, `:active`, `:focus-visible`) to the link.
2. **Local Font Injection:** I had issues with network blocking when fetching Google Fonts via external URLs, resulting in terminal errors. I solved this by downloading the `Figtree` files locally into a `/fonts` folder and configuring them via `@font-face`.
3. **Fluid Layouts without Media Queries:** Instead of jumping across rigid breakpoints, I combined `clamp()` and `max-content` to ensure the card scales organically between mobile (327px) and desktop (384px) screens.

Below is the code snippet I am most proud of:

```css
/* Responsive, bulletproof card container without a single media query */
.card {
    background-color: var(--color-white);
    width: clamp(20.4375rem, 100%, 24rem); 
    border: 3px solid var(--color-black); 
    padding: var(--space-300);
    box-shadow: 8px 8px 0 0 var(--color-black); 
    margin: 0 auto var(--space-300) auto;
}
```

### Continued development

In my upcoming projects, I want to focus on:
- [ ] Transitioning entirely from pixel-based sizing (`px`) to relative units (`rem`/`em`) for better default zoom experiences.
- [ ] Implementing client-side validation using Native CSS pseudo-classes like `:invalid` and `:valid`.
- [ ] Expanding my structural skill set from purely Flexbox layouts into complex grid designs (`display: grid`).

## Author

- Frontend Mentor - [@Osty-trainee](https://www.frontendmentor.io/profile/Osty-trainee)
- GitHub - [<img width="1919" height="994" alt="Screenshot_2" src="https://github.com/user-attachments/assets/c7ebfc14-45ab-46e8-83db-e0c4c435c959" />
Osty-trainee](https://github.com/Osty-trainee)
