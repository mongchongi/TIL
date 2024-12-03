# function(함수)

길고 복잡한 코드를 짧은 단어로 축약할 때 사용  
특정 기능을 다음에도 쓰기 위해 모듈화해 놓는 문법 (재사용 편리)

```html
<div class="alert-box" id="alert">
  <span>lorem ipsum dolor</span>
  <button onclick="document.getElementById('alert').style.display = 'none';">닫기</button>
</div>

<!-- 함수 호출 -->
<!-- 함수명() -->
<button onclick="openAlert()">열기</button>
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
// 함수 선언
// function 함수명() { 실행할 코드 }
function openAlert() {
  document.getElementById('alert').style.display = 'block';
}
```
