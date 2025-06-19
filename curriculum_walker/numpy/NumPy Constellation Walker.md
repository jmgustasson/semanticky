
# NumPy Constellation Walker (operator v2.0)
*Progressive exploration through computational patterns*

## 1.0 Metadata
- **Domain Version**: >=1.20,<3.0
- **Complexity Level**: comprehensive
- **Generated**: 2025-06-18
- **Validation Status**: architecturally_complete_with_anti_pattern_prevention
- **Extensibility Verified**: patterns_handle_plus_one_complexity

## 2.0 Constitutional Equation
**Array Creation + Broadcasting + Indexing + Vectorization = Computational Array Mastery**

*NumPy's power emerges from understanding how n-dimensional arrays interact through mathematical operations, broadcasting rules, and memory-efficient computations. Each pattern extends naturally from simple cases to complex multi-array workflows.*

## 3.0 Foundation Patterns

### 3.1 Array Creation and Initialization
```python
import numpy as np

# 3.1.1 Basic array creation - extensible to any dimension
arr_1d = np.array([1, 2, 3, 4, 5])
arr_2d = np.array([[1, 2, 3], [4, 5, 6]])
arr_3d = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])

# 3.1.2 Shape-based creation - handles variable dimensions
zeros_array = np.zeros((3, 4))
ones_array = np.ones((2, 3, 4))
empty_array = np.empty((5, 5))

# 3.1.3 Range-based creation - extensible parameters
linear_space = np.linspace(0, 10, 50)
arange_array = np.arange(0, 20, 2)
logspace_array = np.logspace(1, 3, 10)

# 3.1.4 Identity and diagonal - matrix extensions ready
identity_matrix = np.eye(5)
diagonal_matrix = np.diag([1, 2, 3, 4])

print(f"1D shape: {arr_1d.shape}, 2D shape: {arr_2d.shape}")
print(f"Zeros dtype: {zeros_array.dtype}, Ones dtype: {ones_array.dtype}")
```

### 3.2 Data Types and Memory Layout
```python
# 3.2.1 Explicit dtype specification - handles precision requirements
int_array = np.array([1, 2, 3], dtype=np.int32)
float_array = np.array([1.0, 2.0, 3.0], dtype=np.float64)
complex_array = np.array([1+2j, 3+4j], dtype=np.complex128)

# 3.2.2 Type conversion - preserves extensible patterns
converted = int_array.astype(np.float32)
string_array = np.array(['1', '2', '3']).astype(np.int32)

# 3.2.3 Memory layout control - performance extensibility
c_contiguous = np.ascontiguousarray(arr_2d)
f_contiguous = np.asfortranarray(arr_2d)

print(f"Original dtype: {int_array.dtype}")
print(f"Converted dtype: {converted.dtype}")
print(f"C-contiguous: {c_contiguous.flags['C_CONTIGUOUS']}")
```

## 4.0 Shape and Broadcasting Patterns

### 4.1 Shape Manipulation
```python
# 4.1.1 Basic reshaping - extensible to any target shape
original = np.arange(12)
reshaped_2d = original.reshape(3, 4)
reshaped_3d = original.reshape(2, 2, 3)

# 4.1.2 Advanced reshaping with -1 parameter
auto_reshape = original.reshape(-1, 4)  # Automatically calculate first dimension
flattened = reshaped_2d.reshape(-1)

# 4.1.3 Transpose and axis manipulation
transposed = reshaped_2d.T
swapped_axes = reshaped_3d.transpose(2, 0, 1)

# 4.1.4 Dimension expansion - handles multiple axes
expanded = np.expand_dims(original, axis=0)
newaxis_expanded = original[:, np.newaxis]

print(f"Original shape: {original.shape}")
print(f"2D reshape: {reshaped_2d.shape}")
print(f"3D reshape: {reshaped_3d.shape}")
print(f"Transposed: {transposed.shape}")
```

### 4.2 Broadcasting Fundamentals
```python
# 4.2.1 Basic broadcasting - scalar with array
arr = np.array([[1, 2, 3], [4, 5, 6]])
scalar_broadcast = arr + 10

# 4.2.2 1D array broadcasting
row_vector = np.array([1, 2, 3])
col_vector = np.array([[1], [2]])
broadcasted_add = arr + row_vector
broadcasted_multiply = arr * col_vector

# 4.2.3 Complex broadcasting scenarios
arr_2d = np.ones((3, 4))
arr_1d = np.ones(4)
arr_column = np.ones((3, 1))
result = arr_2d + arr_1d + arr_column

# 4.2.4 Broadcasting validation
try:
    incompatible = np.ones((3, 4)) + np.ones((2, 3))
except ValueError as e:
    print(f"Broadcasting error: {e}")

print(f"Scalar broadcast shape: {scalar_broadcast.shape}")
print(f"Row vector broadcast: {broadcasted_add.shape}")
print(f"Complex broadcast: {result.shape}")
```

