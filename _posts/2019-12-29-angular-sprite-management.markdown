---
layout: post
title: "Angular Sprite Management"
date:   2019-12-29 08:18:33 +1300
author: Fernando
categories: web 
tags: Angular 
---

While building a navigation bar for a web based time management app, I designed a few SVG icons and rendered them onto the UI, one question popped into my mind: how fast is the load speed and will it become a problem if I have many SVG images to render? To answer this question, I've done a few simple bench marking tests and proposed a method to load SVG icons from a sprite and cache the fetched images to increase load speed.

### The Common Approach: Load SVG Images within HTML

The first implementation of the nav bar loads separate SVG icons into HTML template: 

```html
<nav>
    <a [routerLink]="['/time-tracker']">
        <img src="assets/img/clock.svg" alt="timer icon">
    </a>
    <a [routerLink]="['/water-tracker']">
        <img src="assets/img/water.svg" alt="water icon">
    </a>
</nav>
```