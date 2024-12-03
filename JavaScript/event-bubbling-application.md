# 이벤트 버블링 응용

```html
<!-- ul 태그에만 이벤트 리스너 등록 -->
<ul class="tab-list">
  <li class="tab-button">lorem</li>
  <li class="tab-button active">harum</li>
  <li class="tab-button">totam</li>
</ul>
<div class="tab-content">
  <h3>lorem</h3>
  <p>lorem ipsum dolor sit</p>
</div>
<div class="tab-content show">
  <h3>harum</h3>
  <p>harum sapiente, tempore, a alias repellat corporis</p>
</div>
<div class="tab-content">
  <h3>totam</h3>
  <p>totam laborum modi architecto iure at iste?</p>
</div>
```

```css
.tab-list {
  padding: 0;
  margin: 0;
  list-style: none;
  background: #eeeeee;
  border-bottom: 2px solid #d2d2d2;
  display: flex;
}

.tab-button {
  padding: 10px 20px;
  cursor: pointer;
}

.active {
  background: #d2d2d2;
}

.tab-content {
  padding: 0 15px;
  display: none;
}

.show {
  display: block;
}
```

```javascript
const tabList = document.querySelector('.tab-list');
const tabButtons = document.querySelectorAll('.tab-button');
const tabContents = document.querySelectorAll('.tab-content');

// 가독성, 재사용을 위해 함수로 축약
function openTab(i) {
  tabButtons[0].classList.remove('active');
  tabButtons[1].classList.remove('active');
  tabButtons[2].classList.remove('active');
  tabContents[0].classList.remove('show');
  tabContents[1].classList.remove('show');
  tabContents[2].classList.remove('show');

  // 축약할 코드에 변수가 있으면 변수를 파라미터로 변경해야 잘 동작
  tabButtons[i].classList.add('active');
  tabContents[i].classList.add('show');
}

// for (let i = 0; i < 3; i++) {
//   tabButtons[i].addEventListener('click', function () {
//     openTab(i);
//   });
// }

// 이벤트 버블링 응용, 이벤트 리스너 1개만 사용
// 이벤트 리스너 사용할 때마다 RAM 용량 차지, 사용량 줄이면 성능 up
tabList.addEventListener('click', function (event) {
  if (event.target === tabButtons[0]) {
    openTab(0);
  } else if (event.target === tabButtons[1]) {
    openTab(1);
  } else {
    openTab(2);
  }
});
```
