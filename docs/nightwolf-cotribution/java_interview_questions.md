# Top 100 Java Interview Questions & Answers 


---
  We have prepared a set of frequently asked Core Java interview questions to help Freshers and Experienced Java developers in their preparations for Interview.

  You will find these questions very helpful in your Java/OOPs interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

---

 {!inpage-ads.md!}

1. What is the difference between an Inner Class and a Sub-Class?

        Ans: An Inner class isa class which is nested within another class. An Inner class has access rights for
        the class which is nesting it and it can access all variables and methods defined in the outer class.
        A sub-class is a class which inherits from another class called super class. Sub-class can access all
        public and protected methods and fields of its super class.

2. What are the various access specifiers for Java classes?

        Ans: In Java, access specifiers are the keywords used before a class name which defines the access scope.
        The types of access specifiers for classes are:
          1. Public: Class, Method, Field is accessible from anywhere.
          2. Protected:Method, Field can be accessed from the same class to which they belong or from the
             sub-classes,and from the class of same package, but not from outside
          3. Default: Method, Field,class can be accessed only from the same package and not from outside
             of it's native package.
          4. Private: Method, Field can be accessed from the same class to which they belong8.

3. What's the purpose of Static methods and static variables?

        Ans: When there is a requirement to share a method or a variable between multiple objects of a class
        instead of creating separate copies for each object, we use static keyword to make a method or variable
        shared for all objects.

4. What is data encapsulation and what's its significance?

        Ans: Encapsulation is a concept in Object Oriented Programming for combining properties and methods in a
        single unit. Encapsulation helps programmers to follow a modular approach for software development as
        each object has its own set of methods and variables and serves its functions independent of other objects.
        Encapsulation also serves data hiding purpose.

5. What is a singleton class? Give a practical example of its usage.

        A singleton class in java can have only one instance and hence all its methods and variables belong to just
        one instance. Singleton class concept is useful for the situations when there is a need to limit the number
        of objects for a class. 
        The best example of singleton usage scenario is when there is a limit of having only one connection to a
        database due to some driver limitations or because of any licensing issues. 

6. What are Loops in Java? What are three types of loops?

        Ans: Looping is used in programming to execute a statement or a block of statement repeatedly. 

        There are three types of loops in Java:
          1) For Loops : For loops are used in java to execute statements repeatedly for a given number of times.
                         For loops are used when number of times to execute the statements is known to programmer.

          2) While Loops: While loop is used when certain statements need to be executed repeatedly until a condition
                          is fulfilled. In while loops, condition is checked first before execution of statements.

          3) Do While Loops: Do While Loop is same as While loop with only difference that condition is checked
                             after execution of block of statements. Hence in case of do while loop, statements are
                             executed at least once.

7. What is an infinite Loop? How infinite loop is declared?

        Ans: An infinite loop runs without any condition and runs infinitely. An infinite loop can be broken by
        definingg any breaking logic in the body of the statement blocks.

        Infinite loop is declared as follows:

          for (;;) {

          //Statements to execute

          // Add any loop breaking logic

          }

8. What is the difference between continue and break statement?

        Ans: break and continue are two important keywords used in Loops. When a break keyword is used in a loop,
        loop is broken instantly while when continue keyword is used, current iteration is broken and loop continues
        with next iteration.

        In below example, Loop is broken when counter reaches 4.

        for (counter-0;counter<10;counter+){
          system.out.println(counter);
          if (counter == 4){
            break;}
        }

        In the below example when counter reaches 4, loop jumps to next iteration and any statements after the 
        continue keyword are skipped for current iteration.

        for (counter=0;counter<10;counter++) {
          system.out.printin(counter);
          if (counter==4){
            continue;
            }
          system.out.println("This will not get printed when counter is 4");
        }

9. What is the difference between double and float variables in Java?

        Ans: In java, float takes 4 bytes in memory while Double takes 8 bytes in memory. Float is single precision
        floating point decimal number while Double is double precision decimal number.

