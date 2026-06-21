```kotlin
package Object  
  
//코틀린에서는 인스턴스가 단 하나뿐인 객체를 만들 수 있다.  
  
//object로 선언한다.  
//오브젝트는 생성자를 가질 수 없다. (괄호를 붙이지 않음)  
//java 싱글톤 생각하면 됨  
//object DoAuth {  
//    fun takeParams(username: String, password: String) {  
//        println("input Auth parameters = $username:$password")  
//    }  
//}  
//fun main() {  
//    // takeParams()가 호출되는 순간 오브젝트가 생성됨  
//    DoAuth.takeParams("coding_ninja", "N1njaC0ding!")  
//    // input Auth parameters = coding_ninja:N1njaC0ding!  
//}  
  
//data object  
//data class와 똑같이 equals(), toString()을 기본으로 제공한다.  
//copy()는 제공하지 않는다. (object는 인스턴스가 하나라 복사할 수 없음)  
//예시코드  
//data object AppConfig {  
//    var appName: String = "My Application"  
//    var version: String = "1.0.0"  
//}  
//  
//fun main() {  
//    println(AppConfig)          // AppConfig  (toString 자동 제공)  
//    println(AppConfig.appName)  // My Application  
//}  
  
//Companion Object  
//class 속에 존재 할 수 있는 object이다.  
//해당 클래스의 모든 인스턴스에서 접근할 수 있음  
//java에서의 static과 같음  
//companion object는 이름을 정하지 않으면 자동으로 Companion 이름을 가지고 생성됨  
class BigBen {  
    companion object Bonger {  
        fun getBongs(nTimes: Int) {  
            repeat(nTimes) { print("BONG ") }  
        }  
    }  
}  
  
//참조할 때는 클래스 이름으로 참조하면 됨  
fun main() {  
    // 클래스가 처음 참조될 때 컴패니언 오브젝트 생성  
    BigBen.getBongs(12)  
    // BONG BONG BONG BONG BONG BONG BONG BONG BONG BONG BONG BONG  
}
```