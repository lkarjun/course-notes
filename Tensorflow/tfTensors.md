# Tensorflow Basis

## Tensors and Variables
---
* Tensors are essentially like multidimentional array. 
* Tensors are stored and processed in multiple devices, either cpu's or gpu's
* tf.debugging.set_log_devices_placement(True)
  * This will print out additional log messages, that is where are tensors are located and operations are executed.

* tf.executing_eagerly()
  * execution mode.

* tf.constant(3) > scalar value.

* tf.constant --> arithmetic operations
  * tf.add()
  * tf.sub()

* tensors are immutable;

* tf.cast --> change the datatype

* can perform numpy operations in tensors.
  * numpy operation is not part of the tensorflow computational graph

* tf.is_tensor() -> check tenor or not

* tf.reshape() -> reshape tensor...

---