In code often we have objective.So algorithm to achieve the objective can be determined during runtime. We can achieve our objective in many way and we can plugin our algorithm
any one of them during runtime.

**UseCase:** Sort the list of String. There are many ways in which we can sort the Strings.

1. In Lexicographical Order
2. In reverse Lexicographical Order
3. Ignore Case
4. Not Ignoring Case
5. Or in custom order -  For instance where "Donald Trump" Always Comes First

**Can Be ignored: Start Here** 
1. Create a bunch of algorithm object
2. Each of which implements the Comparator<String> inteface
3. Each object which implements this interface has a method (int compare(String s1,String s2)) which determine which string comes first
4. Each algorithm object can specify its own logic to determine this order
5. Once you have these algorithm objects ready pass any one of them into Collection.sorts(List<String>,Comparator<String> comparator) method of Collections class

**End Here**

# Strategy Pattern
The strategy Pattern is used to specify a behavior (How to sort here) on the fly( when user select a sort method from UI/during runtime) 
by passing algorithm objects in as member variables.

Algorithm objects are passed as member variable into a function which allows us to sort
**Memeber variable:**
1. It is defining characteristic of the strategy pattern that it uses composition (member variable) over inheritance (interfaces or abstract classes) in the class being modified
2. It is also a defining characteristic that the algorithm objects implement a standard interface.

These two defining characteristics make the strategy pattern closely  related to
1. The "Command pattern" --> which involves defining algirithm as objects
2. "Dependency Injection" --> set member variables of object on the fly(during runtime)

# Implementing the Strategy Design Pattern
```
List<String> listOfStrings = new ArrayList<>();
// add multiple Strings

Collections.sort(listOfStrings, new Comparator<String>(){
    
    public int compare(String s1,String s2){
        if(s1.equals("Donald Trump") && !s2.equals("Donald Trump"){
          return 1;
        }
        else if(s2.equals("Donald Trump") && !s1.equals("Donald Trump"){
          return -1;
        }      
         return s1.compareTo(s2);       
       }    
   });
```

The above logic is sort the list of String Lexicographically but if String "Donald Trump" came then it must be first String.

1. Create and instantiate a class that implements the Comparator<String> interface in single line
2. Comparator<String> interface has one member function that needs to be implemented
3. Then pass the object of this class(implemented class) right into the Collections.sort() method
4. We can create as many different Comparator object  as we like each defining a different sort algorithm - and use them all on fly(during runtime)

