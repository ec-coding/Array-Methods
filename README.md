<h1>Array Methods Review</h1>

- **.charAt()**
  - Returns a new string consisting of the character located at the specified `index`. If the `index` is out of range, `charAt()` returns an empty string.

  - Examples:
```
const sentence = 'The quick brown fox jumps over the lazy dog.';

const index = 4;

console.log(`The character at index ${index} is ${sentence.charAt(index)}`);
// expected output: "The character at index 4 is q"
```

```
let text = "HELLO WORLD";
let letter = text.charAt(text.length-1);

document.getElementById("demo").innerHTML = letter;

// expected output: "D"
```
