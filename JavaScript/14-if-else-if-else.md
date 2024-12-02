# if & else if & else 조건문

코드를 항상 실행하는 게 아닌 특정 조건에 따라 실행할 때 사용

```html
<input type="text" id="id" placeholder="아이디" />
<input type="password" id="pw" placeholder="비밀번호" />
<button class="sign-up-button">회원가입</button>
```

```javascript
document.querySelector('.sign-up-button').addEventListener('click', function () {
  
  // if (조건) { 조건이 참(true)일 때 실행할 코드 }
  if (document.querySelector('#id').value === '') { // .value : input 태그에 입력한 값을 가져옴
    alert('아이디를 입력해주세요.');

  // else if (조건) { 조건이 참(true)일 때 실행할 코드 }, 조건을 연달아 작성할 때 사용, 여러 번 비교 가능
  } else if (document.querySelector('#pw').value === '') {
    alert('비밀번호를 입력해주세요.');
  } else if (document.querySelector('#pw').value.length < 6) { // .value.length : input 태그에 입력한 값의 길이를 가져옴
    alert('비밀번호를 6자 이상 입력해주세요.');

  // else { 조건이 거짓(false)일 때 실행할 코드 }
  } else {
    alert('회원가입 완료');
  }
});
```
