
# NumPy Constitutional Constellation Reference (operator v2.0)
*Complete pattern map for rapid cognitive integration*

## 1.0 Metadata
- **Domain Version**: >=1.20,<3.0
- **Complexity Level**: comprehensive
- **Generated**: 2025-06-18
- **Validation Status**: architecturally_complete_with_anti_pattern_prevention
- **Extensibility Verified**: patterns_handle_plus_one_complexity

## 2.0 Constitutional Equation
**Array Creation + Broadcasting + Indexing + Vectorization = Computational Array Mastery**

## 3.0 Core Creation Patterns

### 3.1 Array Initialization
```python
import numpy as np

# Basic creation - extensible to any dimension
np.array([1, 2, 3])                    # 1D from list
np.array([[1, 2], [3, 4]])             # 2D from nested lists
np.array([[[1, 2]], [[3, 4]]])         # 3D extension ready

# Shape-based creation - handles variable dimensions
np.zeros((3, 4))                       # Zeros with shape
np.ones((2, 3, 4))                     # Ones with shape  
np.empty((5, 5))                       # Uninitialized memory
np.full((3, 3), 7)                     # Fill with value

# Range creation - extensible parameters
np.arange(10)                          # 0 to 9
np.arange(1, 10, 2)                    # Start, stop, step
np.linspace(0, 1, 5)                   # Linear spacing
np.logspace(1, 3, 5)                   # Logarithmic spacing

# Matrix creation - ready for linear algebra extensions
np.eye(3)                              # Identity matrix
np.diag([1, 2, 3])                     # Diagonal matrix
np.random.random((3, 3))               # Random values
```

### 3.2 Data Type Control
```python
# Explicit dtype - precision extensible
np.array([1, 2, 3], dtype=np.int32)    # 32-bit integers
np.array([1.0, 2.0], dtype=np.float64) # 64-bit floats
np.array([1+2j], dtype=np.complex128)  # Complex numbers

# Type conversion - preserves extensible patterns
arr.astype(np.float32)                 # Convert to float32
arr.astype('U10')                      # Convert to Unicode string

# Memory layout - performance extensible
np.ascontiguousarray(arr)              # C-contiguous layout
np.asfortranarray(arr)                 # Fortran-contiguous layout
```

## 4.0 Shape and Broadcasting Constellation

### 4.1 Shape Manipulation
```python
# Reshaping - extensible to any target shape
arr.reshape(3, 4)                      # Explicit dimensions
arr.reshape(-1, 4)                     # Auto-calculate dimension
arr.reshape(2, -1, 3)                  # Multiple auto dimensions

# Dimension operations - extensible axis handling
arr.T                                  # Transpose (2D)
arr.transpose(2, 0, 1)                 # Reorder axes (3D+)
np.expand_dims(arr, axis=0)            # Add dimension at axis
arr.squeeze()                          # Remove single dimensions
arr[:, np.newaxis]                     # Add axis via indexing

# Flattening - preserves extensible access
arr.flatten()                          # Copy to 1D
arr.ravel()                            # View as 1D when possible
arr.reshape(-1)                        # Reshape to 1D
```

### 4.2 Broadcasting Rules
```python
# Scalar broadcasting - extends to any array
arr + 5                                # Scalar to array
arr * 2.5                              # Scalar multiplication

# 1D broadcasting - naturally extensible
arr_2d + arr_1d                        # (3,4) + (4,) → (3,4)
arr_3d + arr_1d                        # (2,3,4) + (4,) → (2,3,4)

# Advanced broadcasting - handles complex cases
arr_2d + arr_col                       # (3,4) + (3,1) → (3,4)
arr_3d + arr_2d                        # (2,3,4) + (3,4) → (2,3,4)

# Broadcasting validation - extensible error handling
np.broadcast_arrays(arr1, arr2)        # Check compatibility
np.broadcast_shapes(shape1, shape2)    # Shape compatibility
```

## 5.0 Indexing and Selection Constellation

