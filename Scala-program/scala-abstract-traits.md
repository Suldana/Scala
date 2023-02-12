
object MyClass extends App {
    // abstract == the super class
    abstract class Animal {
        val typekisa: String = "dabjoog"
        def eat: Unit
    }
    class dog extends Animal {
        override val typekisa: String = "madow"
        override val eat: Unit = println("crunch crunch")
    }
    
    
    // traits
    trait hilibcune {
        def eat(animal: Animal): Unit
    }
    
    // lets have more traits
    trait duurjoog
    
    class crocodile extends Animal with hilibcune with duurjoog {
       override val typekisa: String = "croc"
        def eat: Unit = println("nomnom")
        def eat(animal: Animal): Unit = println(s"I am a crocdile and i am eating $(animal.typekisa)")
    }
    
    val dog = new Dog
    val croc = new crocodile
    croc.eat(dog)
}


// abstract classes have both abstract and non-abstract like this
// val typekisa: String = "dabjoog" //this is not abstract
//  def eat: Unit   //this is abstract class
 // multiple traits may be inheritant by the same class