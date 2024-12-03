# 다크 모드 만들기

```html
<button class="mode-button">다크 모드로 보기</button>

<h1>lorem</h1>
<p>
  lorem ipsum dolor sit amet consectetur adipisicing elit. Rem ratione autem soluta enim ut voluptas impedit explicabo
  magnam reprehenderit eius accusamus consectetur, maiores, vero ipsa fugiat nesciunt repudiandae in eligendi!
</p>
```

```css
.dark {
  background: black;
  color: white;
}
```

```javascript
// 변수에는 거의 모든 데이터 저장 가능
const modeButton = document.querySelector('.mode-button');
const body = document.querySelector('body');

let count = 0; // 클릭 횟수

modeButton.addEventListener('click', function () {
  count++; // 변수에 +1하는 방법 (count = count + 1 또는 count += 1로도 작성 가능)

  if (count % 2 === 1) {
    // count % 2 === 0 : 짝수
    // count % 2 === 1 : 홀수

    modeButton.innerHTML = '라이트 모드로 보기';
    body.classList.add('dark');
  } else {
    modeButton.innerHTML = '다크 모드로 보기';
    body.classList.remove('dark');
  }
});
```
