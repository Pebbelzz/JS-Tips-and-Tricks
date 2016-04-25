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
