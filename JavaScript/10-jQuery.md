# 간단한 jQuery 사용법

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
<ul class="list-group">
  <li class="list-group-item">An item</li>
  <li class="list-group-item">A second item</li>
  <li class="list-group-item">A third item</li>
  <li class="list-group-item">A fourth item</li>
  <li class="list-group-item">And a fifth one</li>
</ul>

<!-- jQuery CDN 추가 필요 -->
<!-- 최신 버전의 minified -->
<script
  src="https://code.jquery.com/jquery-3.7.1.min.js"
  integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo="
  crossorigin="anonymous"
></script>
```

```css
.list-group {
  display: none;
}

.show {
  display: block;
}
```

```javascript
$('.navbar-toggler').on('click', function () {
  $('.list-group').toggleClass('show');
});
// querySelector() & querySelectorAll() => $()
// addEventListener() => on()
// classList.toggle() => toggleClass()

$('.list-group-item').css('color', 'green'); // 한 줄의 코드로 모두 변경
// style.?? = '??' => css('??', '??')

$('.st-group-item').eq(1).html('lorem');
// [] => eq()
// innerHTML = '' => html('')
```
