# Result Type

Solana Suite's responses are implemented using the Result Type, a pattern
commonly used in functional programming languages like Rust. Handling responses
from functions can be done as follows. Additionally, exceptions occurring
internally are converted to Result Type using Try().

### Example1 type guard

```js
// success, ok  => ex1.value
// failed,  err => ex1.error

ex1.isOk && console.log("# ex1: ", ex1.value);

if (ex1.isOk) {
  console.log("# ex1: ", ex1.value);
} else if (ex1.isErr) {
  console.log("# ex1 error: ", ex1.error);
}
```

### Example2 unwrap

```js
ex2.unwrap());
```

### Example3 map

```js
const mapped = ex3
   .map(
     (value: number) => number * 100,
     (error: Error) => new Error(error.message),
   )
```

### Example4 match

```js
ex4.match(
  (value: number) => console.log('# value: ', value),
  (error: Error) => console.error(error),
);
```