# 정규 표현식

문자 안에 특정 문자가 들어있는지 검사할 때 사용  
범위 지정, 특정 문자로 시작 또는 끝나는지, 최소 숫자 1개 들어있는지 등 세세한 검사 O

```javascript
// 'abc' 안에 'a'가 들어있는지
console.log(/a/.test('abc')); // true

// a ~ z 중 아무거나 1개 들어있는지
console.log(/[a-z]/.test('abc')); // true

// A ~ Z 중 아무거나 1개 들어있는지
console.log(/[A-Z]/.test('Abc')); // true

// 0 ~ 9 중 아무거나 1개 들어있는지
console.log(/[0-9]/.test('abc0')); // true

// 한글(모음, 자음) 아무거나 1개 들어있는지
console.log(/[ㄱ-ㅎ가-힣ㅏ-ㅣ]/.test('abcㄱ')); // true

// 아무거나 1개 들어있는지 (특수 문자 포함)
console.log(/\S/.test('abc@')); // true

// 특정 문자로 시작하는지
console.log(/^a/.test('abc')); // true

// 특정 문자로 끝나는지
console.log(/c$/.test('abc')); // true

// 둘 중 1개 들어있는지
console.log(/a|e/.test('abc')); // true

// 간단한 이메일 형식 검사
console.log(/\S+@\S+\.\S+/.test('aaa@bbb.ccc')); // true
// + : 왼쪽 문자 반복 검사
```
