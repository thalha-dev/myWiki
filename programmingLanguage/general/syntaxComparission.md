# PROGRAMMING LANGUAGE COMPARISON 

### HELLO WORLD

#### JAVA

```java

public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}

```

#### C++

```c++ 
#include <iostream>
    using namespace std;

    int main() {
      cout << "Hello World!";
      return 0;
    }
```
---

### OUTPUT

#### JAVA

```java 
System.out.println("Hello World!");
```

#### C++

```c++ 
cout << "Hello World!";
```
---

### COMMENTS

#### JAVA

```java 
System.out.println("Hello World"); // This is a comment
/* The code below will print the words Hello World
to the screen, and it is amazing */
System.out.println("Hello World");
```

#### C++

```c++ 
cout << "Hello World!"; // This is a comment
/* The code below will print the words Hello World!
to the screen, and it is amazing */
cout << "Hello World!";
```
---

### VARIABLES

#### JAVA

```java 
int myNum;
myNum = 15;
System.out.println(myNum);
```

#### C++

```c++ 
int myNum = 15;  // myNum is 15
myNum = 10;  // Now myNum is 10
cout << myNum;  // Outputs 10
```
---

### DATA TYPES

#### JAVA

```java 
int myNum = 5;               // Integer (whole number)
float myFloatNum = 5.99f;    // Floating point number
char myLetter = 'D';         // Character
boolean myBool = true;       // Boolean
String myText = "Hello";     // String
```

#### C++

```c++ 
int myNum = 5;               // Integer (whole number)
float myFloatNum = 5.99;     // Floating point number
double myDoubleNum = 9.98;   // Floating point number
char myLetter = 'D';         // Character
bool myBoolean = true;       // Boolean
string myText = "Hello";     // String
```
---


### IF ELSE

#### JAVA

```java 
int time = 22;
if (time < 10) {
  System.out.println("Good morning.");
} else if (time < 20) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening."

int time = 20;
String result = (time < 18) ? "Good day." : "Good evening.";
System.out.println(result);

```

#### C++

```c++ 
int time = 22;
if (time < 10) {
  cout << "Good morning.";
} else if (time < 20) {
  cout << "Good day.";
} else {
  cout << "Good evening.";
}
// Outputs "Good evening."

int time = 20;
string result = (time < 18) ? "Good day." : "Good evening.";
cout << result;
```
---


### SWITCH

#### JAVA

```java 
int day = 4;
switch (day) {
  case 6:
    System.out.println("Today is Saturday");
    break;
  case 7:
    System.out.println("Today is Sunday");
    break;
  default:
    System.out.println("Looking forward to the Weekend");
}
// Outputs "Looking forward to the Weekend"

```

#### C++

```c++ 
int day = 4;
switch (day) {
  case 6:
    cout << "Today is Saturday";
    break;
  case 7:
    cout << "Today is Sunday";
    break;
  default:
    cout << "Looking forward to the Weekend";
}
// Outputs "Looking forward to the Weekend"
```
---

### WHILE LOOP

#### JAVA

```java 
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
```

#### C++

```c++ 
int i = 0;
while (i < 5) {
  cout << i << "\n";
  i++;
}
```
---

### DO WHILE LOOP

#### JAVA

```java 
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
```

#### C++

```c++ 
int i = 0;
do {
  cout << i << "\n";
  i++;
}
while (i < 5);
```
---

### FOR LOOP

#### JAVA

```java 
-- NORMAL FOR LOOP
for (int i = 0; i < 5; i++) {
  System.out.println(i);
}

-- FOR EACH LOOP
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```

#### C++

```c++ 
for (int i = 0; i < 5; i++) {
  cout << i << "\n";
}
```
---

### ARRAYS

#### JAVA

```java 
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
System.out.println(cars[0]);
// Now outputs Opel instead of Volvo

-- length
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars.length);
```

#### C++

```c++ 
string cars[4] = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
cout << cars[0];
// Now outputs Opel instead of Volvo

You don't have to specify the size of the array. But if you don't,
it will only be as big as the elements that are inserted into it:

-- length
int myNumbers[5] = {10, 20, 30, 40, 50};
int getArrayLength = sizeof(myNumbers) / sizeof(int);
cout << getArrayLength;
```
---

