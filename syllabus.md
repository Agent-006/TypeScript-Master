# MANDATORY STUFF:

Install vs code, nodejs and tyepscript

# LET'S WRITE SOME CODE:

## Basic Types

- Number, String, Boolean
- Arrays, Typles
- Any, Unknown, Never, Void
- Enums

### Number, String, Boolean
```
let arr: [];
let arr3: string;

let variable: number;
let variable1: boolean;
```
### Arrays, Typles
```
let variable2: [];
let array: [boolean ,number, string] = [false, 1, 'hello'];

array.push(2);
console.log(array);
```

### any, unknown
these 2 have some differences will discuss later
```
let variable3: unknown;
let variable4: any;
```

### never
never is used when a function never returns anything
```
function runInfiniteLoop(): never {
    while(true) {
        console.log('Infinity');
    }
}

runInfiniteLoop();
```
running the function will cause the program to run infinitely and never return anything back to the caller function. Also the code below the function will not run as the function will run infinitely.

### void

 * The function `efgh` logs 'Hello' to the console.
```
function efgh(): void {
    console.log('Hello');
}
```

`efgh();` is calling the function named `efgh` in TypeScript. This function logs 'Hello' to the
console. So, when `efgh();` is executed, it will output 'Hello' to the console. 
```
efgh();
```


 * The function "abcd" in TypeScript returns the number 12.
 * @returns The function `abcd` is returning the number 12.
```
function abcd(): number {
    return 12;
}

abcd();
```
### Enums

```
let upDirection = "UP";
let downDirection = "DOWN";
let leftDirection = "LEFT";
let rightDirection = "RIGHT";
```

## Type Inference

Type inference is a feature in many programming languages where the compiler or interpreter automatically deduces the types of variables or expressions without the need for explicit type annotations by the programmer.

For example, if you write a line of code like let x = 5 in a language that supports type inference, the compiler can infer that x is of type integer based on the value 5. This makes the code more concise and often easier to write, as the programmer doesn't need to manually specify the type of every variable.

```
let a = 12;
let b = 'a';
let c = true;
```

Type inference is common in statically typed languages like TypeScript, Swift, and Rust, and helps in reducing boilerplate code while still maintaining type safety.

## Union and Intersection Types

### Union

```
let variable: string | null;

variable = null;
variable = 'abcd';
```

```
function abcd(variable: string | number) {
    if (typeof variable === 'string') {
        variable.toUpperCase();
    } else {
        variable.toFixed(2);
    }
}

abcd('abcd'); // OK
abcd(123); // OK
// abcd(true); // Error
```

### Intersection
```
type City = {
    name: string;
    population: number;
}

type Planet = {
    name: string;
    cities: number;
}

type CitiesInPlanet = City & Planet;

let value: CitiesInPlanet = {
    name: 'Earth',
    population: 7_594_000_000,
    cities: 1_000_000
}
```

## Type Aliases



## Interfaces

## Classes

- Constructors
- Public, Private, Protected Members
- Readonly Properties


