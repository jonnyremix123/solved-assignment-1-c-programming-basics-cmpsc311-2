Download Link: https://assignmentchef.com/product/solved-assignment-1-c-programming-basics-cmpsc311-2
<br>
In this assignment you will develop a program to manage several data types, data structures and arrays. The purpose of this exercise is to either remind or familiarize student with the basics of C programming, as well as to expose students to the management and use of UNIX. Please read the following instructions very carefully and perform the assignment per the instructions.

<b><span style="color: red;">Note</span>: Study the example output (in #8 below) before beginning, as it will help you understand what needs to be done.</b>

<ol id="assignlist">

 <li>Login to your virtual machine. Install the <code>wget</code> utility using the <code>apt-get</code> tool. Refer to the course notes for details on how to perform installation of programs.</li>

 <li>From your virtual machine, download the starter source code provided for this assignment. To do this, use the <code>wget</code> utility to download the file off the main course website:

  <center>

   <a href="http://www.cse.psu.edu/~mcdaniel/cmpsc311-f15/docs/assign1-starter.tgz">http://www.cse.psu.edu/~mcdaniel/cmpsc311-f15/docs/assign1-starter.tgz</a>

  </center></li>

 <li>Create a directory for your assignments and copy the file into it. Change into that directory.<code>% mkdir cmpsc311</code><code>% cp assign1-starter.tgz cmpsc311</code><code>% cd cmpsc311</code><code>% tar xvfz assign1-starter.tgz</code>Once unpacked, you will have the following starter files in the assign1 directory: <code>Makefile</code>, <code>cmpsc311-f15-assign1.c</code> and <code>a1support.h</code>. The <code>Makefile</code> contains commands to make your program from the source code. <code>cmpsc311-f15-assign1.c</code> contains the main function which reads in values from standard input, as well as calls the functions you are to create as part of this exercise. The <code>a1support.h</code> partially defines functions that you are to implement in the course of this assignment (see below).</li>

 <li>You are to complete the <code>cmpsc311-f15-assign1</code> program. The <code>cmpsc311-f15-assign1</code> program receives 20 floating point values, one per line. The code for reading those values from standard input are provided in the assignment source code starter file.</li>

 <li>You are to create a new file <code>a1support.c</code>. This will include the code for each of the functions defined in <code>a1support.h</code>. You are also to complete the function definitions in <code>a1support.h</code>.</li>

 <li>Complete the code in the <code>cmpsc311-f15-assign1.c</code> and <code>a1support.h</code> files. Places where code or declarations needs to be added are indicated by <code>???</code>. See in file comments for hints. The program shall perform the following functions in order as implemented within the <code>main()</code> function:

  <ol>

   <li>Read in 20 float numbers into an array. (<i>this code is provided to you</i>).</li>

   <li>For each value in float arrays, convert as follows:

    <ol>

     <li>Numbers greater than of equal to 10 should be multiplied by Π. Note that Π is in the file <code>math.h</code> as <code>M_PI</code>.</li>

     <li>Numbers less than 10 should be multiplied by 42.4.</li>

    </ol></li>

   <li>Declare and assign values to a second array of 20 integers, where the value is rounded absolute value of the float of the same index (i.e., integer at index 1 should be assigned the rounded absolute value of the float value at index 1).</li>

   <li>Implement a function (in <code>a1support.c</code>) to print out the values of the float and integer arrays, as below. Each function should take two values, the array length and the array itself. The functions are defined <code>print_array_float</code> (this function should print out the float values to three decimal places, one per line), and <code>print_array_integer</code> (this should be print the integer values, one per line).Call both functions in the main function.</li>

   <li>Create a function implementing Euclid’s algorithm (<code>euclids_algorithm</code>) to calculate the greatest common divisor of two integers. The inputs to this function are two integers, <b>a</b> and <b>b</b>. See:

    <center>

     <a href="https://en.wikipedia.org/wiki/Euclidean_algorithm">http://en.wikipedia.org/wiki/Euclidean_algorithm</a>

    </center></li>

   <li>In the main function, write a loop to compute and print out GCD of all adjacent values in the integer array using <code>euclids_algorithm</code>, i.e., euclids_algorithm(array[0], array[1]), euclids_algorithm(array[1], array[2]), …, euclids_algorithm(array[18], array[19])</li>

   <li>Implement two functions that compute the sum of values for each array and return the value; <code>sum_array_float</code> and <code>sum_array_integer</code> . Each function should take two values, the array length and the array itself. Call these two functions on the arrays and print out the result values.</li>

   <li>Implement a selection sort that sorts the arrays in place; <code>selection_sort_float</code> and <code>selection_sort_integer</code>. Call both functions to sort in the main function, then print out the values using the <code>print_array_integer</code> and <code>print_array_integer</code> functions. For insight into how the selection sort works, see:

    <center>

     <a href="https://en.wikipedia.org/wiki/Selection_sort">http://en.wikipedia.org/wiki/Selection_sort</a>

    </center></li>

   <li>You are to graph a multiplier of the sin function in a C function <code>graph_sin</code>. More specifically, you are to graph the function <b>y=sin(x*mult)</b> where <b>mult</b> is a floating point number passed into the graphing function. You will use text to graph the function as provided by the C <code>printf</code> function. The Y axis should go from -1.5 to 1.5 at 0.1 increments, and the X axis should go from -3.5 to 3.5 at 0.1 increments. Make label the axes as shown in the sample output.</li>

   <li>Call <code>graph_sin</code> from the main function with four input values (1.0, 1.5, 2.0, and 3.0).</li>

  </ol></li>

 <li>Add comments to all of your files stating what the code is doing. Fill out the comment function header for each function you are defining in the code. A sample header you can copy for this purpose is provided for the main function in the code.</li>

 <li>The assignment starter package also includes a sample input (<code>test-input1.txt</code>) and output <code>test-output1.txt</code> which you can use to test your program. The <code>test-input.txt</code> file was input used to produce <code>test-output1.txt</code>. To test your program with these inputs, run the code an pipe in the input file to the program as follows:

  <center>

   <code>./cmpsc311-f13-assign1 &lt; test-input1.txt</code>

  </center>Please try to make the output for your program at close to that of the test program output.</li>

</ol>

<b>To turn in</b>:

<ol>

 <li>Create a tarball file containing the <code>assign1</code> directory, source code and build files as completed above. Email the program to <a href="/cdn-cgi/l/email-protection#bad7d9dedbd4d3dfd6fad9c9df94cac9cf94dfdecf">Professor McDaniel</a> and the section TA (listed on course website) by the assignment deadline (11:59pm of the day of the assignment). The tarball should be named <code>LASTNAME-PSUEMAILID-assign1.tgz</code>, where LASTNAME is your last name in all capital letters and PSUEMAILID is your PSU email address without the “@psu.edu”. For example, the professor was submitting a homework, he would call the file <code>MCDANIEL-pdm12-assign1.tgz</code>. <span style="color: red;">Any file that is incorrectly named, has the incorrect directory structure, or has misnamed files, will be assessed a one day late penalty.</span></li>

 <li>Before sending the tarball, test it using the following commands (in a temporary directory — NOT the directory you used to develop the code):<pre>% tar xvzf LASTNAME-PSUEMAILID-assign1.tgz% cd assign1% make... (TEST THE PROGRAM)</pre><pre></pre></li>

</ol>

<hr class="dashline">

<b>Note</b>: Like all assignments in this class you are prohibited from copying any content from the Internet or discussing, sharing ideas, code, configuration, text or anything else or getting help from anyone in or outside of the class. Consulting online sources is acceptable, but under no circumstances should <i>anything</i> be copied. Failure to abide by this requirement will result dismissal from the class as described in our course syllabus.