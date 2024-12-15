# Top 100 Java Interview Questions - 2 


---
  We have prepared a set of frequently asked Core Java interview questions to help Freshers and Experienced Java developers in their preparations for Interview.

  You will find these questions very helpful in your Java/OOPs interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

---

 {!inpage-ads.md!}

51. Give an example of use of Pointers in Java class.

        Ans: There are no pointers in Java. So we can't use concept of pointers in Java. 

52. How can we restrict inheritance for a class so that no class can be inherited from it?

        Ans: If we want a class not to be extended further by any class, we can use the keyword Final with the
        class name.

        In the following example, Stone class is Final and can not be extended:

          public Final Class Stone {
            // Class methods and Variables
          }

53. What's the access scope of Protected Access specifier?

        Ans: When a method or a variable is declared with Protected access specifier, it becomes accessible in the
        same class,any other class of the same package as well as a sub-class.

      ******************************* Access Levels *********************************

      |Modifier     |Class|Package|SubClass| World | 
      |-------------|-----|-------|--------|------ |
      |public       |   Y |  Y    |   Y    |  Y    |
      |protected    |   Y |  Y    |   Y    |  N    |
      |no modifier  |   Y |  Y    |   N    |  N    |
      |private      |   Y |  N    |   N    |  N    |

54. What's difference between Stack and Queue?

        Ans: Stack and Queue both are used as placeholder for a collection of data. The primary difference between
         a stack and a queue is that stack is based on Last in First out (LIFO) principle while a queue is based on
         FIFO (First In First Out) principle.

55. In java, how we can disallow serialization of variables?

        Ans: If we want certain variables of a class not to be serialized, we can use the keyword transient while
        declaring them. For example, the variable trans_var below is a transient variable and can not be serialized:

        public class transientExample {
          private transient trans_var;
          // rest of the code 
        }

56. How can we use primitive data types as objects?

        Ans: Primitive data types like int can be handled as objects by the use of their respective wrapper classes.
        For example, Integer is a wrapper class for primitive data type int. We can apply different methods to a
        wrapper class, just like any other object.

57. Which types of exceptions are caught at compile time?

        Ans: Checked exceptions can be caught at the time of program compilation. Checked exceptions must be
        handled by using try catch block in the code in order to successfully compile the code.

58. Describe different states of a thread.

        Ans: A thread in Java can be in either of the following states:

            Ready: When a thread is created, it is in Ready state.
            Running: A thread currently being executed is in running state.
            Waiting: A thread waiting for another thread to free certain resources is in waiting state.
            Dead: A thread which has gone dead after execution is in dead state.

59. Can we use a default constructor of a class even if an explicit constructor is defined?

        Ans: Java provides a default no argument constructor if no explicit constructor is defined in a Java class.
        But if an explicit constructor has been defined, default constructor can not be invoked and developer can
        use only those constructors which are defined in the class.

60. Can we override a method by using same method name and arguments but different return types?

        Ans: The basic condition of method overriding is that method name, arguments as well as return type must be
        exactly same as is that of the method being overridden. Hence usinga different return type does not
        override a method.

61. What will be the output of following piece of code?

        public class operatorExample {
          public static void main(String args[]) {
              int x=4;
              system.out.println(x++); 
          }
        }
 
      ---
        
        Ans: In this case postfix ++ operator is used which first returns the value and then increments. Hence
        the output will be 4.

62. A person says that he compiled a java class successfully without even having a main method in it? Is it possible?

        Ans: main method is an entry point of Java class and is required for execution of the program.
        However a class gets compiled successfully even if it does not have a main method. It can not be run though.

63. Can we call a non-static method from inside a static method?

        Ans: Non-Static methods are owned by objects of a class and have object level scope and in order to call
        the non-Static methods from a static block (like froma static main method), an object of the class needs
        to be created first. Then using object reference, these methods can be invoked.

64. What are the two environment variables that must be set in order to run any Java programs?

        Ans: Java programs can be executed in a machine only once following two environment variables have been
        properly set:

            1. PATH variable
            2. CLASSPATH variable

65. Can variables be used in Java without initialization?

        Ans: In Java, if a variable is used ina code without prior initialization by a valid value, program does
         not compile and gives an error as no default value is assigned to variables in Java.

