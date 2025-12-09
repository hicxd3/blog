+++
date = '2025-12-07T18:53:24+03:00'
title = 'Локальные и глобальные переменные в функциях  JavaScript'
+++

### Локальные переменные

Это переменные объявленные внутри тела функции и их будет видно только внутри функции

Например

```JavaScript
function hiEva () {
	let sayHi = "Привет Шиноби"; // локальная переменная
	console.log(sayHi);
}
hiEva(); // Привет Шиноби
console.log(sayHi); // Ошибка, значения переменной видно только внутри функции
```

### Внешние переменные

У функции есть доступ к внешним переменным, то есть во время исполнения функции мы можем прочитать как локальные данные так и внешние, например

```JavaScript
let userName = Eva;

function showMessage() {
	let message = 'Привет, ' + userName;
	console.log(message);
}

showMessage(); // Привет, Eva
```

Так же функция обладает полным доступом к внешним переменным и даже может изменять их значения

```JavaScript
let userName = Alice;

function showMessage () {
	userName = "Eva"; // Меняем значение
	let message = "Привет, " + userName;
	console.log(message);
}

console.log(userName); // Alice

showMessage();

console.log(userName); // Привет, Eva
```

При выполнении кода, функция сначала ищет локальные переменные, если не находит обращается в внешним

