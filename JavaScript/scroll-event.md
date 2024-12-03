# scroll 이벤트

스크롤 관련 기능을 만들 때 사용

```html
<!-- Bootstrap 사용 -->

<body style="height: 3000px">
  <nav class="navbar bg-body-tertiary">
    <div class="container-fluid">
      <a class="navbar-brand">Navbar</a>
    </div>
  </nav>

  <div class="lorem">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident, tempore dolores molestias illo numquam
    reiciendis facilis hic, accusantium maxime perspiciatis, eius sunt libero debitis in natus fugit eveniet impedit
    accusamus.
  </div>
</body>
```

```css
.navbar {
  position: fixed;
  width: 100%;
  height: 56px;
}

.navbar-brand {
  transition: all 1s;
}

.lorem {
  position: fixed;
  top: 100px;
  left: 20px;
  width: 200px;
  height: 100px;
  border: 1px solid black;
  padding: 10px;
  overflow-y: scroll;
}
```

```javascript
const navbarBrand = document.querySelector('.navbar-brand');
const loremBox = document.querySelector('.lorem');

// window : 현재 페이지 의미
// window > document > HTML
window.addEventListener('scroll', function () {
  if (window.scrollY > 100) {
    navbarBrand.style.fontSize = '14px';
  } else {
    navbarBrand.style.fontSize = '20px';
  }

  // window.scrollY : 세로 방향으로 스크롤 한 양
  // window.scrollX : 가로 방향으로 스크롤 한 양
  // window.scrollTo(x좌표, y좌표) : 원하는 위치로 강제 스크롤
  // window.scrollBy(x좌표, y좌표) : 현재 위치에서부터 원하는 위치로 강제 스크롤
});

// 스크롤 이벤트 주의점
// 1. 이벤트 리스너 안에 코드는 1초에 60번 이상 실행, 많이 사용 시 컴퓨터에 부담
// 2. 1초에 60번 이상 실행되다 보니 여러 번 중복 실행될 수 있음, 이를 방지하는 기능 필요

let scrolled = false; // 중복 실행 방지 기능

// HTML 요소에서의 scroll 이벤트
loremBox.addEventListener('scroll', function () {
  const scrollAmount = loremBox.scrollTop;
  const actualHeight = loremBox.scrollHeight;
  const visibleHeight = loremBox.clientHeight;

  // 찾은 요소.scrollTop : 세로 방향으로 스크롤 한 양
  // 찾은 요소.scrollHeight : 스크롤 가능한 실제 높이
  // 찾은 요소.clientHeight : 화면에 보이는 높이

  // 세로 방향으로 스크롤 한 양은 정수 단위로 나오지 않고 OS마다 부정확, 여유를 두고 비교하는 게 좋음
  if (scrollAmount + visibleHeight > actualHeight - 5 && scrolled === false) {
    alert('모두 읽음');
    scrolled = true;
  }
});
```
