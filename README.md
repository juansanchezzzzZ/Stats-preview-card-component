# Frontend Mentor - Stats Preview Card Component Solution

<div align="center">

![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![NEWBIE](https://img.shields.io/badge/Frontend_Mentor-NEWBIE-3DB8FF?style=for-the-badge)

</div>

A responsive stats preview card built as part of a Frontend Mentor challenge.  
This project focuses on responsive layouts, Flexbox, image manipulation using pure CSS, and modern CSS techniques without JavaScript.

---

## Preview

![Design preview for the Stats Preview Card Component challenge](./preview.jpg)

---

## Live Demo

- Live Site: [live demo](https://juansanchezzzzz.github.io/Stats-preview-card-component/)
- Frontend Mentor Challenge: https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62

---

# Overview

This project recreates a modern statistics preview card featuring a responsive desktop and mobile layout, a custom image color effect, and clean typography hierarchy.

The main goal was to practice:

- Semantic HTML5
- Responsive layouts
- Flexbox
- Media Queries
- CSS Blend Modes
- CSS Custom Properties
- Mobile-first thinking

---

# Built With

- HTML5
- CSS3
- Flexbox
- CSS Custom Properties
- Media Queries
- CSS Blend Modes

---

# Image Color Manipulation

One of the biggest challenges of this project was reproducing the purple image effect from the design without modifying the image itself.

This was achieved using a pseudo-element combined with `mix-blend-mode: multiply`, allowing the purple overlay to blend naturally with the image underneath.

```css
.image-container::after{
    content: "";
    position: absolute;
    inset: 0;

    background: var(--Purple500);

    mix-blend-mode: multiply;
}
```

This technique creates a more realistic effect while keeping the original image unchanged.

---

# Responsive Layout

Another major challenge was handling the responsive design.

The desktop version uses a horizontal layout, while the mobile version transforms into a vertical card with the image positioned above the content.

```css
@media (max-width: 1000px){

    main{
        flex-direction: column-reverse;
        height: auto;
        max-width: 22rem;
    }

}
```

The mobile version also swaps the desktop image for a dedicated mobile image:

```css
@media (max-width: 1000px){

    .image-container img{
        content: url("images/image-header-mobile.jpg");
    }

}
```

These changes allow the component to closely match the provided mobile design.

---

# What I Learned

Through this challenge I improved my understanding of:

- CSS blend modes
- Responsive Flexbox layouts
- Media query design patterns
- Image overlays using pseudo-elements
- Managing different layouts across screen sizes

---
