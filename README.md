# Frontend Mentor - Art gallery website solution

This is a solution to the [Art gallery website challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/art-gallery-website-yVdrZlxyA). Frontend Mentor challenges help you improve your coding skills by building

- [My process](#my-process)

Built with HTML, CSS and Javascript.

- [What I learned](#what-i-learned)

There were some tricky aspects to this task.

1. Use of th filter--invert method on the social media links.
   Given an image that is inherently white; use the filter to turn
   the color the other way around.

```

.location__footer .social__links a img {
filter: invert(100%);
}

```

**The tricky h1 in the hero**

2. First, the container positioning the h1 takes the 33% from 
the left pane of page as its middle point. Then we styled from there. 
The unique combination of background-clip, and transparent text means 
that the text absorbs the colors colors of the h1's linear gradient; 
without that linear-gradient actually styling the background. 

```
.relative__title__left {
  position: absolute;
  top: 170px;
  right: 57%; 
  left: 23.35%;
  height: fit-content;
  display: flex;
  flex-direction: row;

  h1 {
    background: linear-gradient(90deg,
    $white__shade 50%,
    $black__shade 50%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent; 
    color: transparent;
  }
}
```


