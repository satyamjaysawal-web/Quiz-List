


Here’s a comprehensive list of commonly used NumPy functions and keywords, organized in a table format. This includes functions for array creation, manipulation, mathematical operations, statistical analysis, and more.

| **Category**               | **Function/Keyword**        | **Description**                                           |
|----------------------------|-----------------------------|-----------------------------------------------------------|
| **Array Creation**         | `array()`                   | Create an array.                                         |
|                            | `arange()`                  | Create an array with evenly spaced values.               |
|                            | `linspace()`                | Create an array of evenly spaced values over a range.    |
|                            | `zeros()`                   | Create an array filled with zeros.                        |
|                            | `ones()`                    | Create an array filled with ones.                         |
|                            | `empty()`                   | Create an empty array (values are uninitialized).        |
|                            | `full()`                    | Create an array filled with a specified value.           |
|                            | `eye()`                     | Create a 2D identity matrix.                              |
|                            | `identity()`                | Create a 2D identity matrix (similar to `eye()`).       |
|                            | `fromfunction()`            | Create an array by executing a function over grid indices. |
|                            | `fromiter()`                | Create an array from an iterable.                        |
| **Array Manipulation**     | `reshape()`                 | Reshape an array without changing its data.              |
|                            | `ravel()`                   | Flatten a multi-dimensional array.                        |
|                            | `transpose()`               | Permute the dimensions of an array.                       |
|                            | `swapaxes()`               | Interchange two axes of an array.                        |
|                            | `concatenate()`             | Join two or more arrays along an existing axis.         |
|                            | `stack()`                   | Join a sequence of arrays along a new axis.             |
|                            | `hstack()`                  | Stack arrays in sequence horizontally.                   |
|                            | `vstack()`                  | Stack arrays in sequence vertically.                     |
|                            | `split()`                   | Split an array into multiple sub-arrays.                |
|                            | `hsplit()`                  | Split an array into multiple sub-arrays horizontally.    |
|                            | `vsplit()`                  | Split an array into multiple sub-arrays vertically.      |
| **Mathematical Functions** | `add()`                     | Add arrays element-wise.                                 |
|                            | `subtract()`                | Subtract arrays element-wise.                            |
|                            | `multiply()`                | Multiply arrays element-wise.                            |
|                            | `divide()`                  | Divide arrays element-wise.                              |
|                            | `power()`                   | Raise elements in an array to a specified power.        |
|                            | `sqrt()`                    | Compute the square root of an array.                    |
|                            | `sin()`, `cos()`, `tan()`   | Compute trigonometric functions.                         |
|                            | `log()`                     | Compute the natural logarithm.                           |
|                            | `exp()`                     | Compute the exponential of all elements in the array.   |
| **Statistical Functions**  | `mean()`                    | Compute the arithmetic mean.                             |
|                            | `median()`                  | Compute the median.                                     |
|                            | `std()`                     | Compute the standard deviation.                          |
|                            | `var()`                     | Compute the variance.                                   |
|                            | `min()`                     | Return the minimum value.                               |
|                            | `max()`                     | Return the maximum value.                               |
|                            | `sum()`                     | Sum of array elements.                                  |
|                            | `prod()`                    | Product of array elements.                              |
|                            | `cumsum()`                  | Cumulative sum of array elements.                       |
|                            | `cumprod()`                 | Cumulative product of array elements.                   |
| **Logical Functions**      | `any()`                     | Test whether any array element is true.                 |
|                            | `all()`                     | Test whether all array elements are true.               |
|                            | `where()`                   | Return elements chosen from two arrays based on a condition. |
|                            | `logical_and()`             | Compute the element-wise logical AND.                   |
|                            | `logical_or()`              | Compute the element-wise logical OR.                    |
|                            | `logical_not()`             | Compute the element-wise logical NOT.                   |
| **Linear Algebra**         | `dot()`                     | Dot product of two arrays.                               |
|                            | `matmul()`                  | Matrix product of two arrays.                            |
|                            | `inv()`                     | Compute the (multiplicative) inverse of a matrix.       |
|                            | `pinv()`                    | Compute the (Moore-Penrose) pseudo-inverse of a matrix.|
|                            | `det()`                     | Compute the determinant of an array.                    |
|                            | `eig()`                     | Compute eigenvalues and right eigenvectors of an array. |
| **File I/O**               | `loadtxt()`                 | Load data from a text file.                             |
|                            | `savetxt()`                 | Save an array to a text file.                           |
|                            | `save()`                    | Save an array to a binary file.                         |
|                            | `load()`                    | Load an array from a binary file.                       |
| **Random Sampling**        | `random.rand()`             | Generate random numbers uniformly distributed over [0, 1). |
|                            | `random.randn()`            | Generate samples from the standard normal distribution. |
|                            | `random.randint()`          | Generate random integers between specified limits.      |
|                            | `random.choice()`           | Randomly select elements from an array.                 |
|                            | `random.seed()`             | Seed the random number generator for reproducibility.   |
| **Miscellaneous**          | `copy()`                    | Return a copy of the array.                             |
|                            | `astype()`                  | Cast an array to a specified type.                      |
|                            | `flatten()`                 | Return a copy of the array collapsed into one dimension.|
|                            | `clip()`                    | Limit the values in an array.                           |
|                            | `unique()`                  | Find the unique elements of an array.                   |
|                            | `argsort()`                 | Returns the indices that would sort an array.          |
|                            | `sort()`                    | Sort an array.                                         |
|                            | `setdiff1d()`              | Find the set difference of two arrays.                  |
|                            | `intersect1d()`            | Find the intersection of two arrays.                     |

