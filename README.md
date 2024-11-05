# CyEinsum
CyEinsum is a C++ based Python library designed for efficient tensor contraction, employing the Einstein summation convention.

# Prerequisite
Before installation, ensure Python is equipped with Numpy and Cython

# Install
To install the CyEinsum library, navigate to the folder containing the `setup.py` file and run the following command:

```bash
python setup.py build_ext --inplace
```

This command compiles the source and generates the shared object file `einsum(version).so`, making it ready for use within your Python environment.

# Usage

Incorporating CyEinsum into your workflow is straightforward:

1. Import CyEinsum at the beginning of your Python script:

```python
import einsum
```

2. Call the library's function, `c_einsum`, with numpy ndarray objects and a string detailing the Einstein summation subscripts:

```python
einsum.c_einsum('ijab,kjca->ikbc', A, B)
```

CyEinsum's interface mirrors that of NumPy's `einsum` function, allowing for a familiar and user-friendly experience. The added advantage of C++ integration ensures that your tensor contractions are performed with optimal efficiency and speed.
