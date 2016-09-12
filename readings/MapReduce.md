# MapReduce
## Introduction
Map reduce is a _programming model_ which specifies an implementation for processing and generating large datasets. The name is inspired by the map and reduce primitives found in Lisp.

MapReduce hides the messy details of parallelization, fault-tolerance, data distribution, and load balancing through a library. Through this, programmers without any experience with parallel and distributed systems can utilize the resources of a large distributed system.

## The Model
The model can be expressed as a system which takes as input key/value pairs and produces key/value pairs. The output key/value pairs are produced via two user-defined functions, map and reduce. The map function takes the input to the system and produces a set of _intermediate_ key/value pairs. The set of intermediate key/value pairs are sorted by key and made available as input to the reduce function via an iterator. For each key in the intermediate pairs, the reduce function merges the values together. Since an iterator is used to supply the values to the reduce function, the system can handle value lists that are too large to fit in memory.

#### Note on Data Types
 The input keys and values are drawn from a different domain than the output keys and values. The intermediate keys and values are from the same domain as the output keys and values.

 ### Examples of MapReduce Programs
 * Word counting
 * Distributed Grep
 * Count of URL access frequency
 * Reverse Web-Link Graph
 * Term-Vector per Host
 * Inverted Index
 * Distributed Sort
 
