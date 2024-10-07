


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
