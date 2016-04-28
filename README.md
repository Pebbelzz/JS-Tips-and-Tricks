# JS-Tips-and-Tricks

<h3>Need to sort Numbers?</h3>
<p>Javascript's .sort() default order is lexicographical, or in other words alphabetical order. So this would be converting to strings and then returning them in dictionary order.</p>
<p> So if you need to sort numbers this is what you will need:</p>
```javascript
  var numbers = [10, 3, 1 ,17, 33, 67, 4, 15];
  function numbersNeedSorting(a, b) {
     return a - b;
  }
  numbers.sort(numbersNeedSorting);
```

<h2>Algorithims</h2>

<h3>Sum all the numbers in an Array</h3>
<p>Using <strong>forEach</strong> Method</p>
```javascript
  var numbers = [1, 2, 3];
  var sum = 0;
  numbers.forEach(
    function sumArray(num){
      sum += num;
    }
  );
  console.log(sum);  
```

<h3>Sum all Primes up to provided value</h3>
```javascript

function sumPrimes(num) {
	var numArray = [];
	var primeArray = [];

	//make array of all numbers up to num starting with 2(the first prime);
	for(var n= 2; n <= num; n++){
		numArray.push(n);
	}
    
    //take each number in numArray and test it to see if it is 
    //divisible by any number from 2 up until number-1
    //if it is, then toggle primeStatus to false and the number
    //is not prime
	numArray.forEach(
		function(number){
			primeStatus = true;
			for(var i = 2; i < number; i++){
				if(number%i === 0){
					primeStatus = false;	
				}
			}
            //of prime status is still true after all tests by division
            //then put it in primeArray
			if(primeStatus === true){
				primeArray.push(number);
			}
		}
	);
    
  
    //sum all the values in Prime Array
	var sum = 0;
	primeArray.forEach(
		function sumArray(value){
			sum += value;
		}
	);
	return sum;
}
```

<h3>Convert Binary to English</h3>

```javascript
function binaryAgent(str) {
  //split str into an array
  str = str.split(" ");
  var asciiArray = [];
  
  //on each binary now in array, turn it into a decimal number
  //and then get what character it should be based on dec number
  str.forEach(
    function(bin){
      bin = parseInt(bin, 2).toString(10);
      bin = String.fromCharCode(bin);
      asciiArray.push(bin);
    }
  );
  
  //join array into string
  asciiArray = asciiArray.join("");
  return asciiArray;
}
```
