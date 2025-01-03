# Off-by-one error in C++ vector iteration

This repository demonstrates a common off-by-one error in C++ when iterating over a `std::vector`.  The error arises from incorrectly using `<=` in the loop condition, leading to accessing an element beyond the vector's valid index range.

## Bug Description
The code attempts to iterate through a vector and print each element. However, the loop condition `i <= myVector.size()` is incorrect.  Vectors are zero-indexed, meaning the last valid index is `size() - 1`. Accessing `myVector[size()]` results in undefined behavior.

## Solution
The solution corrects the loop condition to `i < myVector.size()`, ensuring that the loop iterates only up to the last valid index of the vector.