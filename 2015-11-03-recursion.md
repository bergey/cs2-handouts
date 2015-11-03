Write a program in Haskell that uses recursion, and draws something.  

* Define and use at least 5 functions, including:
* At least one function that recurses on numbers (Number, Int, Float, or Double)
* At least one function that recurses on lists
* At least one function that has two or more arguments (2 or more arrows in the type signature)

Any program that satisfies the above is OK.  If you don't have a plan in mind, you can write the following:

Draw an animation that shows polygons of increasing number of sides.  For example, it shows a triangle for 1 second, then a square for 1 second, then a pentagon for one second, and on.  Break the program into functions as follows:

* `Number -> (Number, Number)` - The input is an angle.  The result is a point on the unit circle `angle` radians CCW from the +x axis
* `Number -> Number -> [Number]` -> The inputs are a starting value and a step size.  Return a list of numbers from the starting value to 2 * pi, increasing by the given step size.  *Use recursion.*
* `Int -> [Number]` - `Int` angles spaced evenly from 0 to 2 * pi.  Use the function you wrote above.
* `[Number] -> [(Number, Number)]` - use the function you wrote above to make a point for each angle in the list.  *Use recursion.*
* `Int -> Picture` - a polygon with the given number of sides.
* `Number -> Picture` - Use `floor` to convert the Number to an Int.  Use the function you wrote above to make a `Picture`.
