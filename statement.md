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
data class MyDataClass(name:String , note:Double){
    var studenta_Name = name
    val student_Note = note
}
class Student(){
        var arrList = ArrayList<MyDataClass>()
        
        arrList.add(MyDataClass("Mohamed Ahmed Saleh", 16.5))
        arrList.add(MyDataClass("Babe Haimeddat", 13.0))
        arrList.add(MyDataClass("Brahim Bousebat", 18.5))
        arrList.add(MyDataClass("Imran ElKaa", 10))
        arrList.add(MyDataClass("Haitam Mintaki", 15))
        arrList.add(MyDataClass("Elhili Abdoullatif", 12.5))
        arrList.add(MyDataClass("Chaimaa Wahoudi", 11))

        fun getNote(studentName:String):Double{
            for(i in arrList){
                if(i.name == studentName){
                    return i.note 
                    } else{
                        return 0.0 }
            }  
        }
}
```