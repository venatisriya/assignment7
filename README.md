# Assignment7
## Sriya Reddy 

For this assignment, I used the datasets in R - the mtcars dataset. 
I loaded the data into the variable `cars` using the `> cars <- mtcars` function.
Displaying the data - 

```
> cars
                     mpg cyl  disp  hp drat    wt  qsec vs am gear carb
Mazda RX4           21.0   6 160.0 110 3.90 2.620 16.46  0  1    4    4
Mazda RX4 Wag       21.0   6 160.0 110 3.90 2.875 17.02  0  1    4    4
Datsun 710          22.8   4 108.0  93 3.85 2.320 18.61  1  1    4    1
Hornet 4 Drive      21.4   6 258.0 110 3.08 3.215 19.44  1  0    3    1
Hornet Sportabout   18.7   8 360.0 175 3.15 3.440 17.02  0  0    3    2
Valiant             18.1   6 225.0 105 2.76 3.460 20.22  1  0    3    1
Duster 360          14.3   8 360.0 245 3.21 3.570 15.84  0  0    3    4
Merc 240D           24.4   4 146.7  62 3.69 3.190 20.00  1  0    4    2
Merc 230            22.8   4 140.8  95 3.92 3.150 22.90  1  0    4    2
Merc 280            19.2   6 167.6 123 3.92 3.440 18.30  1  0    4    4
Merc 280C           17.8   6 167.6 123 3.92 3.440 18.90  1  0    4    4
Merc 450SE          16.4   8 275.8 180 3.07 4.070 17.40  0  0    3    3
Merc 450SL          17.3   8 275.8 180 3.07 3.730 17.60  0  0    3    3
Merc 450SLC         15.2   8 275.8 180 3.07 3.780 18.00  0  0    3    3
Cadillac Fleetwood  10.4   8 472.0 205 2.93 5.250 17.98  0  0    3    4
Lincoln Continental 10.4   8 460.0 215 3.00 5.424 17.82  0  0    3    4
Chrysler Imperial   14.7   8 440.0 230 3.23 5.345 17.42  0  0    3    4
Fiat 128            32.4   4  78.7  66 4.08 2.200 19.47  1  1    4    1
Honda Civic         30.4   4  75.7  52 4.93 1.615 18.52  1  1    4    2
Toyota Corolla      33.9   4  71.1  65 4.22 1.835 19.90  1  1    4    1
Toyota Corona       21.5   4 120.1  97 3.70 2.465 20.01  1  0    3    1
Dodge Challenger    15.5   8 318.0 150 2.76 3.520 16.87  0  0    3    2
AMC Javelin         15.2   8 304.0 150 3.15 3.435 17.30  0  0    3    2
Camaro Z28          13.3   8 350.0 245 3.73 3.840 15.41  0  0    3    4
Pontiac Firebird    19.2   8 400.0 175 3.08 3.845 17.05  0  0    3    2
Fiat X1-9           27.3   4  79.0  66 4.08 1.935 18.90  1  1    4    1
Porsche 914-2       26.0   4 120.3  91 4.43 2.140 16.70  0  1    5    2
Lotus Europa        30.4   4  95.1 113 3.77 1.513 16.90  1  1    5    2
Ford Pantera L      15.8   8 351.0 264 4.22 3.170 14.50  0  1    5    4
Ferrari Dino        19.7   6 145.0 175 3.62 2.770 15.50  0  1    5    6
Maserati Bora       15.0   8 301.0 335 3.54 3.570 14.60  0  1    5    8
Volvo 142E          21.4   4 121.0 109 4.11 2.780 18.60  1  1    4    2
```

Now, I tried out some generic functions on this dataset as shown below. 
```
> isS4(cars)
[1] FALSE
```
The function `isS4` returns `FALSE` as the dataset is S3. Therefore only S3 can be assigned to the mtcars dataset.
```
> head(cars)
                   mpg cyl disp  hp drat    wt  qsec vs am gear carb
Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1
```
The function `head` provides the first 6 rows of the dataset and hence it works for the dataset.

The function `> plot(cars)` provides the following plot and hence this function works for the dataset. 

