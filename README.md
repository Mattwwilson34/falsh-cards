# falsh-cards
JS flash cards

# Flash Cards
*** 
Q: What does `Undefined` mean?
A: `Undefined` means, value of the variable is not defined.
E: [MDN Undefined](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined) The global `undefined` property represents the primitive value `undefined`. It is one of JavaScript's [primitive values](https://developer.mozilla.org/en-US/docs/Glossary/Primitive) and is treated as [falsy](https://developer.mozilla.org/en-US/docs/Glossary/Falsy) for boolean operations.

***
Q: What does `Null` mean?
A: `null` means empty or non-existent value which is used by programmers to indicate “no value”.
E: [MDN Null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null) The value `null` represents the intentional absence of any object value. It is one of JavaScript's [primitive values](https://developer.mozilla.org/en-US/docs/Glossary/Primitive) and is treated as [falsy](https://developer.mozilla.org/en-US/docs/Glossary/Falsy) for boolean operations.

***
Q: [Difference between `null` and `undefined`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null#difference_between_null_and_undefined "Permalink to Difference between null and undefined")
A:  `null` means empty or non-existent value,  `undefined` means value of the variable is not defined.
E:
```javascript
typeof null          // "object" (not "null" for legacy reasons)
typeof undefined     // "undefined"
null === undefined   // false
null  == undefined   // true
null === null        // true
null  == null        // true
!null                // true
isNaN(1 + null)      // false
isNaN(1 + undefined) // true
```

***
Q: Difference betwenn equalliy (`==`) Vs. strict equality (`===`)
A: Equality (`==`) checks equlaity attempting to convert and compare operands of different types. The strict equality operator (`===`) checks equality, but always considers operands of different types to be different. Both equality operators return Bollean (`True/false`)

***
Close style flash card
**Rule for implicit coercion**
-   If both operands are same type use {`===`}
-   undefined {`==`} null
-   If one operands is string and another is a number, convert string to {`number`}
-   If one is boolean and another is non-boolean, convert boolean to {`number`} and then perform comparison
-   While comparing a string or number to an object, try to convert the object to a {` primitive type`} and then try to compare
