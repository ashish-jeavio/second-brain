1. What is Javascript ? 
2. Is javascript interpreted or compiled language ?
3. What are the datatypes in Javascript ? 
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
39. Reduce vs Map vs Filter function 
40. If I have a normal function, and outside of it there is just a simple variable (no outer function involved), and I access that variable inside my function — does that count as a closure? Why or why not?”
41. Predict the output
```
let t = { a: 1 };
let r = t;
t = { a: 2 };
console.log(r.a);
```
42. Predict the output :
```
const arr = [1, 2, 3];
arr[10] = 99;
console.log(arr.length);
console.log(arr[5]);
```
43. Predict the output :
```
console.log([1] + [1, 2]);
console.log([] == ![]);
console.log([] == []);
console.log([] === []);
```
44. Predict the output :
```
async function run() {
  console.log(1);
  await Promise.resolve();
  console.log(2);
}
setTimeout(() => console.log(3));
run();
console.log(4);
```
45. Predict the output :
```
function make() {
  const out = [];
  for (var i = 0; i < 3; i++) {
    out.push(() => i);
  }
  return out;
}
const fns = make();
console.log(fns[0](), fns[1](), fns[2]());
```
46. Predict the output :
```
const user = { name: "A" };
Object.freeze(user);
user.name = "B";
console.log(user.name);
```
47. Predict the output :
```
const obj = {
  val: 1,
  inc() {
    return () => {
      this.val++;
    };
  }
};
const fn = obj.inc();
fn();
console.log(obj.val);
```
48. Predict the output :
```
function A() {}
A.prototype.x = 1;
const a1 = new A();
A.prototype = { x: 2 };
const a2 = new A();
console.log(a1.x, a2.x);
```
49. Predict the output :
```
function A() {}
A.prototype.x = 1;
const a1 = new A();
A.prototype.x = 2;
const a2 = new A();
console.log(a1.x, a2.x);
```
50. Predict the output : 
```
function calc(a = b, b = 10) {
  return a + b;
}
console.log(calc());
```
51 Predict the output :
```
function* g1() {
  yield 1;
  yield 2;
}
function* g2() {
  yield* g1();
  yield 3;
}
console.log([...g2()]);
```
52. Predict the output : 
```
const target = { x: 1 };
const proxy = new Proxy(target, {
  get(t, p) {
    if (p === "x") return t.x * 10;
    return Reflect.get(t, p);
  }
});
console.log(proxy.x, target.x);
```
53. What is call, apply, bind ?
54. What is prototype inheritance ?
55. Write your own map function : `Array.prototype.myMap = function(cb) { … }`
56. Predict the output :
```
function T() {}
const t1 = new T();
const t2 = { __proto__: T.prototype };
console.log(t1 instanceof T);
console.log(t2 instanceof T);
```
57. What is event delegation ?
58. What is `!!` operator in JS ?
59. Predict the output : 
```
console.log(1 + "2" + 3);
console.log(1 + 2 + "3");
console.log("5" - 2);
console.log("5" + 2);
console.log("10" - "5" + "2");
console.log("10" - "5" + 2);
console.log(true + "1");
console.log(true - "1");
console.log([] + []);
console.log([] + {});
console.log({} + []);
console.log("2" * "3");
console.log(null + 1);
console.log(undefined + 1);
console.log(" " - 1);
console.log(" 10 " - 5);
console.log("10" / "2");
```
60. Explain event bubbling and event capturing.
61. Predict the output :
```
console.log(1 + "2" + "2");
console.log(1 + +"2" + "2");
```
62. Predict the output :
```
console.log(NaN == NaN);
console.log(NaN === NaN);
```