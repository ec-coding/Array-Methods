<h1>Array Methods Review</h1>

- **.filter()**
  - Creates a copy of a portion of a given array, filtered down to just the elements from the given array that pass the conditions set forth by the provided function.

  - Examples:
```
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]
```

```
const ages = [32, 33, 16, 40];

document.getElementById("demo").innerHTML = ages.filter(checkAdult);

function checkAdult(age) {
  return age >= 18;
}

// expected output: Array [32,33,40]
```
