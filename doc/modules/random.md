## random — Generate Pseudo-Random Numbers

This module implements functions of the `random` module. It contains pseudo-random number generators for various distributions. To use this module, make sure include `import random` first.

### Some Functions

* `random.choice(seq)` : Returns a random element from the non-empty sequence *seq*.
* `random.randint(a, b)` : Returns a random integer *N* such that *a <= N <= b*.
* `random.random` : Returns the next random floating point number in the range [0.0, 1.0).
* `random.randrange(stop)` : See below.
* `random.randrange(start, stop[, step])` : Returns a randomly selected element from *range(start, stop, step)*. This is equivalent to *choice(`range(start, stop, step)`)*.
* `random.sample(population, k)`: Returns a *k* length list of unique elements chosen from the *population* sequence.
* `random.seed(x)` : Initializes the random number generator.
* `random.shuffle(x)` : Shuffles the sequence *x* in place.
* `random.triangular(low, high, mode)`: Returns a random floating point number N such that ***low <= N <= high*** and with the specified mode.
* `random.uniform(a, b)`: Returns a random floating point number *N* such that *a <= N <= b* for a <= b and b <= N <= a for b < a.


### Example

```python
import random

lst = [1, 2, 3, 4, 5]

print(random.choice(lst))

print(random.randint(1, 10))

print(random.random())

random.shuffle(lst)
print(random.sample(lst, 2))
print(lst)

print(random.sample(range(100), 10))
```


### Reference

* [Random Module](https://docs.python.org/3/library/random.html) at *docs.python.org*