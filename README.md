# Technical-Interview-Questions
Practice Java Interview Queestions
1) What is difference between JDK,JRE and JVM?

JVM

JVM is an acronym for Java Virtual Machine, it is an abstract machine which provides the runtime environment in which java bytecode can be executed. It is a specification.

JVMs are available for many hardware and software platforms (so JVM is platform dependent).

JRE

JRE stands for Java Runtime Environment. It is the implementation of JVM.

JDK

JDK is an acronym for Java Development Kit. It physically exists. It contains JRE + development tools.


2) How many types of memory areas are allocated by JVM?
1) Classloader

Classloader is a subsystem of JVM that is used to load class files.

2) Class(Method) Area

Class(Method) Area stores per-class structures such as the runtime constant pool, field and method data, the code for methods.

3) Heap

It is the runtime data area in which objects are allocated.

4) Stack

Java Stack stores frames.It holds local variables and partial results, and plays a part in method invocation and return.
Each thread has a private JVM stack, created at the same time as thread.
A new frame is created each time a method is invoked. A frame is destroyed when its method invocation completes.
5) Program Counter Register

PC (program counter) register. It contains the address of the Java virtual machine instruction currently being executed.

6) Native Method Stack

It contains all the native methods used in the application.

7) Execution Engine

It contains:
1) A virtual processor
2) Interpreter: Read bytecode stream then execute the instructions.
3) Just-In-Time(JIT) compiler: It is used to improve the performance.JIT compiles parts of the byte code that have similar functionality at the same time, and hence reduces the amount of time needed for compilation.Here the term ?compiler? refers to a translator from the instruction set of a Java virtual machine (JVM) to the instruction set of a specific CPU.

3) What is JIT compiler?

Just-In-Time(JIT) compiler:It is used to improve the performance. JIT compiles parts of the byte code that have similar functionality at the same time, and hence reduces the amount of time needed for compilation.Here the term “compiler” refers to a translator from the instruction set of a Java virtual machine (JVM) to the instruction set of a specific CPU.

4) What is platform?

A platform is basically the hardware or software environment in which a program runs. There are two types of platforms software-based and hardware-based. Java provides software-based platform.

5) What is the main difference between Java platform and other platforms?

The Java platform differs from most other platforms in the sense that it's a software-based platform that runs on top of other hardware-based platforms.It has two components:

  1.Runtime Environment
  2.API(Application Programming Interface)

6) What gives Java its 'write once and run anywhere' nature?

The bytecode. Java is compiled to be a byte code which is the intermediate language between source code and machine code. This byte code is not platform specific and hence can be fed to any platform.

7) What is classloader?

The classloader is a subsystem of JVM that is used to load classes and interfaces.There are many types of classloaders e.g. Bootstrap classloader, Extension classloader, System classloader, Plugin classloader etc.

8) Is Empty .java file name a valid source file name?

Yes, save your java file by .java only, compile it by javac .java and run by java yourclassname Let's take a simple example:

9) Is delete,next,main,exit or null keyword in java?

No.

10) If I don't provide any arguments on the command line, then the String array of Main method will be empty or null?

It is empty. But not null.

11) What if I write static public void instead of public static void?

Program compiles and runs properly.

12) What is the default value of the local variables?

The local variables are not initialized to any default value, neither primitives nor object references.
13) What is difference between object oriented programming language and object based programming language?

Object based programming languages follow all the features of OOPs except Inheritance. Examples of object based programming languages are JavaScript, VBScript etc.

14) What will be the initial value of an object reference which is defined as an instance variable?
    The object references are all initialized to null in Java.
    
15) What is constructor?

Constructor is just like a method that is used to initialize the state of an object. It is invoked at the time of object creation.
more details...
16) What is the purpose of default constructor?

The default constructor provides the default values to the objects. The java compiler creates a default constructor only if there is no constructor in the class.more details...
17) Does constructor return any value?

Ans:yes, that is current instance (You cannot use return type yet it returns a value).more details...

18)Is constructor inherited?

No, constructor is not inherited.

19) Can you make a constructor final?

No, constructor can't be final.

20) What is static variable?

static variable is used to refer the common property of all objects (that is not unique for each object) e.g. company name of employees,college name of students etc.
static variable gets memory only once in class area at the time of class loading.
more details...
21) What is static method?

