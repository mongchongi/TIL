# querySelector() & querySelectorAll() selector

CSS 선택자로 HTML 요소를 찾을 때 사용

```html
<h2 id="lorem">lorem ipsum</h2>
<h3 class="dolor">dolor sit</h3>
<h4>amet consectetur</h4> <!-- [0] -->
<h4>adipisicing elit</h4> <!-- [1] -->
```

```javascript
// querySelector는 맨 위에 요소 하나만 찾음
console.log(document.querySelector('#lorem')); // <h2 id="lorem">lorem ipsum</h2> (id로 찾을 때)
console.log(document.querySelector('.dolor')); // <h3 class="dolor">dolor sit</h3> (class로 찾을 때)
console.log(document.querySelector('h4')); // <h4>amet consectetur</h4> (tag로 찾을 때)

// querySelectorAll은 모든 요소를 찾음
// []를 붙여 찾은 것 중 몇 번째 요소인지 순서(index) 명시 필요
// index는 0부터 시작 (0: 첫 번째, 1: 두 번째, ...)
console.log(document.querySelectorAll('h4')); // NodeList(2) [h4, h4]
console.log(document.querySelectorAll('h4')[0]); // <h4>amet consectetur</h4>
console.log(document.querySelectorAll('h4')[1]); // <h4>adipisicing elit</h4>
```