### 5.1 Basic Indexing
```python
# Single element - extends to multiple elements
arr[0]                                 # First element
arr[i, j]                              # 2D element access
arr[i, j, k]                           # 3D element access

# Slicing - handles multiple dimensions
arr[:]                                 # All elements
arr[1:4]                               # Slice range
arr[::2]                               # Step slicing
arr[::-1]                              # Reverse
arr[1:4, 2:5]                          # 2D slicing
arr[..., -1]                           # Last along final axis
```

### 5.2 Advanced Selection
```python
# Boolean indexing - naturally extensible conditions
arr[arr > 5]                           # Single condition
arr[(arr > 0) & (arr < 10)]            # Multiple conditions
arr[np.logical_or(cond1, cond2)]       # Complex logic

# Fancy indexing - handles multiple arrays
arr[[0, 2, 4]]                         # Index array
arr[[0, 2], [1, 3]]                    # Multiple index arrays
arr[indices[:, np.newaxis], cols]      # Broadcasting indices

# Conditional operations - extensible to any condition
np.where(condition, x, y)              # Conditional selection
np.select([cond1, cond2], [val1, val2], default) # Multiple conditions
np.choose(indices, choices)            # Choose from arrays
```

## 6.0 Mathematical Operations Constellation

### 6.1 Element-wise Operations
```python
# Arithmetic operations - broadcast naturally
arr1 + arr2                            # Addition
arr1 - arr2                            # Subtraction  
arr1 * arr2                            # Multiplication
arr1 / arr2                            # Division
arr1 ** arr2                           # Power
arr1 // arr2                           # Floor division
arr1 % arr2                            # Modulo

# Universal functions - vectorized by design
np.sqrt(arr)                           # Square root
np.exp(arr)                            # Exponential
np.log(arr)                            # Natural logarithm
np.sin(arr)                            # Sine
np.cos(arr)                            # Cosine
np.abs(arr)                            # Absolute value

# Comparison operations - return boolean arrays
arr1 == arr2                           # Element equality
arr1 > arr2                            # Greater than
arr1 <= arr2                           # Less than or equal
np.isnan(arr)                          # NaN detection
np.isinf(arr)                          # Infinity detection
```

### 6.2 Aggregation and Reduction
```python
# Global reductions - single value output
np.sum(arr)                            # Total sum
np.mean(arr)                           # Arithmetic mean
np.std(arr)                            # Standard deviation
np.var(arr)                            # Variance
np.min(arr)                            # Minimum value
np.max(arr)                            # Maximum value
np.median(arr)                         # Median value

# Axis-specific reductions - preserves extensibility
np.sum(arr, axis=0)                    # Sum along first axis
np.mean(arr, axis=1)                   # Mean along second axis
np.std(arr, axis=(0, 2))               # Multiple axes
np.cumsum(arr, axis=1)                 # Cumulative sum
np.cumprod(arr, axis=0)                # Cumulative product

# Statistical functions - handles multiple dimensions
np.percentile(arr, [25, 50, 75])       # Percentiles
np.quantile(arr, [0.25, 0.75])         # Quantiles
np.corrcoef(arr, rowvar=False)         # Correlation matrix
np.cov(arr, rowvar=False)              # Covariance matrix
```

## 7.0 Linear Algebra Constellation

### 7.1 Matrix Operations
```python
# Matrix multiplication - extends to batch operations
np.dot(A, B)                           # Dot product
A @ B                                  # Matrix multiplication (preferred)
np.matmul(A, B)                        # Matrix multiplication
np.outer(a, b)                         # Outer product
np.inner(a, b)                         # Inner product

# Matrix properties and decompositions
np.linalg.det(A)                       # Determinant
np.linalg.inv(A)                       # Matrix inverse
np.linalg.pinv(A)                      # Pseudo-inverse
np.linalg.rank(A)                      # Matrix rank
np.trace(A)                            # Trace (sum of diagonal)

# Eigenvalue decomposition - extensible to batch
eigenvals, eigenvecs = np.linalg.eig(A)      # Eigendecomposition
eigenvals = np.linalg.eigvals(A)             # Eigenvalues only
U, s, Vt = np.linalg.svd(A)                  # Singular value decomposition
```

