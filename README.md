Download Link: https://assignmentchef.com/product/solved-comp-348-principles-of-programming-languages-assignment-2
<br>
<strong><u>Note:</u> </strong>For this assignment, you can make use of all the in-built <strong>predicate</strong> functions like oddp, evenp, atom, etc. However, you can’t use any other utility functions such as length of list. You will need to use the “error” function, description is available at:

<a href="http://www.lispworks.com/documentation/lw61/CLHS/Body/f_error.htm"> </a><a href="http://www.lispworks.com/documentation/lw61/CLHS/Body/f_error.htm">http://www.lispworks.com/documentation/lw61/CLHS/Body/f_error.htm</a>     <strong> </strong>

<strong> </strong><strong> </strong>

<h1>Question 1 (15 pts)</h1>

<strong> </strong>

Write a lisp function mytable that takes in one argument x and prints the table for it. Your program should print an appropriate message for decimal as well as string values of x. Sample program output is shown below.

(mytable 2.3) Decimal values not allowed, please enter an integer

(mytable ‘dd) String values not allowed, please enter an integer




(mytable 5)




5 1      5

5 2      10

5 3      15

5 4      20

5 5      25

5 6      30

5 7      35

5 8      40

5 9 45 5 10 50







<h1>Question 2 (15 pts)</h1>

<strong> </strong>

Given an input list of mixed items (such as: integers, decimals, characters, strings, or other nested lists). Write a lisp function that can compute sum of all the elements of the input list which are odd integers. Your program must be able to handle decimal values, character or string values, as the elements inside of its nested lists. Sample program output is shown below.







<ol>

 <li>‘((1 4) ((f 9.0 6) (5))) è 6</li>

 <li>‘((1 a b) ((f 9 6) (7))) è 17</li>

 <li>‘((1 ( ) 7)(((3 (g) 2)))) è 11</li>

 <li>‘((2 4 f a) (8) (w 6)) è 0</li>

 <li>‘(2 4 ( ) ((( ))) 5 ( ) 2) è 5</li>

</ol>




<strong> </strong>

<h1>Question 3 (15 pts)</h1>




<ol>

 <li>Compare these two functions (sum-list1 and sum-list2), what these function do?</li>

 <li>Which one is more efficient or more readable? and why?</li>

</ol>




(defun sum-list1 (L)

(if (null L) 0

(+ (first L)

(sum-list1 (rest L)))))




(defun sum-list2 (L)

(apply #’+ L))




<strong> </strong>

<h1>Question 4 (15 pts)</h1>




Write a lisp program to check whether the two binary trees have the same structure. The structure of a binary tree is represented through list as (root left right). For two trees to have same structure the values don’t need to be the same. A sample tree structure can be displayed as

(23 (9 (5)) (18 9 (45 14 27)))




<strong><img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/06/876.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

  <noscript>

   <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/06/876.png?w=980&amp;ssl=1" data-recalc-dims="1">

  </noscript> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong><u>Question 5</u> (20 pts)</strong>

<strong> </strong>

<ol>

 <li>a) The Tetranacci sequence of numbers is a modified version of the Fibonacci sequence of numbers. The Tetranacci numbers start with four predetermined terms, each term afterwards being the sum of the preceding four terms. The first few Tetranacci numbers are:</li>

</ol>




0, 0, 0, 1, 1, 2, 4, 8, 15, 29, 56, 108, 208, 401, 773, 1490, …




<ul>

 <li>Write a lisp program that computes the Tetranacci numbers using:

  <ol>

   <li>an iterative approach</li>

   <li>a recursive approach</li>

  </ol></li>

 <li>Test both implementations of part 1 for Tetranacci(10), Tetranacci(20), etc. in increments of 10 up to Tetranacci (100) or higher and comment your results.</li>

</ul>

<strong> </strong>

<strong> </strong>

<strong><u>Question 6</u> (20 pts)</strong>

Write a lisp program to compute series for functions ln (1+ <em>x</em>) and <em>e<sup>x</sup></em> depending on a switch variable <em>s</em>.

Write a function that takes in three arguments e.g. function <em>compute-trig</em>(<em>x</em>, <em>s</em>, <em>n</em>), where

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/06/704.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/06/704.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>

<em>s</em> is the switch variable that decides which function to evaluate, <em>n</em> is the precision variable and <em>x</em> is the parameter variable. Parameters <em>s</em> and <em>x</em> should be defined as keyword parameters and <em>n</em> should be an optional parameter with default value of <em>n</em>=5. You are not allowed to use any inbuilt functions except predicate functions to check value type. Your program should print an apt error for string and decimal values for <em>s</em> and <em>n</em>. Additionally, there is a limit for <em>x</em> with <em>s</em>=2.

<strong> </strong>

<strong> </strong>

<strong><u>Bonus Question:</u> (Extra 5 points</strong> if you <u>complete this question correctly</u>)

Given two lists, A (containing elements) and B (containing the pairs of indices) output a list consisting of concatenated elements based on index pairs in B. Sample program output is shown below.

<ul>

 <li>Implement the function using recursion</li>

 <li>Implement the function using loop</li>

</ul>




(print (mystring ‘(a e i o u) ‘((1 3) (2 1) (2 2))))

((A I) (E A) (E E))




(print (mystring ‘(a e i o u) ‘((1 3) (2 6) (3 7))))

((A I) (E NIL) (I NIL))




(print (mystring ‘(a e i o u) ‘((1 3) (2 6) (q 7))))

Error(s), warning(s):

*** – Index Q is a non-integer value




(print (mystring ‘(a e i o u) ‘((1 3) (2.3 6) (1 7)))) Error(s), warning(s):

*** – Index 2.3 is a non-integer value




(print (mystring ‘(a e i o u) ‘((1 3) (2 6) (-3 7))))

Error(s), warning(s):

*** – Index -3 must be positive integer

<strong> </strong>