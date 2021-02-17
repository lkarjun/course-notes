# Variables

> Variables are the recommended way to share persistent.

* Variables are mutable container in tensorflow.

* tf.Variables() 
```python
v1 = tf.Variable([[1.5, 2, 5], [2, 6, 8]])
v1
```
> <tf.Variable 'Variable:0' shape=(2, 3) dtype=float32, numpy=array([[1.5, 2. , 5. ],[2. , 6. , 8. ]], dtype=float32)>

* tf.Variable don't share memory.

* Variable.assign([323]) -> assigning new values
```python
v1.assign([[10, 20, 30], [40, 50, 60]])
v1
```
> <tf.Variable 'Variable:0' shape=(2, 3) dtype=float32, numpy=array([[10, 20, 30], [40, 50, 60]], dtype=float32)>

* variable.assign_add([323]) -> add 323 without changing old values
```python
v1.assign_add([[1, 1, 1], [1, 1, 1]])
v1
```
> <tf.Variable 'Variable:0' shape=(2, 3) dtype=float32, numpy=array([[11.,  21.,  31.],[ 41.,  51.,  61.]], dtype=float32)>