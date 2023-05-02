Download Link: https://assignmentchef.com/product/solved-cmsc403-a6-common-lisp-functions-and-macros
<br>
Define the following Common Lisp functions and macros. Please save your common lisp code in a file named Assignment6.lisp and upload the file to Gradescope when the assignment is complete. A few notes about the assignment:

<ul>

 <li>lisp is expected to contain only the methods described in this assignment manual. (load “Assignment6.lisp”) should return T and print no other information to the console.</li>

 <li>Parameter names can be arbitrary. I gave the parameters names to identify them in the assignment manual but your implementation does not need to use those specific names.

  <ul>

   <li>Function and macro names, on the other hand, must be exactly as specified.</li>

  </ul></li>

 <li>Parameters <strong>must</strong> be in the order they are listed in the assignment manual.</li>

 <li>You may use as many optional parameters as you like, even if no optional parameters are described in the assignment manual.</li>

 <li>Functions are expected to return values, not print values to the console.

  <ul>

   <li>Functions should not print <strong>any </strong>information to the console when executed.</li>

  </ul></li>

 <li>Do not use defun inside of a function body.</li>

 <li>Do not define any global variables with defvar. For local variables inside functions, use let and let* blocks.</li>

 <li>Assume all inputs are valid, you do not need to do any parameter validation in your functions.</li>

 <li>You are allowed (and encouraged) to utilize methods defined in Common Lisp which have not been discussed in class. The documentation for Common Lisp can be found at <a href="http://clhs.lisp.se/">http://clhs.lisp.se/</a> (I advise using Google to search the site. Although the information is good, the web design aspect leaves much to be desired)</li>

 <li>You <strong>must</strong> comment your Common Lisp code. The ; character is used to denote comments.</li>

 <li>You <strong>cannot</strong> use any destructive operations in any of your functions. This includes: the setq special operator, setf, delete, nconc, push, or any derivatives of the setq special operator. Destructive operations go against the functional paradigm described in class.

  <ul>

   <li>A non-destructive alternative to nconc is the append function</li>

  </ul></li>

 <li>I highly recommend against using looping macros and online compilers for the development of this assignment, historically they have caused significant confusion.</li>

 <li>I do not have a preference on what environment you develop your Common Lisp code on. But Gradescope will be testing it on SBCL version 1.4.12.</li>

</ul>

<ol>

 <li>Write a Common Lisp function named myList which creates the following list and returns it</li>

</ol>

(4 (7 22) “art” (“math” (8) 99) 100)

<ol start="2">

 <li> Write a Common Lisp function named leapYear which takes no parameters and returns an ordered list containing all leap years from 1800 though 2020. The list of leapyears <strong>must </strong>be calculated, no points will be given for a hard-coded list.</li>

 <li> Write a Common Lisp function named union- which takes two list parameters. union- returns a single list which contains the separate unique entities from both lists, with no duplication. You are not allowed to use the predefined union function for this function.</li>

 <li> Write a Common Lisp function named avg with a single parameter named aList. avg returns the average of all elements in aList. Assume all elements in aList are numbers. If given an empty list, avg should return NIL. The avg function <strong>must</strong> be tail recursive.</li>

 <li> Write a Common Lisp function named isType which takes a single parameter named dataType. isType will return an anonymous function which takes a single parameter and returns true if the parameters data type is the data type specified in dataType. Otherwise the anonymous function returns false.</li>

 <li> Write a Common Lisp function named taxCalculator with three parameters: limit, rate, and values. limit and rate will be numbers, values will be a list. taxCalculator returns a list with the same elements and ordering of the values parameter EXCEPT every element which is greater than limit is multiplied by rate. Assume that all elements of the values list are numbers.BONUS: Make taxCalculator tail recursive +5 points</li>

 <li>Write a Common Lisp function named clean which takes two parameters: aFunc and aList. aFunc will be a function and aList a list. aFunc is expected to be a function which takes a single parameter and returns a boolean value. clean will return a list which contains all values in aList which, when passed to aFunc, return true. if aList contains sublists, clean should create a new sublist with only the values which return true when passed to aFunc</li>

 <li>Define a Common Lisp macro named threeWayBranch which takes three parameters, x y and toExecute. x and y will be numbers and toExecute a list with three sublists. The threeWayBranch macro will execute statements in toExecute’s first sublist if x &lt; y, the second sublist if x &gt; y, and the third sublist if x = y. Assume each of toExecute’s sublists contain an arbitrary number of statements.</li>

</ol>