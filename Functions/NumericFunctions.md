## Numeric

### ABS
ABS( ) returns the absolute value of a number.
```
ABS(number)
```
### ACOS
ACOS( ) returns the arc cosine of a number, which must be between -1 and 1.
```
ACOS(number)
```
### ASIN
ASIN( ) returns the arc sine of a number, which must be between -1 and 1.
```
ASIN(number)
```
### ATAN
ATAN( ) returns the arc tangent of one or two numbers.
```
ATAN(number)

OR

ATAN(a, b)
```
### ATAN2
ATAN2( ) returns the arc tangent of two numbers.
```
ATAN2(a, b)
```
### AVG
AVG( ) returns the average value of an expression.
```
AVG(expression)
```
### CEIL
CEIL( ) returns the smallest integer value that is bigger than or equal to a number. This is the same as CEILING( ).
```
CEIL(number)
```
### CEILING
CEILING( ) returns the smallest integer value that is bigger than or equal to a number. This is the same as CEIL( ).
```
CEILING(number)
```
### COS
COS( ) returns the cosine of a number.
```
COS(number)
```
### COT
COT( ) returns the cotangent of a number.
```
COT(number)
```
## COUNT
COUNT( ) returns the number of records return by a select query.
```
SELECT COUNT(expression)
```
### DEGREES
DEGREES( ) converts a value in radians to degrees.
```
SELECT DEGREES(number)
```
### DIV
DIV( ) is used for integer division. An integer is returned.
```
SELECT x DIV y                              # x: A value that will be divided by y.
                                            # y: The divisor.
```
### EXP
EXP( ) returns e raised to the power of the specified number.
```
SELECT EXP(number)
```
### FLOOR
FLOOR( ) returns the largest integer value that is smaller than or equal to a number.
```
SELECT FLOOR(number)
```
### GREATEST
GREATEST( ) returns the greatest value of the list of arguments.
```
SELECT GREATEST(arg1, arg2, arg3, ...)
```
### LEAST
LEAST( ) returns the smallest value of the list of arguments.
```
SELECT LEAST(arg1, arg2, arg3, ...)
```
### LN
LN( ) returns the natural logarithm of a number.
```
SELECT LN(number)
```
### LOG
LOG( ) returns the natural logarithm of a specified number or the logarithm of the number to the specified base.
```
SELECT LOG(number)
```
### LOG10
LOG10( ) returns the natural logarithm of a number to base-10.
```
SELECT LOG10(number)
```
### LOG2
LOG2( ) returns the natural logarithm of a number to base-2.
```
SELECT LOG2(number)
```
### MAX
MAX( ) returns the maximum value in a set of values.
```
SELECT MAX(expression)
```
### MIN
MIN( ) returns the minimum value in a seat of values.
```
SELECT MIN(expression)
```
### MOD
MOD( ) or modulo returns the remainder of a number divided by another number.
```
SELECT MOD(x, y)

OR

x MOD y

OR

x % y
```
### PI
PI( ) returns the value of PI
```
SELECT PI( )
```
### POW
POW( ) returns the value of a number raised to the power of another number.
```
SELECT POW(x, y)                            # x: The base.
                                            # y: The exponent.
```
### POWER
POWER( ) returns the value of a number raised to the power of another number. This is the same as POW( ).
```
SELECT POWER(x, y)
```
### RADIANS
RADIANS( ) converts a degree value into radians.
```
SELECT RADIANS(number)
```
### RAND
RAND( ) returns a random number between 0 inclusive and 1 exclusive.
```
SELECT RAND( )
```
### ROUND
ROUND( ) rounds a number to a specified number of decimal places.
```
SELECT ROUND(number, decimals)              # number: The number to be rounded.
                                            # decimals: The number of decimal places to round number to. Optional.
```
### SIGN
SIGN( ) returns the sign of a number.
```
SELECT SIGN(number)                         # If number is positive, it returns 1.
                                            # If number is positive, it returns -1.
                                            # If number is 0, it returns 0.
```
### SIN
SIN( ) returns the sine of a number.
```
SELECT SIN(number)
```
### SQRT
SQRT( ) returns the square root of a number.
```
SELECT SQRT(number)
```
### SUM
SUM( ) calculates the sum of a set of values.
```
SELECT SUM(espression)
```
### TAN
TAN( ) returns the tangent of a number.
```
SELECT TAN(number)
```
### TRUNCATE
TRUNCATE( ) truncates a number to the specified number of decimal places.
```
SELECT TRUNCATE(number, decimals)           # number: The number to be truncated.
                                            # decimals: The number of decimal places to truncate to.
```
