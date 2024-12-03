# dataset

HTML 요소에 몰래 정보를 저장하고 출력할 때 사용

```html
<!-- ul 태그에만 이벤트 리스너 등록 -->
<ul class="tab-list">
  <!-- 정보 저장 -->
  <!-- data-이름="값" -->
  <li class="tab-button" data-id="0">lorem</li>
  <li class="tab-button active" data-id="1">harum</li>
  <li class="tab-button" data-id="2">totam</li>
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

tabList.addEventListener('click', function (event) {
  // 저장한 정보 출력
  // 찾은 요소.dataset.이름
  openTab(parseInt(event.target.dataset.id));
});
```