10. What is Final Keyword in Java? Give an example.

        Ans: In java, a constant is declared using the keyword Final. Value can be assigned only once and after
        assignment, value of a constant can't be changed.

        In below example, a constant with the name const_val is declared and assigned avalue:
          private final int const_val=100

        When a method is declared as final,it can NOT be overridden by the subclasses.This method are faster than
        any other method,because they are resolved at complied time.
        When a class is declares as final,it cannot be subclassed. Example String,Integer and other wrapper classes. 

11. What is ternary operator? Give an example.

        Ans: Ternary operator, also called conditional operator is used to decide which value to assign to a variable
        based on a Boolean value evaluation. It's denoted as?

        In the below example, if rank is 1, status is assigned a value of "Done" else "Pending".

        public class conditionTest {
          public static void main(String args[]) {
            string status;
            int rank 3;
            status = (rank == 1)? "Done": "Pending":
            System.out.println(status);
          }
        }

12. How can you generate random numbers in Java?

        Ans: 

        - Using Math.random() you can generate random numbers in the range greater than or equal to 0.1 and less
          than 1.0
        - Using Random class in package java.util

13. What is default switch case? Give example.

        Ans: In a switch statement, default case is executed when no other switch condition matches. Default case is
        an optional case. It can be declared only once all other switch cases have been coded.

        In the below example, when score is not 1 or 2, default case is used.

          public class switchExample {
            int score=4;
            public static void main(String args[]) {
              switch (score) {
                  case 1:
                    system.out.println("Score is 1");
                    break;
                  case 2:
                    system.out.println("Score is 2");
                    break;
                  default:
                    system.out.println("Default Case") 
                }
            }
          }

14. What is the base class in Java from which all classes are derived?

        Ans: java.lang.object

15. Can main() method in Java can return any data?

        Ans: In java, main() method can't return any data and hence, ite's always declared with a void return type.

16. What are Java Packages? What's the significance of packages?

        Ans: In Java, package is a collection of classes and interfaces which are bundled together as they are
        related to each other. Use of packages helps developers to modularize the code and group the code for
        proper re-use. Once code has been packaged in Packages, it can be imported in other classes and used.

17. Can we declare a class as Abstract without having any abstract method?

        Ans: Yes we can create an abstract class by using abstract keyword before class name even if it doesn't
        have any abstract method. However, if a class has even one abstract method, it must be declared as abstract
        otherwise it will give an error.

18. What's the difference between an Abstract Class and Interface in Java?

        Ans: The primary difference between an abstract class and interface is that an interface can only possess
        declaration of public static methods with no concrete implementation while an abstract class can have
        members with any access specifiers (public, private etc) with or without concrete implementation.

        Another key difference in the use of abstract classes and interfaces is that a class which implements an
        interface must implement all the methods of the interface while a class which inherits from an abstract
        class doesn't require implementation of all the methods of its super class.

        A class can implement multiple interfaces but it can extend only one abstract class.

19. What are the performance implications of Interfaces over abstract classes?

        Ans: Interfaces are slower in performance as compared to abstract classes as extra indirections are required
        for interfaces. Another key factor for developers to take into consideration is that any class can extend
        only one abstract class while a class can implement many interfaces.

        Use of interfaces also puts an extra burden on the developers as any time an interface is implemented in a
        class; developer is forced to implement each and every method of interface. 

20. Does Importing a package imports its sub-packages as well in Java?

        Ans: In java, when a package is imported, its sub-packages are not imported and developer needs to import
        therm separately if required.

        For example, if a developer imports a package university.*, all classes in the package named university are
        loaded but no classes from the sub-package are loaded. To load the classes from its sub-package
        ( say department), developer has to import it explicitly as follows:

        Import university.department.*

21. Can we declare the main method of our class as private?

        Ans: In java, main method must be public static in order to run any application correctly. If main method
        is declared as private, developer will not get any compilation error however, it will not get executed and
        will give a runtime error.

22. How can we pass argument to a function by reference instead of pass by value?

        Ans: In java, we can pass argument to a function only by value and not by reference.

