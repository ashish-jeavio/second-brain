
1. What is React, and what are its main features?
2. What is JSX and how does it work?
3. Explain the concept of the Virtual DOM in React.
4. How does virtual DOM in React work? What are its benefits and downsides?
5. What are React Fragments used for?
6. What is the purpose of the `key` prop in React?
7. Guess the output :
   ```
	const [count, setCount] = useState(0);

	<button onClick={() => {
	  setCount(count + 1);
	  setCount(count + 1);
	  setCount(count + 1);
	}}>
   ```
8. Guess the output : 
```
const [count, setCount] = useState(0);

<button onClick={() => {
  setCount(c => c + 1);
  setCount(c => c + 1);
  setCount(c => c + 1);
}}>
```
9. Guess the output :
```
const [count, setCount] = useState(0);

<button onClick={() => {
  setCount(count + 1);
  setTimeout(() => {
    setCount(count + 1);
  }, 0);
}}>

```
10. Guess the output :
```
const [count, setCount] = useState(0);

<button onClick={() => {
	setCount(count + 1);
	setCount(prev => prev + 1);
	setCount(count + 1);
}}>
```
11. Guess the output :
```
const [count, setCount] = useState(0);

<button onClick={() => {
	setCount(count + 4);
	setCount(prev => prev + 2);
	setCount(count + 1);
}}>
```
12. Guess the output : 
```
const [value, setValue] = useState(10);

console.log("A:", value);
setValue(20);
console.log("B:", value);

setTimeout(() => console.log("C:", value), 0);
```
13. Why we need useEffect hook ?
14. Can we call multiple useEffects in one Component ? 
15. What is reconciliation?
16. What are the rules of React hooks?
17. What does the dependency array of `useEffect` affect?
18. What is the consequence of using array indices as keys in React?
19. How would you lift the state up in a React application, and why is it necessary?
20. What is the `useRef` hook in React and when should it be used?
21. What are some common performance optimization techniques in React?
22. What is pure component ?
23. What is HOC Design pattern ? 
24. Why can't we make useEffect function async ?
25. What is `React.memo` ?
26. CSR vs SSR vs SSG vs ISR ? How can we decide which to use ?
27. Difference between `useMemo` and `useCallback`.