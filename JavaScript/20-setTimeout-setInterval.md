# setTimeout() & setInterval()

타이머 함수

```html
<!-- Bootstrap 사용 -->

<div class="alert alert-danger"><span class="num">5</span>초 이내 구매 시 사은품 증정!</div>
```

```javascript
const alertBox = document.querySelector('.alert');
const num = document.querySelector('.num');

let count = 5;

// setTimeout(콜백 함수, 시간(ms 단위)) : x초 후 코드 실행
setTimeout(function () {
  alertBox.style.display = 'none';

  // 타이머 함수 삭제
  clearInterval(timer); // 또는 clearTimeout()
}, 5000); // 5000ms(밀리초) => 5s(초)

function decreaseCount() {
  count--; // 변수 -1하는 방법
  num.innerHTML = count;
}

// setInterval(콜백 함수, 시간(ms 단위)) : x초마다 코드 실행
const timer = setInterval(decreaseCount, 1000);
// 콜백 함수 자리에 미리 만들어 놓은 함수 넣기 가능
// 타이머 함수를 삭제할 땐 변수에 저장 필요
```
