# Interactive-rating-component
This is a solution to the Interactive rating component challenge on Frontend Mentor(https://www.frontendmentor.io/challenges/interactive-rating-component-koxpeBUmI).

## Table of contents

Overview
The challenge
Screenshot
Links
My process
Built with
What I learned
Continued development
Useful resources
Author

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the app depending on their device's screen size
- See hover states for all interactive elements on the page
- Select and submit a number rating
- See the "Thank you" card state after submitting a rating

### Links

- Solution URL: https://github.com/Arkadiusz-coder/interactive-rating-component
- Live page URL: https://arkadiusz-coder.github.io/Interactive-rating-component/

## My process

### Built with

Semantic HTML5 markup
CSS custom properties
Sass 
Flexbox
Mobile-first workflow
JavaScript

### What I learned

I learn that creating layout is not so dificult. I see progress in that area. I gave myself about 23h to make this project. I finished it in about 15h. Making layout similar to the original was relatively easy and joyful. Nothing turn to mess when some element was changed.

I practice using 'onclick' attribute. Necessary to diploy changes on numers and submit button. Like bellow: 

```html
           <div class="number" onclick="selectDiv(this)"><span class="mySpan" onclick="selectNumber(1)">1</span></div>
```

Dificult part was figure how to properly use javascript to make exactely what I want. After houers with chatGPT I finally found the solutions I needed. Part responsible for changing one layout (.style.display = 'none') to another (.style.display = 'block') seems to be intuitive right now. I just had to refresh my knowladge about js syntax.

Much more harder to figure and to understand the logic, was the part that remove property 'selected' from most numbers and adds tat property only to one of them: 

```js

let selectedNumber;

function selectNumber(number) {
  selectedNumber = number;
  const numbers = document.querySelectorAll('.number');
  numbers.forEach((num) => {
    num.classList.remove('selected');
  });

  const selectedNum = document.querySelector(`.number:nth-child(${number})`);
  selectedNum.classList.add('selected');
}
```
Now I understand used syntax, but definitelly need to use it more, to become fluent at using it.


### Continued development

Additionaly to js I need to practice making circles with divs with css. Because I couldn't create desired shape of divs containing rating numbers. I don't know where is the mistake
```css
.number
{
    color: var(--medium-grey);
    background-color: var(--midium-dark-blue);
    transition: background-color 0.3s;
    font-size: .65rem;
    font-weight: 700;
    padding: .75rem;
    border-radius: 50%; 
}
```

### Useful resources

My recourse was chatGPT 3.5. I've spend houers checking variants of some solutions, both in js and css as well as getting beter understanding of syntax.'

## Author

- GitHub - https://github.com/Arkadiusz-coder
- Frontend Mentor - https://www.frontendmentor.io/profile/Arkadiusz-coder
