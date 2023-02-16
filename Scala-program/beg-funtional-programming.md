

// object MyClass {
//     val adder = new function2(Int, Int, Int) {
//             override def apply(a: Int, b: Int): Int = a + b

//     def main(args: Array[String]) {
//         print(adder(23, 12))
//     }
// }


// Scala program to illustrate how to
// concatenate strings
object GFG
{
	// str1 and str2 are two strings
	var str1 = "Welcome! Juweria's Code "
	var str2 = " Practice"
	
	// Main function
	def main(args: Array[String])
	{
		
		// concatenate str1 and str2 strings
		// using concat() function
		var Newstr = str1.concat(str2);
		
		// Display strings
		println("String 1:" +str1);
		println("String 2:" +str2);
		println("New String :" +Newstr);
		
		// Concatenate strings using '+' operator
		println("This is the tutorial" +
					" of Scala language" +
					" on github portal");
	}
}








object MyClass extends App {
    // use functions as first class elements
    // oops 
    
}

// class Action {
//     def execute(element: Int): String = 
// }
    val dounler = new myfunction[Int, Int] {
        override def Apply(element: Int): Int = element *2
    }
    
    println(doubler(2))
    
    // function type = function[A, B]
    val stringtoIntconverter = new function[String, Int]
        override def apply(string: String): Int = string.toInt
        }
        
        println(stringtoIntconverter("3") + 4)
        
        val adder = new function2(Int, Int, Int) {
            override def apply(a: Int, b: Int): Int = a + b
        }
        
        // function types fuction[A, B, R] === [A, B] => R
        // ALL SCALA FUNCTIONS ARE OBJECTS
        
        /*
        1. a function which takes 2 strings and concatenates them
        2. transform the mypredicate and mytransformer into function types
        3. define a  function which takes an int and returns and returns another function which takes an int  and returns an Int
                -what's the type of this function
                -how to do it
        
        }

trait myfunction[A, B] {
    
    def Apply(element: A): B
}