
object Generics extends App {
    clss mylist[A] {
        // use the type A
    }
    
    class mymap[key, value]
    val listofintegers = new mylist[Int]   // the type int will replace the generic type A
    val listofstring = new mylist[String]  // its reuseble every fo every single type we can store our generic 
    
    // generic methods
    object mylist {
        def empty[A]: mylist[A] = ???
    }
    Val emptylistofintegers = mylist.empty[Int]
    
    // variance problem
    class animal 
    class cat extends animal
    class dog extends animal
    
    //  yes list[cat] extends list[animal] = covariance
     
    class covariantlist[+A]
    val Animal: animal = new cat
    val Animallist: covariantlist[animal] = new covariantlist[cat]
}