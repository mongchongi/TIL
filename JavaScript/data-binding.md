# 데이터 바인딩

HTML에 데이터를 꽂아 넣는 것

```html
<!-- Bootstrap 사용 -->

<div class="card-group container">
  <div class="card">
    <img src="https://via.placeholder.com/600" />
    <div class="card-body">
      <h5>Card title</h5>
      <p>가격 : 70000</p>
      <button class="btn btn-danger">주문하기</button>
    </div>
  </div>
  <div class="card">
    <img src="https://via.placeholder.com/600" />
    <div class="card-body">
      <h5>Card title</h5>
      <p>가격 : 70000</p>
      <button class="btn btn-danger">주문하기</button>
    </div>
  </div>
  <div class="card">
    <img src="https://via.placeholder.com/600" />
    <div class="card-body">
      <h5>Card title</h5>
      <p>가격 : 70000</p>
      <button class="btn btn-danger">주문하기</button>
    </div>
  </div>
</div>
```

```javascript
const productTitles = document.querySelectorAll('.card-body h5');
const productPrices = document.querySelectorAll('.card-body p');

// 데이터
const products = [
  { id: 0, price: 70000, title: 'Blossom Dress' },
  { id: 1, price: 50000, title: 'Springfield Shirt' },
  { id: 2, price: 60000, title: 'Black Monastery' },
];

// 데이터 바인딩
for (let i = 0; i < products.length; i++) {
  productTitles[i].innerHTML = products[i].title;
  productPrices[i].innerHTML = '가격 : ' + products[i].price;
}
```
