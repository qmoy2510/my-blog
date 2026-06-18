```kotlin
package org.example.Collection  
  
fun main() {  
    //Set  
    //불변 Set    val readOnlySet = setOf("감자", "당근", "고구마");  
    //명시적 타입 선언이 있는 가변 셋  
    val mySet: MutableSet<String> = mutableSetOf("감자", "토마토", "고구마");  
    println(readOnlySet);  
    println(mySet);  
  
    //요소가 셋 내부에 존재하는지 확인  
    println("감자" in mySet);  
  
    //.add(), .remove() 메서드로 추가, 삭제 가능  
    mySet.add("김재휘");  
    mySet.remove("고구마");  
  
    //Set이라 중복 요소는 안들어가짐  
    mySet.add("감자");  
  
    println(mySet);  
  
}
```

<hr>

같이 보면 좋은 내용들
- [[List]]
- [[Map]]
- [[Collection]]