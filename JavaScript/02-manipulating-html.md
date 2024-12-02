# HTML 조작

거의 모든 것을 조작 가능

```html
<h1 id="hello">hello</h1>
```

```javascript
// 찾은 요소.??(무엇을) = ??(어떻게)
document.getElementById('hello').innerHTML = 'hi'; // 내부 HTML
document.getElementById('hello').style.color = 'green'; // 글자 색
document.getElementById('hello').style.fontSize = '1rem'; // 글자 크기
```