23. How an object is serialized in java?

        Ans: In java, to convert an object into byte stream by serialization, an interface with the name Serializable
        is implemented by the class. All objects of a class implementing serializable interface get serialized and
        their state is saved in byte stream.

024. When we should use serialization?

        Ans: Serialization is used when data needs to be transmitted over the network. Using serialization, object's
        state is saved and converted into byte stream. The byte stream is transferred over the network and the
        object is re-created at destination.

25. Is it compulsory for a Try Block to be followed by a Catch Block in Java for Exception handling?

        Ans: Try block needs to be followed by either Catch block or Finally block or both. Any exception thrown
        from try block needs to be either caught in the catch block or else any specific tasks to be performed
        before code abortion are put in the Finally block.

26. Is there any way to skip Finally block of exception even if some exception occurs in the exception block?

        Ans: If an exception is raised in Try block, control passes to catch block if it exists otherwise to
        finally block. Finally block is always executed when an exception occurs and the only way to avoid execution
        of any statements in Finally block is by aborting the code forcibly by writing following line of code at
        the end of try block: 

          System.exit(0);

27. When the constructor of a class is invoked?

        Ans: The constructor of a class is invoked every time an object is created with new keyword. For example,
        in the following class two objects are created using new keyword and hence, constructor is invoked two times.

        public class const_example {
          const_example() {
          system.out.println("Inside constructor");
          }

          public static void main(String args[]){
            const_example cl=new const_example();
            const example c2=new const_example();
          }
        }

28. Can a class have multiple constructors?

        Ans: Yes, a class can have multiple constructors with different parameters. Which constructor gets used for
        object creation depends on the arguments passed while creating the objects.

29. Can we override static methods of a class?

        Ans: We cannot override static methods. Static methods belong to a class and not to individual objects and
        are resolved at the time of compilation (not at runtime). Even if we try to override static method, we will
        not get an complitaion error,nor the impact of overriding when running the code.

30. In the below example, what will be the output?

        public class superclass { 
          public void displayResult(){
            system.out.printin("Printing from superclass");
          }
        }

        public class subclass extends superclass{
          public void displayResult() {
            system.out.println("Displaying from subClass");
            super.displayResult();
          }
  
          public static void main(String args[]){
            subclass obj=new subclass);
            obj.displayResuit();
          }
        }

      ---

          Ans: Output will be:

              Displaying from subclass
              Displaying from superclass

31. Is String a data type in java?

        Ans: String is not a primitive data type in java. When a string is created in java, it is actually an
        object of Java. lang.String class that gets created. After creation of this string object, all built-in
        methods of String class can be used on the string object.

32. In the below example, how many String Objects are created?

        String s1="l am Java Expert";
        String s2-"l am C Expert"; 
        String s3-"l am Java Expert"

      ---

        Ans: In the above example, two objects of Java.Lang.String class are created. s1 and s3 are references to
        same object.

033. Why Strings in Java are called as Immutable?

        Ans: In java, string objects are called immutable as once value has been assigned to a string, it can not 
        be changed and if changed, a new object is created.

        In below example, reference str refers to a string object having value "Value one".

          String str="Value One"

        When a new value is assigned to it, a new String object gets created and the reference is moved to the new
        object.

          str="New Value";

34. What's the difference between an array and Vector?

        Ans: An array groups data of same primitive type and is static in nature while vectors are dynamic in nature
        and can hold data of different data types.

35. What is multi-threading?

        Ans: Multi threading is a programming concept to run multiple tasks in a concurrent manner within a single
        program. Threads share same process stack and running in parallel. It helps in performance improvement of
        any program.

36. Why Runnable Interface is used in Java?

        Ans: Runnable interface is used in java for implementing multi threaded applications. Java.Lang.Runnable
        interface is implemented by a class to support multi threading.

37. What are the two ways of implementing multi-threading in Java?

        Ans: Multi threaded applications can be developed in Java by using any of the following two methodologies:

          1. By using Java.Lang.Runnable Interface. Classes implement this interface to enable multi threading. 
             There is a Run() method in this interface which is implemented. 

          2. By writing a class that extend Java.Lang.Thread class.

