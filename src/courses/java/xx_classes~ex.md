> NB This file has a temporary name

# Class Exercises

## Implementing a Dynamic Array

As we know, Arrays are of fixed length. This is due to the fact that they are pre-allocated in memory when instantiated. To fix this, we can create our own dynamic array which doubles in size every time its full by redeclaring the array.

### Create a Dynamic Array Class (easy version)

Create a class with the following methods:

```java
/**
 * This class describes a dynamic list
 */
public class DynamicArray {
  /**
   * Get element at position index
   */
  public T get(int index) {

  }
  /**
   * Insert element after last element
   */
  public void add(T element) {

  }
  /**
   * Insert element at index position
   */
  public void addAt(T element, int index) {

  }
  /**
   * Remove the last element
   */
  public T remove() {

  }
  /**
   * Remove element at index position
   */
  public T removeAt(int index) {

  }
}
```

### Create an ArrayList Class w/ Generics

Create a class that implements the following interface:

```java
/**
 * This interface describes a dynamic list
 */
interface DynamicList<T> {
  /**
   * Get element at position index
   */
  public T get(int index);
  /**
   * Insert element after last element
   */
  public void add(T element);
  /**
   * Insert element at index position
   */
  public void addAt(T element, int index);
  /**
   * Remove the last element
   */
  public T remove();
  /**
   * Remove element at index position
   */
  public T removeAt(int index);
}
```
