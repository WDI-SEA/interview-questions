## Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```
"1020"

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```
var add = function(2) {
    return function(5) { return 2 + 5; };
}

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

"goh angasal a m'i"

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
Hello World

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
2

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```
{n: 2};

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');

one
three
undefined
two