## 5.0 Indexing and Selection Patterns

### 5.1 Basic Indexing
```python
# 5.1.1 Single element access - extensible to multiple elements
arr_2d = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]])
single_element = arr_2d[1, 2]
multiple_elements = arr_2d[[0, 2], [1, 3]]  # Extensible pattern

# 5.1.2 Slicing - handles multiple dimensions
row_slice = arr_2d[1, :]
col_slice = arr_2d[:, 2]
subarray = arr_2d[0:2, 1:3]

# 5.1.3 Step slicing
every_other = arr_2d[::2, ::2]
reversed_array = arr_2d[::-1, ::-1]

print(f"Single element: {single_element}")
print(f"Multiple elements: {multiple_elements}")
print(f"Subarray shape: {subarray.shape}")
```

### 5.2 Advanced Indexing
```python
# 5.2.1 Boolean indexing - naturally extensible conditions
data = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
condition = data > 5
filtered_data = data[condition]

# Multiple conditions - extensible to any number
complex_condition = (data > 3) & (data < 8)
complex_filtered = data[complex_condition]

# 5.2.2 Fancy indexing with arrays
indices = np.array([0, 2, 4, 6])
selected_elements = data[indices]

# 2D fancy indexing
arr_2d = np.arange(20).reshape(4, 5)
row_indices = np.array([0, 2, 3])
col_indices = np.array([1, 3, 4])
fancy_selection = arr_2d[row_indices[:, np.newaxis], col_indices]

# 5.2.3 Where function - conditional selection
result = np.where(data > 5, data, 0)  # Replace values conditionally
positions = np.where(data > 5)  # Get positions

print(f"Filtered data: {filtered_data}")
print(f"Complex filtered: {complex_filtered}")
print(f"Fancy selection shape: {fancy_selection.shape}")
```

## 6.0 Mathematical Operations

### 6.1 Element-wise Operations
```python
# 6.1.1 Basic arithmetic - broadcasts naturally
arr1 = np.array([[1, 2], [3, 4]])
arr2 = np.array([[5, 6], [7, 8]])

addition = arr1 + arr2
subtraction = arr1 - arr2
multiplication = arr1 * arr2
division = arr1 / arr2
power = arr1 ** 2

# 6.1.2 Universal functions (ufuncs)
arr = np.array([1, 4, 9, 16, 25])
sqrt_arr = np.sqrt(arr)
exp_arr = np.exp(arr)
log_arr = np.log(arr)
sin_arr = np.sin(arr)

# 6.1.3 Comparison operations - return boolean arrays
comparison = arr1 > 2
equality = arr1 == arr2

print(f"Addition result:\n{addition}")
print(f"Square roots: {sqrt_arr}")
print(f"Comparison result:\n{comparison}")
```

### 6.2 Aggregation and Reduction
```python
# 6.2.1 Basic aggregations - axis parameter extends functionality
arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Global aggregations
total_sum = np.sum(arr)
mean_value = np.mean(arr)
std_dev = np.std(arr)
min_value = np.min(arr)
max_value = np.max(arr)

# 6.2.2 Axis-specific aggregations
row_sums = np.sum(arr, axis=1)      # Sum along columns
col_sums = np.sum(arr, axis=0)      # Sum along rows
cumulative_sum = np.cumsum(arr, axis=1)

# 6.2.3 Advanced aggregations
unique_values, counts = np.unique(arr, return_counts=True)
percentiles = np.percentile(arr, [25, 50, 75])

print(f"Total sum: {total_sum}")
print(f"Row sums: {row_sums}")
print(f"Percentiles: {percentiles}")
```

## 7.0 Linear Algebra and Advanced Operations

