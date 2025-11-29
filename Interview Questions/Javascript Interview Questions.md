2. Is javascript interpreted or compiled language ?
3. What are the datatypes in Javascript ? 
1. What is Javascript ? 
4. What is the difference between `==` and `===` ?
5. What is hoisting ?
6. What is the difference between var, let and const ?
7. What is the closure ?
8. What is `this` keyword ?
9. What is spread and rest operator ? 
10. What is the difference between `map()` and `forEach()` ?
11. Predict the output :
```
console.log(a);
var a = 5;
console.log(a);
```
12. Predict the output : 
```
console.log(b);
let b = 10;
console.log(b);
```
13. Predict the output : 
```
foo();
function foo() {
  console.log("A");
}
foo = function () {
  console.log("B");
};
foo();
```
14. What is currying ?
15. Predict the output : 
```
bar();
var bar = function () {
  console.log("X");
};
```
16. Predict the output : 
```
function test() {
  console.log(x);
  var x = 20;
  console.log(x);
}
test();
```
17. Predict the output : 
```
function run() {
  console.log(y);
  let y = 30;
}
run();
```
18. Explain the behavioral difference between calling `funcs.forEach(fn());` and `funcs.forEach(fn => fn());` when `funcs` is an array of functions.
19. Predict the output : 
```
var x = 1;
function outer() {
  console.log(x);
  var x = 2;
  console.log(x);
}
outer();
```
20. Predict the output : 
```
function demo() {
  console.log(typeof z);
  const z = 50;
}
demo();
```
21. Describe the difference between function declaration hoisting and function expression hoisting.
22. Explain the Temporal Dead Zone and why it exists.
23. Why does JavaScript hoist declarations during the compilation phase instead of execution?
24. Predict the output :
```
console.log(m);
var m = 1;
let m = 2;
console.log(m);
```
25. Explain Javascript runtime ? 
26. What is difference between Task Queue and Micro-task Queue ?
27. Predict the output : 
```
Promise.resolve()
	.then(() => console.log(1));

setTimeout(() => console.log(2), 10);

queueMicroTask(() => {
	console.log(3);
	queueMicroTask(() => console.log(4));
});

console.log(5);
```
28. What is callback in Js ?
29. Predict the output: 
```
person = { "name" : "Ashish" } 
person2 = { "name": "Ashish" } 
console.log(person === person2) 
console.log(person == person2)
```
30. Predict the output: 
```
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 100);
}
```
31. Predict the output:
```
for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 100);
}
```
32. Predict the output:
```
function makeCounter() {
  var count = 0;

  return function () {
    count++;
    console.log(count);
  };
}

const c1 = makeCounter();
c1();
c1();
```
33. Consider this object `test: { a:'1', b:{c:'2', d:'3'} }`. Now, define a function `getProperty(test, path)` such that if `path` is `"b.c"`, it prints `'2'` because `test.b.c` is `'2'`.
34. Implement a deep clone : deepClone({ a: 1, b: { c: 2 } })
35. Implement a deep equal : deepEqual(obj1, obj2)
36. What is debouncing and throttling?
37. setTimeout vs setInterval
38. What are the ES6 features you know ?


---
Resources :

https://youtu.be/eiC58R16hb8?si=gqzp_p5MthCBuc5P

https://youtu.be/vKJpN5FAeF4?si=vlfqtFJe39MgU_Mb

