About the live-session materials:

1)  Instructors may or may not use these resources; they're offered both as in-class guides and often can be used as review/how-to guides. 

2) Each week there is a jupyter notebook (.ipynb file).  bCanvas doesn't display this kind of file, so it's worth downloading to your own machine and running it locally.  These notebooks are great guides, demonstrating some of the main points of the lesson as well as a way to ask questions and see the result.

3)  Sometimes parts of the notebooks go beyond the main lesson to suggest applications.  

4)  Optional resources:  given the very wide range of backgrounds, there are always holes in our knowledge.  So optional resources are offered as complements or supplements.  For week 1, for instance, there's a notebook about using Unix commands and Jupyter.

NOTES FOR SLIDES - WEEK 1
1) Welcome
2) Agenda
3) Quick introduction - getting to know your interests, needs, backgrounds helps your classmates and instructors.
4)  A truism in computing: text books cover fundamentals or extremely pointed topics - there's rarely anything in the middle - so much of computing is figuring out how to problem-solve.   We encourage you to consider your working style and especially to read error messages for debugging.

6) Curriculum - the topics to expect.
7) The Grading: 
a)  if you're going to be late, let the instructors/graders know.  You have a number of late days this term without loosing points.
b) Project 1 is an assigned topic, covering Object-Oriented Programming;  Project 2 is a small team project integrating all the course content on a theme of your own choice.
c) Exams: there's a 2 week window in which to take them; once you start the exam you should complete it in 48 hours.
d)  Participation is what it is - join in!

9) Breakout Rooms: we try to have time for everyone to work together.  Some weeks that's not possible but you'll see be able to review the solution for the breakout room activity.

12)  Tools you'll need.  If you've downloaded Anaconda, you can start Jupyter right from there; or if you prefer use jupyter right from the terminal window.  The command is just "jupyter notebook" (no quotes).

Relationship of Code + Hardware:
	Just a note in passing about programming languages.  There's scripts and compiled.  Scripts are interpreted by some command language executable file (like "python.exe").  You may have used R or SPSS or JavaScript - they are all scripts that are interpreted ("just in time interpreter") that converts the source to object code and then executed.  Scripts are faster to develop and can be fixed; on the other hand there's a bit of computing overhead since the interpreter + script have to be run fresh at every invocation.  Compiled languages take source code, too but then use a special program (a compiler) to do a "two-pass compilation."  The first pass checks syntax.  If there are bugs you'll have to fix them before proceeding.  The 2nd pass is the compiler's optimizing the code.  The result is an object or class file that can be read by an executable language (like Java) or made into a stand-alone application.  Compiled code runs faster, tends to have less bugs.
	
	IDEs and Text Editors: text editors are just that - they're a kind of word processing (WP) program that holds only the string of characters.  WP programs and other applications, on the other hand, have a hidden section (called the directory or header) that contains data about the program, version, date, fonts, etc.   This is why a document written on on WP mayn't run on a different version of the same WP!  Depending on the operating system and the choice of encoding, text files hold text and commands between 0 - 255 (8-bit ASCII); or 0-FFFFFFFF (utf-8) about 1,114,112 possible characters (for Unicode).  The letter "A" for instance is 65 in Decimal [more on decimal, octal, hex, binary later!]; the Kangxi radical "man" ⼈ is 2F08 (hex).  The point is that text with no hidden features like a directory can be read by any computer ... and the compiler can read the source code (written with a text editor) with no problem.  
	Since there's a lot to know about coding, integrated development environments (IDEs) are programs, like a word processor but for coding.  These IDEs color-code your script by data type, help find bugs, have coding hints, etc.  Spyder is one popular one - there are lots!  
	But as a program, any IDE needs a way to communicate w/ the operating system, while a programming language running from the terminal window can do so directly (yes, with the appropriate libraries).   This accounts for why sometimes the script running in Jupyter may act a tiny bit differently than when running from a terminal window.
	
14: The purpose of this slide is to suggest the relationship of the tools we have.  Notice that RAM comes into play.  In short we have a limited amount of space in RAM - our variables and how we declare them will consume different parts of the heap and the stack.  Since python doesn't use explicit pointers, like C++ or Objective-C, which are variables of addresses in RAM, there's a little space taken up by linking between the name space (our variable names) and object space (where the variable is in RAM and how we access them and their values).  
	Python gains speed by using 3rd party libraries, usually written in C++ or Assembly, that hide the pointers but benefit from the speed of data manipulation in RAM.  [Otherwise we have to fetch and decode ... long story but fascinating - check out Sipser, Introduction to theory of computation, in the optional resources area [tba].]
	
15 and Optional Notebook for this week:  Even experienced coders may not have to deal w/ the OS nor think about file permissions.  Recall or fyi all files/directories (folders) have access rights for the owner, groups of users, and everyone else.  For instance, if you create a web page, you're the owner.  if you are part of a group at work (say the "web dev team") the sys admin may have included you and a set of colleagues in the same "group" with the same read/write/execute permissions on files and folders.  When we post our website to the world, we want others (or the "world") to be able to read the file, but not overwrite or execute code on it.   It's suprisingly useful to know about file permissions and you'll find you have to change them on the job.

Note, too, the letters and other characters or glyphs.  In Unix (and any computing situation) the SPACE character is meaningful.  The command "echo" [means echo or print to the currently selected output (stdout) - the monitor] takes a parameter - something to print on the screen.  The space is used to separate the command from the parameters: echo hello.    Notice that if there's a space in the parameter we need to pass the parameters as a String - a contiguous set of letters - and we do this by enclosing in " " - double quotes.  Python isn't picky - matching single quotes or matching double quotes is cool either way.  

16)  Virtual Environments - a common technique for creating a safe working area.

Finally ... NOTE ... python has a funky syntax in that it does not use { } for code blocks - it uses the tab \t or 4-spaces.  And you'll find that the workhorse of so many programs (the array) isn't really something we get to play with until later in the course when we use two very popular libraries, numpy and pandas.  Nevertheless python will provide techniques and code practices that help you learn to problem-solve with code, to write code that's more efficient in RAM, and which will scale up nicely when we start to use really large data stores.

Have fun!