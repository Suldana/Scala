// exercise 
    /*
    head = first element of the list
    tail = remainder of the list
    isempty = is this list empty
    add(int) => new list with this element added
    toString => a string representation of the list
    */
    
    // answer
abstract class mylist {
    def head: Int
    def tail: mylist
    def isempty: Boolean
    def add(element: Int): mylist
    // toString method
    def printelement: String
    override def toString: String = "[" + printelement + "]"
}

// object extendes with classes
object empty extends mylist {
    // def head: Int = ??? // it doesn't return anything
    // def tail: mylist
    // def isempty: Boolean
    // def add(element: Int): mylisy
    
    def head: Int = throw new NoSuchElementException
    def tail: mylist = throw new NoSuchElementException
    def isempty: Boolean = true
    def add(element: Int): mylist = new conis(element, empty)
    def printelement: String = ""
}
// this have to return something
class conis(h: Int, t: mylist) extends mylist {
    def head: Int = h
    def tail: mylist = t
    def isempty: Boolean = false
    def add(element: Int): mylist = new conis(element, this)
    def printelement: String = 
        if(t.isempty) "" + h
        else h + " " + t.printelement
}
object listTest extends App {
    // val list = new conis(1, empty)
    val list = new conis(1, new conis(2, new conis(3, empty))) // you can say this to print 2
    // println(list.head)
    println(list.tail.head)
    println(list.add(4).head)
    
    // polymorphic methodd call
    println(list.toString)   
}