### JavaScript Best Style Guide NY(c)

#### __1.Объявление переменных__
В JavaScript теперь есть два дополнительных способа объявления переменных: let и const.
let является преемником var. Хотя var все еще доступен, let ограничивает
область переменных в блоке (а не в функции), в котором они объявлены,
что снижает вероятность ошибки:
```javascript
    // bad
    for (var i = 1; i < 5; i++) {
      console.log(i);
    }
    // <-- logs the numbers 1 to 4
    console.log(i);
    // <-- 5 (variable i still exists outside the loop)
    
    // good
    for (let j = 1; j < 5; j++) {
      console.log(j);
    }
    console.log(j);
    // <-- 'Uncaught ReferenceError: j is not defined'
```
#### __2.Стрелочные функции__
Стрелочные функции делают синтаксис лаконичным и устраняют некоторые трудности с ним. Отдавайте предпочтение стрелочным функциям, вместо ключевого слова function, особенно для вложенных функций.
```javascript
    // bad
    var add = function(a, b) {
      return a + b;
    }
    // good
    const add = (a, b) => a + b;
```
#### __3.Улучшенный синтаксис класса__
Если вы поклонник объектно-ориентированного программирования, вам может понравиться добавление
классы к языку поверх существующего механизма на основе прототипов.
Хотя это в основном синтаксический сахар, он обеспечивает более понятный синтаксис для разработчиков.
пытаясь подражать классической объектной ориентации с помощью прототипов.
```javascript
    class Person {
      constructor(name) {
        this.name = name;
      }
    greet() {
      console.log(`Hello, my name is ${this.name}`);
      }
    }
```
#### __4.Promises / Асинхронные функции__
Асинхронный характер JavaScript уже давно представляет собой проблему; любой
нетривиальное приложение рискует попасть в 'ад' обратных вызовов при работе с
такие вещи, как запросы Ajax.
К счастью, в ES2015 добавлена встроенная поддержка promises. Promise представляют
значения, которые не существуют на момент вычисления, но могут быть
доступны позже, что делает управление вызовами асинхронных функций более
управляемым, не вдаваясь в глубоко вложенные обратные вызовы.
ES2017 представил асинхронные функции (иногда называемые async / await), которые
вносить улучшения в этой области, позволяя рассматривать асинхронный код, как если бы он
были синхронными:
```javascript
    async function doAsyncOp () {
    var val = await asynchronousOperation();    
    console.log(val);
    return val;
};

```
#### __5.Объявление переменных__
```javascript
    // bad
    for (var i = 1; i < 5; i++) {
      console.log(i);
    }
    // <-- logs the numbers 1 to 4
    console.log(i);
    // <-- 5 (variable i still exists outside the loop)
    
    // good
    for (let j = 1; j < 5; j++) {
      console.log(j);
    }
    console.log(j);
    // <-- 'Uncaught ReferenceError: j is not defined'
```
#### __6.Объявление переменных__
```javascript
    // bad
    for (var i = 1; i < 5; i++) {
      console.log(i);
    }
    // <-- logs the numbers 1 to 4
    console.log(i);
    // <-- 5 (variable i still exists outside the loop)
    
    // good
    for (let j = 1; j < 5; j++) {
      console.log(j);
    }
    console.log(j);
    // <-- 'Uncaught ReferenceError: j is not defined'
```
#### __7.Объявление переменных__
```javascript
    // bad
    for (var i = 1; i < 5; i++) {
      console.log(i);
    }
    // <-- logs the numbers 1 to 4
    console.log(i);
    // <-- 5 (variable i still exists outside the loop)
    
    // good
    for (let j = 1; j < 5; j++) {
      console.log(j);
    }
    console.log(j);
    // <-- 'Uncaught ReferenceError: j is not defined'
```
#### __8.Объявление переменных__
```javascript
    // bad
    for (var i = 1; i < 5; i++) {
      console.log(i);
    }
    // <-- logs the numbers 1 to 4
    console.log(i);
    // <-- 5 (variable i still exists outside the loop)
    
    // good
    for (let j = 1; j < 5; j++) {
      console.log(j);
    }
    console.log(j);
    // <-- 'Uncaught ReferenceError: j is not defined'
```
#### __9.Объявление переменных__
```javascript
    // bad
    for (var i = 1; i < 5; i++) {
      console.log(i);
    }
    // <-- logs the numbers 1 to 4
    console.log(i);
    // <-- 5 (variable i still exists outside the loop)
    
    // good
    for (let j = 1; j < 5; j++) {
      console.log(j);
    }
    console.log(j);
    // <-- 'Uncaught ReferenceError: j is not defined'
```
#### __10.Объявление переменных__
```javascript
    // bad
    for (var i = 1; i < 5; i++) {
      console.log(i);
    }
    // <-- logs the numbers 1 to 4
    console.log(i);
    // <-- 5 (variable i still exists outside the loop)
    
    // good
    for (let j = 1; j < 5; j++) {
      console.log(j);
    }
    console.log(j);
    // <-- 'Uncaught ReferenceError: j is not defined'
```
