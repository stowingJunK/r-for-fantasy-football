# Data Types

## Vectors
Now that you know the different classes of objects in R and the many attributes they can hold, we can begin exploring more complex objects. A majority of the objects we created in the previous sections contained only single values, but there were also a few vectors and matrices. This section talks about vectors, a sequence of data elements of the same basic type. Each value within a vector is called a component.

### Creating Vectors
Vectors can be created with the function `c()`. For example:
```r
> yards <- c(15.1, 0.5)                    # Numeric
> yards
[1] 15.1  0.5

> wins <- c(TRUE, TRUE)                    # Logical
> wins
[1] TRUE TRUE

> teams <- c('cowboys', 'broncos')         # Character
> teams
[1] "cowboys" "broncos"

> record <- c(15L, 1L)                     # Integer
> record
[1] 15  1

> brownsRecord <- c(0, 0+16i)              # Complex
> brownsRecord
[1] 0+ 0i 0+16i
```
Alternatively, integer vectors can be created sequentially as shown below.
```r
> game <- 1:16
> game
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16
```
Vectors contain only a single class of values otherwise coercion occurs such as `brownsRecord`. Though the first value was inputed as a numeric, the vector coerces to a complex vector due to the second, complex, value. 

### Explicit Coercion
Similar to single-element objects, the `as.*` functions from the [Classes](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_data_types/lesson_03_classes.md) lessons can

## Summary
Functions used:
* c

## References
John Hopkins University Data Science Specialization

http://www.r-tutor.com/