### Summary
This table provides a broad overview of key NumPy functions and keywords. NumPy is an essential library for numerical computing in Python, offering a wide range of tools for array manipulation, mathematical calculations, and data analysis. Mastering these functions will greatly enhance your ability to work with data in Python.


---
---
Here’s a list of important NumPy functions with code examples and outputs:

### 1. `np.array()`
Creates an array from a list.

```python
import numpy as np
arr = np.array([1, 2, 3, 4])
print(arr)
# Output: [1 2 3 4]
```

### 2. `np.arange()`
Creates an array of evenly spaced values.

```python
arr = np.arange(0, 10, 2)
print(arr)
# Output: [0 2 4 6 8]
```

### 3. `np.linspace()`
Creates an array of `n` evenly spaced values.

```python
arr = np.linspace(0, 1, 5)
print(arr)
# Output: [0.   0.25 0.5  0.75 1.  ]
```

### 4. `np.zeros()`
Creates an array filled with zeros.

```python
arr = np.zeros((2, 3))
print(arr)
# Output:
# [[0. 0. 0.]
#  [0. 0. 0.]]
```

### 5. `np.ones()`
Creates an array filled with ones.

```python
arr = np.ones((3, 2))
print(arr)
# Output:
# [[1. 1.]
#  [1. 1.]
#  [1. 1.]]
```

### 6. `np.eye()`
Creates an identity matrix.

```python
arr = np.eye(3)
print(arr)
# Output:
# [[1. 0. 0.]
#  [0. 1. 0.]
#  [0. 0. 1.]]
```

### 7. `np.reshape()`
Reshapes an array without changing its data.

```python
arr = np.arange(6).reshape((2, 3))
print(arr)
# Output:
# [[0 1 2]
#  [3 4 5]]
```

### 8. `np.concatenate()`
Joins arrays along an axis.

```python
arr1 = np.array([1, 2])
arr2 = np.array([3, 4])
result = np.concatenate((arr1, arr2))
print(result)
# Output: [1 2 3 4]
```

### 9. `np.add()`
Adds two arrays element-wise.

