```kotlin
package org.example.Functions  
  
//kotlin에서는 fun 키워드로 사용자 지정 함수 선언 가능  
fun hello() {  
    return print("안뇽");  
}  
  
//작성 규칙  
//매개변수는 괄호 안에 작성 ()//각 매개변수는 타입이 있어야하며 쉼표로 구분  
//함수의 본문은 중괄호 안에 입력  
//return으로 값 반환 or 함수 종료  
  
fun sum(x: Int, y: Int): Int{  
    return x+y;  
}  
  
//명명된 함수  
//함수 매개변수에 이름도 같이 넣을 수 있음  
//이 때 변수의 순서는 상관이 없음  
//fun main() {  
//    print(sum(y=3,x=5));  
//}  
  
//매개변수의 기본 값  
//기본값을 설정해줄 수 있음  
//기본값 넣은 파라미터 생략하면 뒤에 파라미터들은 직접 명시해서 채워야함  
fun printMessage(message: String, user: String = "박현빈", time: String){  
    println("${user}: ${message}, ${time}시");  
}  
  
//함수에 반환값을 명시하지 않으면 기본적으로 Unit을 명시하게 되어있음  
//Unit은 java에서의 void와 똑같다고 생각하면 됨 (살짝 다르긴 함)  
//fun printMessage: Unit = fun printMessage  
  
//위에서 선언했던 sum함수는 단일 표현식 함수를 통해 줄일 수 있음  
//중괄호를 없애고 결과값만 존재하게 놔두면 kotlin이 알아서 값을 추론해서 리턴해줌  
//fun sum(x: Int, y: Int) = x+y;  
//그래도 결과값은 명시 해주는게 좋음  
//fun sum(x: Int, y: Int): Int = x+y;  
  
  
fun main() {  
    print(printMessage(message="안뇽",time="3"));  
}
```