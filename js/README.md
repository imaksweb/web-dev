<h1 align="center">JavaScript CheatSheet</h1>

## Основы

### Falsy values:

* 0
* NaN
* ""
* false
* null
* undefined

## Деструктуризация

### Как поменять значения переменных местами с помощью деструктуризации

```js
let a = 1, b = 2;

[b, a] = [a, b];
```

### Присвоение переменным данных из объекта с помощью деструктуризации

```js
const suspects = [
  {
    firstName: 'John',
    lastName: 'Doe'
  },
  {
    firstName: 'Raphael',
    lastName: 'Nadal'
  }
]

const [{firstName: suspectOne}, {firstName: suspectTwo}] = suspects;

console.log(suspectOne); // John
console.log(suspectTwo); // Raphael
```

## Циклы

### List Transformations with forEach and Function

```js
function createSuspectObjects(name) {
  return {
    firstName: name.split(' ')[0],
    lastName: name.split(' ')[1],
    speak() {
      consloe.log('My name is', name);
    }
  }
}

const suspects = ['John Doe', 'Raphael Nadal', 'Rodger Federer'];
let suspectsList = [];

suspects.forEach(suspect => {
  suspectsList.push(createSuspectObjects(suspect));
})
```