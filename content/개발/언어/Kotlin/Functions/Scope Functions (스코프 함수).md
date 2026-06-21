```kotlin
package ScopeFunctions  
  
//스코프란? : 변수, 객체가 인식되는 범위  
//전역 스코프 (global scope) : 프로그램 어디서나 접근 가능  
//지역 스코프 (local scope) : 정의된 블록 안에서 접근 가능  
  
//스코프 함수 : 객체에 대한 임시 스코프를 생성하고, 그안에서 코드가 돌아갈 수 있게끔 해주는 함수  
//임시 스코프 안에서는 그 객체를 it, this 등으로 호출하면 되기 때문에 코드가 간결해짐  
  
//스코프 함수는 5개가 있음, let, apply, run, also, with  
  
//Let  
//fun sendNotification(recipientAddress: String): String {  
//    println("Yo $recipientAddress!")  
//    return "Notification sent!"  
//}  
//  
//fun getNextAddress(): String {  
//    return "sebastian@jetbrains.com"  
//}  
//  
//fun main() {  
//    val address: String? = getNextAddress()  
//  
//    //let을 사용하면 호출한 객체를 let 스코프 안에서 다시 사용할 수 있음  
//    //아래 코드에선 널비스 연산자를 사용해서 address가 null이면 null값을 반환하고  
//    //null이 아니라면 스코프 함수 let이 실해오디어 address를 인자삼아 람다의 내용이 실행됨  
//    //이렇게 작성하면 confirm을 재활용 할 수 있음  
//    val confirm = address?.let {  
//        sendNotification(it)  
//    }  
//}  
  
//Apply  
//객체를 생성할 때 바로 초기화를 하고싶다면 사용하는 함수이다.  
//class Client() {  
//    var token: String? = null  
//    fun connect() = println("connected!")  
//    fun authenticate() = println("authenticated!")  
//    fun getData() : String {  
//        println("getting data!")  
//        return "Mock data"  
//    }  
//}  
//  
//val client = Client()  
//  
//fun main() {  
//    client.token = "asdf"  
//    client.connect()  
//    client.authenticate()  
//    client.getData()  
//}  
  
//원래라면 위 코드와 같이  
//객체 생성 -> 객체 초기화를 따로 해야하지만  
//apply 스코프 함수를 이용하면  
  
//val client = Client().apply {  
//    token = "asdf"  
//    connect()  
//    authenticate()  
//}  
  
//한번에 생성, 초기화를 같이할 수 있다.  
  
//Run  
//val client: Client = Client().apply {  
//    token = "asdf"  
//}  
//  
//fun main() {  
//    val result: String = client.run {  
//        connect()  
//        authenticate()  
//        getData()  
//    }  
//}  
  
//let과 apply를 합친 느낌  
//마지막 줄에 있는 값을 반환해서 즉시 객체를 만들어서 값을 반환할 때 사용됨  
  
//also  
//val reversedLongUppercaseMedals: List<String> =  
//    medals  
//        .map { it.uppercase() }  
//        .also { println(it) }  
//        // [GOLD, SILVER, BRONZE]  
//        .filter { it.length > 4 }  
//        .also { println(it) }  
//        // [SILVER, BRONZE]  
//        .reversed()  
  
//also는 람다를 실행시키고 객체를 반환함  
//로깅이나, 흐름에 영향을 주지않는 작업에서 많이 쓰임  
  
//With  
//with는 스코프 함수중에 유일하게 확장 함수가 아님  
  
//val canvas = Canvas()  
//with(canvas) {  
//    text(10, 10, "Foo")  
//    rect(20, 30, 100, 50)  
//    circ(40, 60, 25)  
//    // ... 객체 이름 없이 멤버 함수 호출  
//}  
  
//with는 객체를 인자로 받아 그 객체 있는 함수들을 한번에 실행 시킬수 있음  
//사용하면 코드가 간결해짐
```