66. Can a class in Java be inherited from more than one class?

        Ans: In Java, a class can be derived from only one class and not from multiple classes. Multiple
        inheritances is not supported by Java.

67. Can a constructor have different name than a Class name in Java?

        Ans: Constructor in Java must have same name as the class name and if the name is different, it does not
        act as a constructor and compiler thinks of it as a normal method.

68. What will be the output of Round(3.7) and Ceill3.7)?

        Ans: Round(3.7) returns 4 and Ceil(3.7) returns 4. 

69. Can we use goto in Java to go to a particular line?

        Ans: In Java, there is not goto keyword and java doesn't support this feature of going to a particular
        labeled line.

70. Can a dead thread be started again?

        Ans: In java, a thread which is in dead state can't be started again. There is no way to restart a dead
        thread.

71. Is the following class declaration correct?

            public abstract final class testClass{
                // Class methods and variables
            }

     ---

        Ans: The above class declaration is incorrect as an abstract class can not be declared as Final.

72. Is JDK required on each machine to run a Java program?

        Ans: JDK is development Kit of Java and is required for development only and to run a Java program on a
        machine, JDK isn't required. Only JRE is required.

73. What's the difference between comparison done by equals method and == operator?

        Ans: In Java, equals() method is used to compare the contents of two string objects and returns true if
        the two have same value while == operator compares the references of two string objects.

        In the following example, equals() returns true as the two string objects have same values.
        However "==" operator returns false as both string objects are referencing to different objects:

            public class equalsTest {
              public static void main(String args[]) {
                String str1 = new String("Hello World");
                String str2 new String("Hello World");

                if (str1.equals(str2))
                {
                  // this condition is true 
                  System.out.printin("str1 and str2 are equal in terms of values");
                }

                if (str1== str2)
                {
                  //This condition is true
                  System.out.println("Both strings are referencing same object");
                } else
                  {
                    //This condition is NOT true
                    System.out.println("Both strings are referencing different objects");
                  }
              }
            }

74. Is it possible to define a method in Java class but provide it's implementation in the code of another language like C?

        Ans: Yes, we can do this by use of native methods. In case of native method based development, we define
        public static methods in our Java class without its implementation and then implementation is done in
        another language like C separately.

75. How are destructors defined in Java?

        Ans: In Java, there are no destructors defined in the class as there is no need to do so. Java has its own
        garbage collection mechanism which does the job automatically by destroying the objects when no longer
        referenced.

76. Can a variable be local and static at the same time?

        Ans: No a variable can't be static as well as local at the same time. Defining a local variable as static
        gives compilation error.

77. Can we have static methods in an Interface? 

        Ans: Static methods can not be overridden in any class while any methods in an interface are by default
        abstract and are supposed to be implemented in the classes being implementing the interface. So it makes
        no sense to have static methods in an interface in Java.

78. In a class implementing an interface, can we change the value of any variable defined in the interface?

        Ans: No, we can not change the value of any variable of an interface in the implementing class as all
        variables defined in the interface are by default public, static and Final and final variables are like
        constants which can not be changed later.

79. Is it correct to say that due to garbage collection feature in Java, a java program never goes out of memory?

        Ans: Even though automatic garbage collection is provided by Java, it does not ensure that a Java program
        will not go out of memory as there is a possibility that creation of Java objects is being done at a faster
        pace compared to garbage collection resulting in filling of all the available memory resources.

        So, garbage collection helps in reducing the chances of a program going out of memory but it does not
        ensure that.

80. Can we have any other return type than void for main method?

        Ans: No, Java class main method can have only void return type for the program to get successfully
        executed. Nonetheless, if you absolutely must return a value to at the completion of main method, you can
        use System.exit(int status).

81. I want to re-reach and use an object once it has been garbage collected. How it's possible?

        Ans: Once an object has been destroyed by garbage collector, it no longer exists on the heap and it can not
        be accessed again. There is no way to reference it again.

82. In Java thread programming, which method is a must implemetation for all threads?

        Ans: Run() is a method of Runnable interface that must be implemented by all threads.

83. I want to control database connections in my program and want that only one thread should be able to make database connection at a time. How can I implement this logic?

        Ans: This can be implemented by use of the concept of synchronization. Database related code can be placed
        in a method which hs synchronized keyword so that only one thread can access it at a time.

