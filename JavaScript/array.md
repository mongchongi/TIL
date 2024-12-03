# Array

하나의 변수에 여러 값을 순서대로 저장할 때 사용
순서 개념 존재, 값을 정렬하거나 중간에 자르기 등 가능

```javascript
// 저장
const car = ['소나타', 50000]; // 아무거나 저장 가능

// 출력
console.log(car[0]); // 소나타

// 추가
car[2] = 'white';
console.log(car); // ['소나타', 50000, 'white']

// 수정
car[0] = '아반떼';
console.log(car); // ['아반떼', 50000, 'white']
```
