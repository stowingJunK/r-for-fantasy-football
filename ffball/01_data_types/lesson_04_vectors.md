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
Similar to single-element objects, the `as.*` functions from the [Classes](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_data_types/lesson_03_classes.md) lessons can be used to coerce an object to another class. Just like other objects, non-sensical coercion will result in `NA`s. 
```r
> as.numeric(teams)
[1] NA NA
```

### Lists
A different type of vector that allows elements of different classes are lists. Lists are created using the `list` function.
```r
> exampleList <- list(49L, 'San Francisco', 10.5)
> exampleList
[[1]]
[1] 49

[[2]]
[1] "San Francisco"

[[3]]
[1] 10.5
```

## Summary
Vectors are a useful form of storing data and are much more better suited for representing a set of similar data. This is especially useful if you have many data values, and you don't want to store each value as a seperate variable. In the next leson, I discuss objects with more than one dimension, arrays or more commonly known as matrices.

Functions used:
* c
* list

Next lesson: [Matrices](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_data_types/lesson_05_matrices.md)

## References
John Hopkins University Data Science Specialization

http://www.r-tutor.com/