38. When a lot of changes are required in data, which one should be a preference to be used? String or StringBuffer?

        Ans: Since StringBuffers are dynamic in nature and we can change the values of StringBuffer objects unlike
        String which is immutable, it is always a good choice to use StringBuffer when data is being changed too
        much. If we use String in such a case, for every data change a new String object will be created which
        will be an extra overhead.

39. What's the purpose of using Break in each case of Switch Statement?

        Ans: Break is used after each case (except the last one) in a switch so that code breaks after the valid
        case and does not flow in the proceeding cases too.
        If break is not used after each case, all cases after the valid case also get executed resulting in wrong
        results.

40. How garbage collection is done in Java?

        Ans: In java, when an object is not referenced any more, garbage collection takes place and the object is
        destroyed automatically. For automatic garbage collection java calls either System.gc) method or
        Runtime.gc() method.

41. How we can execute any code even before main method?

        Ans: If we want to execute any statements before even creation of objects at load time of class, we can
        use a static block of code in the class. Any statements inside this static block of code will get
        executed once at the time of loading the class even before creation of objects in the main method.

42. Can a class be a super class and a sub-class at the same time? Give example.

        Ans: If there is a hierarchy of inheritance used, a class can be a super class for another class and a
        sub-class for another one at the same time.
        In the example below, continent class is sub-class of world class and it's super class of country class.

        public class world {
          ------------
        }

        public class continenet extends world {
          ------------
        }

        public class country extends continent{
          ------------
        }

43. How objects of a class are created if no constructor is defined in the class?

        Ans: Even if no explicit constructor is defined in a java class, objects get created successfully as a
        default constructor is implicitly used for object creation. This constructor has no parameters.

44. In multi-threading how can we ensure that a resource isn't used by multiple threads simultaneously?

        Ans: In multi-threading, access to the resources which are shared among multiple threads can be controlled
        by using the concept of synchronization. Using synchronized keyword, we can ensure that only one thread
        can use shared resource at a time and others can get control of the resource only once it has become free
        from the other one using it.

45. Can we call the constructor of a class more than once for an object?

        Ans: Constructor is called automatically when we create an object using new keyword. It is called only once
        for an object at the time of object creation and hence, we can not invoke the constructor again for an
        object after its creation.

46. There are two classes named classA and classB. Both classes are in the same package. Can a private member of classA can be accessed by an object of classB?

        Ans: Private members of a class are not accessible outside the scope of that class and any other class even
        in the same package can not access them.

47. Can we have two methods in a class with the same name?

        Ans: We can define two methods in a class with the same name but with different number/type of parameters.
        Which method is to get invoked will depend upon the parameters passed.

        For example in the class below we have two print methods with same name but different parameters. Depending
        upon the parameters, appropriate one will be called:

          public class methodExample {

            public void print() {
              system.out.println("Print method without parameters.");
            }

            public void print(String name){
              system.out.printin("Print method with parameter");
            }

            public static void main(String args[]){
              methodExample objl= new method Example();
              obj1.print();
              objl.print("xx");
            }
        }

48. How can we make copy of a java object?

        Ans: We can use the concept of cloning to create copy of an object. Using clone, we create copies with the
        actual state of an object.

        Clone() is a method of Cloneable interface and hence, Cloneable interface needs to be implemented for making
        object copies.

49. What's the benefit of using inheritance?

        Ans: Key benefit of using inheritance is reusability of code as inheritance enables sub-classes to reuse the
        code of its super class. Polymorphism (Extensibility ) is another great benefit which allow new functionality
        to be introduced without effecting existing derived classes.

50. What's the default access specifier for variables and methods of a class?

        Ans: Default access specifier for variables and method is package protected i.e variables and class is
        available to any other class but in the same package,not outside the package.

---
[<h3 style="text-align: center;font-family: cursive;"> Next Page </h3>](java_interview_questions-2.md)

---

<br>

{!footer.md!}
