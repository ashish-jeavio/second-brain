1. How can you get a Typescript type from a Javascript value ?
```
const object = {
	foo: 'foo',
	bar: 123,
}
```
2. How can a value be either of type string or number ?
```
const user1: User = {
	id: 123,
};

const user2: User = {
	id: '123'
}
```
3. How can you combine two types ?
4. What are the resulting types C and D ? 
```
type A = 1 | 2;
type B = 2 | 3;

type C = A | B;
type D = A & B;
```
5. How do you remove the Typescript error ? 
```
const app = document.getElementById('app');
app.append('Welcome!');

ERROR : 'app' is possibly 'null'.
```
6. What is `keyof` operator in TS ?
7. Predict the output : 
```
const count = 0;
const username = "";
const preference = null;

// Using || (Logical OR):
const countOr = count || 10;     
const userOr = username || 'Guest';
const preferenceOr = preference || 'default_value'

// Using ?? (Nullish Coalescing):
const countNullish = count ?? 10;
const userNullish = username ?? 'Guest'; 
const preferenceNullish = preference ?? 'default_value'; 
```

