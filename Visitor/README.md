#   Visitor Design Pattern


##  What is the Visitor Design Pattern
>   The intent of the Visitor Design Pattern is to represent an operation to be performed on the elements of an object structure. Visitor
    lets you define a new operation without changing the classes of the elements on which it operates.
    
>   The Visitor pattern is useful when designing an operation across a heterogeneous collection of objects of a class hierarchy. The
    Visitor pattern allows the operation to be defined without changing the class of any of the objects in the collection. To accomplish
    this, the Visitor pattern suggests defining the operation in a separate class referred to as a visitor class.
    
![UML diagram](https://github.com/11andrew1991/design_patterns/blob/master/Visitor/img/visitor.PNG)


### Visitor
-   Declares a Visit operation for each class of ConcreteElement in the object structure. The operation’s name and signature
    identifies the class that sends the Visit request to the visitor. That lets the visitor determine the concrete class of the
    element being visited. Then the visitor can access the element directly through its particular interface.

### ConcreteVisitor
-   Implements each operation declared by Visitor. Each operation implements a fragment of the algorithm defined for the
    corresponding class of object in the structure. ConcreteVisitor provides the context for the algorithm and stores its local
    state. This state often accumulates results during the traversal of the structure.

### Element
-   Defines an Accept operation that takes a visitor as an argument.

### ConcreteElement
-   Implements an Accept operation that takes a visitor as an argument.

### ObjectStructure
-   Can enumerate its elements.
-   May provide a high-level interface to allow the visitor to visit its elements.
-   May either be a composite or a collection such as a list or a set.