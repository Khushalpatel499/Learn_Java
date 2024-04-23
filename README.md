# Learn_Java

1.we are going to use JDK version 17 and JDK stands for Java Development kit and it's the software that is used to create and run java Programs.
2.Java is a language while the JDK help us to write the java programs.
3.We run java programs with a java virtual machine (JVM) with java runtime edition (JRE).
4.Oracle(Owners of Java) has moved to ans LTS model for java stands for Long term support.
5.We need to install some programs to write java programs ,st with JDK and then IDE. 6. GO to java.sun.com and dowload JDK.
6.Software tool we will be using to begiin to explore the java programming lanugae.jShell.
7.to check the version of jdk we are using on the terminal by command: java -version.
8.Jshell beacame a standard component of the java developer kit.It is known as Read-Eval-Print-loop(REPL). 9. Jshell runs in a terminal(or on the command line in window). 10. Launch jshell by command jshell in command terminal. 11.in Jshell if we want to write a couple 0f code but dont want to put all on the same line by using curly brackes{ 12. exit command for jshell /exit.

13.hello world- System.out.print("Hello World"); 14. Keyword is any one of a number of reserved words,that have a predefined meaning in java language. 15. Java syntax are case sensitive . 16. primitive data types are: boolean,byte,char,double,float,int ,long ,short

17. Variables are a way to store information in our computers.the statement is the complete command to be executed.
    18.An expression is a coding construct,that evaluates to a single value.or is the code segment that is on the right side of the equals sign in an assigment or declaration statement.
18. for check all the statement we executed in jshell by using /list.
19. to check variables declare in jshell by using /var.

20./vars command in jshell can help you identify any misspellings you may have made. and keyword will be in lowercase.

21. in java we cannot redeclare same variable but in jshell it allow us to redeclare.

22. Primitive data types.
    a. use a wrapper class, a special category of data type,which offers additional functionality that primitive type don'ts.
    b. whole number: byte,short,int,long
    real number: float,double
    single character: char
    boolean value: boolean

23. to get minimum int value: Integer.MIN_VALUE;
    to get max: Integer.MAX_VALUE;
24. The plus(+) used in System.out.print will print different data type together as a single line of text.
25. whatever follow the plus sign in System.out.print , is coverted to a String by Java, and concatenated to the String before it.
    26.A class is a building block for object-oriented programming. and allow us to build custom data types.

27.Java uses the concept of a wrapper class, for all of its eight primitive data types.A wrapper class provides simple operations,as well as some basic information about the rimtive data type which cannot be stored on the primitve itself.(we saw MIN_VALUE and MAX_VALUE are element of this basic information for the int data type.)
28.The wrapper class name is same for primitive data type with the uppercase letter at the start(like byte is Byte, short is Short, float is Float etc) but for char is Character and for int is Integer
29.try to put value larger than maximum, value into an int called overflow situation. try to put value smaller than the minimum value into an int , called underflow situation.These situation are also known as integer wraparounds. 30. The maximum value, when it overflows ,wraps around to the minimum value and the minimum value,when it underflows, wraps around to the maximum value. 30. this int new 2147483648 is given errror while System.out.print(Integer.MAX_VALUE+1) give the wrong output why?

31. in java we cannot put commas in a numeric literal ex:int myNumber =2,147,483,647 is not valid syntax.
    so alternate way is use underscore.
    int myNumber= 2_147_483_647; but we cannot use underscore at the start or end of the numeric literal.

32. byte has the smallest range while long has the largest range.the minimum value of a byte is -128. and maximum value of byte is 127. the minimum value of a short is -32768 while maximum value is 32767.

33. size or width is the amount of space that determines(or limit) the range of values we have:

data type width(in bits)  
 byte 8
short 16
int 32
long 64

imp:
A. a byte can store 256 numbers and occupies eight bits, and has a width of 8.

34.to get the size we use Long.SIZE; 35. long number=100;
the number 100 by default is an int.
java allow certain numeric literals to have a suffix appended to the value to force it to be a different data type from the default type.
for long its suffix is an 'L';
here few instances java is not case sensitive, a lowercase'l' or an uppercase'L' at the end of a whole number means the same thing - the number is a long.
long number=100L;

35. long bigLong=2345893458439234;
    it give error: integer too large

so a numeric literal that exceed Integer.MAX_VALUE must use the 'L' suffix.

36.casting: which is a way to get java to treat a variable of one type like a different data type.
casting means to treat or convert number from one type to another. We put the type we want the number to be in parentheses like this:
(byte)(myMinByteValue/2)

37.What does it mean when java defaults the data type to an int?
int myTotal =(myMinIntValue/2);
this statement works because the result is an int and assiging to an int varible is fine.

short myNewShortValue =(myMinShortValue)/2;
this statemnt doesn't work,because the expression (myMinShortValue/2) is an int ,and an int can't be assigned to a short,becuase the compiler won't guess the result.

short myNewShortValue =(-128/2);
this statement works,because the result of (-128/2) is an int, but when calculations use only literal values,the compiler can determine the result immediately, and knows the value fits into a short.

38. there are two primitive type in java for expressing floating point numbers float and double.
    the double is java default type of any decimal or real number.
    data type width(in bits)
    float 32
    double 64
39. as a default the double is used for float data type can be sepcified as anumeric literal with a suffix of lowercase 'f' or uppercase 'F'.
    for double suffix d or D.
40. float myOtherFloatValue =5.25;
    the number 5.25 is a double so assigning it to a float will raise an error.
41. float and double are great for general floating point operationns. but neither should be used when precise calculations are required-this is due to a limitation with how floating points numbered are stored.
    Java has a class called BigDecimal that overcomes this.
42. A char occupies two bytes of memory ,or 16 bits and thus has a width of 16.
    43.Unicode is an encoding stardard for use with different language and script by which each letter ,digit or symbol is assigned a unique numeric value.
43. for unicode character we need to put a \u and those four digits.
    ex: char myUnicode='\u0044';
    so there are three way to assign a value to a char:
    a literal character : char myChar ='D';
    a Unicode value : char myChar ='\u004'
    an integer value : char myChar =68;
    44.Why you start your boolean variale name with the prefix 'is'?
    this creates a name that seems to ask a question.
44. way to create your own data type ,which in Java are called classes. java's built-in classes like
    Wrappers(Boolean,Byte,Character,etc)
    BigDecimal
    String

45. intersting about classes is that we can combine data types like, one or more ints,doubles,booleans,etc and create a sort of super data type. which are called classes in Java.

46. string is not a primitive type , it actually a class bit of favoritism in Java to make it easier to use than a regular class(basically it is a class that contains a sequence of characters)
47. Strings are immutable means that we can't change a String after it's created.
    Java provides a class in its library to address the inefficieny of the immutable String when we are creating a large amount of text from many smaller parts.
    48.THe StringBuilder class is mutable ,but does not share the String's special features such as being able to assign it a String literal or use the + operator on it.

48.comment: //
