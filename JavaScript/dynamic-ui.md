# 동적 UI 만드는 방법

1. HTML과 CSS로 UI 미리 디자인, 필요하면 평소엔 숨김
2. 버튼을 누르거나 할 때 숨긴 UI를 보여달라는 JavaScript 코드 작성

```html
<!-- step 1 -->
<div class="alert-box" id="alert">
  <span>lorem ipsum dolor</span>
  <button>닫기</button>
</div>

<!-- step 2 -->
<button onclick="document.getElementById('alert').style.display = 'block';">열기</button>
<!-- onclick : 클릭했을 때 JavaScript 코드 실행 -->
```

```css
/* step 1 */
.alert-box {
  background: cornflowerblue;
  color: white;
  padding: 20px;
  border-radius: 5px;
  display: none; /* UI 숨김 */
}
```
