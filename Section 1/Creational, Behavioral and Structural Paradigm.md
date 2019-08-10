# Creational, Behavioral and Structural Paradigm
Design patterns are often classified into three categories
1. Behavioral 
2. Structural
3. Creational

## Creational Design Pattern
1. Creational patterns relate to how objects are constructed
2. They usually seek to decouple the construction of an object from its use
3. Hide the implementation of an object, only reveal its interface
4. Defer instantiation until run-time (try to instantiate the object possibly at last minute)
5. Have families of related objects that must be used together
6. Only allow creation of a finit number of instances

**All the above features are implemented by one or more than one design pattern**

|   Behavioral   |  Structural    |
|:--------------:|:--------------:|
| How do **Objects of a class** behave and interact with each other? |How do **classess** beahave and interact with each other?|
 
 **Other definition:**
 Let's say a design pattern relates to some entities (usually classess).
 
 All these entities together constitute **a logical unit**
 
 |   Behavioral   |  Structural    |
 |:--------------:|:--------------:|
 | If the pattern governs **how the logical unit as a whole interacts with the outside world**, its a Behavioral Pattern |If the pattern governs **how classes within the logical unit interact with each other**, its a Structural Pattern |
 
 In the sense Behavioral patters are interface and Structural Patterns are implementation.
 
 (Logical unit may or may contains one or more than one class)
 
 **Behavioral Pattern Example:-**
 
 Consider the Iterator Pattern. The **Logical unit** contains just 1 class, the Iterator class.
 
 This pattern governs how the iterator is **used by the client (the outside world)**
 
 So,Iterator is a behavioral Pattern
 
 **Structural Pattern Example:-**
 
 Consider the MVC paradigm. The **Logical Unit** contains 3 classes, the Model, the View and the Controller.
 
 This pattern **governs how the Model, the View and the Controller** interact with each other.
 
 So, MVC paradigm is a Structural Pattern