```python
arr1 = np.array([1, 2])
arr2 = np.array([3, 4])
result = np.add(arr1, arr2)
print(result)
# Output: [4 6]
```

### 10. `np.dot()`
Computes the dot product of two arrays.

```python
arr1 = np.array([[1, 2], [3, 4]])
arr2 = np.array([[5, 6], [7, 8]])
result = np.dot(arr1, arr2)
print(result)
# Output:
# [[19 22]
#  [43 50]]
```

### 11. `np.sum()`
Computes the sum of elements in an array.

```python
arr = np.array([1, 2, 3])
print(np.sum(arr))
# Output: 6
```

### 12. `np.mean()`
Computes the mean of elements in an array.

```python
arr = np.array([1, 2, 3])
print(np.mean(arr))
# Output: 2.0
```

### 13. `np.std()`
Computes the standard deviation.

```python
arr = np.array([1, 2, 3])
print(np.std(arr))
# Output: 0.816496580927726
```

### 14. `np.min()` and `np.max()`
Finds the minimum and maximum values.

```python
arr = np.array([1, 2, 3])
print(np.min(arr))  # Output: 1
print(np.max(arr))  # Output: 3
```

### 15. `np.random.rand()`
Generates random numbers in [0, 1).

```python
arr = np.random.rand(2, 2)
print(arr)
# Output: Random 2x2 matrix with values between 0 and 1
```

### 16. `np.unique()`
Finds the unique elements of an array.

```python
arr = np.array([1, 2, 2, 3])
print(np.unique(arr))
# Output: [1 2 3]
```

### 17. `np.sort()`
Sorts an array.

```python
arr = np.array([3, 1, 2])
print(np.sort(arr))
# Output: [1 2 3]
```

These codes cover the most commonly used NumPy functions along with their outputs.



---
---
Certainly! Here are more essential NumPy functions and operations along with code examples and their corresponding outputs:

### 18. `np.transpose()`
Transposes the dimensions of an array.

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])
transposed = np.transpose(arr)
print(transposed)
# Output:
# [[1 4]
#  [2 5]
#  [3 6]]
```

### 19. `np.flatten()`
Flattens a multi-dimensional array into a one-dimensional array.

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])
flattened = arr.flatten()
print(flattened)
# Output: [1 2 3 4 5 6]
```

### 20. `np.clip()`
Limits the values in an array.

```python
arr = np.array([-1, 0, 1, 2, 3])
clipped = np.clip(arr, 0, 2)
print(clipped)
# Output: [0 0 1 2 2]
```

### 21. `np.cumsum()`
Computes the cumulative sum of the elements along a specified axis.

```python
arr = np.array([1, 2, 3])
cumulative_sum = np.cumsum(arr)
print(cumulative_sum)
# Output: [1 3 6]
```

### 22. `np.cumprod()`
Computes the cumulative product of the elements along a specified axis.

```python
arr = np.array([1, 2, 3])
cumulative_product = np.cumprod(arr)
print(cumulative_product)
# Output: [1 2 6]
```

### 23. `np.random.randint()`
Generates random integers between specified limits.

```python
rand_ints = np.random.randint(0, 10, size=(2, 3))
print(rand_ints)
# Output: Random 2x3 matrix of integers between 0 and 10
```

### 24. `np.where()`
Returns elements chosen from two arrays based on a condition.

```python
arr = np.array([1, 2, 3, 4, 5])
result = np.where(arr % 2 == 0, arr, -1)
print(result)
# Output: [-1  2 -1  4 -1]
```

### 25. `np.split()`
Splits an array into multiple sub-arrays.

```python
arr = np.array([1, 2, 3, 4, 5, 6])
sub_arrays = np.split(arr, 3)
print(sub_arrays)
# Output: [array([1, 2]), array([3, 4]), array([5, 6])]
```

### 26. `np.hstack()`
Stacks arrays in sequence horizontally.

