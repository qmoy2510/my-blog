```kotlin
package org.example.Null  
  
//코틀린은 기본적으로 null safety 기능을 제공함  
//기본적으로 선언된 변수들은 null 허용이 안됨  
//하지만 타입 끝에 ?를 붙이면 null값을 허용 할 수 있음  
//fun main() {  
//    var text: String = "감자";  
//    var text2: String? = "튀김";  
//  
//    //얜 안되고  
//    text = null;  
//  
//    //얜 됨  
//    text2 = null;  
//  
  
//안전 호출 연산자  
//?.을 통해서 사용할 수 있는 연산자이다  
//이 연산자를 호출했을 때 값이 null값이면 호출을 건너뛰고 null값을 반환하고  
//아니라면 정상적으로 호출한 값을 반환한다.  
  
//fun lengthString(maybeString: String?): Int? = maybeString?.length  
//  
//fun main() {  
//    val nullString: String? = null  
//    println(lengthString(nullString))  
//    // null  
//}  
  
//엘비스 연산자  
//엘비스 연산자는 왼쪽 값이 null이라면  
//오른쪽 값을 대신 반환하는 연산자이다.  
fun main() {  
    val nullString: String? = null  
    println(nullString?.length ?: 0)  
    // 0  
}
```