84. How can an exception be thrown manually by a programmer? 

        Ans: In order to throw an exception in a block of code manually, throw keyword is used. Then this exception
        is caught and handled in the catch block.

          public void topMethod() {
            try {
              excMethod();
            }catch(ManualException e){}
          }

          public void excMethod{
            String name=null;
            if(name == null}{
                throw (new ManualException("Exception thrown manually ");
            }
          }

85. I want my class to be developed in sucha way that no other class (even derived class) can create its objects. How can I do so?

        Ans: If we declare the constructor of a class as private, it will not be accessible by any other class and
        hence, no other class will be able to instantiate it and formation of its object will be limited to itself
        only.

86. How objects are stored in Java?

        Ans: In java, each object when created gets a memory space from a heap. When an object is destroyed by a
        garbage collector, the space allocated to it from the heap is re-allocated to the heap and becomes
        available for any new objects.

87. How can we find the actual size of an object on the heap?

        Ans: In java, there is no way to find out the exact size of an object on the heap.

88. Which of the following classes will have more memory allocated?

        Class A: Three methods, four variables, no object
        Class B: Five methods, three variables, no object

     ---

        Ans: Memory is not allocated before creation of objects. Since for both classes, there are no objects
        created so no memory is allocated on heap for any class.

89. What happens if an exception is not handled in a program?

        Ans: If an exception is not handled in a program using try catch blocks, program gets aborted and no
        statement executes after the statement which caused exception throwing.

90. I have multiple constructors defined in a class. Is it possible to call a constructor from another constructor's body?

        Ans: If a class has multiple constructors, it's possible to call one constructor from the body of
        another one using this().

91. What's meant by anonymous class?

        Ans: An anonymous class is a class defined without any name in a single line of code using new keyword.
        For example, in below code we have defined an anonymous class in one line of code:

          public java.util.Enumeration testMethod()
          {
            return new java.util.Enumeration()
            @Override
              public boolean hasMoreElements()
              {
                // TODO Auto-generated method stub
                return false;
              }
              @Override

              public Object nextElement()
              {
                // TODO Auto-generated method stub
                return null; 
              }
          }

92. Is there a way to increase the size of an array after its declaration?

        Ans: Arrays are static and once we have specified its size, we can not change it. If we want to use such
        collections where we may require a change of size ( no of items), we should prefer vector Over array.

93. If an application has multiple classes in it, is it okay to have a main method in more than one class?

        Ans: If there is main method in more than one classes in a java application, it will not cause any issue
        as entry point for any application will be a specific class and code will start from the main method of
        that particular class only.

94. I want to persist data of objects for later use. What's the best approach to do so?

        Ans: The best way to persist data for future use is to use the concept of serialization.

95. What is a Local class in Java?

        Ans: In Java, if we define a new class inside a particular block, it is called a local class. Such a class
        has local scope and is not usable outside the block where its defined.

96. String and StringBuffer both represent String objects. Can we compare String and StringBuffer in Java?

        Ans: Although String and StringBuffer both represent String objects, we can not compare them with each other
        and if we try to compare them, we get an error.

97. Which APl is provided by Java for operations on set of objects?

        Ans: Java provides a Collection APl which provides many useful methods which can be applied on a set of
        objects. Some of the important classes provided by Collection API include ArrayList, Hash Map, TreeSet
        and TreeMap.

98. Can we cast any other type to Boolean Type with type casting?

        Ans: No, we can neither cast any other primitive type to Boolean data type nor can cast Boolean data type
        to any other primitive data type.

99. Can we use different return types for methods when overridden?

        Ans: The basic requirement of method overriding in Java is that the overridden method should have same
        name, and parameters.But a method can be overridden with a different return type as long as the new return
        type extends the original.

        For example, method is returning a reference type.

          Class B extends A {
            A method(int x){
              // original method
            }
            B method(int x){
              //overridden method
            }
          }

100. What's the base class of all exception classes?

        Ans: In Java, Java.lang.Throwable is the super class of all exception classes and all exception classes are
        derived from this base class.

101. What's the order of call of constructors in inheritiance?

        Ans: In case of inheritance, whena new object of a derived class is created, first the constructor of the
        super class is invoked and then the constructor of the derived class is invoked. 

---

<br>

{!footer.md!}