```python
arr1 = np.array([1, 2])
arr2 = np.array([3, 4])
hstacked = np.hstack((arr1, arr2))
print(hstacked)
# Output: [1 2 3 4]
```

### 27. `np.vstack()`
Stacks arrays in sequence vertically.

```python
arr1 = np.array([[1], [2]])
arr2 = np.array([[3], [4]])
vstacked = np.vstack((arr1, arr2))
print(vstacked)
# Output:
# [[1]
#  [2]
#  [3]
#  [4]]
```

### 28. `np.inner()`
Computes the inner product of two arrays.

```python
arr1 = np.array([1, 2])
arr2 = np.array([3, 4])
inner_product = np.inner(arr1, arr2)
print(inner_product)
# Output: 11 (1*3 + 2*4)
```

### 29. `np.outer()`
Computes the outer product of two arrays.

```python
arr1 = np.array([1, 2])
arr2 = np.array([3, 4])
outer_product = np.outer(arr1, arr2)
print(outer_product)
# Output:
# [[3 4]
#  [6 8]]
```

### 30. `np.isin()`
Tests whether each element of an array is present in another array.

```python
arr = np.array([1, 2, 3, 4])
test_values = np.array([2, 4])
isin_result = np.isin(arr, test_values)
print(isin_result)
# Output: [False  True False  True]
```

### 31. `np.argsort()`
Returns the indices that would sort an array.

```python
arr = np.array([3, 1, 2])
sorted_indices = np.argsort(arr)
print(sorted_indices)
# Output: [1 2 0]
```

### 32. `np.unique()`
Finds the unique elements of an array and returns them in sorted order.

```python
arr = np.array([1, 2, 2, 3])
unique_elements = np.unique(arr)
print(unique_elements)
# Output: [1 2 3]
```

### 33. `np.isnan()`
Tests element-wise for NaN and returns a boolean array.

```python
arr = np.array([1, 2, np.nan])
nan_check = np.isnan(arr)
print(nan_check)
# Output: [False False  True]
```

### 34. `np.nanmean()`
Computes the mean of an array while ignoring NaN values.

```python
arr = np.array([1, 2, np.nan])
mean_value = np.nanmean(arr)
print(mean_value)
# Output: 1.5
```

### 35. `np.nanstd()`
Computes the standard deviation of an array while ignoring NaN values.

```python
arr = np.array([1, 2, np.nan])
std_value = np.nanstd(arr)
print(std_value)
# Output: 0.7071067811865476
```

### 36. `np.random.seed()`
Sets the seed for the random number generator for reproducibility.

```python
np.random.seed(42)
rand_numbers = np.random.rand(3)
print(rand_numbers)
# Output: [0.37454012 0.95071431 0.73199394]
```

### 37. `np.save()`
Saves an array to a binary file.

```python
arr = np.array([1, 2, 3])
np.save('my_array.npy', arr)
# No output, but 'my_array.npy' file is created.
```

### 38. `np.load()`
Loads an array from a binary file.

```python
loaded_arr = np.load('my_array.npy')
print(loaded_arr)
# Output: [1 2 3]
```

### 39. `np.savez()`
Saves multiple arrays into a single `.npz` file.

```python
np.savez('arrays.npz', a=arr, b=arr*2)
# No output, but 'arrays.npz' file is created.
```

### 40. `np.load()` for `.npz` files
Loads arrays from a `.npz` file.

```python
loaded_arrays = np.load('arrays.npz')
print(loaded_arrays['a'])  # Accessing the 'a' array
# Output: [1 2 3]
```

### Summary
This list of NumPy functions covers a wide range of functionalities, including array creation, manipulation, mathematical operations, statistics, and random number generation. Understanding these functions is crucial for effective data manipulation and analysis in Python using NumPy. Feel free to reach out if you have more specific questions or need further explanations!


---
---

Certainly! Here are more important NumPy functions and operations with code examples and their corresponding outputs:

