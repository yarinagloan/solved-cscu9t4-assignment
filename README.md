Download Link: https://assignmentchef.com/product/solved-cscu9t4-assignment
<br>
This is the assignment for CSCU9T4 Managing Information. It is a single software development project, partitioned into 2 sections.

Full marks for the assignment are 100 points and they are divided as follows:

<ul>

 <li><strong>Java Object-oriented programming 75 points, thereof:</strong>

  <ul>

   <li>Program implementation</li>

   <li>Coding practices and style</li>

   <li>Documentation</li>

  </ul></li>

 <li><strong>XML 25 points, thereof:</strong>

  <ul>

   <li>XML schema definition</li>

   <li>XML to HTML implementation</li>

  </ul></li>

</ul>




<h1>2)    Programming</h1>

<h2>i)                    Introduction</h2>

The goal of this part of the assignment is to exercise your skills in programming in Java. You will read a file containing some information and use this information to create a set of objects. In addition, in response to some user interaction, you may produce some output files. The assignment aims to test you on the material in the module CSCU9T4: that is, on the structuring and use of objects, and on the writing of resilient programs. The marking will concentrate on the structure of the program, on the documentation – and on whether it actually works!

Completion of this task requires a number of technical Java requirements:

<ul>

 <li>Creation and description of a suitable object model in which to store the data (using the information below),</li>

 <li>construction of the GUI to browse and amend the data (e.g., based on that from the practical exercises),</li>

 <li>reading, parsing, and validating an XML file (with SAX or DOM representation),</li>

 <li>using Java to write an XML file.</li>

</ul>

<h2>i)                    The system to implement</h2>

Implementing the system to the requirements below is worth 60% of your total mark for the assignment, good coding practices (e.g., consistency, tidiness/readability of your code, and reasonable structural choices) is worth another 10%, and documentation (concise, clear and helpful Javadoc comments) is worth 5%.

Your goal is to create a Java program that allows researchers to collect and keep track of academic references (citations): a simplistic bibliography. These are the requirements of the System:

<ul>

 <li>Users should be able to add references manually through a GUI.

  <ul>

   <li>They should be able to omit information without getting an error</li>

  </ul></li>

 <li>Each reference should hold the following information (we omit some essential info traditionally used by bibliographies):

  <ul>

   <li>The title</li>

   <li>The type of publication</li>

   <li>A list of Authors</li>

   <li>The year of publication</li>

   <li>Name of the publisher</li>

   <li>The Digital Object Identifier (DOI)</li>

   <li>The date added to the system (can be omitted by the user and the system will then add it automatically)</li>

  </ul></li>

 <li>For simplicity we only assume there are 3 types of publications and each holds additional information:

  <ul>

   <li>Journal papers

    <ul>

     <li>The name of the journal</li>

     <li>The volume and issue</li>

    </ul></li>

   <li>Conference papers

    <ul>

     <li>The name of the conference</li>

     <li>The location of the conference</li>

    </ul></li>

   <li>Book chapters

    <ul>

     <li>The title of the book</li>

     <li>The name of the editor</li>

    </ul></li>

   <li>The system should implement the following search options which should return a string that could be copied directly into a bibliography (the citations should be ordered in alphabetical order of the first author):

    <ul>

     <li>Find all citations from a specific journal</li>

     <li>Find all citations from a specific conference venue</li>

     <li>Find all citations from a specific Publisher</li>

    </ul></li>

   <li>The user should be able to import many citations at once by reading them from a csv document (examples are provided)

    <ul>

     <li>The import functionality should be able to figure out the type of reference from what fields are present and contain information.</li>

    </ul></li>

   <li>The user should be able to export citations to a file in the following ways:

    <ul>

     <li>To an XML file that conforms to a schema. The user provides the schema file as input to the operation</li>

     <li>To a .txt file with the same text as from the search</li>

     <li>In addition to all citations, the user should also be able to export each search option from above to the 2 file formats</li>

    </ul></li>

  </ul></li>

</ul>

You are provided with an “empty” (very reduced) Netbeans Maven project with a Junit test suite from which you should start your implementation. If you are using GitHub, then fork it to a private repository before checking out a local copy. Alternatively, you can download the zip file from Canvas. Figure 1 (classdiagram.png) displays the class diagram as it will be tested. At minimum, your code must implement what is presented there. You are allowed to implement additional classes, operations/methods, and attributes. Depending on your design choices, you might need to implement additional functionality, it will be subjectively evaluated but not be tested explicitly.

<h2>ii)                  Evaluation of the program implementation (marking)</h2>

Your code will be evaluated on 3 criteria: a) functionality, b) coding practice, and c) documentation.

