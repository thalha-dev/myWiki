# Binary Search 



>Binary search is an efficient algorithm for finding an item from a sorted list of items. It works by repeatedly dividing in half the portion of the list that could contain the item, until you've narrowed down the possible locations to just one.

```java

package com.module2.external.Search.BinarySearchDSA;

public class BinarySearch {

  static int binarySearch(int[] arr, int target) {

    int start = 0;
    int end = arr.length - 1;

    while (start <= end) {
      // int mid = start + end / 2;
      // start + end might exceed the range of integer
      int mid = start + (end - start) / 2;
      // this is better
      if (target < arr[mid]) {
        end = mid - 1;
      } else if (target > arr[mid]) {
        start = mid + 1;
      } else {
        return mid;
      }
    }
    return -1;
  }

  public static void main(String[] args) {
    int[] arr = {
      2, 3, 4, 5, 6, 12, 19, 21, 27, 38, 48, 55,
    };
    int ans = binarySearch(arr, 5);
    System.out.println(ans);
  }
}

```

#### Technique

```java
      // int mid = start + end / 2;
      // start + end might exceed the range of integer
      int mid = start + (end - start) / 2;
      // this is better
```
if you solve the equation it turns out to ```mid = start + end```


## Order Agnostic Binary Search

```java

package com.module2.external.Search.BinarySearchDSA;

public class OrderAgnosticBiSearch {

  static int binarySearch(int[] arr, int target) {

    int start = 0;
    int end = arr.length - 1;
    boolean isAsc = arr[start] < arr[end];

    while (start <= end) {
      int mid = start + (end - start) / 2;
      if (arr[mid] == target) {
        return mid;
      }
      if (isAsc) {
        if (target < arr[mid]) {
          end = mid - 1;
        } else if (target > arr[mid]) {
          start = mid + 1;
        } else {
          return mid;
        }
      } else {
        if (target > arr[mid]) {
          end = mid - 1;
        } else if (target < arr[mid]) {
          start = mid + 1;
        } else {
          return mid;
        }
      }
    }
    return -1;
  }

  public static void main(String[] args) {
    int[] arr = {
      2, 3, 4, 5, 6, 12, 19, 21, 27, 38, 48, 55,
    };
    int ans = binarySearch(arr, 5);
    System.out.println(ans);
  }
}
```



