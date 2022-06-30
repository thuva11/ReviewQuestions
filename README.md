
## Review Questions Scala - Week-4
- **What is Git?**

	Git is a version control software that allows a developer to easily keep track of changes made to their program and to restore earlier version if necessary.

- **What about GitHub? How are they related?**

	A free, commonly used remote repository for git.

- **What command moves changes from GitHub to our local repo?**
	
	git pull

- **What command moves changes from our local repo to GitHub?**
	
	git push

- **What two commands are used in sequence to save changes to our local repo?**
	
	git add and git commit (alternatively git commit -a can be used to perform both steps at once)

- **What is the JDK and what does it let us do?**
	The Java Development Kit is a tool used by Java developers that allows for the compilation of Java code into .class files as well as the execution of these files. JDK contains the JRE.

- **What is the JRE and what does it let us do?**
	
	The Java Runtime Environment is a compiler that compiles .class files into machine code and then runs them within the JVM(Java Virtual Machine). The JRE contains the JVM.

- **What's the name for the code written in .class files?**
	
	Bytecode

- **How does Scala relate to Java?**
	
	Scala is a language built on top of java, and can utilize many of the functions implemented in java

- **What is sbt (high level)?**
	
	A tool like Maven or Gradle that can manage dependencies and libraries for our projects automatically.

- **How does Scala relate to the JRE and JVM?**
	
	Scala requires a JRE/JVM to run, as Scala is compiled (or decompiled, depending how you look at it) into bytecode to run on the JVM.

- **Is Scala statically or dynamically typed?**
	
	Statically typed. Variables cannot change types after they have been declared.

- **Do we need to declare type for our variables in Scala? always?**
	
	No, Scala has type inferencing, but it can be good to list it explicitly for clarity.

- **What are integer types in Scala?**
	
	Byte, Short, Int, Long

- **Decimal types?**
	
	Double, Float

- **What is the size of an Int? a Double? (the default integer and decimal types)**
	
	32 bits, and 64 bits

- **What is the difference between val and var?**
	
	val - value - Data cannot be changed or edited
	var - variable - Data can be changed or edited

- **Why do we make use of programming paradigms like Functional Programming and Object Oriented Programming?**
	
	To make the program easier to understand and write as the program becomes larger and more complicated

- **What are the 4 pillars of OOP: Abstraction, Encapsulation, Inheritance, Polymorphism? (a bit on each)**
	
	-*Abstraction*: Focusing on relevant details in a given context. Hiding the details of how something is implemented.
	-*Encapsulation*: Objects control access to their own state and behavior with access modifiers (public/private/protected)
	-*Inheritance*: Child classes inherit state and behavior from their parent classes, letting us reuse code
	-*Polymorphism*: Objects and methods can take multiple forms depending on the context. (Type casting)

- **What are classes? Objects?**

	Classes - the blueprint of an object which defines the behavior
	Objects - specific instances of a class

- **What is the significance of the Any class in Scala?**
	
	Everything is a child class of Any

- **What does it mean that functions are first class citizens in Scala?**
	
	You can pass a function into another function, return a function from functions, and store functions in variables and data structures

- **What is a pure function?**
	
	A function with no side effects

- **What is a side effect?**
	
	A function doing anything other than returning a value

- **What's the difference between an expression and a statement?**
	
	An expression returns a value, statements do not

- **What's the difference between a while loop and a do-while loop?**
	
	A while loop may or may not execute, but a do-while loop will always execute at least once.

- **How does String interpolation work in Scala?**
	
	It uses the s character before printing a string. For example: s"Hello, $name"

- **How do operators work in Scala?  Where is "+" defined?**
	
	They work like functions and are defined in Int.scala

- **How do we define an auxiliary constructor?**
	
	Using the "def this" keyword

- **What is a REPL?**
	
	Read-Evaluate-Print-Loop

- **How does the Scala REPL store the results of evaluated expressions?**
	
	It stores it in a res0, res1, res2... variable

- **What is a higher order function?**
	
	A function that takes a function used to transform every element in a data structure

- **Why might we want to write an application using pure functions instead of impure functions?**
	
	So you don't alter any of the data you are working on

- **Why might we want mutable state (OOP) in our application?**  
	
	You want the user to be able to alter the data they are working with, think of like a game  the player should be able to change the state of the game.

- **Why might we want immutable state (FP)?**
	
	You don't want the user to be able to change any of the data they are working with, like in a database accessible by multiple people.

- **What are some examples of side effects?**
	 
	Printing things to the console, writing to a file, changing the value of any variable, etc.

- **What is a Lambda?**
	
	Anonymous inline functions
	