### 41. `np.repeat()`
Repeats elements of an array.

```python
arr = np.array([1, 2, 3])
repeated = np.repeat(arr, 2)
print(repeated)
# Output: [1 1 2 2 3 3]
```

### 42. `np.tile()`
Constructs an array by repeating the input array.

```python
arr = np.array([1, 2, 3])
tiled = np.tile(arr, 2)
print(tiled)
# Output: [1 2 3 1 2 3]
```

### 43. `np.expand_dims()`
Expands the shape of an array by adding a new axis.

```python
arr = np.array([1, 2, 3])
expanded = np.expand_dims(arr, axis=0)
print(expanded)
# Output: [[1 2 3]]
```

### 44. `np.squeeze()`
Removes single-dimensional entries from the shape of an array.

```python
arr = np.array([[1], [2], [3]])
squeezed = np.squeeze(arr)
print(squeezed)
# Output: [1 2 3]
```

### 45. `np.meshgrid()`
Generates coordinate matrices from coordinate vectors.

```python
x = np.array([1, 2, 3])
y = np.array([4, 5])
xx, yy = np.meshgrid(x, y)
print(xx)
# Output:
# [[1 2 3]
#  [1 2 3]]
print(yy)
# Output:
# [[4 4 4]
#  [5 5 5]]
```

### 46. `np.random.shuffle()`
Shuffles the contents of an array in place.

```python
arr = np.array([1, 2, 3, 4, 5])
np.random.shuffle(arr)
print(arr)
# Output: Randomly shuffled array, e.g., [3 1 5 2 4]
```

### 47. `np.linalg.inv()`
Computes the inverse of a matrix.

```python
matrix = np.array([[1, 2], [3, 4]])
inverse = np.linalg.inv(matrix)
print(inverse)
# Output:
# [[-2.   1. ]
#  [ 1.5 -0.5]]
```

### 48. `np.linalg.det()`
Computes the determinant of a matrix.

```python
matrix = np.array([[1, 2], [3, 4]])
determinant = np.linalg.det(matrix)
print(determinant)
# Output: -2.0000000000000004
```

### 49. `np.linalg.eig()`
Computes the eigenvalues and right eigenvectors of a square array.

```python
matrix = np.array([[1, 2], [2, 1]])
eigenvalues, eigenvectors = np.linalg.eig(matrix)
print("Eigenvalues:", eigenvalues)
# Output: Eigenvalues: [3.  -1.]
print("Eigenvectors:\n", eigenvectors)
# Output: 
# Eigenvectors:
#  [[ 0.70710678 -0.70710678]
#   [ 0.70710678  0.70710678]]
```

### 50. `np.random.choice()`
Generates a random sample from a given 1-D array.

```python
arr = np.array([1, 2, 3, 4, 5])
random_sample = np.random.choice(arr, size=3)
print(random_sample)
# Output: Random selection of 3 elements from arr
```

### 51. `np.histogram()`
Computes the histogram of a set of data.

```python
data = np.array([1, 2, 1, 3, 3, 3, 4, 4, 5])
hist, bin_edges = np.histogram(data, bins=5)
print(hist)
# Output: [2 2 3 2 1] (Counts for each bin)
print(bin_edges)
# Output: [1.  2.  3.  4.  5.  6.] (Bin edges)
```

### 52. `np.corrcoef()`
Computes the correlation coefficients of the input data.

```python
data1 = np.array([1, 2, 3])
data2 = np.array([4, 5, 6])
correlation = np.corrcoef(data1, data2)
print(correlation)
# Output:
# [[1. 1.]
#  [1. 1.]]
```

### 53. `np.cov()`
Computes the covariance matrix.

```python
data = np.array([[1, 2, 3], [4, 5, 6]])
covariance = np.cov(data)
print(covariance)
# Output:
# [[ 1.  1.]
#  [ 1.  1.]]
```

### 54. `np.angle()`
Returns the angle (or phase) of a complex number.

