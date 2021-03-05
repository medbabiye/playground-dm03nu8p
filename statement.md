# Welcome!

This Kotlin template lets you get started quickly with a simple one-page playground.

```kotlin runnable
fun main(args: Array<String>) {


    println("Enter your Name :")
    var name:String = readLine()!!.toString()
    val student = Student()
    val note = student.getNote(name)
    if(note == 0.0) { 
        println("Student not found!!")
        }else {
            println("your note is $note")
         }

}
class Student(){
       
        var names = arrayOf("Mohamed Ahmed Saleh","Babe Haimeddat","Brahim Bousebat","Imran ElKaa","Haitam Mintaki","Elhili Abdoullatif","Chaimaa Wahoudi")
        var notes = arrayOf( 16.5 , 13.0 , 18.5 , 10.0 , 15.0 , 12.5 , 11.5 )
       
        fun etNote(studentName:String):Double{
            var noteStudent:Double = 0.0
            for(i in 0 until names.size){
                if(names.contains(studentName)){
                   noteStudent = notes[i] 
                }
            } 
            return noteStudent  
        }
}

```