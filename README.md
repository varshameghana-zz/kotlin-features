# kotlin-features
Working on some cool features of Kotlin and how it compares with Java .

1) Printing in Kotlin 

      - Reduces a lot of boiler plate code
      - Internally calling System.out.println()
      
                                   Java                                  Kotlin
                      System.out.println("Hello World");      |    println("Hello, World!")
                                                              

2) Declaring variables and constants 

     - Variables are declared using 'val' or 'var' , provided they are immutable or mutable.
     - Java uses additional 'final' keyword to make variables immutable
     - Advantages using 'val' : Concise , predictable behavior, thread safety
                     
                     
                       int number = 10 ;                       |     var number = 10
                       final int radius = 5;                   |     val radius = 5;
                       
                       
3) Strings in Kotlin  

     - Like Java, strings are immutable in Kotlin
     - Use val keyword to declare strings

                       String name = "JAVA" ;                  |     val greeting = "KOTLIN"
                    
                       
4) String literals

    - Escaped string vs Raw Strings
    - Escaped string can contain escape characters in them
         val escString = "Kotlin escaped string!\n"
    - Raw string can contain newlines and arbitrary text, is delimited by a triple quote """ .<br />
           val myString = """<br />
                   line 1 <br />
                   line 2 <br />
           """

5) String concatenation
   
    String firstName = "Varsha";                                 |   val firstName = "Varsha"; 
    String lastName = "Kanmuri";                                 |   val lastName = "Kanmuri";
    print("My name is: " + firstName + " " + lastName);          |   val message = "My name is: $firstName $lastName"
    
6) if-else expression 
   
   - In Kotlin, if is an expression, i.e. it returns a value. Therefore there is no ternary operator (condition ? then : else)
   
                        val max = if (a > b) a else b            |    int max = (a>b) ? a : b
                        
 7) In Kotlin, the type system distinguishes between references that can hold null (nullable references) and those that can not (non-null references).<br />
 
    var x: String = "one"<br />
    x = null // compilation error<br />

   Nullable string can be defined as follows, written String?:<br />
   var y: String? = "one"<br />
   y = null // ok<br />
   print(y)<br />

  Safe calls for accessing nullable values :<br />
    - val length = b?.length<br />
    

8) Range (..) of values :<br />
    
    - Makes range comparision concise <br />
 
                      if (b>0 && b<10) { }                       |     if(b in 0..10)
                      
   
9) "when" expression - Replacement for switch in java (ignore need of redundant break statement)
     
     val operator = "-"
 
     val result = when (operator) {
          "+" -> print("add")<br />
          "-" -> print("sub")<br />
          "*" -> print("mul")<br />
          "/" -> print("div")<br />
          else -> "$operator is invalid operator."
     }

10) Collections in Kotlin

      - Simpler way to create collections :
           val items = listOf(1, 2, 3)