```python
complex_arr = np.array([1+2j, 3+4j])
angles = np.angle(complex_arr)
print(angles)
# Output: [1.10714872 0.92729522]
```

### 55. `np.real()`
Returns the real part of a complex number.

```python
complex_arr = np.array([1+2j, 3+4j])
real_part = np.real(complex_arr)
print(real_part)
# Output: [1. 3.]
```

### 56. `np.imag()`
Returns the imaginary part of a complex number.

```python
complex_arr = np.array([1+2j, 3+4j])
imaginary_part = np.imag(complex_arr)
print(imaginary_part)
# Output: [2. 4.]
```

### 57. `np.fft.fft()`
Computes the one-dimensional discrete Fourier Transform.

```python
arr = np.array([0, 1, 2, 3])
fft_result = np.fft.fft(arr)
print(fft_result)
# Output: [ 6.+0.j -2.+2.j -2.+0.j -2.-2.j]
```

### 58. `np.fft.ifft()`
Computes the one-dimensional inverse discrete Fourier Transform.

```python
arr = np.array([6, -2+2j, -2, -2-2j])
ifft_result = np.fft.ifft(arr)
print(ifft_result)
# Output: [0.+0.j 1.+0.j 2.+0.j 3.+0.j]
```

### 59. `np.median()`
Computes the median of an array.

```python
arr = np.array([1, 2, 3, 4, 5])
median_value = np.median(arr)
print(median_value)
# Output: 3.0
```

### 60. `np.nanstd()`
Computes the standard deviation of an array, ignoring NaNs.

```python
arr = np.array([1, 2, np.nan])
nan_std_value = np.nanstd(arr)
print(nan_std_value)
# Output: 0.7071067811865476
```

### 61. `np.ravel_multi_index()`
Converts a pair of arrays into a single array of indices.

```python
arr1 = np.array([0, 1, 2])
arr2 = np.array([0, 1, 2])
indices = np.ravel_multi_index((arr1, arr2), (3, 3))
print(indices)
# Output: [0 4 8]
```

### 62. `np.unravel_index()`
Converts a flat index into a coordinate in a multi-dimensional array.

```python
index = 5
shape = (3, 3)
unraveled = np.unravel_index(index, shape)
print(unraveled)
# Output: (1, 2)
```

### 63. `np.count_nonzero()`
Counts the number of non-zero elements in an array.

```python
arr = np.array([1, 0, 2, 0, 3])
non_zero_count = np.count_nonzero(arr)
print(non_zero_count)
# Output: 3
```

### 64. `np.array_equal()`
Checks whether two arrays are equal.

```python
arr1 = np.array([1, 2, 3])
arr2 = np.array([1, 2, 3])
equal = np.array_equal(arr1, arr2)
print(equal)
# Output: True
```

### 65. `np.zeros_like()`
Creates an array of zeros with the same shape and type as a given array.

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])
zeros_like = np.zeros_like(arr)
print(zeros_like)
# Output:
# [[0 0 0]
#  [0 0 0]]
```

### 66. `np.ones_like()`
Creates an array of ones with the same shape and type as a given array.

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])
ones_like = np.ones_like(arr)
print(ones

_like)
# Output:
# [[1 1 1]
#  [1 1 1]]
```

### 67. `np.empty()`
Creates a new array of given shape and type, without initializing entries.

```python
empty_arr = np.empty((2, 2))
print(empty_arr)
# Output: Random values, e.g., 
# [[1.5e-323 0.0e+000]
#  [0.0e+000 0.0e+000]]
```

### 68. `np.full()`
Creates a new array of given shape and type, filled with a specified value.

```python
full_arr = np.full((2, 2), 7)
print(full_arr)
# Output:
# [[7 7]
#  [7 7]]
```

### 69. `np.partition()`
Partitions an array into two parts: elements less than the kth element, and elements greater than or equal to the kth element.

