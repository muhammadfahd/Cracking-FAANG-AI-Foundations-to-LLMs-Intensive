# W1 Day 4: Math for Machine Learning – Linear Algebra

### Overview  
Linear Algebra forms the mathematical foundation of Machine Learning.  
It provides the language and tools for representing data, transformations, and computations efficiently.

---
- [W1 Day 4: Math for Machine Learning – Linear Algebra](#w1-day-4-math-for-machine-learning--linear-algebra)
    - [Overview](#overview)
    - [🔢 Core Concepts](#-core-concepts)
      - [Vectors](#vectors)
      - [🧮 Matrices](#-matrices)
    - [Application in Machine Learning](#application-in-machine-learning)
    - [Using NumPy in Python](#using-numpy-in-python)
  - [Real-Life Applications](#real-life-applications)
  - [Key Takeaways](#key-takeaways)



### 🔢 Core Concepts

#### Vectors  
- Represent data points, directions, or features.  
- Can be visualized as arrows in space or as arrays of numbers.  

**Operations:**
- **Addition / Subtraction:** Combine or compare vectors.  
- **Scaling:** Adjust vector magnitude using scalar multiplication.  
- **Dot Product:**  
  - Fundamental in **Neural Networks** and **SVMs**.  
  - Measures **similarity** between two vectors.  

---

#### 🧮 Matrices  
- A **rectangular array** of numbers arranged in **rows** and **columns**.  
- Represent datasets, transformations, or relationships between features.

**Matrix Multiplication:**  
- Combines multiple vectors.  
- Crucial for linear transformations and neural network weight computations.  
- Formula:  
  \[
  C = A \times B
  \]
  where element \( C_{ij} = \sum_k A_{ik} \times B_{kj} \)

---

### Application in Machine Learning

| Concept | ML Use Case |
|----------|--------------|
| **Vectors** | Represent features or input data |
| **Dot Product** | Compute similarity, cosine similarity, projections |
| **Matrices** | Store datasets, represent model weights |
| **Matrix Multiplication** | Feedforward operations in neural networks |
| **NumPy** | Efficient implementation of vectorized operations |

---

### Using NumPy in Python

```python
import numpy as np

# Vector
v1 = np.array([2, 3])
v2 = np.array([1, 4])

# Dot Product
dot = np.dot(v1, v2)
print("Dot Product:", dot)

# Matrix Multiplication
A = np.array([[1, 2], [3, 4]])
B = np.array([[2, 0], [1, 3]])
C = np.dot(A, B)

```
## Real-Life Applications

* **Recommendation Systems**: Compute similarity between users/items.
* **Neural Networks**: Represent weights, activations, and layers as matrices.

* **Data Representation**: Model complex relationships using vector spaces.

* **Computer Graphics**: Apply transformations like rotation and scaling.

* **Genomics & NLP**: Represent DNA sequences or word embeddings as vectors.


## Key Takeaways

* Vectors, dot products, and matrices form the core of ML computation.

* Understanding Linear Algebra improves interpretability and debugging in ML.

* NumPy simplifies complex linear operations, making ML implementation efficient.
