```kotlin
package org.example.ControlFlow  
  
fun main() {  
    val d: Int;  
    val check = true;  
  
    //일반 if문과 사용법이 똑같음  
    if(check) {  
        d = 1;  
    } else{  
        d = 2;  
    }  
  
    println(d);  
  
    //코틀린엔 삼항연산자가 없음  
    //대신에 한줄로 if문 표현 가능  
    val a = 1;  
    val b = 2;  
    println(if(a>b) a else b);  
}
```