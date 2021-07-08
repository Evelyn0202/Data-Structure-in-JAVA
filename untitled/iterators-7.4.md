---
description: （Data Structures and Algorithms in JAVA 6th Edition)
---

# Iterators 7.4

An **iterator** is a software design pattern that abstracts the process of scanning through a sequence of elements, one element at a time.

* `hasNext()`: Returns true if there is at least one additional element in the sequence, and false otherwise.
* `next()`: Returns the next element in the sequence.
* `remove()`: Removes from the collection the element returned by the most recent call to next\(\). Throws an IllegalStateException if next has not yet been called, or if remove was already called since the most recent call to next.
  * This method can be used to filter a collection of elements, for example to dis- card all negative numbers from a data set.
* `iterator()`: Returns an iterator of the elements in the collection.

As an example, the following loop can be used to remove all negative numbers from an ArrayList of floating-point values.

```text
ArrayList<Double> data; // populate with random numbers (not shown) Iterator<Double> walk = data.iterator();
while (walk.hasNext()){
    if (walk.next() < 0.0){
        walk.remove( );
    }
}
        
```

