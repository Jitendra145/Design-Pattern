1. Program to an **Interface** not an implementation.
   For example: In Plug Point/Wall Socket we really care about shape of pin that could fit into plug point not the wiring. So that is what it means 
   "Program to an **Interface** not an implementation.". 
 
 2. Think of the interface as the surface that a **unit** offers to the outside world.
 3. That **unit** could be a single class,but it could even be a collection of classes.
 4. Implementation is the guts -the inside-of that unit
 5. Never make assumptions about the guts of any unit.Ever
 ```
 public ArrayList<Integer> getList();
 ```
 above method in interface violates our design principle.**Don't do this**
 ```
 public List<Integer> getList();
 ```
 is correct way to declare a method.
 
 this principle is used across the multiple design pattern. Like decorator,iteratorr,adapter