### STRUCTRUE

#### C++

```c++ 
// Create a structure variable called myStructure
struct {
  int myNum;
  string myString;
} myStructure, my2, my3;

// Assign values to members of myStructure using "." (dot) operator
myStructure.myNum = 1;
myStructure.myString = "Hello World!";

// Print members of myStructure
cout << myStructure.myNum << "\n";
cout << myStructure.myString << "\n";

// NAMED STRUCTURE

// Declare a structure named "car"
struct car {
  string brand;
  string model;
  int year;
};

int main() {
  // Create a car structure and store it in myCar1;
  car myCar1;
  myCar1.year = 1999;

  // Create another car structure and store it in myCar2;
  car myCar2;
  myCar2.year = 1969;
 
  // Print the structure members
  cout << myCar1.year << "\n";
  cout << myCar2.year << "\n";
 
  return 0;
}
```
---

### REFERENCE

#### C++
```c++
// using & symbol, '&var' get the memory address of the variable 'var'
string food = "Pizza";
string &meal = food;

cout << food << "\n";  // Outputs Pizza
cout << meal << "\n";  // Outputs Pizza
```
---

### POINTER

#### C++
```c++
// CREATING POINTER

string food = "Pizza";  // A food variable of type string
string* ptr = &food;    // A pointer variable, with the name ptr, that stores the address of food

// Output the value of food (Pizza)
cout << food << "\n";

// Output the memory address of food (0x6dfed4)
cout << &food << "\n";

// Output the memory address of food with the pointer (0x6dfed4)
cout << ptr << "\n";

// DEREFERENCING

// Dereference: Output the value of food with the pointer (Pizza)
cout << *ptr << "\n";

// MODIFY

// Change the value of the pointer
*ptr = "Hamburger";

```
---

### FUNCTIONS

#### JAVA

```java
public class Main {
  static void myMethod(String fname, int age) {
    System.out.println(fname + " is " + age);
  }

  public static void main(String[] args) {
    myMethod("Liam", 5);
  }
}
```

#### C++

```c++ 
void myFunction(string fname); // or declare and define below main

int main() {
  myFunction("Liam");
  return 0;
}

void myFunction(string fname) {
  cout << fname << " Refsnes\n";
}
```
---

### FUNCTIONS OVERLOADING

#### JAVA

```java
static int plusMethod(int x, int y) {
  return x + y;
}

static double plusMethod(double x, double y) {
  return x + y;
}

public static void main(String[] args) {
  int myNum1 = plusMethod(8, 5);
  double myNum2 = plusMethod(4.3, 6.26);
  System.out.println("int: " + myNum1);
  System.out.println("double: " + myNum2);
}
```

#### C++

```c++ 
int plusFunc(int x, int y) {
  return x + y;
}

double plusFunc(double x, double y) {
  return x + y;
}

int main() {
  int myNum1 = plusFunc(8, 5);
  double myNum2 = plusFunc(4.3, 6.26);
  cout << "Int: " << myNum1 << "\n";
  cout << "Double: " << myNum2;
  return 0;
}
```
---

### RECURSION

#### JAVA

```java
public class Main {
  public static void main(String[] args) {
    int result = sum(5, 10);
    System.out.println(result);
  }
  public static int sum(int start, int end) {
    if (end > start) {
      return end + sum(start, end - 1);
    } else {
      return end;
    }
  }
}
```

#### C++

```c++ 
int sum(int k) {
  if (k > 0) {
    return k + sum(k - 1);
  } else {
    return 0;
  }
}

int main() {
  int result = sum(10);
  cout << result;
  return 0;
}
```
### OOPS


#### JAVA

