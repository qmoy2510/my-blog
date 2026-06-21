```kotlin
package org.example.Functions  
  
//다음과 같은 함수가 있을 때  
//fun uppercaseString(text: String): String {  
//    return text.uppercase()  
//}  
//아래처럼 짧게 쓸 수 있음  
//fun main() {  
//    val upperCaseString = { text: String -> text.uppercase() }  
//    println(upperCaseString("hello"))  
//    // HELLO  
//}  
  
//람다 규칙  
//람다식은 중괄호 ({) 안에 작성된다.  
//매개변수 뒤에 ->를 쓴다.  
//-> 뒤에 함수 본문이 온다  
//매개변수가 없는 경우엔 ->를 쓰지 않아도 된다.  
  
//사용법  
//1. 람다식은 다른 함수의 매개변수로 전달할 수 있다.  
//2. 함수에서 람다식을 반환할 수 있다.  
//3. 람다식만 호출해서 쓸 수 있다.  
  
//1번 사용법의 예시  
//fun main() {  
//    val numbers = listOf(1, -2, 3, -4, 5, -6);  
//  
//    val positives = numbers.filter({ x -> x>0});  
//  
//    val isNegative  = {x: Int -> x < 0};  
//    val negatives = numbers.filter(isNegative);  
//  
//    println(positives);  
//    println(negatives);  
//}  
  
//함수 타입  
//함수의 타입으로 함수를 지정할 수 있음  
//아래 모양으로 작성하면 됨  
//매개변수가 없으면 괄호를 비워두면 됨  
//(파라미터 타입) -> 함수 반환 타입  
//(String) -> Int  
  
//val upperCaseString: (String) -> String = { text -> text.uppercase() }  
//  
//fun main() {  
//    println(upperCaseString("hello"))  
//    // HELLO  
//}  
  
//함수의 반환 타입으로 람다를 설정할 수도 있음  
//fun toSeconds(time: String): (Int) -> Int = when (time) {  
//    "시간" -> { value -> value * 60 * 60 }  
//    "분" -> { value -> value * 60 }  
//    "초" -> { value -> value }  
//    else -> { value -> value }  
//}  
//fun main() {  
//    val timesInMinutes = listOf(2, 10, 15, 1)  
//    val min2sec = toSeconds("분")  
//    val totalTimeInSeconds = timesInMinutes.map(min2sec).sum()  
//    println("총 시간은 $totalTimeInSeconds 초입니다.")  
//    // Total time is 1680 secs  
//}  
  
//람다식을 쓰고 그 뒤에 괄호와 매개변수값을 적으면 람다식 하나로 실행 시킬 수 있음  
fun main() {  
    println({text: String -> text.uppercase() }("hello") );  
}
```