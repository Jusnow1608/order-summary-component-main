# Frontend Mentor - Results summary component solution

This is a solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

Below are the screenshots showcasing the final implementation of the component, including responsive layouts and interactive states:

#### Desktop View
![Desktop Layout Preview](./solution/solution-desktop.jpg)

*The full presentation of the component optimized for larger desktop viewports, featuring centered 2-column alignment and balanced card proportions.*

#### Mobile View
![Mobile Layout Preview](./solution/solution-mobile.jpg)

*The compact, responsive layout of the card adapted for mobile screens, ensuring text blocks and score summaries scale fluidly.*

#### Active States & Hover Effects
![Active State - Category Items](./solution/solution-active-change-link.jpg)
*Demonstration of the interactive state (hover/active) for the summary categories, highlighting clean focus indications and accessible layer feedback.*

![Active State - Continue Button](./solution/solution-active-button.jpg)
*Demonstration of the interactive state for the main "Continue" button, showcasing dynamic background transitions and depth shadow adaptations without layout shift.*

![Active State - Focus Indicators](./solution/solution-active-cancel-link.jpg)
*Demonstration of fully accessible keyboard focus states (`:focus-visible`) across interactive layers to satisfy accessibility guidelines.*

### Links

- Solution URL: [Frontend Mentor Solution](https://www.frontendmentor.io/solutions/results-summary-component-built-with-semantic-html-and-modern-css-vF6QzsjKb7)
- Live Site URL: [GitHub Pages Live Preview](https://jusnow1608.github.io/results-summary-component-main/)

## My process

### Built with

- Semantic HTML5 structural markup (incorporating strict accessibility landmarks)
- CSS Custom Properties (Variables) for centralized theme and color management
- Flexbox & CSS Grid for alignment, fluid item distribution, and two-column component splitting
- Mobile-first approach coupled with fluid media queries using modern relative units (`em`, `rem`)
- Accessibility-first development practices (including screen-reader optimized headings)

### What I learned

During this project, I drastically improved my clean-coding habits by shifting away from quick cosmetic fixes and aligning my workflow with modern automated validator standards. 

#### 1. Accessible Document Structure (Landmarks)
I learned that every piece of content must reside within an accessible landmark to assist screen readers. I fixed automated warnings by wrapping the component structure inside a semantic `<main>` tag and including a visually hidden `<h1>` for proper page hierarchy:

```html
<main class="results-container">
  <h1 class="visually-hidden">Results Summary</h1>
  
  <section class="results-panel">...</section>
  <section class="summary-panel">...</section>
</main>
```
2. HTML Validity & Button Types
I discovered that leaving native buttons without an explicit type attribute triggers validation errors. I ensured all semantic actions are clearly defined:

```HTML
<button type="button" class="continue-button">Continue</button>
```
3. Shifting from Pixels to Relative Units (rem / em)
To respect global user font-size preferences and prevent layouts from shattering on system zoom, I refactored the entire styling codebase. I replaced all absolute values (px, pt) with relative units (rem, em) inside margins, padding, gaps, and media queries:

```CSS
/* Transitioned from absolute units to accessible, scalable values */
.summary-wrapper {
  gap: 1.25rem; 
}

@media (max-width: 37.5em) {
  body {
    /* Responsive overrides using clean, relative breakpoints */
  }
}
```
### Continued development
Moving into future frontend challenges, my focus will remain on:

- Logical Properties: Replacing traditional directional values (like margin-bottom or left) with logical alternatives (like margin-block-end or inline-start) to naturally support internationalization and multi-directional text reading flows.

- Fluid Typography: Experimenting with advanced responsive CSS functions such as clamp(), min(), and max() to create smooth transitions for layout scaling without relying too heavily on rigid media query breakpoints.

### AI Collaboration
I collaborated with Gemini AI as an automated linting partner and design code-reviewer to refine this project.

- How I used it: I uploaded the raw validation feedback sheets and error logs directly into the prompt terminal. We parsed through warning reports highlighting absolute layout dependencies, un-typed structural tags, and un-anchored document content.

- What worked well: The system effectively pinpointed minor semantic syntax omissions (like missing semicolons in roots or improper class declarations in responsive media tags) and walked me through structural refactoring steps to establish a fully responsive, clean, and accessible final product.

### Author

- GitHub - [@Jusnow1608](https://github.com/Jusnow1608)
- Frontend Mentor - [@Jusnow1608](https://www.frontendmentor.io/profile/Jusnow1608)
- LinkedIn - [@Justyna-Nowak-Szrajnert](https://www.linkedin.com/in/justyna-nowak-szrajnert-a5168713b/)

