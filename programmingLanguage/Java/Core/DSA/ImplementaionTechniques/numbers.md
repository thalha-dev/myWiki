# NUMBERS

### To get the last digit of a number

```java
int num = 34235;
int l = num % 10;
System.out.println(l);
```

### To get rid of the last digit of a number

```java
int num = 34235;
int rest = num / 10;
System.out.println(rest);
```

### To check that the number has only one digit

```java
int num = 34235;
boolean r = (num % 10) == num;
System.out.println(r);
```
