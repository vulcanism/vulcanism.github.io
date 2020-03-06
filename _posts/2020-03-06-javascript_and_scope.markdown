---
layout: post
title:      "JavaScript and Scope"
date:       2020-03-06 12:28:55 -0500
permalink:  javascript_and_scope
---


So, what is "scope," anyway? In simple terms, scope determines where variables and other resources (like functions) are visible in the code you write. There are three different types of scope in JavaScript: global scope, block scope, and function scope. Some may group the latter two together, referring to both as "local scope."

Functions or variables defined in the global scope, or global execution context, are accessible anywhere in your JavaScript code. For example, take the following code: 

![](https://i.imgur.com/FE5hRsP.png)

Running `logX()` successfully logs the number 11 to the console, because `x` is defined in the global scope. It is not defined inside a function or a block statement.

Block scope, as the name suggests, is scope that exists within a block of code. This could be an `if` statement, or a `for` loop. Variables that are defined within a block statement are not accessible outside of that block. So, for instance, if I were to define `let x = 11` within an `if` statement, and then tried to run `console.log(x)` outside of that `if` statement, JavaScript would throw me an error. As far as the `console.log` knows, `x` was never defined, because it only exists within the block scope of the `if` statement.

It is worth noting that only variables defined with `let` or `const` are block-scoped. Variables declared with `var` are not.

That leaves function scope, which refers to the scope within a written function. Similar to block scope, the variables defined within a function cannot be accessed outside of that function. They can, however, be accessed anywhere within it. So, looking at the code below:

![](https://i.imgur.com/KbrCaTH.png)

Calling `a()` would return the number 24. If I were to attempt to `return y * 2` outside of `function a()`, however, JavaScript would give me an error. This is because `y` only exists within the context of `function a()`. It's for this reason that variable names can be reused within different, separate (i.e. not nested) functions in JavaScript without getting errors. Although, reusing variable names too much is likely to cause problems in other ways.

Additionally, it is possible to "chain" scopes within a function. If `function b()` exists within `function a()`, then `function b()` has access to any variables defined in `function a()`. That said, this type of chaining only works in one direction—an inner scope can access an outer scope, but *not* vice versa.

It can be easy to get caught up in all the little details when it comes to scope, and to overlook why your `console.log` isn't printing the correct value. Like many aspects of JavaScript, though, all it'll take to get used to it is a lot of practice.
