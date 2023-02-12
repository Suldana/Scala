object MyClass extends App{
    class person(val name: String, movie: String) {
        def likes(bestmovie: String): Boolean = bestmovie == movie
        def hangoutwith(anotherperson: person): String = s"${this.name} is hanging out with ${anotherperson.name}"
        def +(anotherperson: person): String = s"${this.name} is hanging out with ${anotherperson.name}"
        def unary_! : String = s"$name, what the heck!"
        // def isAlive = Boolean = true
        def apply(): String = s"Hi, my name is $name and i like $movie"
    }
    
    val aisha = new person("aisha", "haboon")
    println(aisha.likes("haboon"))
    println(aisha likes "haboon") //equavalent  object method parameter
    //  this operators are called infix notation = operator notation or syntatic notation
    
    val tom = new person("tom", "super powers")
    println(aisha hangoutwith tom)
    println(aisha + tom)
    println(1.+(2))
    // all operators are methods.
    
    
    // prefix notation
    
    val x = -1   // -1 is uniry operators  also maethod
    val y = 1.unary_-
    
    println(!aisha)
    // println(aish.unary_!)
    
    // postfix notation
    // println(aisha.isAlive)
    // println(aisha isAlive) //a sugar syntatics -- but is available without parameters
    
    // special method called apply
    println(aisha.apply())
}


// questions: -- 
/*
1. overload the + operator
    aisha + "the rockstar" => new person "aisha (the rockstar)"
2. add an age to the person class 
    add  aunary + operator => new person with the age +1 
    +aisha => aisha with the age incrementer
3. add a "learns" method in the person class => "aisha learns scala"
    add alearnsscala method , calls learns method with "scala"
    use it in postfix notation
4. overload the apply method
    aisha.apply(2) => "aisha watched haboon 2 times"
*/ 




object MyClass extends App{
    class person(val name: String, movie: String, val age: Int = 0) {
        def likes(bestmovie: String): Boolean = bestmovie == movie
        def hangoutwith(anotherperson: person): String = s"${this.name} is hanging out with ${anotherperson.name}"
        // def +(anotherperson: person): String = s"${this.name} is hanging out with ${anotherperson.name}"
        def unary_! : String = s"$name, what the heck!"
        // def isAlive = Boolean = true
        def apply(): String = s"Hi, my name is $name and i like $movie"
        // questions -- answer
        def +(therockstar: person): String = s"${this.name} is hanging out with ${therockstar.name}"
        def +(nickname: String): person = new person(s"$name ($nickname)", movie)
        
        def Unary_+ : person = new person(name, movie, age + 1)
        // def learns(learnsscala: person): String = s"${this.name} learns scala"
        def learns(thing: String) = s"$name is learning $thing"
        def learnsscala = this learns "scala"
        // def apply(2): String = s"Hi, my name is $name and i like $movie"
        def apply(n: Int): String = s"$name is whatching $movie $n times"
    }
    
    val aisha = new person("aisha", "haboon")
    println(aisha.likes("haboon"))
    println(aisha likes "haboon") //equavalent  object method parameter
    //  this operators are called infix notation = operator notation or syntatic notation
    
    val tom = new person("tom", "super powers")
    println(aisha hangoutwith tom)
    // println(aisha + tom)
    println(1.+(2))
    // all operators are methods.
    
    
    // prefix notation
    
    val x = -1   // -1 is uniry operators  also maethod
    val y = 1.unary_-
    
    println(!aisha)
// println(!aish.unary_!)
    
    // postfix notation
    // println(aisha.isAlive)
    // println(aisha isAlive) //a sugar syntatics -- but is available without parameters
    
    // special method called apply
    println(aisha.apply())

    val rockstar = new person("rockstar", "new movie") 
    println(aisha + rockstar)
    println((aish + "the rockstar").apply())
    println((+aisha).age)
    
    // println(aisha.learns(learnsscala))
    println(aisha.learnsscala)
    // println(aisha.apply(2))
    println(aisha(10))
}