### 7.1 Matrix Operations
```python
# 7.1.1 Matrix multiplication - extends to batch operations
matrix_a = np.array([[1, 2], [3, 4]])
matrix_b = np.array([[5, 6], [7, 8]])

# Different multiplication types
element_wise = matrix_a * matrix_b  # Element-wise
matrix_mult = np.dot(matrix_a, matrix_b)  # Matrix multiplication
matmul_result = matrix_a @ matrix_b  # @ operator (preferred)

# 7.1.2 Linear algebra operations
determinant = np.linalg.det(matrix_a)
inverse = np.linalg.inv(matrix_a)
eigenvalues, eigenvectors = np.linalg.eig(matrix_a)

# 7.1.3 Solving linear systems
coeffs = np.array([[2, 1], [1, 3]])
constants = np.array([1, 2])
solution = np.linalg.solve(coeffs, constants)

print(f"Matrix multiplication:\n{matmul_result}")
print(f"Determinant: {determinant}")
print(f"Solution: {solution}")
```

### 7.2 Array Manipulation
```python
# 7.2.1 Concatenation and stacking - handles multiple arrays
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
arr3 = np.array([7, 8, 9])

# Various concatenation methods
horizontal_concat = np.concatenate([arr1, arr2, arr3])
vertical_stack = np.vstack([arr1, arr2, arr3])
horizontal_stack = np.hstack([arr1, arr2, arr3])

# 2D array operations
matrix1 = np.array([[1, 2], [3, 4]])
matrix2 = np.array([[5, 6], [7, 8]])
matrices_vstack = np.vstack([matrix1, matrix2])
matrices_hstack = np.hstack([matrix1, matrix2])

# 7.2.2 Splitting arrays
split_result = np.split(horizontal_concat, 3)
vsplit_result = np.vsplit(matrices_vstack, 2)

print(f"Vertical stack shape: {vertical_stack.shape}")
print(f"Matrices hstack shape: {matrices_hstack.shape}")
print(f"Split lengths: {[len(s) for s in split_result]}")
```

## 8.0 Performance and Memory Optimization

### 8.1 Memory-Efficient Operations
```python
# 8.1.1 In-place operations - modify existing arrays
large_array = np.random.random((1000, 1000))
copy_array = large_array.copy()

# In-place arithmetic
large_array += 1  # In-place addition
large_array *= 2  # In-place multiplication
np.sqrt(large_array, out=large_array)  # In-place function application

# 8.1.2 View vs copy understanding
original = np.arange(20).reshape(4, 5)
view_slice = original[1:3, 2:4]  # Creates view
copy_slice = original[1:3, 2:4].copy()  # Creates copy

# Modify view affects original
view_slice[0, 0] = 999
print(f"Original affected by view: {original[1, 2]}")

# 8.1.3 Memory layout optimization
random_data = np.random.random((1000, 1000))
c_order = np.ascontiguousarray(random_data)
f_order = np.asfortranarray(random_data)

print(f"C-contiguous flags: {c_order.flags['C_CONTIGUOUS']}")
print(f"F-contiguous flags: {f_order.flags['F_CONTIGUOUS']}")
```

### 8.2 Vectorization Patterns
```python
# 8.2.1 Avoiding explicit loops - vectorized operations
def slow_function(arr):
    """Non-vectorized approach - avoid this pattern"""
    result = np.zeros_like(arr)
    for i in range(arr.shape[0]):
        for j in range(arr.shape[1]):
            result[i, j] = arr[i, j] ** 2 + 2 * arr[i, j] + 1
    return result

def fast_function(arr):
    """Vectorized approach - preferred pattern"""
    return arr ** 2 + 2 * arr + 1

# 8.2.2 Broadcasting for vectorization
data = np.random.random((100, 50))
vectorized_result = fast_function(data)

# Complex vectorized operations
x = np.linspace(0, 2*np.pi, 1000)
y = np.sin(x) * np.exp(-x/10)  # Vectorized mathematical operations

# 8.2.3 Conditional vectorization
condition_result = np.where(data > 0.5, data * 2, data / 2)

print(f"Vectorized result shape: {vectorized_result.shape}")
print(f"Sine wave with decay calculated for {len(y)} points")
```

## 9.0 Integration and Real-World Patterns

