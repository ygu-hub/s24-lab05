# Inheritance and Delegation

This repository is set up for discussion on relative strengths and weaknesses of 
`inheritance` and `delegation`.

Lab05 Handout can be found at: [https://github.com/CMU-17-214/s2024/blob/main/labs/lab05.md](https://github.com/CMU-17-214/s2024/blob/main/labs/lab05.md)


Inheritance promotes code reusability by letting the child class inherits member variables and methods from the parent class, without having to overwrite all the super methods from interface, like what composition needs to do.

Composition promotes lower coupling by simpling composing a SortedIntList object, without inheriting from another class, to override method by adding extra decoration codes besides calling on the import object's source method. Also, in order to be a IntegerList object, composition requires to implement the interface and rewrite all the parent abstract methods.

1. Inheritance. Composition can choose to overwrite the whole method by looking at API of interface IntegerList.java/
2. Composition. Because it is more independent on the implementation details of SortedIntList and so it may turn out breaking due to changes in SortedIntList.
3. High coupling. Get rid of inheritance but use decoration pattern.
4. When the class have high coupling currently or its interface does not contain too much method to override or both happen concurrently, we prefer to use Composition. 
When the class have low coupling currently and adopting the interface may contain too much redundent code for the subclass to override, then we prefer to choose Inheritance.
