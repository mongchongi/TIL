# 문자 중간에 변수 넣는 방법

## 방법 1

```javascript
const name = 'kim';

// + 기호 사용
console.log('hello, ' + name + '!'); // hello, kim!

// 참고
// 숫자 + 숫자
console.log(1 + 2); // 3

// 문자 + 숫자
console.log(1 + '2'); // '12' (숫자를 문자로 변환 후 합침)
```

## 방법 2

```javascript
const name = 'kim';

// ``(역 따옴표, 백틱)으로 감싸고 ${} 사용
console.log(`hello, ${name}!`); // // hello, kim!
```
