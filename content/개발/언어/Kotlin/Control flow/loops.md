```kotlin
package org.example.ControlFlow  
  
fun main() {  
    //..연산자를 이용해서 범위를 넣음  
    for(number in 1..5){  
        print(number);  
    }  
  
    val cakes = listOf("딸기", "치즈", "초콜릿")  
  
    //컬렉션에 있는 값도 가져와서 넣을 수 있음  
    for (cake in cakes) {  
        println("${cake} 케이크 맛있겠당");  
    }  
  
    //while문은 java랑 똑같아서 생략  
  
}
```