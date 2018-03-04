# Data Types
This section provides the goundwork for solving any problems using R. Without an understanding of the various data types, one will have difficulty coding in R.


## Objects
In R, there are five basic or "atomic" classes of objects. 
* Character
* Numeric (real numbers)
* Integer
* Complex
* Logical

An object's class can be retrieved by the `class` function.
```r
> recYards <- 72
```
For example, if I want to find out the type of data used to represent reception yards, I would enter this:
```r
> class(recYards)
[1] "numeric"
```

### Numeric
Numeric objects are used to represent decimal values in R. An example of a numeric object is `7` or `3`. This is also the default computational data type. In most cases, R defines an object's class as soon as you set the variable; variables set as numbers are automatically defined as *numeric*. You can use functions to explicitly define an object's class, otherwise known as explicit coercion. 
```r
> player <- 'foles'
> yards <- as.integer(373)
> mvp <- TRUE
> imaginary <- 5 + 5i

> as.numeric(player)
[1] NA
Warning message:
NAs introduced by coercion
```

### Integer
Integer objects must be 
```r
x <- as.integer(10.5)
```

### Complex


### Character
Character objects are used to represent string values in R. Examples of a character object is `brady` or `foles`. 


### Logical

## Attributes

## Summary
attributes
as.numeric
as.integer
as.complex
as.character
as.logical

## References
http://www.r-tutor.com/
