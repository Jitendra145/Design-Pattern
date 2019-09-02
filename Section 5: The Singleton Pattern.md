# What is a Singleton?
1. There are situations where exactly one object of a particular type is needed.
2. Where it would be bad to have any more than one object of a particular class.
3. Device drivers, registry setting managers or other system-wide shared objects are classic examples
4. Singleton object also makes sense where the state of an object consumes a lot of memory and just one version of that state is sufficient for the entire application

In such situations, a standard and widely used way of achieving this is via **The Singleton Pattern**

A Singleton object must satisfy two attributes:
1. Exactly one (at most one) instance of the object should exist.
2. Everyone ought to be able to access that one singleton object

**It is surprisingly difficult to gaurantee that an object is instantiated exactly once.**

**That means that the object needs to be globally accessible.**

```
public class Singleton
{
  // A static private member variable t o hold the singleton
	private static Singleton singleton;
  
	private Singleton(){
		// The constructor of Singleton must be private 
    //So that nobody outside this class can instantiate
	}
  
	 //A static getter method which instantiates 
   //the singleton the first time it is called.
   // the method must be marked synchronized , else
   //it is possible that 2 different threads might
   //enter this method simultaneously and create
   // more than 1 instance of object
	public static synchronized Singleton getInstance(){
		if(singleton==null){
   
			singleton = new Singleton();
		}
		return singleton;
	}
}
```
