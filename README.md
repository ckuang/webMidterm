# Web Development Midterm

## 1. Variables & Type
```js
var test1 = (6 > 5);
var test2 = 10 * 2 > 19 ? 'this is a test' : null;
var test3 = 0 || {huh: 'what am i ?'};
var test4;
var test5 = parseInt('22');
```
Match the correct letter/type to each variable above.
a. object <br/>
b. boolean <br/>
c. undefined <br/>
d. string <br/>
e. number <br/>


## 2. Truthy and Falsy 1
What would the following lines of code output to the console?
```js
a. console.log(0 || 1);
b. console.log(1 || 2);
c. console.log(0 && 1);
d. console.log(1 && 2);
```

## 3. Truthy and Falsy 2
```js
function checkcheck(value) {
  if (value) {
    return true
  } else {
    return false
  }
}
```
**For example:**
`checkcheck(NaN)` // returns: false
**For each of the below problems, write whether they would return `true` or `false`:**
a. `checkcheck(false)`
b. `checkcheck(true)`
c. `checkcheck(null)`
d. `checkcheck(42)`
e. `checkcheck(undefined)`
f. `checkcheck(0)`
g. `checkcheck("")`
h. `checkcheck("foo")`


## 4. Push & Slice
What will the following code log to the console?
```js
var arr = [];
arr.push('RZA');
arr.push('GZA');
arr.push('Raekwon');
arr.push('Ghostface');
arr.slice(0);
console.log(arr);
```

## 5. Array log
What will the following code log to the console?
```js
var arr = ['RZA', 'GZA', 'Raekwon', 'Ghostface'];

function mystery(arr) {
  console.log(arr[arr.length - 2]);
}

mystery(arr);
```

## 6. Array sum
What will the following code log to the console?
```js
var arr = [1, 2, 3];

function mystery(arr) {
  var sum = 0;
  for(var i = 0; i < arr.length; i++) {
    var toAdd = arr[i] * 2;
    sum += toAdd;
  }
  return sum;
}

console.log(mystery(arr));
```

## 7. Array loop
What will the following code log to the console?
```js
var arr = [10, 1, 15, 2, 20, 3];

function mystery(arr) {
  for(var i = 0; i < arr.length; i++) {
    console.log(Math.max(5, i));
  }
}

mystery(arr);
```

## 8. Filter
What will the following code log to the console?
```js
var arr = [10, 1, 15, 2, 20, 3];

function mystery(arr) {
  return arr.filter(function(val) {
    return val % 2 === 0;
  })
}

console.log(mystery(arr));
```

## 9. Map
What will the following code log to the console?
```js
var arr = [1, 2, 3, 4, 5];

function mystery(arr) {
  return arr.map(function(val) {
    return val * 3;
  })
}

console.log(mystery(arr));
```

## 10. Array logical operators
What will the following code log to the console?
```js
var arr = [10, 2, 3, 4, 5];

function mystery(arr) {
  for(var i = 0; i < arr.length; i++) {
    if(arr[i] >= 10 || arr[i] % 2 === 0 && arr[i] <= 5) {
      console.log(arr[i]);
    }
  }
}

mystery(arr);
```

## 11. Scope
What will the following code log to the console?
```js
var counter = 10;
function mystery1(){
  counter += 1;
  console.log(counter);
}

function mystery2() {
  var counter = 5;
  counter += 1;
  console.log(counter)
}
mystery2();
mystery1();
mystery1();
```

## 12. Scope & Closure
What will the following code log to the console?
```js
var counter = 20;
function mystery1() {
  var counter = 10;
  return function(num) {
    console.log(counter + num);
  }
}

var mystery2 = mystery1();
mystery2(10);
```

## 13. DOM
`index.html` file:
```html
<html>
    <head>
        <script src="index.js" defer></script>
    </head>
    <body>
		<div>
      <p class="text1">Cat</p>
			<p id="text1">Dog</p>
      <p id="text2">Bear</p>
		</div>
    </body>
</html>
```
What will the following code log to the console?
`index.js` file:
```js
a. console.log(document.getElementById('text1').innerHTML);
b. console.log(document.getElementsByTagName('p')[2].innerHTML);
c. console.log(document.getElementsByClassName('text1')[2].innerHTML);
```

## 14. Constructor Functions
Given the following test cases, write a constructor function called  `Drink` that will allow you to make new `Drink` objects with a `name` and `carbonated` property. The `Drink` function should also include a `shake` prototype method that produces the following results:
```js
let sprite = new Drink('Sprite', true)
sprite.name // returns 'Sprite'
sprite.carbonated // returns true
sprite.shake() // returns "EXPLOSION!!!"

let oj = new Drink('Orange Juice', false)
sprite.name // returns 'Orange Juice'
sprite.carbonated // returns false
oj.shake() // returns "nothing happens..."
```

## 15. Odd nums
Write a function `oddNums` that receives an array of strings and numbers and returns an array of only the odd numbers.
```js
oddNums([1, 'hey', 2, 3, 4, 'hi', 5, 6, 'hello', 7]) // returns [1, 3, 5, 7]
oddNums([3, 18, 'what up', 23, 48, 'cya', 99]) // returns [3, 23, 99]
```

## 16. Loops and Conditionals
Write a function `vowToNum` to replace every letter `e` or `E` with a `3` and every `i` or `I` with a `1` and `o` or `O` with `0`. You can use a if...else or switch...case.
```js
vowToNum("Apple") // returns "Appl3"
vowToNum("Cheese Doodle") // returns "Ch33s3 D00dl3"
vowToNum("hello kitty") // returns "h3110 k1tty"
```

## 17. Function Return
Identify why the following function doesn't work, and then rewrite the correct solution.

The goal of the function is to take in a string and a letter, return `true` if the letter is in the string, and return `false` if the letter is not in the string.

**Rewrite the code so that it works.**
```js
function containsInString(string, letter) {
  for(let i = 0; i < string.length; i++) {
    if(string[i] === letter) {
      return true;
    } else {
      return false;
    }
  }
}

containsInString('pineapple', 'a');
```

## 18. Count the vowels
Write a function called countVowels that takes in a string. It should return an object containing the number of times each vowels appears in the string.

Examples:
```js
countVowels('testing'); //{a: 0, e: 1, i: 1, o: 0, u: 0}
countVowels('poetic justice, put it in a song'); //{a: 1, e: 2, i: 4, o: 2, u: 2}
```

## 19. Recursion
Write a recursive function `stringCombine()` that receives two strings and returns one reconstructed string with alternating letters from the two strings.
```js
stringCombine('abc', 'def') // returns 'adbecf'
stringCombine('cat', 'dog') // returns 'cdaotg'
stringCombine('charles', 'nate') // returns 'cnhaatreles'
```