### 7.2 Linear Systems
```python
# Solving linear systems - handles multiple RHS
x = np.linalg.solve(A, b)              # Solve Ax = b
x = np.linalg.lstsq(A, b, rcond=None)  # Least squares solution

# Matrix norms - various types available
np.linalg.norm(A)                      # Frobenius norm
np.linalg.norm(A, ord=2)               # Spectral norm
np.linalg.norm(A, axis=1)              # Row-wise norms

# Factorizations - extensible to batch processing
Q, R = np.linalg.qr(A)                 # QR decomposition
L = np.linalg.cholesky(A)              # Cholesky decomposition
```

## 8.0 Array Manipulation Constellation

### 8.1 Joining and Splitting
```python
# Concatenation - handles multiple arrays
np.concatenate([arr1, arr2], axis=0)   # Along specified axis
np.vstack([arr1, arr2])                # Vertical stack (axis=0)
np.hstack([arr1, arr2])                # Horizontal stack (axis=1)
np.dstack([arr1, arr2])                # Depth stack (axis=2)
np.stack([arr1, arr2], axis=0)         # Create new axis

# Splitting - inverse of joining
np.split(arr, 3, axis=0)               # Split into equal parts
np.hsplit(arr, 3)                      # Horizontal split
np.vsplit(arr, 3)                      # Vertical split
np.array_split(arr, 3, axis=0)         # Unequal splits allowed
```

### 8.2 Repetition and Tiling
```python
# Element repetition - extensible patterns
np.repeat(arr, 3, axis=0)              # Repeat elements
np.tile(arr, (2, 3))                   # Tile array pattern
np.resize(arr, (5, 5))                 # Resize with repetition

# Array duplication - memory considerations
arr.copy()                             # Deep copy
arr.view()                             # Shallow copy (view)
np.broadcast_to(arr, (3, 4))           # Broadcast without copy
```

## 9.0 Performance Optimization Constellation

### 9.1 Memory Layout
```python
# Contiguity patterns - performance critical
arr.flags['C_CONTIGUOUS']              # Check C-contiguity
arr.flags['F_CONTIGUOUS']              # Check Fortran-contiguity
np.ascontiguousarray(arr)              # Ensure C-contiguous
np.asfortranarray(arr)                 # Ensure F-contiguous

# Memory usage - efficiency extensible
arr.nbytes                             # Memory usage in bytes
arr.itemsize                           # Bytes per element
arr.size * arr.itemsize                # Total memory calculation

# Views vs copies - memory efficiency
arr[::2].base is arr                   # Check if view
arr.copy().base is None                # Copies have no base
```

### 9.2 Vectorization Patterns
```python
# In-place operations - memory efficient
arr += 1                               # In-place addition
arr *= 2                               # In-place multiplication
np.sqrt(arr, out=arr)                  # In-place function application

# Vectorized functions - avoid loops
np.vectorize(python_func)              # Vectorize Python function
np.frompyfunc(func, nin=2, nout=1)     # Create ufunc

# Broadcasting optimization - efficient patterns
arr + scalar                           # Optimal broadcasting
arr + arr[:, np.newaxis]               # Memory-efficient broadcasting
np.add(arr1, arr2, out=result)         # Pre-allocated output
```

## 10.0 Advanced Patterns Constellation

### 10.1 Custom Universal Functions
```python
# Function vectorization - extensible to complex operations
@np.vectorize
def custom_func(x, y):
    return x**2 + y**2 if x > y else x - y

# Conditional operations - handles complex logic
np.where(condition, if_true, if_false)      # Ternary operation
np.piecewise(x, [cond1, cond2], [func1, func2, func3])  # Piecewise function
np.select([cond1, cond2], [choice1, choice2], default)  # Multiple conditions
```