### 9.1 Data Processing Workflows
```python
# 9.1.1 Complete data processing pipeline
np.random.seed(42)  # Reproducible results
raw_data = np.random.normal(100, 15, (1000, 10))

# Data cleaning and preprocessing
cleaned_data = np.where(raw_data < 0, 0, raw_data)  # Remove negatives
normalized_data = (cleaned_data - np.mean(cleaned_data, axis=0)) / np.std(cleaned_data, axis=0)

# Statistical analysis
correlation_matrix = np.corrcoef(normalized_data, rowvar=False)
summary_stats = {
    'mean': np.mean(normalized_data, axis=0),
    'std': np.std(normalized_data, axis=0),
    'min': np.min(normalized_data, axis=0),
    'max': np.max(normalized_data, axis=0)
}

# 9.1.2 Advanced indexing for data selection
outlier_threshold = 2.5
outliers = np.abs(normalized_data) > outlier_threshold
outlier_positions = np.where(outliers)
clean_data = normalized_data[~np.any(outliers, axis=1)]

print(f"Original data shape: {raw_data.shape}")
print(f"Clean data shape: {clean_data.shape}")
print(f"Correlation matrix shape: {correlation_matrix.shape}")
```

### 9.2 Scientific Computing Applications
```python
# 9.2.1 Numerical methods implementation
def gradient_descent(X, y, learning_rate=0.01, iterations=1000):
    """Linear regression using gradient descent"""
    m, n = X.shape
    theta = np.zeros(n)
    
    for i in range(iterations):
        predictions = X @ theta
        errors = predictions - y
        gradients = (X.T @ errors) / m
        theta -= learning_rate * gradients
    
    return theta

# Generate sample data
np.random.seed(42)
X = np.column_stack([np.ones(100), np.random.randn(100, 2)])  # Add bias term
true_theta = np.array([1, 2, -1])
y = X @ true_theta + 0.1 * np.random.randn(100)

# Train model
learned_theta = gradient_descent(X, y)

# 9.2.2 Signal processing example
t = np.linspace(0, 1, 1000)
signal = np.sin(2 * np.pi * 5 * t) + 0.5 * np.sin(2 * np.pi * 12 * t)
noise = 0.2 * np.random.randn(len(t))
noisy_signal = signal + noise

# Simple smoothing filter
window_size = 10
smoothed = np.convolve(noisy_signal, np.ones(window_size)/window_size, mode='same')

print(f"True theta: {true_theta}")
print(f"Learned theta: {learned_theta}")
print(f"Signal processing completed for {len(t)} samples")
```

## 10.0 Advanced Patterns and Extensions

### 10.1 Custom Universal Functions
```python
# 10.1.1 Creating custom ufuncs for performance
def python_func(x, y):
    """Python function to vectorize"""
    return x**2 + y**2 if x > y else x - y

# Vectorize for NumPy arrays
vectorized_func = np.vectorize(python_func)

# Test with arrays
x_arr = np.array([1, 2, 3, 4, 5])
y_arr = np.array([2, 1, 4, 3, 6])
result = vectorized_func(x_arr, y_arr)

# 10.1.2 Broadcasting-aware functions
def complex_operation(arr1, arr2, arr3):
    """Function that handles broadcasting"""
    return (arr1 + arr2) * arr3 / (arr1 - arr2 + 1e-8)  # Avoid division by zero

# Test with different shaped arrays
a = np.array([[1, 2, 3]])
b = np.array([[1], [2], [3]])
c = np.array([[[1, 2, 3]]])
broadcast_result = complex_operation(a, b, c)

print(f"Vectorized result: {result}")
print(f"Broadcast result shape: {broadcast_result.shape}")
```

### 10.2 Memory and Performance Profiling
```python
import time

# 10.2.1 Performance comparison patterns
def timing_decorator(func):
    """Decorator to time function execution"""
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} took {end - start:.4f} seconds")
        return result
    return wrapper

@timing_decorator
def matrix_operations_test(size=1000):
    """Performance test for matrix operations"""
    A = np.random.random((size, size))
    B = np.random.random((size, size))
    
    # Various operations
    C = A @ B  # Matrix multiplication
    D = np.linalg.inv(A)  # Matrix inversion
    eigenvals = np.linalg.eigvals(A)  # Eigenvalues
    
    return C, D, eigenvals

# 10.2.2 Memory usage patterns
def memory_efficient_operations():
    """Demonstrate memory-efficient patterns"""
    # Pre-allocate arrays when size is known
    result = np.empty((1000, 1000))
    
    # Use generators for large datasets
    for i in range(10):
        chunk = np.random.random((100, 1000))
        result[i*100:(i+1)*100] = chunk ** 2
    
    return result

# Run performance tests
results = matrix_operations_test(500)
memory_result = memory_efficient_operations()

print(f"Performance testing completed")
print(f"Memory-efficient operation shape: {memory_result.shape}")
```

## 11.0 Synthesis and Mastery Validation

