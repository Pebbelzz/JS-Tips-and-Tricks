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
