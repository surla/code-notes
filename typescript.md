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


### Arrays
When creating empty array, use type annotations
```
const carMakers: string[] = [];

// Type inference is used when array has objects
const cars = ['ford', 'toyota', 'chevy'];

const carsByMake0: string[][] = []
const carsByMake = [
  ['f150'],
  ['corolla'],
  ['camaro']
]

// Help with inference when extracting values
const car = carMakers[0];
const myCar = carmMakers.pop();

// Prevent incompatitble values
carMakers.push(100);

// Help with 'map'
carMakers.map((car:string): string => {
  return car.toUpperCase();
})
```

**Flexible Type**
```
const importantDates: (Date | string)[] = [new Date(), '2030-10-10'];
importantDates.push('2030-10-20');
importantDates.push(new Date());
```

Use type arrays anytime to represent a collection of records with some arbitrary sort order.

###Tuples
Array-like structure where each element represents some property of a record. Use objects instead of Tuples. 

```
const drink = {
  color: 'brown',
  carbonated: true,
  sugar: 40
};



const pepsi: [string, boolean, number] = ['brown', true, 40];

// Type alias
type Drink = [string, boolean, number];

const pepsi: Drink = ['brown', true, 40];
const sprite: Drink = ['clear', true, 40];
const tea: Drink = ['brown', false, 0];

const carSpecs: [number, number] = [400, 3354];

const carStats = {
  horsepower: 400,
  weight: 3354
}
```

### Interfaces
Creates a new type, describing the property names and values types of an object.

```
interface Vehicle {
  name: string;
  year: Date;
  broken: boolean;
  summary(): string;
}

interface Reportable {
  summary(): string;
}

const oldCivic = {
  name: 'civic',
  year: new Date(),
  broken: true,
  summary(): string {
    return `Name: $[this.name}`;
  }
};`

<!-- const printVehicle = (vehicle: { name: string; year: number; broken: boolean; summary(): string }): void => {
  console.log(`Name: ${vehicle.name}`);
  console.log(`Year: ${vehicle.year}`);
  console.log(`Broken: ${vehicle.broken}`);
}; -->

const printVehicle = (vehicle: Vehicle): void => {
  console.log(`Name: ${vehicle.name}`);
  console.log(`Year: ${vehicle.year}`);
  console.log(`Broken: ${vehicle.broken}`);
  console.log(vehile.summary());
};

const drink = {
  color: 'brown',
  carbonated: true,
  sugar: 40,
  summary(): string {
    return `My drink has ${this.sugar} grams of suga `;
  }
}

const printSummary = (item: Reportable): void => {
  console.log(item.summary());
}

printSummary(oldCivic);
printSummary(drink);
```

General Strategy for reusable code in Typescript:
-Create functions that accept arguments that are typed with interfaces.
-Objects/classes can decide to 'implement' a given interface to work with a function.

### Classes

Blueprint to create an object with fields (values) and methods (functions) to represent a 'thing'

```
class Vehicle {
  constructor(public color: string) {}

  protected honk(): void {
    console.log('Beeeep!);
  }
}

const vehicle = new Vehicle('orange');
console.log(vehicle.color);

class Car extends Vehicle {
  private drive(): void {
    console.log('Zooooom!');
  }

  startDriving(): void {
    this.drive();
    this.honk();
  }
}



const car = new Car('blue');
car.startDriving();
car.honk();


```

**Class method modifiers**
-Public - Method can be called any where, any time.
-Private - This method can only be called by other methods in *this* class.
-Protected - This method can be called by other methods in *this* class, or by other methods in child classes.