```python
arr = np.array([3, 1, 2, 4])
partitioned = np.partition(arr, 2)
print(partitioned)
# Output: [2 1 3 4]
```

### 70. `np.argsort()`
Returns the indices that would sort an array.

```python
arr = np.array([3, 1, 2])
sorted_indices = np.argsort(arr)
print(sorted_indices)
# Output: [1 2 0]
```

### 71. `np.searchsorted()`
Finds indices where elements should be inserted to maintain order.

```python
arr = np.array([1, 2, 4, 5])
index = np.searchsorted(arr, 3)
print(index)
# Output: 2
```

### 72. `np.extract()`
Returns the elements of an array that satisfy a given condition.

```python
arr = np.array([1, 2, 3, 4, 5])
extracted = np.extract(arr > 3, arr)
print(extracted)
# Output: [4 5]
```

### 73. `np.where()`
Return elements chosen from `x` or `y` depending on condition.

```python
arr = np.array([1, 2, 3, 4])
result = np.where(arr % 2 == 0, arr, -1)
print(result)
# Output: [-1  2 -1  4]
```

### 74. `np.tril()`
Returns the lower triangular part of an array.

```python
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
lower_triangular = np.tril(matrix)
print(lower_triangular)
# Output:
# [[1 0 0]
#  [4 5 0]
#  [7 8 9]]
```

### 75. `np.triu()`
Returns the upper triangular part of an array.

```python
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
upper_triangular = np.triu(matrix)
print(upper_triangular)
# Output:
# [[1 2 3]
#  [0 5 6]
#  [0 0 9]]
```

### 76. `np.clip()`
Limits the values in an array.

```python
arr = np.array([1, 2, 3, 4, 5])
clipped = np.clip(arr, 3, 4)
print(clipped)
# Output: [3 3 3 4 4]
```

### 77. `np.meshgrid()`
Creates coordinate matrices from coordinate vectors.

```python
x = np.array([1, 2, 3])
y = np.array([4, 5])
xx, yy = np.meshgrid(x, y)
print(xx)
# Output:
# [[1 2 3]
#  [1 2 3]]
print(yy)
# Output:
# [[4 4 4]
#  [5 5 5]]
```

### 78. `np.roll()`
Rolls array elements along a specified axis.

```python
arr = np.array([1, 2, 3, 4, 5])
rolled = np.roll(arr, 2)
print(rolled)
# Output: [4 5 1 2 3]
```

### 79. `np.swapaxes()`
Interchanges two axes of an array.

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])
swapped = np.swapaxes(arr, 0, 1)
print(swapped)
# Output:
# [[1 4]
#  [2 5]
#  [3 6]]
```

### 80. `np.ravel()`
Flattens an array to one dimension.

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])
raveled = np.ravel(arr)
print(raveled)
# Output: [1 2 3 4 5 6]
```

### 81. `np.sort()`
Returns a sorted copy of an array.

```python
arr = np.array([3, 1, 2])
sorted_arr = np.sort(arr)
print(sorted_arr)
# Output: [1 2 3]
```

### 82. `np.rollaxis()`
Rolls the specified axis backwards, until it lies in a given position.

```python
arr = np.array([[1, 2], [3, 4], [5, 6]])
rolled_axis = np.rollaxis(arr, 1, 0)
print(rolled_axis)
# Output:
# [[1 3 5]
#  [2 4 6]]
```

### 83. `np.ndarray.astype()`
Casts an array to a specified type.

```python
arr = np.array([1, 2, 3])
casted = arr.astype(float)
print(casted)
# Output: [1. 2. 3.]
```

### 84. `np.percentile()`
Computes the nth percentile of the data along the specified axis.

```python
arr = np.array([1, 2, 3, 4, 5])
percentile_value = np.percentile(arr, 50)
print(percentile_value)
# Output: 3.0
```

### 85. `np.std()`
Computes the standard deviation of an array.

