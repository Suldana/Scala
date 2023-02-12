object MyClass extends App {
    // inheritance
    class animal {
        // private hadi ka hormari inta le ku isticmali kara
        // protected kali kan io wixi sub class ah
        def eat = println("moos")
    }
    class dabjoog extends animal {
        val cat = new dabjoog
        cat.eat
    }
    
    // constructors
    class person(name: String, age: Int) {
        def this(name: String) = this(name, 0)
    }
    class adult(name:String, age: Int, idcard: String) extends person(name, age)
    
    
    // overriding
    class dog extends animal {
        override def eat = println()
    }
    val eey = new dog
    eey .eat
}