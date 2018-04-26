# Data Types

## Attributes
Attributes are used to store metadata about objects in R. Common attributes used by R are:
* names
* length
* dimensions
* dimension names
* class

### Names
The attributes `names` is a character vector that gives each element of an object a name. For example, an object can be named when creating a vector:
```r
> redskins <- c('reed' = 86, 'crowder' = 80, 'doctson' = 18)
> redskins
   reed crowder doctson 
     86      80      18 
```
They can also be defined after an object is created:
```r
> browns <- c(29, 80, 12)
> names(browns) <- c('johnson', 'landry', 'gordon')
> browns
johnson  landry  gordon 
     29      80      12
```
The `names` function can be used in retrieving the name of an object.
```r
> names(redskins)
[1] "reed"    "crowder" "doctson"
> names(browns)
[1] "johnson" "landry"  "gordon" 
```
Names do not need to be unique, but are powerful for subsetting, which will be discussed in a later lesson. By the same token, not all elements within an object needs to have a name. If an element does not have a name, the name will be set as an empty evalue, `NA`. 

### Length
The `length` of an object is the number of entries it contains. For example, an object containing only a single value will have a `length` of one.
```r
> player <- 'taylor'
> player
[1] "taylor"
> length(player)
[1] 1
```
An object (or vector) of six values will return a `length` of six.
```r
> players <- c('reed', 'crowder', 'perine', 'njoku', 'gordon', 'hyde')
> players
[1] "reed"    "crowder" "perine"  "njoku"   "gordon"  "hyde"

> length(players)
[1] 6
```

### Dimensions
In R, adding a `dim` attribute to a vector transforms it into a multi-dimensional array, such as a matrix, which has two dimensions. 
```r
> dim(players) <- c(3, 2)

> players
     [,1]      [,2]    
[1,] "reed"    "njoku" 
[2,] "crowder" "gordon"
[3,] "perine"  "hyde"  

> dim(players)
[1] 3 2
```
Alternatively, you can also use the `matrix` function to create an object with multiple dimensions, inputing a vector, a number of rows, and a number of columns.
```r
> players <- matrix(c('reed', 'crowder', 'perine', 'njoku', 'gordon', 'hyde'), nrow = 3, ncol = 2)

> players
     [,1]      [,2]    
[1,] "reed"    "njoku" 
[2,] "crowder" "gordon"
[3,] "perine"  "hyde" 

> dim(players)
[1] 3 2
```

### Dimension Names
As discussed in the previous section, *Dimensions*, some objects such as matrices and other arrays have multiple dimensions. Sometimes it is useful to give a name, or `dimnames`, to each dimension. In the example below, I add row and column names to the matrix, `player`. We can use `dimnames` to set and retrieve dimension names of arrays.
```r
> dimnames(players) <- list(c('te', 'wr', 'rb'), c('redskins', 'browns'))
> players
   redskins  browns  
te "reed"    "njoku" 
wr "crowder" "gordon"
rb "perine"  "hyde" 

> dimnames(players)
[[1]]
[1] "te" "wr" "rb"

[[2]]
[1] "redskins" "browns"  
```
For matrices, `rownames` and `colnames` yield the same result when naming dimensions.
```r
> rownames(players) <- c('te', 'wr', 'rb')
> colnames(players) <- c('redskins', 'browns')
> players
   redskins  browns  
te "reed"    "njoku" 
wr "crowder" "gordon"
rb "perine"  "hyde" 
```

### Class
In R, there are five basic or "atomic" classes of objects. 
* Character
* Numeric (real numbers)
* Integer
* Complex
* Logical

An object's `class` is a blueprint for an object in R. An object's class can be retrieved by the `class` function.
```r
> recYards <- 72
```
For example, if I want to find out the type of data used to represent reception yards, I would enter this:
```r
> class(recYards)
[1] "numeric"
```
There are several types of classes an object can become, each behaving differently and warrants having its own [lesson](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_data_types/lesson_03_classes.md).

## Summary
I hope this section gives you a deeper look into the inside components of objects in R. Any of the attribute functions (`names`, `dim`, `class`, etc.) can be used to retrieve its respective value from an object. In the next lesson, I dive into the specifics of classes of objects, and they can be coerced and manipulated.

Functions used:
* names
* dim
* matrix
* dimnames
* rownames
* colnames
* class
* length
* attr

Next lesson: [Classes](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_data_types/lesson_03_classes.md)

## References
John Hopkins University Data Science Specialization
http://adv-r.had.co.nz/
