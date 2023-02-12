object MyClass extends App {
    // scala objects
    object person {
        val n_eyes = 2
        // objects doesn't receive parameters
        def canflay: Boolean = false
        
        def from(mother: person, father: person): person = new person("Bobbie")
    }
    class person(val name:String) {
        // instant level functionality
    }
    
    println(person.n_eyes)
    println(person.canflay)
    // Scala objects = singleton instance -- by definition with any other code
    // it means they are same instance of person and names
    val aisha = person
    val ali = person
    println(aisha == ali)   //it prints true  because they are same instance
    
    // waxa u diclair garen kartaa as new person lkn ki hore la mid ma ahan
    val aisha = new person("aisha")
    val ali = new person("ali")
    println(aisha == ali)
    
    val bobbie = person.from(aisha, ali)
    
    // scala application
    // is only scala objects with  def main(args: Array[String]): Unit
    // hadi aa app ka kor ku yalo iska turto qeebta hose line kas kuso darso else extends app ku darso
}