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

`Note : Remaining : Generator functions, Proxy & Reflect`

---
Resources :

https://youtu.be/eiC58R16hb8?si=gqzp_p5MthCBuc5P

https://youtu.be/vKJpN5FAeF4?si=vlfqtFJe39MgU_Mb

https://youtu.be/AOPmqw9scfc?si=Z_smWyRnRt_hxNfd

https://youtu.be/IJ6EgdiI_wU?si=N5f4eTGjwZfVem6X

yet to watch : https://youtu.be/TGGoiJBuv-Y?si=GtxDch0sEZghrqaq , https://youtu.be/9jl1lhFylJs?si=OCUHH9NdnR50be5d

---

Notes : Every function that accesses an outer variable is a closure.

----

# 🔥 **THE DEFINITIVE JAVASCRIPT TYPE COERCION CHEAT SHEET**
---

# ✅ **1. JavaScript Does Automatic Type Conversion (Coercion)**

JavaScript tries to convert values **implicitly** when different types are used together.

There are **three** important conversions:

### **1. ToPrimitive (object → primitive)**

### **2. ToString (value → string)**

### **3. ToNumber (value → number)**

Most weirdness comes from these conversions happening at the wrong time.

---

# 🔥 **2. The SINGLE most important rule:**

# 💡 **`+` operator behaves differently from all other operators.**

| Operator                     | Coercion Rule                                                       |
| ---------------------------- | ------------------------------------------------------------------- |
| **`+`**                      | If either operand is a **string**, JS does **string concatenation** |
| **`-`, `*`, `/`, `%`, `**`** | ALWAYS convert operands to **numbers**                              |

This ALONE explains >90% of coercion weird cases.

---

# 🔵 **3. Why `+` behaves weirdly**

Because `+` is **overloaded**:

### It can mean:

* **Numeric addition**
* **String concatenation**

So JS checks:

```
If any operand is string → convert both to string → concatenate.
Else → convert to number → add.
```

### Examples:

```
1 + "1" → "1" + "1" = "11"
"5" + 2 → "5" + "2" = "52"
```

---

# 🔴 **4. Why `-`, `/`, `*` do NOT behave like `+`**

These operators **only have numeric meaning**.

So JS converts operands to **numbers** first:

```
"5" - 2
→ Number("5") - 2
→ 5 - 2 = 3
```

Same for multiply/divide:

```
"2" * "3" → 6
"10" / "5" → 2
```

---

# 🟢 **5. How primitives convert internally**

## **5.1 ToNumber Conversion Rules**

Here’s the full mapping:

| Value       | ToNumber result |
| ----------- | --------------- |
| `"10"`      | 10              |
| `" 10 "`    | 10              |
| `""`        | 0               |
| `" "`       | 0               |
| `true`      | 1               |
| `false`     | 0               |
| `null`      | 0               |
| `undefined` | **NaN**         |
| `"abc"`     | **NaN**         |
| `[]`        | 0               |
| `[5]`       | 5               |
| `{}`        | NaN             |
| `["1","2"]` | NaN             |

---

## **5.2 ToString Conversion Rules**

| Value       | ToString result     |
| ----------- | ------------------- |
| `1`         | `"1"`               |
| `true`      | `"true"`            |
| `[]`        | `""`                |
| `[1,2]`     | `"1,2"`             |
| `{}`        | `"[object Object]"` |
| `null`      | `"null"`            |
| `undefined` | `"undefined"`       |

This explains:

```
[] + [] → "" + "" = ""
[] + {} → "" + "[object Object]"
{} + [] → tricky parsing; can be "[object Object]" or 0
```

---

# 🟣 **6. ToPrimitive (for objects, arrays, dates)**

When JS needs a primitive from an object/array:

1. Try `valueOf()`
2. If still object → try `toString()`
3. If still object → throw error

### Arrays:

```
[].toString() → ""
[1,2].toString() → "1,2"
```

### Objects:

```
{}.toString() → "[object Object]"
```

---

# 🔥 **7. Why these specific weird cases happen**

### **Case: `"10" - "5" + "2"` → `"52"`**

Step 1: `"10" - "5"` → numeric → `5`
Step 2: `5 + "2"` → string concat → `"52"`

---

### **Case: `null + 1` → 1**

Because:

```
null → 0  
0 + 1 = 1
```

---

### **Case: `undefined + 1` → NaN**

Because:

```
undefined → NaN  
NaN + 1 = NaN
```

---

### **Case: `" " - 1` → -1**

```
" " → 0  
0 - 1 = -1
```

---

# 🧠 **8. Operator Precedence with Coercion**

JS evaluates left to right for `+`:

```
1 + 2 + "3"
→ 3 + "3"
→ "33"
```

But:

```
1 + "2" + 3
→ "12" + 3
→ "123"
```

---

# 🧩 **9. The Most Important Summary — Final Rules**

Here is the **everything-in-one-page** summary:

---

## ⭐ **Rule 1: Only `+` does string concatenation.**

If either operand is a string:

```
a + b → String(a) + String(b)
```

---

## ⭐ **Rule 2: All other arithmetic ops → force Number(a).**

```
a - b
a * b
a / b
a % b
```

All convert inputs to numbers.

---

## ⭐ **Rule 3: Coercion Priority**

When performing an operation, JS applies:

1. **Check operator**
2. If `+`, check if any operand → string
3. If not string → convert both to **number**
4. If operand is object/array → apply **ToPrimitive**:

   * `valueOf()`
   * then `toString()`

---

## ⭐ **Rule 4: Special conversions to memorize**

* `null` → **0**
* `true` → **1**
* `false` → **0**
* `""` → **0**
* `" "` → **0**
* `undefined` → **NaN**
* `[]` → **""** (string), **0** (number)
* `{}` → `"[object Object]"` (string), **NaN** (number)

---

# 💯 FINAL CHEAT SHEET (Print this mentally)

### **If operator is `+`:**

* If string involved → **string concat**
* Else → **number addition**

### **If operator is not `+`:**

* Convert everything to **number**

### **Converting to Number:**

* `"10"` → 10
* `""` → 0
* `" "` → 0
* `true` → 1
* `false` → 0
* `null` → 0
* `undefined` → NaN
* `[]` → 0
* `{}` → NaN

### **Converting to String:**

* `[]` → `""`
* `{}` → `"[object Object]"`

---
