## math — Mathematical Functions

This module contains mathematical operations. In order to use these functions, you should ```import math``` at the start of your file.

### Constants

* ```math.e``` : The mathematical constant e = 2.718281... to available precision.
* ```math.pi``` : The mathematical constant π = 3.141592... to available precision.

### Some Functions

* ```math.acos(x)``` : Returns the arccosine of *x* in radians.
* ```math.acosh(x)``` : Returns the inverse hyperbolic cosine of *x*.
* ```math.asin(x)``` : Returns the arcsine of *x* in radians.
* ```math.asinh(x)``` : Returns the inverse hyperbolic sine of *x*.
* ```math.atan(x)``` : Returns the arctangent of *x* in radians.
* ```math.atan2(y, x)``` : Returns *atan(y / x)* in radians. The result is between -pi and pi.
* ```math.atanh(x)``` : Returns the inverse hyperbolic tangent of *x*.
* ```math.ceil(x)``` : Returns the ceiling of *x* as a float, which is the smallest integer value greater than or equal to *x*.
* ```math.copysign(x, y)```: Returns *x* with the sign of *y*. On a platform that supports signed zeros, `copysign(1.0, -0.0)` returns -1.0.
* ```math.cos(x)``` : Returns the cosine of *x* radians.
* ```math.cosh(x)``` : Returns the hyperbolic cosine of *x*.
* ```math.degrees(x)``` : Converts angle *x* from radians to degrees.
* ```math.exp(x)``` : Returns *e\*\*`x`*.
* ```math.fabs(x)``` : Returns the absolute value of *x*.
* ```math.factorial(x)``` : Returns *x* factorial.
* ```math.floor(x)``` : Returns the floor of *x* as a float, the largest integer value less than or equal to `x`.
* ```math.hypot(x, y)``` : Returns the Euclidean norm, *sqrt(x\*x + y\*y)*. This is the length of the vector from the origin to point *(x, y)*.
* ```math.log(x[,base])``` : With one argument, the function returns the natural logarithm of *x* (to *base e*). With two arguments, it returns the logarithm of *x* to the given base, calculated as ***log(x)/log(base)***.
* ```math.log10(x)``` : Returns the base-10 logarithm of *x*. This is usually more accurate than *log(x, 10)*.
* ```math.pow(x, y)``` : Returns *x* raised to the power *y*.
* ```math.radians``` : Converts angle *x* from degrees to radians.
* ```math.sin(x)``` : Returns the sine of *x* radians.
* ```math.sinh(x)``` : Returns the hyperbolic sine of *x*.
* ```math.sqrt(x)``` : Returns the square root of *x*.
* ```math.tan(x)``` : Returns the tangent of *x* radians.
* ```math.tanh(x)``` : Returns the hyperbolic tangent of *x*.
* ```math.trunc(x)``` : Returns the ***real value*** *x* truncated to an ***integral***.


### Example

```python
import math

print(math.pi)
# 3.141592653589793

print(math.sqrt(4))
# 2.0

print(math.sin(math.pi/6))
# 0.49999999999999994

print(math.degrees(math.pi/6))
# 29.999999999999996
```

### Reference

* [Math Module](https://docs.python.org/3/library/math.html) at *docs.python.org*