- **How can we write Lambdas in Scala?**

	```scala
	val myFun = (param: String) => {s"Lambda with input: $param" }
	println(myFun("User's input."))
	```
- **What does map do?**
	
	Map is a higher order function used to transform every element in a data structure. It retains the same number of elements as the original data structure.

- **What does filter do?**
	
	Filter will 'remove' elements from a list, returning a new list with a number of members equal to or less than the original list. It will not change any types/values.

	Note: filter does NOT alter the original list in any way, it will return a 	whole new list.

- **What does it mean that a function returns Unit in Scala?**
	
	It is equal to returning void in java - the function does not return anything.

- **Know the basics of the following Scala Collections: (mutable? indexed? when to use it?)**
	
	  - List -  A list of Scala Collections is much like a Scala array. Except that, it is immutable and
		represents a linked list. An Array, on the other hand, is flat and mutable. While declaring a Scala list, we can also denote the type of elements it 		will hold. If it'll hold more than one kind, we use 'Any'.
		
	  - Set - A Scala Set is a collection that won't take duplicates. By default, Scala uses
		immutable sets. But if you want, you can import the scala.collection.mutable.Set class. To be able to refer to both of these in the same collection, we 		can refer to the immutable set as Set and the mutable set as mutable.Set.
		
	  - Map - A Map in Scala is a collection of key-value pairs, and is also called a hash table. We
		can use a key to access a value. These keys are unique; however, the values may be common. The default Scala Map is immutable. To use a mutable Map, we 		use the scala.collection.mutable.Map class. To use both in the same place, refer to the immutable Map as Map, and to the mutable Map as mutable.Map.
		
	  - ArrayBuffer - To create a mutable, indexed sequence whose size can change
		ArrayBuffer class is used. To use, ArrayBuffer, scala.collection.mutable.ArrayBuffer class is imported, an instance of ArrayBuffer is created. 			Internally, an ArrayBuffer is an Array of elements, as well as the store's current size of the array
			
	  - Vector - Vectors in scala are immutable data structures providing random access
		for elements and is similar to the list. But, the list has incompetence of random access of elements. Below is an implementation of some of the 		operations performed on vectors in Scala:

- **What are Exceptions?**
	
	Some issue that occurred while running your code, for example ArrayIndexOutOfBoundsException, or ArithmaticExcpetion. You should generally try to recover from Exceptions.

- **What are Errors?**
	
	Something happened within the JVM that caused your program to crash and burn, such as OutOfMemoryError, or StackOverflowError. You cannot, and should not try to recover from Errors.

- **What is Throwable?**
	
	The parent class of all exceptions and errors.

- **How would we write code that handles a thrown Exception?**
	
	Inside of a try/catch block, use case statements to match to some exception you are trying to handle

- **How do we write code to throw an Exception?**
	
	Use the 'throws' keyword for the exception you have in mind

- **What does the src folder contain in an sbt project?**
	
	The source code files for your project

- **What is a case class?-->explore**
	
	Case classes are like regular classes with a few key differences. Case classes are good for modeling immutable data. they are useful in pattern matching.
	plain and immutable data-holding objects that should exclusively depend on their constructor arguments.
provides support for functional programming is the case class. A case class has all of the functionality of a regular class, and more. When the compiler sees the case keyword in front of a class, it generates code for you, with the following benefits

- **What methods get generated when we declare a case class?-->explore**

	accessor methods are generated for each parameter.
	An apply method is created in the companion object of the class, so you don't need to use the new keyword to create a new instance of the class.
	An unapply method is generated, which lets you use case classes in more ways in match expressions.
	A copy method is generated in the class. You may not use this feature in Scala/OOP code, but it's used all the time in Scala/FP.
	equals and hashCode methods are generated, which let you compare objects and easily use them as keys in maps.
	A default toString method is generated, which is helpful for debugging.

- **What does the apply method do?-->explore**

	Apply is just a mathematical name for applying a function to
a value/set of values.
	In a programming language speak calling this function can
be defined as Call function/method f(x) with value x.

- **What is a Thread?-->explore**
-
	A thread is a single flow of program execution.
	Our computer is not limited to doing one thing at a time. Your processor might be able to simultaneously work on 4, 8, 16, ... tasks at the same time. Our 	programs can be responsible for more than one of those tasks at the same time, as well.
	
- **In what situations might we want to use multiple threads? (just some)-->explore**

	We can use threads to wait and listen for events to occur and take action in response. If you want to process some twitter data as soon as it becomes available, you'd need to have a Thread listening for that Twitter data to become available, at which point that Thread could trigger (multithreaded) processing



