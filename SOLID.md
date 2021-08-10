# SOLID

### Single responsibility (SRP)
- Each class should have a **unique objective** or should be **useful for a specific case**. Any logic that is not part of the objective of the class should be the responsibility of some other class. A class that has lots of responsibilities is sometimes called a god class and should be avoided.

### Open-closed
- The software entities of your app: classes, methods, etc. should be open for extension but closed for modification. This means that you should design them in such a way that adding new features or modifying behavior shouldn’t require you to modify too much of your existing code but instead add new code or create new classes.

### Liskov substitution
- Also called **design by contract**, it states that an app that uses an object of a base class should be able to use objects of derived classes without knowing about that and continue working. Therefore, your code should not be checking the subtype. In the subclass you can override some of the parent methods as long as you continue to comply with its semantics and maintain the expected behavior.

### Interface segregation
- This principle encourages you to create fine grained interfaces that are client specific. Clients should have access to only what they need and nothing more.

### Dependency inversion
- This principle states that a concrete class A should not depend on a concrete class B, but an abstraction of B instead. This abstraction could be an interface or an abstract class.