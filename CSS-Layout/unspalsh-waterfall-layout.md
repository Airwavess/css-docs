# Unspalsh waterfall layout (column count)

使用 `column-count` 實現 Unspalsh 的瀑布流照片佈局。

`column-count` 可以用來描述元素的行數，不用特別指定每個元素的位置，CSS便會自動計算每個元素應該排放在哪個位置。

使用起來很輕量，如果是遇到瀑布流佈局，可以考慮使用 `column-count`，一鍵完成。

HTML:

```HTML
<div class="container">
  <div class="images">
    <img src="https://images.unsplash.com/photo-1586339159856-0923c0cb110c?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1586963312987-3c96f9ace15a?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1586264470882-e23232308cbb?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1586095696706-2ec1948e8939?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1587112899738-9f72efb2afe5?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1587725544964-bbcb2604c220?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1586953208456-9dd42767140f?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1585907945577-717ee2bf18d3?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1586901533048-0e856dff2c0d?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1585857472137-1495dba46b42?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
    <img src="https://images.unsplash.com/photo-1586560615973-2d5aae054ae5?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max" />
  </div>
</div>
```

SCSS:

```SCSS
.container {
  column-count: 3;
  column-gap: 15px;
}

.images {
  img {
    width: 100%;
  }
}
```

範例:

<iframe height="492" style="width: 100%;" scrolling="no" title="Unsplash waterfall layout" src="https://codepen.io/Airwavess/embed/ZEbXVoP?height=492&theme-id=dark&default-tab=result" frameborder="no" allowtransparency="true" allowfullscreen="true" loading="lazy">
  See the Pen <a href='https://codepen.io/Airwavess/pen/ZEbXVoP'>Unsplash waterfall layout</a> by Airwaves
  (<a href='https://codepen.io/Airwavess'>@Airwavess</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>