# generator-function
Generator can return multiple values
Syntax construct: function* generator() {
	yield 1;
	yield 2;
	yield 3;
	return 4;
	}
The main method is next(). The result of method next() is object with two properties: -value: yielded value; -done: true if the function code has finished, otherwise false.



