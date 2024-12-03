# 변수

데이터를 잠깐 저장할 때 사용  
길고 복잡한 데이터가 있을 때 저장해서 쓰면 편리  
특정 데이터를 컴퓨터에 기록 가능

| 키워드 | 선언과 할당 분리 | 재선언 | 재할당 |      범위      |
| :----: | :--------------: | :----: | :----: | :------------: |
|  var   |        O         |   O    |   O    | function(함수) |
|  let   |        O         |   X    |   O    |    {}(블록)    |
| const  |        X         |   X    |   X    |    {}(블록)    |

```javascript
// var
var lorem = 'lorem'; // 선언과 할당
lorem = 'lorem ipsum'; // 재할당

var dolor; // 선언
dolor = 'dolor'; // 할당

var lorem = 'lorem ipsum odit'; // 재선언

// let
let amet = 'amet'; // 선언과 할당
amet = 'amet consectetur'; // 재할당

let adipisicing; // 선언
adipisicing = 'adipisicing'; // 할당

// let amet = 'amet consectetur elit'; // 재선언, 에러

// const
const dolorem = 'dolorem'; // 선언과 할당
// dolorem = 'dolorem commodi'; // 재할당, 에러

// const maxime; // 선언, 에러
// maxime = 'maxime'; // 할당

// const dolorem = 'dolorem commodi vero'; // 재선언, 에러

// 범위
var a = 'a';
let b = 'b';
const c = 'c';

function test() {
  var d = 'd';
  let e = 'e';
  const f = 'f';

  // 함수 밖에 선언된 변수는 함수 안에서 사용 O
  console.log(a); // a
  console.log(b); // b
  console.log(c); // c

  // 함수 안에 선언된 변수는 함수 안에서 사용 O
  console.log(d); // d
  console.log(e); // e
  console.log(f); // f
}

test();

// 함수 안에 선언된 변수는 함수 밖에서 사용 X
// console.log(d); // 에러
// console.log(e); // 에러
// console.log(f); // 에러

if (true) {
  var g = 'g';
  let h = 'h';
  const i = 'i';

  // 블록 밖에 선언된 변수는 블록 안에서 사용 O
  console.log(a); // a
  console.log(b); // b
  console.log(c); // c

  // 블록 안에 선언된 변수는 블록 안에서 사용 O
  console.log(g); // g
  console.log(h); // h
  console.log(i); // i
}

// 블록 안에 선언된 var 변수는 함수 범위라 블록 밖에서 사용 O
console.log(g); // g

// 블록 안에 선언된 let, const 변수는 블록 범위라 블록 밖에서 사용 X
// console.log(h); // 에러
// console.log(i); // 에러
```
