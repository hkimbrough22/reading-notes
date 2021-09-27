# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 06 -->
## Inheritance and Interfaces
[comment]: <> (https://docs.oracle.com/javase/tutorial/java/concepts/)

[comment]: <> (https://docs.oracle.com/javase/tutorial/java/IandI/index.html)
### Inheritance
- Object-oriented programming allows classes to inherit commonly used state and behavior from other classes.
- The syntax for creating a subclass is simple. At the beginning of your class declaration, use the extends keyword, followed by the name of the class to inherit from:
```Java
class MountainBike extends Bicycle {
    // new fields and methods defining 
    // a mountain bike would go here
}
```

### Interfaces
- Implementing an interface allows a class to become more formal about the behavior it promises to provide. 
- Interfaces form a contract between the class and the outside world, and this contract is enforced at build time by the compiler. 
- If your class claims to implement an interface, all methods defined by that interface must appear in its source code before the class will successfully compile.
 ```Java
interface Bicycle {

  //  wheel revolutions per minute
  void changeCadence(int newValue);

  void changeGear(int newValue);

  void speedUp(int increment);

  void applyBrakes(int decrement);
  }
``` 
To implement this interface, the name of your class would change, and you'd use the `implements` keyword in the class declaration:
```Java

class ACMEBicycle implements Bicycle {

    int cadence = 0;
    int speed = 0;
    int gear = 1;

// The compiler will now require that methods
// changeCadence, changeGear, speedUp, and applyBrakes
// all be implemented. Compilation will fail if those
// methods are missing from this class.

    void changeCadence(int newValue) {
         cadence = newValue;
    }

    void changeGear(int newValue) {
         gear = newValue;
    }

    void speedUp(int increment) {
         speed = speed + increment;   
    }

    void applyBrakes(int decrement) {
         speed = speed - decrement;
    }

    void printStates() {
         System.out.println("cadence:" +
             cadence + " speed:" + 
             speed + " gear:" + gear);
    }
}
```

[BACK TO HOME](../README.md)
