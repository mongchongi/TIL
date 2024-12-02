# classList

HTML 요소에 class를 탈부착할 때 사용  
애니메이션 추가 쉬움, 나중에 재사용 편리

```html
<!-- Bootstrap 사용 -->

<nav class="navbar bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand">Navbar</a>
    <button class="navbar-toggler" type="button">
      <span class="navbar-toggler-icon"></span>
    </button>
  </div>
</nav>

<!-- ul 태그에 class 탈부착 -->
<ul class="list-group">
  <li class="list-group-item">An item</li>
  <li class="list-group-item">A second item</li>
  <li class="list-group-item">A third item</li>
  <li class="list-group-item">A fourth item</li>
  <li class="list-group-item">And a fifth one</li>
</ul>
```

```css
.list-group {
  display: none;
}

/* 탈부착할 class */
.show {
  display: block;
}
```

```javascript
document.getElementsByClassName('navbar-toggler')[0].addEventListener('click', function () {
  document.getElementsByClassName('list-group')[0].classList.toggle('show');
});
// classList.add() : class 추가
// classList.remove() : class 삭제
// classList.toggle() : class 없으면 추가, 있으면 삭제
```
