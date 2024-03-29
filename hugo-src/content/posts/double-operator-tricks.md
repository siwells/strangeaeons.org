+++
title = "Double Operator Tricks in JS"
date = 2021-08-06T16:56:43+01:00
tags = ["coding", "javascript"]
draft = false
+++


Here are two, occasionally useful, Javascript tricks that I recently discovered. They both involve doubling up operators.


# !!

Doubling up the standard logical NOT/negation operator '!', into '!!' will turn most values into booleans, i.e. cast to a boolean. So if you quickly want to pass a numeric or string value into a function that actually requires a boolean value as input then this is one way to do that. For example:

```
> !!true
true
> !!false
false
> !!1
true
> !!0
false
> !!console
true
> !![]
true
> !!{}
true
> !!lskdjflkdsj
Uncaught ReferenceError: lskdjflkdsj is not defined
> !!'fsd'
true
> !!"dsfdsfds"
true
> !!1.123213
true
> !!-12312321.23432
true
```


# ~~

Doubling up the bitwise NOT/negation operator, '~', into '~~' gives us a fast way to round down a value to a whole number. So it is essentially a hack that gives us a floor function but without having to explicitly call Math.floor(). Internally ~ is taking its operand and converting it to a 32-bit intger before inverting it. The effect is to round the value towards zero (so not technically a floor function which would give us the greatest integer less than or equal to the operand which would as this rounds towards zero on negative values whereas Math.floor() continues to round down). Another thing to consider is that the range of values that ~~ and Math.floor() operate over is different which could lead to a logical error in your code further down the road.


```
> ~~1
1
> ~~0
0
> ~~-1
-1
> ~~1.342
1
> ~~-1.342
-1
> ~~23423
23423
> ~~23423.98238932
23423
> ~~"hello"
0
> ~~null
0
> ~~undefined
0
> ~~{}
0
> ~~[]
0
> ~~true
1
> ~~false
0

```

This is a performance hack more than anything else so is useful in those circumstances where you want to eke out every last bit of performance (although if we're at that point in our JS coding journey then perhaps leaping to we assembly is a more sensible step?).

That said, it could also provide a simpler way to get a 'floored' value for clean and streamlined code, albeit at the expense of code clarity.


# Summary

How should we think about these, and similar tricks, from a learning perspective though? Especially when learning a new language, or working on a codebase? Hacks like these can be useful and save on keystrokes, without a doubt, but how likely is it that someone else who subsequently works on your code will know the same tricks? If they don't then they'll have to look it up. This is where things get tricky, and part of the reason for writing this post. A web search for '!!' of '~~' isn't particularly edifying and none of the standard JS documentation sources included it in their indexes so it took a fair bit of google-fu to get there. So I'm going to file tricks like these into the special spice category, that is, excellent when used sparingly and appropriately.

