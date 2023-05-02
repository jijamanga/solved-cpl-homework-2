Download Link: https://assignmentchef.com/product/solved-cpl-homework-2
<br>
<ol>

 <li>Be sure your Java program from HW1 has base class Shape with one data member, name, of type string. Shape must have a constructor that takes a string parameter to initialize this name data member. Each derived class should have a constructor that takes a parameter for the name, plus parameters for any added data members, then call the base class (Shape) constructor with this name as a parameter, then initialize any data members added in the derived class. You should have a total of five classes in your Java program for Shape and its derived classes and another (sixth) class for Picture.</li>

 <li>(100 points) Translate the entire class hierarchy you defined in HW1 into C as shown in​   Instead of using class Picture with a linked list of Shapes, you may use an array of Shapes in main as I did in my example linked below.  As usual, start with <a href="https://en.wikipedia.org/wiki/Virtual_method_table">Wikipedia fo</a><u>​     </u><a href="https://en.wikipedia.org/wiki/Virtual_method_table">r</a> <a href="https://en.wikipedia.org/wiki/Virtual_method_table">an overview of virtual method tables.</a>  There are lots of images on the Internet that show​       how vtables, vpointers, and member function pointers are organized. <a href="http://www.cs.ust.hk/~dekai/library/ECKEL_Bruce/TICPP-2nd-ed-Vol-one/TICPP-2nd-ed-Vol-one-html/TIC2Vo16.gif">Here is one</a><u>​  </u><a href="http://www.cs.ust.hk/~dekai/library/ECKEL_Bruce/TICPP-2nd-ed-Vol-one/TICPP-2nd-ed-Vol-one-html/TIC2Vo16.gif">.</a> <u>​ </u>Note that Brass::adjust is inherited from its parent class Wind.  Most other methods are overridden (defined) in the class.  Follow the following procedure for generating the definitions:

  <ol>

   <li>For each concrete class define the following:

    <ul>

     <li>a C struct for the data in each class instance plus the Vpointer</li>

     <li>member functions

      <ol>

       <li>add _this formal parameter</li>

       <li>prefix methods with _this-&gt;</li>

      </ol></li>

     <li>vtable 4) constructor

      <ol>

       <li>call the parent constructor</li>

       <li>set the vpointer</li>

      </ol></li>

    </ul></li>

  </ol></li>

</ol>

<ol>

 <li>Write the main function

  <ul>

   <li>allocate an object of each type with malloc (and free them appropriately)</li>

   <li>call the appropriate constructor on each object</li>

   <li>use the formula for dynamic binding to call each method on each object You can find my example files in the following two files along with a Makefile:         <a href="https://www.ics.uci.edu/~klefstad/public/141/hw2/CircleTest.java">http://www.ics.uci.edu/~klefstad/public/141/hw2/CircleTest.jav</a>​   <a href="https://www.ics.uci.edu/~klefstad/public/141/hw2/CircleTest.java">a</a>         <a href="https://www.ics.uci.edu/~klefstad/public/141/hw2/Circle.cpp">http://www.ics.uci.edu/~klefstad/public/141/hw2/Circle.cp</a>​ <a href="https://www.ics.uci.edu/~klefstad/public/141/hw2/Circle.cpp">p</a>         <a href="https://www.ics.uci.edu/~klefstad/public/141/hw2/Makefile">http://www.ics.uci.edu/~klefstad/public/141/hw2/Makefil</a>​   <a href="https://www.ics.uci.edu/~klefstad/public/141/hw2/Makefile">e</a></li>

  </ul></li>

</ol>

Note: I used C++ and the compiler g++, but only used C features.  In C++, I implemented only class Circle and ACircle. There is a comment at the top of Circle.cpp that explains the algorithm for generating the definitions (similar to the one above). Focus on understanding how inheritance and polymorphism are implemented and avoid just copying what I have done.

Output:

Output should be similar to the previous assignment. I will provide your program with two arguments (arg1 and arg2) and you should use those as the dimensions for your objects. Similar to last assignment, be sure that your output follows this general structure:




FirstTriangle(5, 5) : 12.5 SecondTriangle(4, 4) : 8




FirstCircle(5) : 78.54 SecondCircle(4) : 50.27




FirstSquare(5) : 25 SecondSquare(4) : 16




FirstRectangle(5, 5) : 25 SecondRectangle(4, 4) : 16




<h1>Total : 231.31</h1>




You can put the actual shape drawings either all at the end (in any order), or immediately after you give the name and area of the shape. Ensure you follow the format for the shape name and area as above.