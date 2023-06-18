# Frontend Mentor - Huddle landing page with single introductory section solution

This is a solution to the [Huddle landing page with single introductory section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/huddle-landing-page-with-a-single-introductory-section-B_2Wvxgi0). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the page depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![](dist/images/solution-screenshot.jpg)

### Links

- Solution URL: [https://github.com/CareKajzeX/Huddle-Landing-Page](https://github.com/CareKajzeX/Huddle-Landing-Page)
- Live Site URL: [https://carekajzex.github.io/Huddle-Landing-Page/](https://carekajzex.github.io/Huddle-Landing-Page/)

## My process

### Built with

- Semantic HTML5 markup
- [BEM](https://en.bem.info/) - Methodology
- CSS custom properties
- CSS Grid
- Mobile-first workflow
- Media Queries
- [Sass](https://sass-lang.com/) - CSS Preprocessor
- Variables
- Nesting
- Partials
- Functions
- Mixins

### What I learned

I tried to implement BEM methodology.

I was determined to use some of the responsive functions in this project as well. For example transformation for px to rem as well as em.

Then combining this functions in resposive(). I would still need to work on it a bit.

```scss
// Transforms px to rem unit
@function rem($pixel) {
  @if math.is-unitless($pixel) {
    @return math.div($pixel, 16) + rem;
  } @else {
    @error 'Don\'t use units when using rem() function; only numbers.';
  }
}
```

```scss
// Transforms px to em unit
@function em($pixel) {
  @if math.is-unitless($pixel) {
    @return math.div($pixel, 16) + em;
  } @else {
    @error 'Don\'t use units when using em() function; only numbers.';
  }
}
```

```scss
// Make responsive font-size, image etc..
@function responsive($min, $preffered, $vw, $max) {
  @if (
    math.is-unitless($min) and
      math.is-unitless($preffered) and
      math.is-unitless($max)
  ) {
    @return clamp(rem($min), rem($preffered) + $vw, rem($max));
  } @else {
    @error 'Don\'t use units when using responsive() function; only numbers';
  }
}
```

### Continued development

I need to work on BEM would really like to hear any opinion of how I did.

I also have to take a closer look at the sass functions, make a few adjustments.

### Useful resources

- [Traversy Media](https://www.youtube.com/@TraversyMedia) - Place where I learn everything.
- [Grid Crash Course](https://www.youtube.com/watch?v=0xMQfnTU6oo) - Great resource for grid
- [Sass and BEM for Beginners](https://www.youtube.com/watch?v=jfMHA8SqUL4) - Really great video, learned a lot of stuff you can find in this project
- [Markdown Crash Course](https://www.youtube.com/watch?v=HUBNt18RFbo) - Helped me to get my feet wet with Markdown

## Author

- Github - [@CareKajzeX](https://github.com/CareKajzeX/)
- Frontend Mentor - [@CareKajzeX](https://www.frontendmentor.io/profile/CareKajzeX)
- Twitter - [@CareKajze](https://twitter.com/CareKajze)