```python
arr = np.array([1, 2, 3])
std_value = np.std(arr)
print(std_value)
# Output: 0.816496580927726
```

### 86. `np.sum()`
Calculates the sum of array elements over a given axis.

```python
arr = np.array([[1, 2], [3, 4]])
sum_value = np.sum(arr)
print(sum_value)
# Output: 10
```

### 87. `np.count_nonzero()`
Counts the number of non-zero elements in an array.

```python
arr = np.array([1, 0, 2, 0, 3])
count = np.count_nonzero(arr)
print(count)
# Output: 3
```

### 88. `np.any()`
Tests whether any array element along a given axis evaluates to True.

```python
arr = np.array([0, 0, 1])
any_true = np.any(arr)
print(any_true)
# Output: True
```

### 89. `np.all()`
Tests whether all array elements along a given axis evaluate to True.

```python
arr = np.array([1, 1, 1])
all_true = np.all(arr)
print(all_true)
# Output: True
```

### 90. `np.isclose()`
Tests whether two arrays are element-wise equal within a tolerance.

```python
arr1 = np.array([1.0, 2.0, 3.0])
arr2 = np.array([1.0, 2.0, 3.0000001])
close = np.isclose(arr1, arr2)
print(close)
# Output: [ True  True  True]
```

### 91. `np.copy()`
Returns a copy of an array.

```python
arr = np.array([1, 2, 3])
copied = np.copy(arr)
print(copied)
# Output: [1 2 3]
```

### 92. `np.unique()`
Finds the unique elements of an array.

```python
arr = np.array([1, 2, 2, 3])
unique_elements = np.unique(arr)
print(unique_elements)
# Output: [1 2 3]
```

### 93. `np.isin()`
Tests whether each element of an array is present in another array.

```python
arr = np.array([1, 2, 3, 4])
test_values = np.array([2, 4])
isin_result = np.isin(arr, test_values)
print(isin_result)
# Output: [False  True False  True]
```

### 94. `np.savez_compressed()`
Saves multiple arrays into a single compressed `.npz` file.

```python
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
np.savez

_compressed('arrays.npz', arr1=arr1, arr2=arr2)
# Output: A file named 'arrays.npz' will be created.
```

### 95. `np.load()`
Loads arrays from a `.npz` file.

```python
data = np.load('arrays.npz')
print(data['arr1'])
# Output: [1 2 3]
```

### 96. `np.fromiter()`
Creates a 1-D array from an iterable object.

```python
iterable = (x*x for x in range(5))
arr = np.fromiter(iterable, dtype=int)
print(arr)
# Output: [0 1 4 9 16]
```

### 97. `np.fromfunction()`
Constructs an array by executing a function over each coordinate.

```python
arr = np.fromfunction(lambda i, j: i + j, (3, 3), dtype=int)
print(arr)
# Output:
# [[0 1 2]
#  [1 2 3]
#  [2 3 4]]
```

### 98. `np.isfinite()`
Tests element-wise for finiteness (not NaN or infinite).

```python
arr = np.array([1, 2, np.nan, np.inf])
finite_check = np.isfinite(arr)
print(finite_check)
# Output: [ True  True False False]
```

### 99. `np.isinf()`
Tests element-wise for positive or negative infinity.

```python
arr = np.array([1, 2, np.nan, np.inf, -np.inf])
inf_check = np.isinf(arr)
print(inf_check)
# Output: [False False False  True  True]
```

### 100. `np.isnan()`
Tests element-wise for NaN (Not a Number).

```python
arr = np.array([1, 2, np.nan, 4])
nan_check = np.isnan(arr)
print(nan_check)
# Output: [False False  True False]
```

### Summary

The above functions cover a wide range of operations you can perform using NumPy. These examples demonstrate the flexibility and power of NumPy for numerical computations and array manipulations. If you have more specific areas or additional functions you’d like to explore, feel free to ask!

---
---
---



