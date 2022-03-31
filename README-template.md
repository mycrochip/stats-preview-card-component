# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![Mobile-view](images/screenshot-mobile.jpg)
![Desktop-view](/images/screenshot-desktop.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)


## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

Overall, I just learned the more because I faced more and more problems as I move on to more demanding projects.
What surprised the most was that certain code snippets that proved very useful in my other projects just seemed impossible to apply in this project. There most be some lapses in their use cases. This could be as a result of the display types I used and some other conflicting variables; however, adding them here would just be too tiresome.
I however learned one particular hitch with trying to manipulate custom variables:

```css
:root {
  --cl-accent-a: 277 64% 61%;
}
```

The above css made me feel that ommitting the commas in hsl values such as below is a new norm

```css
div {
  background-color: hsl(0 0% 100%);;
}

/* OR */
div {
  background-color: hsl(var(--cl-white));
}

/* Instead of: */
div {
  background-color: hsl(0, 0%, 100%);;
}

```

The variable method above is very useful incase I want to tweak the color variable to add an alpha value for opacity as follows:

```css
div {
  background-color: hsl(var(--cl-white) / 0.75);  /* This won't work with commas*/
}
```

The main problem arised from me defining a custom hsl value without commas and add an alpha value as follows:
```css
:root {
  --cl-white-75: hsl(0 0% 100% 0.75);
}
```

IT JUST DAWNED ON ME AS I WRITE THIS THAT IT IS STILL VALID! 
I SHOULD HAVE USED hsla() in place of hsl(). Oh what a headache I had in trying to find out why my .description color wont receive less white.
Thanks to developer tools.

```css
:root {
  --cl-white-75: hsla(0 0% 100% 0.75);
}
```

### Continued development

More challenges and more solutions....

### Useful resources

- [Complete guide to grid](https://css-tricks.com/snippets/css/complete-guide-grid/) 
- [A guide to flex-box](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) 

 The above resources are web genies for short! They are majical and I will keep using their resource.


## Author

- Frontend Mentor - [@mycrochip](https://www.frontendmentor.io/profile/mycrochip)
- Twitter - [@mycrochip_world](https://www.twitter.com/mycrochip_world)


## Acknowledgments

A shout out to all developers at [Frontend Mentor](https://www.frontendmentor.io).
Nice to be part of such a community. Kudos to the creator as well, for such thoughtfulness