---
title: How do you determine two values same or not using object 
categories: ["programming"] 
tags: ["JS"]
---
     The Object.is() method determines whether two values are the same value. For example, the usage with different types of values would be,
     ```javascript
     Object.is('hello', 'hello');     // true
     Object.is(window, window);   // true
     Object.is([], []) // false
     ```
     Two values are the same if one of the following holds:
     1. both undefined
     2. both null
     3. both true or both false
     4. both strings of the same length with the same characters in the same order
     5. both the same object (means both object have same reference)
     6. both numbers and
        both +0
        both -0
        both NaN
        both non-zero and both not NaN and both have the same value.

     **[⬆ Back to Top](#table-of-contents)**

