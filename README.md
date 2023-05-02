Download Link: https://assignmentchef.com/product/solved-cosc220-project-1-5
<br>
Improve the implementation of your mini-database system to manage employee information developed in the previous project. Your database should still allow users to insert, delete, modify and retrieve employee records. Initially all the data in the database is still stored in an external file called “employeeSorted.db”. When your database program starts, the data in the file is loaded into a sorted singly linked list with template dynamically created first. Then a user interacts with the list during your program execution. When the user decides to exit the program, the data in the list (with all the current updates) is written into the external file (overwrite existing content).




However, there are some significant features in this new version:

<ul>

 <li>You need to use <u>sorted singly linked list with template</u> to store the employee information in your program. You can use re-use the code you write in Lab 4 for this project. You need the templated Node class and all the functions for sorted linked list manipulations.</li>

 <li>db file stores the employee information in the order of their ssn. When you read in the employee information, you will store them in the order of their ssn as well. When you insert/delete employees, you need to make sure the updated list is still in order.</li>

 <li>You need to use the free function approach to overload operators “&gt;&gt;” or “&lt;&lt;” for the Employee class so you can read in and display an employee information as below (instead of output each piece of information separately): Employee emp; inputFile &gt;&gt; emp; or outputFile &lt;&lt; emp;</li>

</ul>




<ul>

 <li>You also need to use the member function approach to overload operator “&lt;”, “&gt;” and “==” for Employee class so that when you compare two Employee objects using those operators, you are comparing their ssn numbers. So you can write the code below without having :</li>

</ul>

Employee emp1, emp2;

if (emp1 &gt; emp2) // comparing the ssn of emp1 with emp2 or   if (emp1 &lt; emp2)  or   if (emp1 == emp2)

<ul>

 <li>Modify the implementation of the function below:</li>

</ul>

void printDatabase(Node&lt;Employee&gt;* eList, int  eCount);

The new version of the function will allow users to choose to display the whole database in various ways as below. You should use one of the sorting algorithms discussed in class (bubble sort or selection sort).

<ul>

 <li>Default: display by the order of their ssn (ascending)</li>

 <li>Display by the order of their last name (ascending) and then first name (ascending) if they share the same last name. o Display by the order of their birthday (ascending) o Display by the order of their income (ascending)</li>

</ul>




Below are the revised prototypes of all the functions you have to implement. Please note that           instead of a pointer to an array of Employee, it is a pointer to the first Node object in the linked      list and the value field of the Node object is

void readDatabase(Node&lt;Employee&gt;* &amp;eList, int &amp; eCount); void writeDatabase(Node&lt;Employee&gt;* eList, int  eCount); void printDatabase(Node&lt;Employee&gt;* eList, int  eCount); bool insertEmployee(Node&lt;Employee&gt;* &amp;eList, int &amp;eCount); bool modifyEmployee(Node&lt;Employee&gt; * eList, int eCount); bool deleteEmployee(Node&lt;Employee&gt;* &amp;eList, int &amp;eCount); void retrieveEmployee(Node&lt;Employee&gt;* eList, int eCount);




<h1>OTHER REQUIREMENTS</h1>

<strong><em> </em></strong>

<ol>

 <li>Make sure to start work on your project early and make steady progress.</li>

 <li>Make sure to test your program thoroughly before you hand in your program.</li>

 <li>Make sure that you give proper names to your variables, program files.</li>

 <li>Make sure that your program is nicely indented and has meaningful comments.</li>

</ol>


