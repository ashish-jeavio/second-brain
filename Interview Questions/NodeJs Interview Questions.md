1. What is NodeJs ?
2. Explain NodeJs runtime environment ?
3. What is middleware in NodeJs ? 
4. setImmediate vs setTimeout
5. Event loop waits for call stack to be empty?
6. Predict the output :
```
console.log(1);

setTimeout(() => console.log(2), 0);

Promise.resolve().then(() => console.log(3));

console.log(4);
```
7. What is the role of libuv in Node.js?
8. Compare browser event loop vs Node.js event loop. What is different?
9. Predict the output :
```
setTimeout(() => console.log("timeout"), 0);
setImmediate(() => console.log("immediate"));
Promise.resolve().then(() => console.log("promise"));
process.nextTick(() => console.log("nextTick"));
```
10. Why is setTimeout not guaranteed to run exactly at the delay you pass? What factors affect timing?
11. How do browsers handle rendering frames inside the event loop?
12. Predict the output : 
```
const fs = require('fs');

fs.readFile(__filename, () => {
  console.log("I/O");

  setTimeout(() => console.log("timeout"), 0);

  setImmediate(() => console.log("immediate"));

  Promise.resolve().then(() => console.log("promise"));

  process.nextTick(() => console.log("nextTick"));
});

console.log("sync");
```
13. Why does Node.js have both nextTick and microtasks? What problem does nextTick solve?
14. How do you handle heavy CPU-bound tasks without blocking the event loop ?

---

https://youtu.be/Vdpx-9Oehdk?si=l7K8DueJvkEfmoDF