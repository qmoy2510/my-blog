```kotlin
package org.example.ControlFlow  
  
fun main() {  
    //when은 조건식에 여러 분기가 있으면 사용  
    val obj = "Hello";  
  
    //kotlin에서의 Switch, case 구문이라고 생각하면 된다.  
    when (obj) {  
        "1" -> println("One");  
        "Hello" -> println("Greeting");  
        else -> println("Unkonwn");  
    }  
  
    //표현식으로도 사용할 수 있다.  
    var result = when (obj){  
        "1" -> "ONE";  
        "Hello" -> "Greeting";  
        else -> "Unkonwn";  
    }  
    println(result);  
  
    //그냥 깡으로 When만 때서 쓸 수도 있음  
    val trafficLightState = "Red"  
    result = when{  
        trafficLightState == "Green" -> "Go"  
        trafficLightState == "Yellow" -> "Slow down"  
        trafficLightState == "Red" -> "Stop"  
        else -> "Malfunction"  
    }  
  
    println(result);  
}
```