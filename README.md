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

Q: There are 6 *falsy* things in JS, what are they?
A: False, Null, Undefined, ""/empty string, 0, NaN
	1. false
	2. Null
	3. undefined
	4. empty string
	5. 0
	6. NaN
***
## Rapid Fire Truthy/Falsy
**Q:** Is `'false'` is false?
**A:** No. Because, it's a string with length greater than 0. Only empty string is false.

**Q:** Is `' '` is false?
**A:** No. Because, it's not an empty string. There is a white space in it.

**Q:** What about `{}`?
**A:** true. It's an object. An object without any property is an object can't be falsy.

**Q:** Tell me about `[]`?
**A:** This is also truthy. It's an array object (array is child of object) is truthy.

**Q:** You talked bout `''` to be falsy. What about `new String('')`?
**A:** Though you are passing empty string to the string constructor, it is creating an String object. More precisely a instance of String object. It becomes an object. Hence, it is not false. so, it is truthy.

**Q:** Tell me about `new Boolean(false)`
**A:** truthy. As it creates an instance of the Boolean object which is an object. Object is truthy.

**Q:** `Boolean(function(){})`
**A:** `true` if you pass a truthy value to Boolean, it will be true.

**Q:** `Boolean(/foo/)`
**A:** `true`

**Q:** `true%1`
**A:** 0. When you are trying to find reminder of true, true becomes 1 and reminder of 1 while dividing by 1 is 0. you will get same result if you doe `false%1`

**Q:** `''%1`
**A:** 0
***
**Q:** As `[]` is true, `[]==true` should also be true. right?
A: Implicit Conversion! This is false
    1. true is converted to number and true = 1 `[]==1`
    2. JS tries to convert `[]` with 
