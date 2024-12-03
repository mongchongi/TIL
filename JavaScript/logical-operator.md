# 논리 연산자

조건 2개 이상을 동시에 비교할 때 사용

```javascript
// && : 둘 다 true면 true, 하나라도 false면 false (ADN, 그리고)
console.log(1 === 1 && 1 === 2); // false

// || : 하나라도 true면 true, 둘 다 false면 false (OR, 또는)
console.log(1 === 1 || 1 === 2); // true

// ! : true면 false로, false면 true로 (NOT, 부정)
console.log(1 === 1 && !(1 === 2)); // true
```
