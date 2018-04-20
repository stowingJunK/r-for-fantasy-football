# Data Types
This section provides the goundwork for solving any problems using R. Without an understanding of the various data types, one will have difficulty coding in R. This lesson gives a brief overview about objects in R.


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

## Summary
Functions used:
* class

Next lesson: [Classes](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_data_types/02_lesson_classes.md)

## References
http://www.r-tutor.com/