A static method belongs to the class rather than object of a class.
A static method can be invoked without the need for creating an instance of a class.
static method can access static data member and can change the value of it.
more details...
22) Why main method is static?

because object is not required to call static method if It were non-static method,jvm creats object first then call main() method that will lead to the problem of extra memory allocation.more details...

23) What is static block?

Is used to initialize the static data member.
It is excuted before main method at the time of classloading.
more details...
24) Can we execute a program without main() method?

Ans) Yes, one of the way is static block.more details...

25) What if the static modifier is removed from the signature of the main method?

Program compiles. But at runtime throws an error "NoSuchMethodError".

26) What is difference between static (class) method and instance method?

static or class method	                                      instance method
1)A method i.e. declared as static is known as static method.	A method i.e. not declared as static is known as instance method.
2)Object is not required to call static method.	             Object is required to call instance methods.
3)Non-static (instance) members cannot be accessed 
in static context (static method, static block and 
static nested class) directly.	                            static and non-static variables both can be accessed in instance                                                              methods.
4)For example: public static int cube(int n){ return n*n*n;}	For example: public void msg(){...}.

27) What is this in java?

It is a keyword that that refers to the current object.more details...

28)What is Inheritance?

Inheritance is a mechanism in which one object acquires all the properties and behaviour of another object of another class. It represents IS-A relationship. It is used for Code Resusability and Method Overriding.

more details...
29) Which class is the superclass for every class.

Object class.

30) Why multiple inheritance is not supported in java?

To reduce the complexity and simplify the language, multiple inheritance is not supported in java in case of class.more details...
31) What is composition?

Holding the reference of the other class within some other class is known as composition.

32) What is difference between aggregation and composition?

Aggregation represents weak relationship whereas composition represents strong relationship. For example: bike has an indicator (aggregation) but bike has an engine (compostion).

33) Why Java does not support pointers?

Pointer is a variable that refers to the memory address. They are not used in java because they are unsafe(unsecured) and complex to understand.

34) What is super in java?

It is a keyword that refers to the immediate parent class object.more details...

35) Can you use this() and super() both in a constructor?

No. Because super() or this() must be the first statement.

36)What is object cloning?

The object cloning is used to create the exact copy of an object. 

40) What is method overriding:

If a subclass provides a specific implementation of a method that is already provided by its parent class, it is known as Method Overriding. It is used for runtime polymorphism and to provide the specific implementation of the method.more details...

41) Can we override static method?

No, you can't override the static method because they are the part of class not object.

42) Why we cannot override static method?

It is because the static method is the part of class and it is bound with class whereas instance method is bound with object and static gets memory in class area and instance gets memory in heap.

43) Can we override the overloaded method?

Yes.

44) Difference between method Overloading and Overriding.
Method Overloading	Method Overriding
1) Method overloading increases the readability of the program.	Method overriding provides the specific implementation of the method that is already provided by its super class.
2) method overlaoding is occurs within the class.	Method overriding occurs in two classes that have IS-A relationship.
3) In this case, parameter must be different.	In this case, parameter must be same.

45) Can you have virtual functions in Java?

Yes, all functions in Java are virtual by default.

46) What is covariant return type?

Now, since java5, it is possible to override any method by changing the return type if the return type of the subclass overriding method is subclass type. It is known as covariant return type. more details...

47) What is final variable?

If you make any variable as final, you cannot change the value of final variable(It will be constant).more details...

48) What is final method?

Final methods can't be overriden.more details...

49) What is final class?

Final class can't be inherited. more details...

50) What is blank final variable?

A final variable, not initalized at the time of declaration, is known as blank final variable.more details...

51) Can we intialize blank final variable?

Yes, only in constructor if it is non-static. If it is static blank final variable, it can be initialized only in the static block.more details...

52) Can you declare the main method as final?

Yes, such as, public static final void main(String[] args){}.

Core Java - OOPs : Polymorphism Interview Questions

53) What is Runtime Polymorphism?

Runtime polymorphism or dynamic method dispatch is a process in which a call to an overridden method is resolved at runtime rather than at compile-time.

In this process, an overridden method is called through the reference variable of a super class. The determination of the method to be called is based on the object being referred to by the reference variable.

more details...
54) Can you achieve Runtime Polymorphism by data members?

No.


55) What is the difference between static binding and dynamic binding?

In case of static binding type of object is determined at compile time whereas in dynamic binding type of object is determined at runtime.


