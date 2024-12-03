# truthy & falsy

```javascript
// falsy
 // if () 안에서 false와 같은 역할
if (0) { console.log(1) }
if ('') { console.log(1) }
if (undefined) { console.log(1) }
if (null) { console.log(1) }
if (NaN) { console.log(1) }
// 위 코드는 모두 실행 X

// truthy
// if () 안에서 true와 같은 역할, falsy 외 모두
if (123) { console.log(2) }
if ('lorem') { console.log(2) }
if ([]) { console.log(2) }
if ({}) { console.log(2) }
// 위 코드는 모두 실행 O
```
