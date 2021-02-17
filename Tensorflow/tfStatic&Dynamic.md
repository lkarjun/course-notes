# Static and Dynamic computational Graph...

> Best Practice: Develop with dynamic, deploy with static

> Eager execution for fast feedback.

> tf.compat.v1.executing_eagerly()  --> checking executing eagerly or not.

## Static
---
* Symbolic programming of NNs
  * First define operations, then execute
       * First define computation, then run

  * Define functions abstractly, no actual computation takes place
       * computation first defined using placeholders

  * computation explicitly compiled before evaluation
       * computation explicitly compiled before evaluation.
       * results in static computation graph. 
  
  * Compilation converts the graph into executable format.





## Dynamic
---
* Eager Executino - Imperative programming to NNs

    * Execution performed as operations defined
       * Computation run as they are defined
        
    * Code actually executed as the function is defined
       * computation directly performed on real operands

    * No explicit compilation step before evaluation
       * No explicit compilation step before evaluation.

    * Results in dynamic computation graph. 
   

    * Graph already in executable format.

---
### Static
* We need to disable executing_eagerly() to perform static compution.
> tf.compat.v1.disable_eager_execution()
* then start a session to execute.
> sess = tf.compat.v1.Session()
> sess.run("computation")
```python
m = tf.Variable([4.0, 5.0, 6.0], tf.float32, name='m')
c = tf.Variable([1.0, 1.0, 1.0])
m
output =  <tf.Variable 'm:0' shape=(3,) dtype=float32>
```
> m, c value is not avaliable until the computation graph is executed.

> trainable parameters are variable. and inputs that you specified to a computation graph were represented as placeholder.

```python
tf.compat.v1.placeholder(tf.float32, shape=[3], name='x')
```

Initializing variables in Tensorflow v1 require a separate special operation.

```python
with tf.compat.v1.Session() as sess:
  sess.run(init)
  y_output = sess.run(y, feed_dict={x: [100.0, 100.0, 100.0]})

  print('Final result: mx + c = ', y_output)
  
  writer = tf.compat.v1.summary.FileWriter('./logs', sess.graph)
  writer.close()

  ```

