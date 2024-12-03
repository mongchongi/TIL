# addEventListener()

이벤트 리스너  
이벤트를 감지하는 일종의 감시자 역할

```html
<div class="alert-box" id="alert">
  <span>lorem ipsum dolor</span>
  <button onclick="closeAlert()">닫기</button>
</div>

<!-- 이벤트 리스너를 사용하면 onclick 필요 X -->
<button class="open-button">열기</button>
```

```css
.alert-box {
  background: cornflowerblue;
  color: white;
  padding: 20px;
  border-radius: 5px;
  display: none;
}
```

```javascript
function closeAlert() {
  document.getElementById('alert').style.display = 'none';
}

// 이벤트 리스너 등록
// 찾은 요소.addEventListener('이벤트', 콜백 함수)
// 이벤트 : 웹 페이지에서 사용자가 클릭, 키 입력, 스크롤, 드래그 등 조작을 가하는 행위
// 콜백 함수 : 코드를 순차적으로 실행할 때 많이 보이는 함수 형태
document.getElementsByClassName('open-button')[0].addEventListener('click', function () {
  document.getElementById('alert').style.display = 'block';
});
```
