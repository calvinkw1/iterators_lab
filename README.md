# Iterators Lab

### Description

In the iterators lab we will be continuing our exploration of
iterators. We have a series of challenges that require you to use the
iterators we discussed in class. We will try to use various testing
methods to verify that your code is working.

### Phase-1

Research the following term and summarize your findings on it two to
three sentences:

* `higher-order function`


Update this README with a description of each of the following and an
example you've created:

* `forEach`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
				This is a replacement for the for loop, allowing you to call this function instead of having to write it out. It results in fewer lines of code and does the same exact thing as a for loop. This can only be called on an array.
					var names = ["Calvin", "Leo", "Jenni", "Brent", "Shilpa"]
					names.forEach(function sayHi(name) {
					    console.log("Hello " + name + "!")
					});

* `map`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
				Map allows you to perform a function on an array without changing the original array. The returned values are placed in a new array which is defined beforehand. This also allows you to replace the for loop.
					var numbers = [1, 2, 3, 4, 5];
					var products = numbers.map(function(num) {
					    return console.log(num * 2);
					});

* `filter`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
				The filter function allows you to create a new array from a previously defined array, but with only the specified contents of that array. Meaning, you can use filter to create a new array of only the items you want in that new array.
					var numbers = [1, 2, 3, 4, 5];
					function multiplesOf2(num) {
					    return num % 2 === 0;
					}
					var filteredNums = numbers.filter(multiplesOf2);
					console.log(filteredNums);

* `reduce`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)
				Reduce can be used to add together an array of numbers, or concatenate an array of strings. It takes in 4 parameters which are Previous Value, Current Value, Array Index, and the Array Name.
					var numbers = [1, 2, 3, 4, 5];
					var strings = ["Hello", "my", "name", "is", "Calvin"]
					numbers.reduce(function(prev, next) {
					    return prev + next;
					});
					strings.reduce(function(prev, next) {
					    return prev + next;
					});

* `some`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
				Some allows you to look for the first specified item in an array by using boolean values. It does not manipulate the contents of the given array as it will only give you the boolean value of your "search" terms.
					var numbers = [1, 2, 3, 4, 5];
					function biggerThan2(num) {
					    return num > 2;
					}
					numbers.some(biggerThan2);

* `every`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
				Every returns a boolean value depending on your condition. If the condition you set finds that every item in the array meets the condition, then this will return a 'true' value. If there's even one falsy value, it will return 'false'.
					var numbers = [1, 2, 3, 4, 5];
					function biggerThan2(num) {
					    return num > 2;
					}
					numbers.every(biggerThan2);

Use the notes provided to help guide you explanation.

### Phase-2

* Run `npm install` from the `iterators_lab` directory.
* Looks at the tests we've written in the `test` folder. Run the tests
  with `npm test` (also from the `iterators_lab` directory). They
  should all fail.
* Get all of the tests to pass by writing the necessary code in
  `src/iterators.js`.

### Phase-3

Refactor the following code using `map` to make only one call to the `map` function versus the two below.


```
var myNumbers = [ -1, 2, -3, 4, -5, 6];

var square = function(num) {
	return num * num;
};

var sqrRoot = function(num) {
	return Math.sqrt(num);
};


var sqrNumbers = map(myNumbers, square);
var absNumbers = map(sqrNumbers, sqrRoot);
```




