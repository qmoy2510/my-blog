```kotlin
package org.example.Classes  
  
//객체는 자바와 똑같이 class로 작성한다  
//클래스에 대한 속성은 선언과 함께 괄호 안에 작성한다.  
//괄호 안에 있는 내용을 클래스 헤더라고 하고  
//클래스 헤더 끝엔 쉼표를 쓸 수 있다.  
class Contact(val id: Int, var email: String){  
    val category: String = "";  
    fun printId() {  
        println(id);  
    }  
}  
  
//인스턴스 생성  
//코틀린은 클래스헤더에 있는 메게변수를 이용해서 생성한다.  
//fun main() {  
//    val contact = Contact(3, "qmoy2510@gmail.com");  
//}  
  
//속성 접근  
//.으로 속성 값에 직접 접근한다.  
//fun main() {  
//    val contact = Contact(3, "qmoy2510@gmail.com");  
//    println(contact.email);  
//}  
  
//데이터 클래스  
//기존 클래스와 동일한 기능들을 가지고 있지만  
//추가적인 멤버 함수가 포함 되어있는 클래스  
//equals(),toString(),copy()가 포함되어있음  
  
//data class User(val name: String, val id: Int)  
//  
//fun main() {  
//    val user = User("감자칼",1);  
//    val user2 = user;  
//  
//    println(user.toString());  
//    println(user.equals(user2));  
//}
```