![](https://github.com/venatisriya/assignment7/blob/main/Rplot2_assgn6.png)

The function `summary` is interesting. It provides the min, max, quartiles, median and mean for each column in the dataset. Below is the result. 

```
> summary(cars)
      mpg             cyl             disp             hp             drat      
 Min.   :10.40   Min.   :4.000   Min.   : 71.1   Min.   : 52.0   Min.   :2.760  
 1st Qu.:15.43   1st Qu.:4.000   1st Qu.:120.8   1st Qu.: 96.5   1st Qu.:3.080  
 Median :19.20   Median :6.000   Median :196.3   Median :123.0   Median :3.695  
 Mean   :20.09   Mean   :6.188   Mean   :230.7   Mean   :146.7   Mean   :3.597  
 3rd Qu.:22.80   3rd Qu.:8.000   3rd Qu.:326.0   3rd Qu.:180.0   3rd Qu.:3.920  
 Max.   :33.90   Max.   :8.000   Max.   :472.0   Max.   :335.0   Max.   :4.930  
       wt             qsec             vs               am        
 Min.   :1.513   Min.   :14.50   Min.   :0.0000   Min.   :0.0000  
 1st Qu.:2.581   1st Qu.:16.89   1st Qu.:0.0000   1st Qu.:0.0000  
 Median :3.325   Median :17.71   Median :0.0000   Median :0.0000  
 Mean   :3.217   Mean   :17.85   Mean   :0.4375   Mean   :0.4062  
 3rd Qu.:3.610   3rd Qu.:18.90   3rd Qu.:1.0000   3rd Qu.:1.0000  
 Max.   :5.424   Max.   :22.90   Max.   :1.0000   Max.   :1.0000  
      gear            carb      
 Min.   :3.000   Min.   :1.000  
 1st Qu.:3.000   1st Qu.:2.000  
 Median :4.000   Median :2.000  
 Mean   :3.688   Mean   :2.812  
 3rd Qu.:4.000   3rd Qu.:4.000  
 Max.   :5.000   Max.   :8.000 
```

The function `class` provides the class of the dataset which is a `data.frame`.
```
> class(cars)
[1] "data.frame"
```

**Questions**

1) We can tell whether the object is S3 or S4, by using the `isS4` function. This function returns TRUE if the object is S4 and FALSE if the object is S3. 

2) We can determine the base type of an object by using the `class` function. Additionaly, the `str` function provides the datatype of every variable in the object.

3) A generic function is a function that can be applied to any type of input and produces an oiutput specific to that type of input. Examples are `print` and `plot` functions. 

4) S3 and S4 are two generations of object oriented programming in R. S3 is simpler in implementation, but is less general. It is more formal and it is difficult to manipulate. S4 is more open to manipulation but requires more effort in coding it. 

5) I created two examples of S3 and S4 as instructed. 

S3 creation:

```
> s <- list(name= "Myself", age = 29, GPA = 3.5)
> s
$name
[1] "Myself"

$age
[1] 29

$GPA
[1] 3.5
```

S4 creation:
We need to first set the class with the `setClass` function. We then use the `new` function to create the S4 object.

```
> setClass("student", representation(name = "character", age = "numeric", GPA = "numeric"))
> s4 <- new("student", name = "Myself", age = 29, GPA = 3.5)
> s4
An object of class "student"
Slot "name":
[1] "Myself"

Slot "age":
[1] 29

Slot "GPA":
[1] 3.5
```

I now created a generic function using the `setGeneric` function. Using the `UseMethod` function, I assigned methods to it as shown (default and student). These methods extract the grade of the student. 

```
setGeneric("grade")
> grade <- function(x) {
+     UseMethod("grade")
+ }

> grade.default <- function(x) {
+     cat("This is a generic function\n")
+ }

> grade.student <- function(x) {
+     cat("Your grade is", x$GPA, "\n")
+ }

> grade(s)
This is a generic function
> grade.student(s)
Your grade is 3.5 
```

Additionally, to explore more, I also created a generic function `car_func` for the mtcars dataset. 

```
> setGeneric("car_func")
[1] "car_func"
```

I created methods for this function as shown below. 

```
> car_func <- function(x, ...)
+ UseMethod("car_func")
> car_func.cyl <- function(x) mean(x$cyl)
> car_func.hp <- function(x) mean(x$hp)
> car_func.maxmpg <- function(x) max(x$mpg)
> car_func.carb_hist <- function(x) hist(x$carb)
```

These methods are designed to extract the mean number of cylinders, the mean hp, the max mpg and plot the histogram of the carb. 
Implementing these, we get the results below. 

```
> car_func.cyl(cars)
[1] 6.1875
> car_func.hp(cars)
[1] 146.6875
> car_func.maxmpg(cars)
[1] 33.9
> car_func.carb_hist(cars)
```

The histogram is shown below. 

![](https://github.com/venatisriya/assignment7/blob/main/Rplot_hist_assg6.png)

This assignment allowed me to explore the creation of generic functions and methods in R and was interesting and challenging. 





