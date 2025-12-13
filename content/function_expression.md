+++
date = '2025-12-10T19:00:00+03:00'
title = 'Function Expression в  JavaScript'
+++

Function Expression - это функция которая создается внутри другого выражения. Вот простой пример:

```JavaScript
const sayHello = function() {
  console.log("Hello Eva!");
};
```

В этом примере функция создается после знака присваивания, и теперь является свойством переменной `sayHello` 

Вызывается точно так же как и Function Declaration

```JavaScript
sayHello(); // "Hello Eva!"
```

Function Expression создается, только тогда когда выполнение доходит до него и только после этого ее можно использовать.

Главные особенности между ними
- Expression: создаётся когда до неё доходит код
- Declaration: создаётся до выполнения всего кода