<ol>

 <li><strong>Functionality (60%): </strong>Provided with the “empty” program outline are a series of Junit tests that form the basis of the test suite that will be used to evaluate the functionality of the program. The provided tests are <strong>not comprehensive,</strong> and you are encouraged to add your own. The evaluation test suite (partially provided) will contain many more test cases, including boundary cases and reflections. The marking will be based on the <strong>proportion of test cases that your code passes</strong> and is semi-automatic, so make sure that your submitted code passes as many tests as possible.</li>

 <li><strong>Coding Practice (10%):</strong> Your code will be assessed by good and recommended coding practices. Including but not limited to: consistency of source code formatting, variable/method naming, and structure.</li>

 <li><strong>Documentation (5%): </strong>You are expected to add clear and concise Javadoc comments to each method and class. Don’t overdo them, just keep them simple but helpful. We expect more information in these than what is produced by using automatic IDE solutions.</li>

</ol>

<h1>3)    XML (25/100)</h1>

<h2>i)                    Introduction</h2>

The goal of this part of the assignment is to evaluate your familiarity of XML and exercise your skills in using XML for data representation. Using Java to handle, convert, and display XML data is evaluated in the programming task above. You will inspect example csv data files and create an appropriate XML schema which can be used in the Java program you implemented for the task above to export a bibliography to an XML file. You will then create an XSLT file that can be used to display a summary of an XML file from your program.

The task within this section, although thematically connected to the programming section, can be achieved independently.

The completion of this task requires a number of skills and knowledge, including but not limited to:

<ul>

 <li>XML schema definitions</li>

 <li>using XSLT to summarise data from an XML</li>

</ul>

<h2>ii)                  Input / data</h2>

The input are the csv files that accompany the Java code from above which are used for testing purposes. They are a number of different data files that represent possible inputs to the bibliography system. Note: they do not represent an exhaustive list of possible inputs but collectively they represent all possible fields (columns).

<h2>iii)                XML Schema (5%)</h2>

<strong>This task is worth 5% of the overall mark.</strong> Finish the XSD file, named <strong><em>bibExport.xsd in the project folder test_files</em></strong><em>,</em> so that it defines a suitable XML schema to represent the bibliography data. The schema should enforce that:

<ul>

 <li>Appropriate types are used.</li>

 <li>Appropriate limitations on elements (e.g., date formats, reference/citation types, etc.)</li>

</ul>

<h2>iv)                XLST – XML to XHTML (20%)</h2>

<strong>This task is worth 20% of the overall mark</strong>. Finish the XSLT file, named <strong><em>xml2xhtml.xsl</em> in the project folder <em>test_files</em></strong>, so that it displays a summary of the data in an XML file (produced by your Java program and that conforms to the schema) as an XHTML file. The concision of your stylesheet will be factored in the marking. Writing a very concise stylesheet may require that you look up methods for parsing groups not seen in the lectures or practical exercises. To produce bibliography.html, you can use online services like <a href="https://www.freeformatter.com/xsl-transformer.html">here</a><a href="#_ftn1" name="_ftnref1">[1]</a>.

The desired output can be seen in Figure 2 (bibSummary.png), the data displayed is from one of the test files in the test_files folder.

<h1>4)    How to submit</h1>

<strong>This assignment is worth 70% of the final marks for the module</strong>. As well as technical accuracy (e.g., correct reading and parsing of the input files, correct writing of output files, and correct implementation of the required functionality for searching), good programming style will also be taken into account (e.g., appropriate use of object-oriented design, appropriate use of Java constructs, effective use of comment text, consistency, legibility and tidiness of program layout, suitably informative choices of variable and method names.)




<strong>You will need to submit your work on Canvas as a zipped file bearing your university student number (7 digits, e.g., 1234567.zip). </strong>

Produce this zip file <strong>from your IDE</strong> (e.g., Netbeans, IntelliJ, Eclipse, etc.) and it must contain the whole Java project from the programming task (if you are just directly working with the project that was provided then all dependencies should have been automatically added to the Maven pom file and therefore do not need to be “physically” included in the zip file).

I recommend following these steps (assuming you have just directly extended the provided project’s source):

<ol>

 <li>Save all files (alternatively commit and push to your private repository if you are working with Git).</li>

 <li>This and the following steps depend on your IDE and/or OS, I use Netbeans on a Mac. Select the project in the project navigation window</li>

 <li>Click “File” and select “Export”</li>

 <li>Select “To zip” or equivalent</li>

 <li>Save the zip file with your student number</li>

 <li>Upload the zip file to Canvas</li>

</ol>







Figure 1: The Class diagram describing the elements of the bibliography system that will be tested.

Figure 2: An example of how the bibliography summary should look. The data is from one of the test files accompanying the reduced project files.

<a href="#_ftnref1" name="_ftn1">[1]</a> https://www.freeformatter.com/xsl-transformer.html