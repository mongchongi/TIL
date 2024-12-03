# 이벤트 버블링 & 이벤트 관련 함수

이벤트가 상위 요소로 퍼지는 현상을 이벤트 버블링이라 함

```html
<!--                        이벤트 버블링 -->
<div class="black-bg"> <!-- 3. 이것도 클릭한 것 -->
  <div class="white-bg"> <!-- 2. 이것도 클릭한 것 -->
    <h3>lorem ipsum dolor sit</h3> <!-- 1. 이거 클릭 시 -->
    <button class="close-button">닫기</button>
  </div>
</div>
<button class="open-button">열기</button>
```

```css
* {
  box-sizing: border-box;
}

.black-bg {
  background: rgba(0, 0, 0, 0.5);
  padding: 30px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  visibility: hidden;
  opacity: 0;
  transition: all 0.5s;
}

.white-bg {
  background: white;
  padding: 30px;
  border-radius: 5px;
}

.show {
  visibility: visible;
  opacity: 1;
}
```

```javascript
const modal = document.querySelector('.black-bg');
const openButton = document.querySelector('.open-button');
const closeButton = document.querySelector('.close-button');

openButton.addEventListener('click', function () {
  modal.classList.add('show');
});

closeButton.addEventListener('click', function () {
  modal.classList.remove('show');
});

// 모달창 검은 배경 클릭 시 닫음
modal.addEventListener('click', function (event) { // event : 이벤트 객체
  if (event.target === modal) {
    modal.classList.remove('show');
  }

  // 이벤트 관련 함수들
  // event.target : 이벤트 발생한 곳
  // event.currentTarget : 이벤트 리스너 등록된 곳
  // event.preventDefault() : 이벤트 기본 동작 차단
  // event.stopPropagation() : 이벤트 버블링 현상 차단
});
```
