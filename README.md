<h1>Array Methods Review</h1>

- **.filter()**
  - Creates a copy of a portion of a given array, filtered down to just the elements from the given array that pass the conditions set forth by the provided function.
  - Does not execute the function for empty elements.
  - Does not mutate the original array.
  - Examples:
```
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]
```

```
const ages = [32, 33, 16, 40];

ages.filter(checkAdult);

function checkAdult(age) {
  return age >= 18;
}

// expected output: Array [32, 33, 40]
```

- **.map()**
  - Creates a new array filled with the results of performing callback functions on every element in the calling array.
  - Does not execute the function for empty elements.
  - Does not mutate the original array.
  - Examples:
```
const array1 = [1, 4, 9, 16];

// pass a function to map
const map1 = array1.map(x => x * 2);

console.log(map1);
// expected output: Array [2, 8, 18, 32]
```

```
const numbers = [4, 9, 16, 25];
numbers.map(Math.sqrt);

// expected output: Array [2, 3, 4, 50]
```

- **.find()**
  - Returns the first element in an array that satisfies the provided testing function.
  - If no values satisfy the testing function, undefined is returned.
  - Does not execute the function for empty elements.
  - Does not mutate the original array.
  - Examples:
```
const array1 = [5, 12, 8, 130, 44];

const found = array1.find(element => element > 10);

console.log(found);
// expected output: 12
```

```
const ages = [3, 10, 18, 20];

ages.find(checkAge);

function checkAge(age) {
  return age > 18;
}

// expected output: 20
```

- **.forEach()**
  - Executes a callback function once for each element in an array.
  - Is not executed for empty elements.
  - Examples:
```
const array1 = ['a', 'b', 'c'];

array1.forEach(element => console.log(element));

// expected output: "a"
// expected output: "b"
// expected output: "c"
```

```
let text = "";
const fruits = ["apple", "orange", "cherry"];
fruits.forEach(myFunction);

document.getElementById("demo").innerHTML = text;
 
function myFunction(item, index) {
  text += index + ": " + item + "<br>"; 
  
// expected output: 0: apple
// expected output: 1: orange
// expected output: 2: cherry
```

```
let sum = 0;
const numbers = [65, 44, 12, 4];
numbers.forEach(myFunction);

function myFunction(item) {
  sum += item;
}

// expected output: 125
```

- **.some()**
  - Checks if any array elements pass a test (via a callback function)
  - Executes the callback function once per each element in the array.
  - Returns `true` (and stops) if the function returns `true` for any one of the array elements.
  - Returns `false` if all of the array elements return `false`.
  - Does not execute the function for empty array elements.
  - Does not mutate the original array.
  - Examples:
```
const array = [1, 2, 3, 4, 5];

// checks whether an element is even
const even = (element) => element % 2 === 0;

console.log(array.some(even));
// expected output: true
```

```
const ages = [3, 10, 18, 20];
ages.some(checkAdult);

function checkAdult(age) {
  return age > 18;
}

// expected output: true
```

- **.every()**
  - Checks if all elements in an array fulfill a certain condition.
  - Returns `true` if the function returns `true` for all of the array elements.
  - Returns `false` if even one of the array elements return `false`.
  - Does not execute the function for empty array elements.
  - Does not mutate the original array.
  - Examples:
```
const isBelowThreshold = (currentValue) => currentValue < 40;

const array1 = [1, 30, 39, 29, 10, 13];

console.log(array1.every(isBelowThreshold));
// expected output: true
```

```
const ages = [32, 33, 16, 40];
ages.every(checkAge);

function checkAge(age) {
  return age > 18;

// expected output: false
```

- **.reduce()**
  - Returns a single value after executing a reducer function on each element in an array.
  - Does not execute the function for empty array elements.
  - Does not mutate the original array.
  - Examples:
```
const array1 = [1, 2, 3, 4];

// 0 + 1 + 2 + 3 + 4
const initialValue = 0;
const sumWithInitial = array1.reduce(
  (previousValue, currentValue) => previousValue + currentValue,
  initialValue
);

console.log(sumWithInitial);
// expected output: 10
```

```
const numbers = [175, 50, 25];
numbers.reduce(myFunc);

function myFunc(total, num) {
  return total - num;
  
// expected output: 100
```

- **.includes()**
  - Returns `true` if an array contains a specified value.
  - Returns `false` if the value is not detected.
  - Is case sensitive
  - Examples:
```
const array1 = [1, 2, 3];

console.log(array1.includes(2));
// expected output: true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// expected output: true

console.log(pets.includes('at'));
// expected output: false
```

```
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.includes("Mango");

// expected output: true
```

```
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.includes("Banana", 3);

// expected output: false
```
