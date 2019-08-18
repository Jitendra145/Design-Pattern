This principle states that classes should be **open for extension** but **closed for modification**. According to this Principle

1. Once you've written a class,its done,never add anything to it after that.
2. No new member variables, no new methods,no new interfaces implemented
3. Classes are closed for modification but are open for extension. There are three mechanism which other classes can incorporate to use the classes which can't be modified.
   These mechanisms are 1. Inheritance 2. Delegation, 3. Composition
   
   **A) Inheritance:** If you structure your code into abstract base classes,others can find new ways to use it via inheritance. **e.g.** Template Pattern 
   
   **B) Delegation:** If you write classes that fire event and expose properties,other code can listen in, and use your code via delegation. **e.g.** Observer,MVC, Chain of responsibility
   
   **C) Composition:** If you take in member variables to determine behaviour,you allow extension via Composition. **e.g.** Strategy Pattern
