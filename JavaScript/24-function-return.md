# function(함수)의 return

함수를 호출한 자리에 뭔가 뱉고 싶을 때 사용 (값 반환)  
함수 종료 기능 존재  
값을 넣으면 규칙에 따라 다른 값이 나오는 변환기 만들 때 유용

```javascript
// 함수 선언 + return
// function 함수명() { return 반환할 값 }
function test() {
  console.log(1); // 1

  return 123; // 함수 호출 시 return 오른쪽에 있는 값을 반환, 아무거나 반환 가능

  // return 밑에 오는 코드는 실행 X
  console.log(2);
}

const result = test(); // const result = 123;
console.log(result); // 123

// 분과 초를 넣으면 밀리초로 변환
function changeTime(minute, second) {
  return (minute * 60 + second) * 1000;
}

console.log(changeTime(1, 30)); // 90000
console.log(changeTime(2, 10)); // 130000
```
