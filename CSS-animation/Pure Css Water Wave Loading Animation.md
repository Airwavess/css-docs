# Pure Css Water Wave Loading Animation

<img src="https://i.imgur.com/tMfLs69.png" />

這個動畫製作起來有點有趣，是用多個圖層重疊在一起形成波浪的特效。

這時候你們一定會以為是製作出下方的水與水面波動的動畫，然後重疊在一起。

**其實不是~~**

而是反過來做，這樣看你們大概就懂了:

<img src="https://i.imgur.com/Q0iGDPK.png" />

你們猜到了嗎? 實際上是用一個大球的邊緣做出波浪的動畫，很神奇吧！

只要**讓上方的大球一直不斷的轉動**就可以變成波浪的模樣。

<img src="https://i.imgur.com/1sesGIq.png" />

因為需要有多層的海浪特效，所以可以用兩個不同 `border-radius` 的圓圈作為海浪，其中一個是 45%，另一個為 47%。

最後再讓兩個圓圈透明化，就可以完成海浪的特效。

HTML:

```HTML
<div class="container">
  <div class="wave"></div>
</div>
```

CSS:

```CSS
body,
html {
  height: 100%;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

.container {
  width: 200px;
  height: 200px;
  padding: 5px;
  border: 5px solid rgb(118, 218, 255);
  border-radius: 50%;
}

.wave {
  position: relative;
  width: 200px;
  height: 200px;
  background-color: rgb(118, 218, 255);
  border-radius: 50%;
}

.wave::before,
.wave::after {
  content: "";
  position: absolute;
  width: 400px;
  height: 400px;
  top: 0;
  left: 50%;
  background-color: rgba(255, 255, 255, 0.4);
  border-radius: 45%;
  transform: translate(-50%, -70%) rotate(0);
  animation: rotate 6s linear infinite;
  z-index: 10;
}

.wave::after {
  border-radius: 47%;
  background-color: rgba(255, 255, 255, 0.9);
  transform: translate(-50%, -70%) rotate(0);
  animation: rotate 10s linear -5s infinite;
  z-index: 20;
}

@keyframes rotate {
  50% {
    transform: translate(-50%, -73%) rotate(180deg);
  }
  100% {
    transform: translate(-50%, -70%) rotate(360deg);
  }
}
```

<iframe height="411" style="width: 100%;" scrolling="no" title="Pure Css Water Wave Loading Animation" src="https://codepen.io/Airwavess/embed/KKdZgjB?height=411&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/Airwavess/pen/KKdZgjB'>Pure Css Water Wave Loading Animation</a> by Airwaves
  (<a href='https://codepen.io/Airwavess'>@Airwavess</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>