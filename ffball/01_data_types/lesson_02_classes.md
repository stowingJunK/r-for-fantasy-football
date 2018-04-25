# Data Types

## Classes
In this lesson, we discuss the different atomic classes of objects, and how to create or coerce them.

### Numeric
Numeric objects are used to represent decimal values in R. An example of a numeric object is `7` or `3`. This is also the default computational data type. In most cases, R defines an object's class as soon as you set the variable; variables set as numbers are automatically defined as *numeric*. You can use functions to explicitly define an object's class, otherwise known as explicit coercion. 
```r
> player <- 'foles'
> yards <- as.integer(373)
> mvp <- TRUE
> imaginary <- 5 + 3i

> as.numeric(player)
[1] NA
Warning message:
NAs introduced by coercion

> as.numeric(yards)
[1] 373

> as.numeric(mvp)
[1] 1

> as.numeric(imaginary)
[1] 5
Warning message:
imaginary parts discarded in coercion 
```
As you can tell, the `as.numeric` function reacts differently to different data types. When invoking the function on a character object, if the string contains anything other than numeric values, NA (Not Available) is returned. If the object only contains numeric values, it will return a numeric object. Similar to `as.numeric`, the other class functions will also react different to different data types.
```r
> folesNumber <- '9'
> as.numeric(folesNumber)
[1] 9
```
Integers convert easily to numerics. When converting logical objects into a numeric, `TRUE` becomes `1` and `FALSE` becomes `
0`. For complex objects, only the real part will be extracted.

`Inf` (or infinity) and `NaN` or (not a number) are also treated as a numeric objects.
```r
> class(Inf)
[1] "numeric"
> 1/0
[1] Inf
> 1/Inf
[1] 0

> class(NaN)
[1] "numeric"
> 0/0
[1] NaN
```

### Integer
Integer objects must be created using the `as.integer` function. If a variable is assigned an integer number without invoking `as.integer`, it automatically becomes a numeric object. For example: 
```r
> points <- 87.8
> class(points)
[1] "numeric"
```
If you want a variable to be an integer object, you must use the `as.integer` function.
```r
> points <- as.integer(points)
> class(points)
[1] "integer"
> points
[1] 87
```
As you can tell, if you invoke `as.integer` on a decimal number, its rounds down to the lower integer. Alternatively, if you want to explicitly want an integer, you can also use the `L` suffix.
```r
> points <- 80L
> class(points)
[1] "integer"
```

Similar to `as.numeric`, NA is returned if the function is applied to a character object. Logical objects, `TRUE` and `FALSE` also become `1` and `0`, respectively. When applied to a complex object, only the real part is extracted. 

### Complex
Complex objects contain an imaginary values , `i`. The easiest way to create a complex object is by using `i`.
```r
> brownsRings <- 0 + 8i
> brownsRings
[1] 0+8i
```
NA will be returned if you attempt to apply the `as.complex` function to a string. Using the function on logicals on integer and numeric values will return a complex number with the number added with an imaginary zero.
```r
> rec <- 5
> as.complex(rec)
[1] 5+0i
```
By the same token, 'TRUE' and 'FALSE' will return `1+0i` and `0+0i`, respectively.

The tricky part about working with complex objects, is that you cannot generate them implicitly from calculations. Otherwise, you generate NaNs.
```r
> lostyards <- -10
> sqrt(lostyards)
[1] NaN
Warning message:
In sqrt(lostyards) : NaNs produced
```
Instead, you must define them ahead of time if you know the result will be complex.
```r
> lostyards <- -10
> sqrt(as.complex(lostyards))
[1] 0+3.162278i
```

### Character
Character objects are used to represent string values in R. Examples of a character object is `brady` or `foles`. Objects can be converted to characters by invoking the `as.character` function. Almost all types of objects can be transformed into characters.
```r
> as.character(50)
[1] "50"

> as.character(TRUE)
[1] "TRUE"

> as.character(6+3i)
[1] "6+3i"

> as.character(NaN)
[1] "NaN"

> as.character(Inf)
[1] "Inf"

> as.character(NA)
[1] NA
```
As you can see, one of the few exceptions, NA (or missing value), cannot be converted into a string value.

Character objects can be concatenated using the `paste` function. For example:
```r
> firstName <- 'Tom'
> lastName <- 'Brady'
> paste(firstName, lastName)
[1] "Tom Brady"
```
### Logical
The only logical values are `TRUE`, `FALSE`, and `NA`. `NA` (or not applicable) is an empty value and is considered a logical object itself.
```r
> class(NA)
[1] "logical"
```
The last atomic object class are logical objects. When invoking the `as.logical` function, all non-zeroes return `TRUE`. This includes complex numbers that only have imaginary parts. Zeroes return `FALSE`. 
```r
> as.logical(10.5)
[1] TRUE
> as.logical(-5)
[1] TRUE
> as.logical(0)
[1] FALSE
> as.logical(0+0i)
[1] FALSE
> as.logical(5+0i)
[1] TRUE
> as.logical(0+5i)
[1] TRUE
```
While numbers return `TRUE` and `FALSE`, strings always return `NA`.
```r
> as.logical('patriots')
[1] NA
```
Standard logical operators are `&` (and), `|` (or), and `!` (negation). 
```r
> foles <- TRUE
> brady <- FALSE

> foles & brady
[1] FALSE

> foles | brady
[1] TRUE

> !foles
[1] FALSE
```

## Summary
Functions used:

* as.numeric

* class

* as.integer

* as.complex

* sqrt

* as.character

* paste

* as.logical


## References
http://www.r-tutor.com/
