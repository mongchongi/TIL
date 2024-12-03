# getElementsByClassName() selector

class로 HTML 요소를 찾을 때 사용

```html
<p class="lorem">lorem ipsum</p> <!-- [0] -->
<p class="lorem">lorem dolor</p> <!-- [1] -->
<p class="amet">amet consectetur</p> <!-- [0] -->
```

```javascript
// class는 중복 가능
// 해당 class를 갖는 요소를 모두 찾음
console.log(document.getElementsByClassName('lorem')); // HTMLCollection(2) [p.lorem, p.lorem]

// []를 붙여 찾은 것 중 위에서부터 몇 번째 요소인지 순서(index) 명시 필요
// index는 0부터 시작 (0: 첫 번째, 1: 두 번째, ...)
console.log(document.getElementsByClassName('lorem')[0]); // <p class="lorem">lorem ipsum</p>
console.log(document.getElementsByClassName('lorem')[1]); // <p class="lorem">lorem dolor</p>

// 해당 class를 갖는 요소가 하나밖에 없더라도 순서 명시 필요
console.log(document.getElementsByClassName('amet')[0]); // <p class="amet">amet consectetur</p>
```
