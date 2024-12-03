# Object

하나의 변수에 여러 값을 각각 이름을 붙여 저장할 때 사용
이름을 붙여 저장하므로 많은 값을 저장해도 기억하기 쉬움

```javascript
// 저장
const car = {
  // key(이름): value(실제 값) 형태로 저장, 아무거나 저장 가능
  name: '소나타',
  price: 50000,
};

// 출력
console.log(car['name']); // 소나타
// 또는 car.name

// 추가
car['color'] = 'white';
// 또는 car.color = 'white'
console.log(car); // {name: '소나타', price: 50000, color: 'white'}

// 수정
car['name'] = '아반떼';
// 또는 car.name = '아반떼'
console.log(car); // {name: '아반떼', price: 50000, color: 'white'}
```
