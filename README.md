# CSS Tips & Tricks

1. [Image Hover](#1-image-hover)
2. [Text With A Background Image](#2-text-with-a-background-image)
3. [Image Drop Shadow](#3-image-drop-shadow)
4. [Gradient Font Color](#4-gradient-font-color)
5. [Type Writer Effect](#5-type-writer-effect)
6. [Background Blend Mode](#6-background-blend-mode)
7. [Font Color Animation](#7-font-color-animation)
8. [Gradient Border](#8-gradient-border)
9. [Text Stroke](#9-text-stroke)
10. [CSS Cards](#10-css-cards)
11. [Center Align Elements](#11-center-align-elements)
12. [CSS Variables in Media Queries](#12-css-variables-in-media-queries)
13. [Responsive Layout Tricks](#13-responsive-layout-tricks)
14. [Shadow Hover Effect](#14-shadow-hover-effect)
15. [Underline Hover Effect](#15-underline-hover-effect)
16. [Flow Root](#16-flow-root)
17. [Equal Width Table Cells](#17-equal-width-table-cells)

##

## 1. Image Hover

```html
<div id="box">
  <img src="Image.png">
</div>
```

```css
#box {
  width: 300px;
  height: 300px;
  background-color: aquamarine;
  overflow: hidden;
}

#box img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: all ease 1s;
}

#box:hover img {
  scale: 1.5;
}
```

##

## 2. Text With A Background Image

```html
<h3>THE BG Effects</h3>
```

```css
h3 {
  font-size: 50px;
  font-weight: 900;
  text-transform: uppercase;
  background-image: url(img.png);
  background-size: cover;
  background-position: center;
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
}
```

##

## 3. Image Drop Shadow

```html
<img src="img.png">
```

```css
img {
  filter: drop-shadow(10px 10px 20px #111);
}
```

##

## 4. Gradient Font Color

```html
<p class="title">CSS stand for Cascading Style Sheet</p>
```

```css
.title {
  background-image: linear-gradient(90deg, #7DF9FF, #DC143C);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  font-size: 5rem;
}
```

##

## 5. Type Writer Effect

```html
<h1>Hello, My Name is TOUFIQ GILANI.</h1>
```

```css
h1 {
  font-size: clamp(1rem, 3vw + 1rem, 4rem);
  position: relative;
  font-family: "Source Code Pro", monospace;
  width: max-content;
}

h1::before,
h1::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
}

h1::before {
  background: #FFF;
  animation: type 6s steps(32) 1s forwards;
}

h1::after {
  width: 0.125em;
  background: #1E90FF;
  animation: type 6s steps(32) 1s forwards, blink 750ms steps(32) infinite;
}

@keyframes type {
  to {
    left: 100%;
  }
}

@keyframes blink {
  to {
    background: transparent;
  }
}
```

##

## 6. Background Blend Mode

```css
body {
  min-height: 100vh;
  background-image: linear-gradient(45deg, red, blue), url(https://unsplash.it/1200/600);
  background-size: cover;
  background-blend-mode: multiply;
}
```

##

## 7. Font Color Animation

```html
<h2><span class="color-gradient">HTML Hyper Text Markup Language</span></h2>
```

```css
h2 {
  margin-top: 2em;
  font-size: 3rem;
  text-align: center;
}

.color-gradient {
  background-image: -webkit-linear-gradient(92deg, #28C76F, #0396FF);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  -webkit-animation: hue 10s infinite linear;
}

@-webkit-keyframes hue {
  from {
    -webkit-filter: hue-rotate(0deg);
  }

  to {
    -webkit-filter: hue-rotate(-360deg);
  }
}
```

##

## 8. Gradient Border

```html
<div id="gradient-border">
  <img src="pro.png">
</div>
```

```css
#gradient-border {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  background: linear-gradient(#D8114D, #362AA5, #1ADBC2, #362AA5, #D8114D);
  padding: 7px;
}

#gradient-border img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50%;
}
```

##

## 9. Text Stroke

```html
<h2 class="h2">LANGUAGE</h2>
```

```css
.h2 {
  font-size: 110px;
  font-weight: 900;
  -webkit-text-stroke: 4px #483D8B;
  color: transparent;
}
```

##

## 10. CSS Cards

```html
<div class="card">
  <div class="header">
    <h1>1</h1>
  </div>
  <div class="container">
    <p>December 1, 2023</p>
  </div>
</div>

<div class="polaroid">
  <img src="img.png" width="250px" alt="Image" />
  <div class="container">
    <p>Flowers</p>
  </div>
</div>
```

```css
.card,
.polaroid {
  width: 250px;
  margin: 1rem auto;
  text-align: center;
  box-shadow: 0 4px 8px 0 rgb(0, 0, 0, 0.5), 0 6px 20px rgb(0, 0, 0, 0.5);
}

.header {
  color: white;
  background-color: #44CC8D;
  font-size: 2.5rem;
  padding: 0.6rem;
}

.container {
  padding: 0.6rem;
}
```

##

## 11. Center Align Elements

```html
<body>
  <h1>Center Align Elements</h1>
</body>
```

```css
body {
  display: grid;
  place-items: center;
  min-height: 100vh;
}
```

##

## 12. CSS Variables in Media Queries

##

## 13. Responsive Layout Tricks

##

## 14. Shadow Hover Effect

##

## 15. Underline Hover Effect

```html
<a href="#" class="link">Click Here</a>
```

```css
.link {
  color: #4169E1;
  font-size: 1.5rem;
  font-weight: 900;
  font-family: "Roboto", sans-serif;
  text-decoration: none;
  position: relative;
}

.link:hover {
  opacity: 0.9;
}

.link::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -5px;
  height: 3px;
  width: 0%;
  background: #4169E1;
  transition: all ease 1s;
}

.link:hover::after {
  width: 100%;
}
```

##

## 16. Flow Root

```html
<div class="card">
  <img src="img.jpg" class="card__img" width="110" alt="...">
  <h2>An Interesting Thing</h2>
  <p>
    But a the and still purple this tempter me never.
    Still back ghastly my it. Broken and sitting than forgotten.
  </p>
</div>
```

```css
.card {
  display: flow-root;
  width: min(80%, 45em);
  margin: 0 auto 2.5em;
  padding: 3em;
  box-shadow: 0 0 1.5em rgba(0, 0, 0, 0.25);
}

.card__img {
  float: left;
  margin: 0 1em 1em 0;
}
```

##

## 17. Equal Width Table Cells

```html
----------
```

## 🚀
