# generators-function
- Generators can return multiple values
- Syntax construct:  function* generator() {

	yield 1;
	
	yield 2;
	
	yield 3;
	
	return 4;
	
	}
- The main method is ```next()```. The result of method ```next()``` is object with two properties: ```value```: yielded value;
  ```done```: ```true``` if the function code has finished, otherwise ```false```.
```
function* generator() {
     yield 'S';
     yield 'c';   
     yield 'r';
     yield 'i';    
     yield 'p'; 
     yield 't';   
 } 
 
 const str = generator();
 console.log(str.next());        //{ value: 'S', done: false } 
 console.log(str.next().value); // c 
```
- Generators work great with iterables
- Can use loop ```for```:
```
function* count(n) {
    for (let i = 0; i < n; i++) {
        yield i;
    }
}
const counter = count(7);

console.log(counter.next().value); // 0
console.log(counter.next().value); // 1
console.log(counter.next().value); // 2
```
- Loop over their values usin ```for..of```:
```
function* count(n) {
    for (let i = 0; i < n; i++) {
        yield i;
    }
}

for (let k of count(7)) {
    console.log(k);       // 0, 1, 2, 3, 4, 5, 6
}
```

