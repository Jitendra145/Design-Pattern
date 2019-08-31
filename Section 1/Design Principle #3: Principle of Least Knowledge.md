# The principle of least knowledge aka Demeter's Law
1. Only talk to friends don't talk to strangers
2. In any class you write, only make method call to **Friends**
3. Objects passed in as parameters to methods of your classes
4. Objects created inside your class (including member variables)
5. Code you write should never include multiple "." operators in the same function call. For e.g below code violate the design this principle

```
int pageNumber = document.getCurrentPage().getPageNumber();//violate the design pattern principle
int pageNumber = document.getCurrentPageNumber();//folloe the design pattern's principle
```

## Interface Blot: 
In the above e.g if we don't have **currentPageNumber()** method, and still we stick to this principle(i.e we don't want to use )
class **getCurrentPage().getPageNumber**, then this will lead **Interface Blot**.
