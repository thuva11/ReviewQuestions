
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
	
	  - List
	  - Set
	  - Map
	  - ArrayBuffer
	  - Vector

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
- **What methods get generated when we declare a case class?-->explore**
- **What does the apply method do?-->explore**
- **What is a Thread?-->explore**
- **In what situations might we want to use multiple threads? (just some)-->explore**