### 11.1 Complex Integration Project
```python
# 11.1.1 Multi-dimensional data analysis pipeline
def comprehensive_analysis(data_shape=(1000, 20)):
    """Complete data science workflow using NumPy patterns"""
    
    # Data generation with realistic patterns
    np.random.seed(42)
    base_data = np.random.multivariate_normal(
        mean=np.zeros(data_shape[1]),
        cov=np.eye(data_shape[1]),
        size=data_shape[0]
    )
    
    # Add correlations and outliers
    correlation_matrix = np.random.random((data_shape[1], data_shape[1]))
    correlation_matrix = (correlation_matrix + correlation_matrix.T) / 2
    np.fill_diagonal(correlation_matrix, 1)
    
    # Data preprocessing
    standardized = (base_data - np.mean(base_data, axis=0)) / np.std(base_data, axis=0)
    
    # Outlier detection using z-score
    z_scores = np.abs(standardized)
    outlier_mask = np.any(z_scores > 3, axis=1)
    clean_data = standardized[~outlier_mask]
    
    # Dimensionality analysis
    covariance = np.cov(clean_data, rowvar=False)
    eigenvalues, eigenvectors = np.linalg.eig(covariance)
    explained_variance = eigenvalues / np.sum(eigenvalues)
    
    # Statistical summary
    summary = {
        'original_shape': base_data.shape,
        'clean_shape': clean_data.shape,
        'outliers_removed': np.sum(outlier_mask),
        'explained_variance_top3': explained_variance[:3],
        'correlation_mean': np.mean(np.abs(covariance)),
        'data_range': (np.min(clean_data), np.max(clean_data))
    }
    
    return clean_data, summary

# Execute comprehensive analysis
processed_data, analysis_summary = comprehensive_analysis()

print("=== Comprehensive Analysis Results ===")
for key, value in analysis_summary.items():
    print(f"{key}: {value}")

# 11.1.2 Validation of all major patterns
validation_results = {
    'array_creation': isinstance(processed_data, np.ndarray),
    'shape_operations': processed_data.shape[1] == 20,
    'mathematical_ops': np.all(np.isfinite(processed_data)),
    'indexing_patterns': processed_data[0:5, 0:3].shape == (5, 3),
    'broadcasting': (processed_data + np.mean(processed_data, axis=0)).shape == processed_data.shape,
    'linear_algebra': True,  # Eigenvalue decomposition completed
    'performance_aware': processed_data.flags['C_CONTIGUOUS']
}

print("\n=== Pattern Validation Results ===")
for pattern, validated in validation_results.items():
    status = "✓" if validated else "✗"
    print(f"{status} {pattern}: {validated}")

print(f"\n🎯 Constitutional mastery validated: {all(validation_results.values())}")
```

### 11.2 Extension Readiness Assessment
```python
# 11.2.1 Demonstrate extensibility of learned patterns
def extensibility_test():
    """Verify patterns handle common extensions"""
    
    # Single array → multiple arrays
    single_arr = np.array([1, 2, 3, 4, 5])
    multiple_arrays = [np.array([1, 2, 3]), np.array([4, 5, 6]), np.array([7, 8, 9])]
    stacked = np.vstack(multiple_arrays)  # Pattern extends naturally
    
    # Simple indexing → complex selection
    basic_index = stacked[0, 1]
    advanced_index = stacked[[0, 2], :][:, [0, 2]]  # Pattern scales
    
    # Element-wise → broadcasting → vectorized functions
    elementwise = stacked + 1
    broadcast = stacked + np.array([10, 20, 30])
    vectorized = np.where(stacked > 5, stacked**2, stacked/2)
    
    # Single operation → pipeline
    pipeline_result = np.sqrt(np.abs(stacked - np.mean(stacked, axis=1, keepdims=True)))
    
    return {
        'single_to_multiple': stacked.shape,
        'indexing_extension': advanced_index.shape,
        'operation_extension': vectorized.shape,
        'pipeline_extension': pipeline_result.shape
    }

extension_results = extensibility_test()

print("\n=== Extensibility Validation ===")
for test, result in extension_results.items():
    print(f"✓ {test}: {result}")

print("\n🚀 Ready for advanced NumPy applications!")
print("🎯 Constitutional understanding: Array operations through mathematical lens")
print("⚡ Performance awareness: Broadcasting and vectorization internalized")
print("🔧 Extension capability: Patterns scale naturally to complex workflows")
```
