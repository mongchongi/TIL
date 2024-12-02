# one-way(일방향) 애니메이션 만드는 방법

1. 시작 스타일 만들기
2. 최종 스타일 만들기
3. 원할 때 최종 스타일로 변하라는 JavaScript 코드 작성
4. 시작 스타일에 transition 추가

```html
<div class="black-bg">
  <div class="white-bg">
    <h3>lorem ipsum dolor sit</h3>
    <button class="close-button">닫기</button>
  </div>
</div>
<button class="open-button">열기</button>
```

```css
* {
  box-sizing: border-box;
}

/* step 1 */
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

  /* step 4 */
  transition: all 0.5s;
}

.white-bg {
  background: white;
  padding: 30px;
  border-radius: 5px;
}

/* step 2 */
.show {
  visibility: visible;
  opacity: 1;
}
```

```javascript
// step 3
document.querySelector('.open-button').addEventListener('click', function () {
  document.querySelector('.black-bg').classList.add('show');
});

document.querySelector('.close-button').addEventListener('click', function () {
  document.querySelector('.black-bg').classList.remove('show');
});
```
