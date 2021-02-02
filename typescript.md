# Typescript

*Typescript* offers all javascript features plus Typescript's type-system.
The main benefit is that it can highlight unexpected behavior, lowering the change of bugs to occur.

**Primitive types**
-number
-boolean
-void
-undefined
-string
-symbol
-null

**Object types**
-functions
-arrays
-classes
-objects

**Type annotations**
Code that tells Typescipt what type of value a variable will refer to.

**Type inference**
Typescipt tries to figure out what type of value a variable refers to.

**Type annotations**
```
let apple: number = 5;
let speed: string = 'fast';
let hasName: boolean = true;
let nothingMuch: null = null;
let nothing: undefined = undefined;

// Built in objects
let now: Date = new Date();

// Array
let colors: string[] = ['red', 'green', 'blue'];
let myNumbers: number[] = [1, 2, 3];
let truths: boolean[] = [true, true, false];

// Classes
class Car {

}
let car: Car;

// Object literal
let point: { x:number; y: number } = {
  x:10,
  y: 20
}

// Function
const logNumber: (i: number) => void = (i: number) => {
  console.log(i)
}
```

**Type inference**
If declaration and initialization are on the same line, Typescript will figure out the type of 'color' for us.
```
const color = 'red';
```

**When to use annotations**
1.Function that returns the 'any' type.
```
const json = '{"x": 10, "y": 20'};
const coordinates: { x: number; y: number} = JSON.parse(json); 
console.log(coordinates)
```
2.Declaring a variable on one line and initializing it later.
```
let words = ['red', 'green', 'blue']
let foundWord: boolean;

for (let i = 0; i < words.length; i++) {
  if (words[i] = 'grren') {
    foundWord = true;
  }
}
```


3.Variables whose type cannot be inferred correctly
```
let numbers = [-10, -1, 12];
let numberAboveZero: boolean | number = false;

for (let i = 0; i < numbers.length; i++) {
  numberAboveZero = numbers[i]
}
```

**Any type**
-A type, simliar to 'string' or 'boolean'
-TS has no idea what this is - can't check for correct propery references
-**Avoid variables with 'any' at all costs**

**Type annotations for functions**
Code added to tell Typescript what type of arguments a function will recieve and what type of values it will return

**Type inference for function**
Typescript tries to figure out what type of value a function will return.