```java
// creating class and object
// -----------------

public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}

// METHODS
// ----------

// Create a Main class
public class Main {
 
  // Create a fullThrottle() method
  public void fullThrottle() {
    System.out.println("The car is going as fast as it can!");
  }

  // Create a speed() method and add a parameter
  public void speed(int maxSpeed) {
    System.out.println("Max speed is: " + maxSpeed);
  }

  // Inside main, call the methods on the myCar object
  public static void main(String[] args) {
    Main myCar = new Main();   // Create a myCar object
    myCar.fullThrottle();      // Call the fullThrottle() method
    myCar.speed(200);          // Call the speed() method
  }
}


// CONSTRUCTOR
// ----------

public class Main {
  int modelYear;
  String modelName;

  public Main(int year, String name) {
    modelYear = year;
    modelName = name;
  }

  public static void main(String[] args) {
    Main myCar = new Main(1969, "Mustang");
    System.out.println(myCar.modelYear + " " + myCar.modelName);
  }
}

// ACCESS MODIFIEERS

//Access Modifiers
// For classes, you can use either public or default:
// public	The class is accessible by any other class	
// default	The class is only accessible by classes in the same package. This is used when you don't specify a modifier. 

// For attributes, methods and constructors, you can use the one of the following:
// public	The code is accessible for all classes	
// private	The code is only accessible within the declared class	
// default	The code is only accessible in the same package. This is used when you don't specify a modifier. 
// protected	The code is accessible in the same package and subclasses. 

// Non-Access Modifiers

// For classes, you can use either final or abstract:
// final	The class cannot be inherited by other classes 
// abstract	The class cannot be used to create objects (To access an abstract class, it must be inherited from another class. 
//For attributes and methods, you can use the one of the following:
// final	Attributes and methods cannot be overridden/modified
// static	Attributes and methods belongs to the class, rather than an object
// abstract	Can only be used in an abstract class, and can only be used on methods. The method does not have a body, for example abstract void run();. The body is provided by the subclass (inherited from). 
// transient	Attributes and methods are skipped when serializing the object containing them
// synchronized	Methods can only be accessed by one thread at a time
// volatile	The value of an attribute is not cached thread-locally, and is always read from the "main memory"


```

#### C++

```c++ 
// creating class and object
// -----------------

class MyClass {       // The class
  public:             // Access specifier
    int myNum;        // Attribute (int variable)
    string myString;  // Attribute (string variable)
};

int main() {
  MyClass myObj;  // Create an object of MyClass

  // Access attributes and set values
  myObj.myNum = 15; 
  myObj.myString = "Some text";

  // Print attribute values
  cout << myObj.myNum << "\n";
  cout << myObj.myString;
  return 0;
}

// METHODS
// -----------------

// inside class
class MyClass {        // The class
  public:              // Access specifier
    void myMethod() {  // Method/function defined inside the class
      cout << "Hello World!";
    }
};

int main() {
  MyClass myObj;     // Create an object of MyClass
  myObj.myMethod();  // Call the method
  return 0;
}

// outside class
// -----------------

class MyClass {        // The class
  public:              // Access specifier
    void myMethod();   // Method/function declaration
};

// Method/function definition outside the class
void MyClass::myMethod() {
  cout << "Hello World!";
}

int main() {
  MyClass myObj;     // Create an object of MyClass
  myObj.myMethod();  // Call the method
  return 0;
}

// CONSTRUCTOR
// ------------

class Car {        // The class
  public:          // Access specifier
    string brand;  // Attribute
    string model;  // Attribute
    int year;      // Attribute
    Car(string x, string y, int z) { // Constructor with parameters
      brand = x;
      model = y;
      year = z;
    }
};

int main() {
  // Create Car objects and call the constructor with different values
  Car carObj1("BMW", "X5", 1999);
  Car carObj2("Ford", "Mustang", 1969);

  // Print values
  cout << carObj1.brand << " " << carObj1.model << " " << carObj1.year << "\n";
  cout << carObj2.brand << " " << carObj2.model << " " << carObj2.year << "\n";
  return 0;
}

// ACCESS SPECIFIER
//    In C++, there are three access specifiers:
//
// public - members are accessible from outside the class
// private - members cannot be accessed (or viewed) from outside the class
// protected - members cannot be accessed from outside the class, however, 
//             they can be accessed in inherited classes.
```
