# function(함수)의 parameter

하나의 함수로 다양한 코드를 실행할 때 사용

```html
<div class="alert-box" id="alert">
  <span>lorem ipsum dolor</span>

  <!-- 함수 호출 + 값 전달 -->
  <!-- 함수명(값) -->
  <!-- 파라미터 개수만큼 값 전달 가능 (값1, 값2, ...) -->
  <button onclick="openAndCloseAlert('none')">닫기</button> <!-- value => 'none' -->
</div>
<button onclick="openAndCloseAlert('block')">열기</button> <!-- value => 'block' -->
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
// 함수 선언 + 파라미터
// function 함수명(파라미터명) { 실행할 코드 }
function openAndCloseAlert(value) { // 파라미터는 여러 개 추가 가능 (파라미터1, 파라미터2, ...)
  document.getElementById('alert').style.display = value; // 가변적인 부분에 파라미터 사용
}
```
