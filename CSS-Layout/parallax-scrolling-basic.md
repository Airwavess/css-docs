# Parallax Scrolling - Basic

這是一個非常簡單滾動視差 (Parallax scrolling) 的範例，使用 `background-attachment` 就可以輕鬆的製作出基本的滾動視差。

HTML:

```HTML
<div>section 1</div>
<div>section 2</div>
<div>section 3</div>
<div>section 4</div>
<div>section 5</div>
<div>section 6</div>
```

CSS:

```CSS
html, body {
  margin: 0;
}

div {
  height: 100vh;
  background-size: cover;
  background-attachment: fixed;
  background-size: cover;
  background-position: center center;
  
  font-size: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
}

div:nth-child(even) {
  color: white;
}

div:nth-child(2) {
  background-image: url(https://images.unsplash.com/photo-1478827536114-da961b7f86d2?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80);
}

div:nth-child(4) {
  background-image: url(https://images.unsplash.com/photo-1528932860067-7e2e27b3185f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80);
}

div:nth-child(6) {
  background-image: url(https://images.unsplash.com/photo-1587387119725-9d6bac0f22fb?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80);
}
```

<iframe height="631" style="width: 100%;" scrolling="no" title="Parallax scrolling - basic" src="https://codepen.io/Airwavess/embed/XWmeOwR?height=631&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true" loading="lazy">
  See the Pen <a href='https://codepen.io/Airwavess/pen/XWmeOwR'>Parallax scrolling - basic</a> by Airwaves
  (<a href='https://codepen.io/Airwavess'>@Airwavess</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>