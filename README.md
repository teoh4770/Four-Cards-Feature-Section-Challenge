# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

<img style="width:350px;" src="https://user-images.githubusercontent.com/98545971/183308851-000d5e2f-dcc5-4515-9e6b-73865dc7786c.png">

![Desktop View](https://user-images.githubusercontent.com/98545971/183308817-c001e93c-30be-4c21-93d9-7e4a9ced965d.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- media query

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

when the border width is the same as the border radius, it wouldn't have the weird curve line at the end

```/* whoooooot? when the border width is the same as the border radius, it wouldn't have the weird curve line at the end */

.card {
  padding: 1.5rem;
  background-color: white;
  border-radius: 4px;
  box-shadow: 0px 5px 15px lightgray;
}

.card:first-child {
  border-top: 4px solid var(--cyan);
}

.card:nth-child(2) {
  border-top: 4px solid var(--red);
}

.card:nth-child(3) {
  border-top: 4px solid var(--orange);
}

.card:last-child {
  border-top: 4px solid var(--blue);
}

```
Adding media query for the tablet view

```

@media (min-width: 560px) {
  h2 {
    font-size: 27px;
  }
  /* when past 550px viewport */
  .inner-container {
    max-width: 540px;
    margin: 0 auto;
  }
}

```
Positioning each card with absolute position and translate X or translate Y.

```
.card:first-child {
    top: 50%;
    transform: translateY(-50%);
  }

  .card:nth-child(2) {
    left: 50%;
    transform: translateX(-50%);
  }

  .card:nth-child(3) {
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
  }

  .card:last-child {
    right: 0;
    top: 50%;
    transform: translateY(-50%);
  }

```


### Useful resources

- [Position Absolute + Translate X/Y](https://stackoverflow.com/questions/32206116/position-absolute-left50-does-not-position-span-in-the-middle) - With this answer from StackOverFlow, I understand the logic behind the translateX / translateY, and able to implement it in my project, which helps me position the cards with ease.



