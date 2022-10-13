# Search Techniques

## Binary Search

> Normally binary search uses two pointers to move between elements.

### Two pointers

1. Sometimes you want to find the largest element from the given target.  
    * If that is the case and there is condition that you have to wrap.
    * you can get the first element using 
    ```java
        int ind = start % arr.length;
    ```
    * it is same as doing
    ```java
        if(start == arr.length){
            int ind = 0;
        }
    ```
1. Same as above but find the end in infinite array,
    ```java
        end = end + (end - start + 1) * 2;
    ```
    * same as,
    ```java
        end = end + (end * 2);
    ```

1. To find the middile element don't use ```start + end / 2```. Because some time the ```start + end``` go beyond the range of integer.
    * Instead use,
    ```java
        int mid = (start + (end - start))/2;
    ```


