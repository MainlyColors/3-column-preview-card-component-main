# Frontend Mentor - 3-column preview card component solution

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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
- See hover states for interactive elements

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid
- Desktop-first workflow
- Reponsive Design Principles 

### What I learned

During this project I was running into some issues with the fluid grid layout for the (3) cards when the screen width was narrow enough for (2) card space. The cards would stack in a ugly 2 rows, 2 columns when really I wanted them to stack in 3 rows, 1 column. After doing some research I came across this [blog](https://blog.logrocket.com/flexible-layouts-without-media-queries/) by [Dannie Vinther](https://blog.logrocket.com/author/dannievinther/) where the technique called the "Holy Albatross" by [Heydon Pickering](https://heydonworks.com/) is explained. The article does a good job explaining exactly how this works but to give a quick summary it takes advantage of how the browser calculates minmax when at extreme values. In the below CSS snipnet the "65.4rem" defines the maxium width before the columns will break into 1 column of 3 rows.

```
ul {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(clamp(33.3333%, (65.4rem - 100%) * 999, 100%), 1fr));
}
```

### Continued development

For the next project I want to focus on mobile-first design, i've been avoiding mobile first because I had the wrong idea about how to go about it. During this project I watched a video series by the CSS master, [Kevin Powell](https://www.youtube.com/kepowob) and realized I was going about this all wrong. I kept trying to think of ways to clamp, min, max, or minmax the design in the desktop to also work for the mobile but its way easier to work with simple then move to complex as mobile first design promotes.


### Useful resources

- [From design to code - HTML & CSS tutorial [ part one ]](https://www.youtube.com/watch?v=hQCRU7hZldE) - This is the first video of 3 part series mentioned in above. This helped me understand the importance of mobile first design. 

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@ryan2505](https://www.frontendmentor.io/profile/ryan2505)
- Twitter - [@MainlyColors](https://twitter.com/MainlyColors)

