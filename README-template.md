# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Stats preview card component solution](#frontend-mentor---stats-preview-card-component-solution)
  - [Table of contents](#table-of-contents)
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


## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![Mobile](/images/mobile_main_index.png)
![Desktop](/images/desktop_main_index.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

- I got stuck on the image color overlay and Stack Overflow told me to use the `background` property. I wasted an hour trying to make `background` work. It didn't. The image just wont show up.

  After half an hour of Googling, I found a better solution, using pseudo objects, `::before`. Even since I've been wasting my time scouring CSS codes on the net I always wondered 'how you do dat tho? before after? WTF?' Determined, I see this as an oppurtunity to dive deep on the dark arts of pseudo objects.

  It was ok. 

  But I never managed to get the same result as the color overlay in the design seems darker.🤔

  ~~Also theres tiny bit of overflow at the bottom of the img. Not sure why the `div` containing the `img` doesn't have the same height dimension as the `img`.~~ 

  ~~Lesson learned, never listen to the first answer on Stack Overflow. I mean why would you dabble with `background` when `<img>` is clearly superior.~~

  edit: I've realized It's harder to make a responsive `<img>` tag which will involve JS, for this challenge I think JS is overkill. So I force myself to learn `background` properly. The main reason my image wasn't showing up is because I didn't set dimensions for the image. 

  I'm not sure whats the best practise when setting dimension for images so feel free to comment if you know.

  Another thing I learned is `background-size` can only be used if it is immeadiately follows `background-position`. Why? CSS, thats why.

css code below
```CSS
.sectionImg::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: hsla(277, 80%, 66%, 0.397);
}
```
```CSS
.sectionImg .img {
  background: center/cover url("/images/image-header-mobile.jpg");
  width: 100%;
  min-height: 15rem;
}
```

### Continued development

**Things I would like to focus more on**

- Breakpoints.
- SASS would simplify CSS coding process. Typing `display:flex` `align-items:center` `justify-content:center` seems cumbersome.
- Build a something similar using CSS grid.

### Useful resources

- [Breakpoint](https://www.freecodecamp.org/news/the-100-correct-way-to-do-css-breakpoints-88d6a5ba1862/) - This helped me understand breakpoint and best practise. I really liked this pattern and will use it going forward.
- [px vs rem](https://stackoverflow.com/questions/6654958/make-body-have-100-of-the-browser-height?rq=1) - Stack Overflow thread that helped me understand px,em or rem. **TL;DR: use px** I'd recommend it to anyone still learning this concept.
- [CSS background property](https://stackoverflow.com/questions/6654958/make-body-have-100-of-the-browser-height?rq=1) - An article that helped me troubleshoot the background preperty.

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@fadhlankhalid](https://www.frontendmentor.io/profile/fadhlanKhalid)
- Twitter - [@mfmk922](https://twitter.com/mfmk922)

## Acknowledgments

Alhamdullilah.