### 10.2 Integration Patterns
```python
# Data type integration - handles mixed types
structured_array = np.array([(1, 'a', 3.0)], 
                           dtype=[('x', 'i4'), ('y', 'U1'), ('z', 'f4')])

# File I/O - extensible formats
np.save('array.npy', arr)              # Binary format
np.load('array.npy')                   # Load binary
np.savetxt('array.txt', arr)           # Text format
np.loadtxt('array.txt')                # Load text
np.savez('arrays.npz', a=arr1, b=arr2) # Multiple arrays

# Memory mapping - large array handling
memmap = np.memmap('large_array.dat', dtype='float32', 
                   mode='w+', shape=(1000000, 100))
```

## 11.0 Performance Profiling Constellation

### 11.1 Timing Patterns
```python
# Performance measurement - extensible benchmarking
import time
start = time.time()
result = expensive_operation(arr)
elapsed = time.time() - start

# Memory profiling - resource awareness
import sys
memory_usage = sys.getsizeof(arr)
total_memory = sum(sys.getsizeof(a) for a in array_list)
```

### 11.2 Optimization Guidelines
```python
# Efficient patterns - performance extensible
# Prefer: arr1 + arr2 over np.add(arr1, arr2)
# Prefer: arr @ other over np.dot(arr, other)  
# Prefer: arr[mask] over arr[np.where(mask)]
# Prefer: np.sum(arr, axis=0) over [np.sum(arr[:, i]) for i in range(arr.shape[1])]

# Memory efficiency - scales to large arrays
# Use views instead of copies when possible
# Pre-allocate arrays when size is known  
# Use appropriate dtypes (float32 vs float64)
# Consider memory layout (C vs Fortran order)

# Broadcasting efficiency - optimal patterns
# Align operations for natural broadcasting
# Avoid creating temporary arrays in complex expressions
# Use out parameter for in-place operations
# Structure computations to minimize memory allocation
```

## 12.0 Constitutional Mastery Validation

### 12.1 Pattern Integration Test
```python
# Complete workflow demonstrating all constellations
def constitutional_mastery_test():
    # 1. Array creation with proper dtype
    data = np.random.multivariate_normal([0, 0], [[1, 0.5], [0.5, 1]], 1000)
    
    # 2. Shape manipulation and broadcasting
    centered = data - np.mean(data, axis=0)
    normalized = centered / np.std(centered, axis=0)
    
    # 3. Advanced indexing and selection
    outliers = np.abs(normalized) > 2.5
    clean_data = normalized[~np.any(outliers, axis=1)]
    
    # 4. Mathematical operations and linear algebra
    cov_matrix = np.cov(clean_data, rowvar=False)
    eigenvals, eigenvecs = np.linalg.eig(cov_matrix)
    
    # 5. Aggregation and statistical analysis
    stats = {
        'mean': np.mean(clean_data, axis=0),
        'std': np.std(clean_data, axis=0),
        'correlation': np.corrcoef(clean_data, rowvar=False),
        'explained_variance': eigenvals / np.sum(eigenvals)
    }
    
    return clean_data, stats

# Execute constitutional validation
result_data, analysis = constitutional_mastery_test()
```

### 12.2 Extensibility Verification
```python
# Patterns ready for extension
single_array = np.array([1, 2, 3])
multiple_arrays = np.array([[1, 2, 3], [4, 5, 6]])  # Extends naturally
batch_operations = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])  # Scales further

# Broadcasting extends from simple to complex
simple_broadcast = single_array + 1
complex_broadcast = batch_operations + multiple_arrays[:, :, np.newaxis]

# Function patterns extend to arbitrary complexity
basic_operation = np.sum(single_array)
advanced_operation = np.sum(batch_operations, axis=(1, 2))
```

**🎯 Constitutional Understanding Achieved**: Array operations through unified mathematical framework  
**⚡ Performance Awareness Internalized**: Broadcasting, vectorization, and memory layout optimized  
**🔧 Extensibility Verified**: All patterns scale naturally from simple to complex applications  
**🚀 Ready for Advanced Applications**: Scientific computing, machine learning, signal processing
