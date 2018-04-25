# Data Types

## Attributes
Attributes are used to store metadata about objects in R. Common attributes used by R are:
* names
* dimension names
* dimensions
* class
* length

### Names
The attributes `names` is a character vector that gives each element of an object a name. An object can be named when creating the vector:
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
The `names` function can be used to retrieve the name of an object.
```r
> names(redskins)
[1] "reed"    "crowder" "doctson"
> names(browns)
[1] "johnson" "landry"  "gordon" 
```
Names do not need to be unique, but are powerful for subsetting, which will be discussed in a later lesson. By the same token, not all elements within an object needs to have a name. If an element does not have a name, the name will be set as an empty evalue, `NA`. 

### Dimension Names
Some objects such as matrices and other arrays have multiple dimensions. Sometimes it is useful to give a name, or `dimnames`, to each dimension. 
```r
> players <- matrix(c('reed', 'crowder', 'perine', 'njoku', 'gordon', 'hyde'), nrow = 3, ncol = 2)
> players
     [,1]      [,2]    
[1,] "reed"    "njoku" 
[2,] "crowder" "gordon"
[3,] "perine"  "hyde"  
```
As you can tell in the matrix above, the row and columns are unlabeled. We can use `dimnames` to set and retrieve dimension names.
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

### Dimensions


### Class
In the previous [lesson](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_data_types/lesson_01_objects.md), I introduced classes, which is a blueprint of an object. There are several types of classes an object can become, each behaving differently, and it warrants having its own [lesson](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_data_types/lesson_03_classes.md). Reiterating the previous lesson, objects can be:
* Characters
* Real numbers
* Complex numbers
* Integers
* Logicals

You can retrieve an object's class by using the `class` function:
```r
> wins <- 10L
> class(wins)
[1] "integer"
```

### Length



## Summary
Functions used:
* names
* dimnames
* rownames
* colnames
* dim
* class
* length
* attr

Nexton lesson: [Classes](https://github.com/stowingJunK/r-for-fantasy-football/blob/master/ffball/01_data_types/lesson_03_classes.md)

## References
John Hopkins University Data Science Specialization
http://adv-r.had.co.nz/
