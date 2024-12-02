# input & change 이벤트

input 태그에서 발생하는 이벤트

```html
<input type="text" />
```

```javascript
// input 이벤트 : input 태그에 값을 입력할 때마다 코드 실행
document.querySelector('input').addEventListener('input', function () {
  console.log('input 이벤트 발생!');
});

// change 이벤트 : input 태그에 값을 입력하고 포커스를 잃을 때 코드 실행
document.querySelector('input').addEventListener('change', function () {
  console.log('change 이벤트 발생!');
});
```
